# The wait: how it works now, and as designed

Vision, 2026-11-06, for the founder. From Zengine `main` at `d7c9fffe` and the trial in
`Zen/reportbacks/clock-reactor-research/reactor.patch`. Code is trimmed to its shape; names are the
real ones unless marked "sketch".

## The picture in two lines

- **Now:** the process sleeps only between turns, at most 10 ms at a time, and nothing can end a
  sleep early. Everything that reads the outside world asks it on a 10 ms Timer beat whether
  anything arrived. At rest that is about 300 turns a second, every one of them finding nothing.
- **Designed:** each reader tells the host what it waits on. The host sleeps on all of it at once,
  plus the Timer's next deadline, and the first of them to happen ends the sleep. Then it wakes
  only the readers that have something. At rest that is about 1 turn a second.

---

## 1. Now

### 1.1 The host's loop (Workshop; `zengine-app` and the snake have the same shape)

```cpp
// workshop/workshop.cpp
while (!host.quit) {
    serve_turn(bus, ...);        // one turn: bus.pump_pending(), what was queued at entry
    rest.after_turn(bus);        // timer/rest.hpp: perhaps sleep (1.2)
}
```

### 1.2 The rest (`timer/rest.hpp`)

```cpp
std::int64_t quiet_ms(const loom::Switchboard& bus) {
    read = bus.observe_office("zengine.timer", TimerRest);   // the Timer's latest claim
    if (no claim, or a stale office holder's)  return 0;
    if (the claim is the same one as last turn) return 0;    // the Timer did not beat this turn
    if (bus.pending() != 1)                     return 0;    // more than the next Drive waits
    return clamp(claim.until_ms - now_ms(), 0, kBeatCapMs);  // kBeatCapMs = 10
}
void after_turn(bus) { if (ms = quiet_ms(bus)) clock.nap_ms(ms); }   // a plain sleep
```

### 1.3 The Timer's beat chain (`timer/timer_weave.hpp`)

```cpp
void on(const Drive&, loom::Mail& mail) {      // always exactly one Drive queued
    fire_due(now, mail);                       // TimerFired to each consumer whose time came
    advance_chain(mail);                       // queue the next Drive
    claim_rest(now, mail);                     // TimerRest{serial, now + min(soonest - now, 10)}
}

struct TimerRest {                             // the claim the rest reads (a Sense: latest value)
    std::int64_t serial = 0;                   // the Drive queued behind this beat
    std::int64_t until_ms = 0;                 // when the next deadline falls, on the Timer's clock
    ZEN_SHAPE(TimerRest, 1, ZEN_FIELD(serial), ZEN_FIELD(until_ms));
};
```

### 1.4 Every reader polls on a Timer beat

```cpp
// input/input_weave.hpp -- the Input office
pump_ = timers().repeat_to_role("zengine.input.pump", 10ms, kInputRole, &on_pump_beat);
void on_pump_beat(const TimerFired&, Mail& m) { for (ev : reader_.poll()) emit(ev, m); }

// graphics/window/window.hpp -- the window, SDL or terminal
timers().repeat("zengine.window.pump", 10ms, &Window::on_pump);
void service_pump(Mail& m) { for (ev : medium_.poll()) route(ev, m); }   // SDL events, console

// editor/neovim-editor/pane.cpp -- each Neovim pane
void on(const TimerFired& f, Mail& m) { if (f.id == kBeatId /*10 ms*/) pump(m); }  // its pipes

// workshop/guest_door.hpp -- the guest door
void on_beat(const TimerFired&, Mail&) { server_->service(); }  // Loom's BridgeServer: accept,
                                                                // read and write every socket
```

Each `poll()` is a non-blocking read that almost always returns nothing.

### 1.5 One idle second, measured

```text
the Timer's Drive        300   one for each distinct deadline; half of them fire nothing
input beat               100   found nothing 100 of 100
window beat              100   found nothing 100 of 100
guest door               100   (BridgeServer says nothing about what it found)
each Neovim pane         100   moved nothing
Flow's clock              62
the host's sleeps        150   each at most 10 ms, and none can end early
```

A key that arrives sits in the OS until the next input or window beat reads it: 0 to 10 ms, about
5 ms on average, before anything in Zengine sees it.

```text
time ------------------------------------------------------------------------------>
host     [turn] sleep<=10ms [turn] sleep<=10ms [turn] sleep<=10ms [turn]
Timer    Drive: window beat  Drive: input beat  Drive: door beat   Drive: window beat ...
OS                key arrives ..........(sits)..........> read at the next input beat
```

---

## 2. As designed

### 2.1 The new vocabulary (sketch)

```cpp
// A reader's wait set: claimed by the reader's own office, a latest value like TimerRest.
struct WaitSet {
    std::vector<std::int64_t> handles;     // Windows HANDLEs, POSIX file descriptors
    bool window_messages = false;          // Windows: this thread's message queue counts (SDL)
    ZEN_SHAPE(WaitSet, 1, ZEN_FIELD(handles), ZEN_FIELD(window_messages));
};

// The host to a reader's office: what you wait on is ready, read it now.
struct Readable { ZEN_SHAPE(Readable, 1); };
```

The trial sent `WaitOn{role, handles, messages}` as a message to a waiter weave the host mounted.
The design makes it a claim, so the claimant is the office and no role field is needed, and there
is no queue to fall behind.

### 2.2 The host's loop

```cpp
while (!host.quit) {
    serve_turn(bus, ...);        // one turn, as now
    reactor.after_turn(bus);     // perhaps wait on everything (2.3)
}
```

### 2.3 The reactor: one wait instead of a sleep (the trial's `timer/reactor.hpp`, trimmed)

```cpp
std::int64_t after_turn(loom::Switchboard& bus) {
    ms = quiet_ms(bus);                    // exactly as the rest decides now (1.2)
    if (ms == 0) return 0;                 // work is queued: no wait at all
    sets  = every office's WaitSet claim;  // who keeps this list is decision 2 (section 3)
    if (an office claims for the first time) { send it Readable{}; return 0; }  // handshake, 2.4
    ready = os_wait(sets, ms);             // ONE call; returns on the first ready handle or at ms
    for (office : ready) bus.send_to_role(office, Readable{});   // wake only who has something
    return ms;
}

// Windows
ready os_wait(sets, ms) {
    handles = every set's handles + one high-resolution waitable timer due in ms;
    MsgWaitForMultipleObjectsEx(handles, INFINITE,
                                any set's window_messages ? QS_ALLINPUT : 0,
                                MWMO_INPUTAVAILABLE);
    return the offices whose handle is still signalled, and the window's if a message waits;
}

// POSIX
ready os_wait(sets, ms) {
    poll(every set's fds, POLLIN, ms);     // stdin, Neovim's pipes, sockets, the display's fd
    return the offices whose fd has revents;
}
```

The high-resolution timer is there because a plain wait's own timeout on Windows rounds to the
scheduler tick (about 15.6 ms).

### 2.4 A reader (sketch, after the trial's input office, window, Neovim pane and door)

```cpp
void on_activated(Mail& m) {
    pump_ = repeat(10ms);                       // poll, as now, until a host says it waits for me
    claim_wait(m);
}
void on(const Readable&, Mail& m) {             // the first is the handshake; later ones, data
    heard_ = true;
    for (ev : reader_.poll()) emit(ev, m);      // read what is ready
    claim_wait(m);
}
void claim_wait(Mail& m) {                      // after every read, and on every beat
    set = reader_.wait_handles();               // console handle, stdin fd, Neovim's pipes ...
    if (set.empty() || !may_stop_beating()) {   // the reader's own rule (below)
        claim(WaitSet{});                       // nothing of mine in the wait just now,
        pump_.ensure();                         // and back to the beat
        return;
    }
    claim(WaitSet{set});                        // says nothing if unchanged; a new handle
                                                // (Neovim restarted ...) replaces the old
    if (heard_) pump_.cancel();                 // waited on: no beat
}
void on_deactivated(Mail& m) {
    claim(WaitSet{});                           // never leave a dead handle in the wait
}
```

A reader has two modes and may move between them for its whole life. Each reader has its own rule
for when it may stop beating; in the trial:

- **the Input office:** while no motion plays (a motion is played out on the beat);
- **the window:** while its medium can be waited on (SDL's message queue, or the console);
- **a Neovim pane:** while it has nothing to write, no question waits out its bound, and its output
  read is outstanding (on Windows a pipe cannot be waited on, so the pane keeps an overlapped read
  in flight and claims that read's event);
- **the guest door:** while no guest is linked (2.7).

A host with no reactor never sends `Readable`, so its readers keep their beats and behave exactly
as now: `zengine-app` until it adopts the reactor, and every test rig.

### 2.5 The Timer's part

- `Drive` and `TimerRest` are unchanged. With no reader polling, the soonest deadline is usually
  the cap, so `kBeatCapMs` goes from 10 ms to a long safety cap (the trial's 1 s) or to none:
  decision 5. That cap is the whole idle cost: one Drive and one turn a second.
- What needed a beat but has no handle becomes a Timer one-shot: a lone Esc on POSIX (Esc, or the
  first byte of a sequence?), a terminal resize, the bound on a question asked of Neovim.

### 2.6 One idle second, and a key

```text
the Timer's Drive          1   the cap's
turns                      1
the host's wait            1   ended early by any key, pipe byte or socket byte
```

```text
time ------------------------------------------------------------------------------>
host     [turn] wait(console, pipes, sockets, deadline) ............ [turn] [turn]
OS                                         key arrives -> the wait returns at once
                                                         Readable -> the Input office
                                                         reads the key in this turn
```

Measured: a key's wait for a read from about 5 ms to under 1 ms.

### 2.7 Loom's part, and where the wait lives

Two readers are Loom's own and hidden from Zengine:

- **`BridgeServer`** (the guest door): an admitted connection's socket is the server's alone, and it
  writes a session's answers only inside `service()`. The trial stopped the door's beat and a
  guest's ask went unanswered for 30 s, so it kept the beat while anyone is linked (200 turns a
  second then).
- **`LineInput`** (`zengine-app`'s console): on Windows it reads on its own thread and offers no
  handle to wait on.

Two ways to place the wait:

```cpp
// (A) The research's: the reactor in Zengine (timer/reactor.hpp, beside rest.hpp).
//     Loom adds what Zengine needs to see (sketch):
socket_set BridgeServer::wait_set() const;   // the listener and every connection
bool       BridgeServer::has_output() const; // answers waiting to be written
handle     LineInput::wait_handle() const;

// (B) Vision's lean: the wait in Loom, beside LineInput and BridgeServer (sketch).
namespace loom::host {
class Reactor {
public:
    explicit Reactor(Switchboard& bus);
    void watch(BridgeServer& server);        // Loom's own readers join from inside
    void watch(LineInput& input);
    // Weaves' WaitSet claims are read by shape; the deadline is the host's to give.
    void wait(std::int64_t ms);              // returns on any ready reader or at ms; sends
};                                           // Readable to each ready office
}

// A Zengine host under (B):
loom::host::Reactor reactor(bus);
reactor.watch(guest_server);
while (!quit) {
    bus.pump_pending();
    if (const auto ms = rest.quiet_ms(bus)) reactor.wait(ms);
}
```

Under (B) nothing of `BridgeServer` or `LineInput` leaks out, the `WaitSet` shape is Loom's, every
Loom host (strangers' too, and `loom-host`) gets the same wait, and the Timer stays Zengine's: the
host still asks the rest how long it may wait.

### 2.8 The frame clock beside it (V5)

```cpp
// the window (sketch)
on(look begins)  { if (!frames_) frames_ = timers().repeat("frame", office_beat /*16 ms*/); }
on(frame)        { compute every playing look at (now - its start); present once; }
on(last look ends, or a steady hold) { frames_.cancel(); }
on(a change while no look plays)     { present now; }      // no frame to wait for
```

While a look plays, the Timer's deadline is the next frame, so the wait ends every 16 ms. When none
plays, the repeat is gone and the host is back to its one turn a second.

---

## 3. What the design commits to

Facts to weigh, not verdicts:

- **Handles are this process's numbers.** A wait set means nothing outside its process, like
  `TimerRest.until_ms` today. A reader must claim again whenever a handle changes or closes: a
  closed handle makes the wait fail at once and the host would then spin, and the next open may be
  given the same number, so a stale claim can watch something else.
- **A handle must stay signalled until its reader reads.** The host checks each handle again after
  the wait to learn who is ready. A manual-reset event (Neovim's reads, a socket's event) and a
  console with input waiting stay signalled; an auto-reset event is cleared by the wait itself and
  its reader would be missed. POSIX's `poll` has no such case.
- **The wait is for reading.** Bytes still to write (to Neovim, to a guest) are not in it; the trial
  keeps those readers on their beat until the bytes are out.
- **One thread waits on everything,** and only what is in the wait ends it. A source that is not a
  handle, a file descriptor or the window's message queue keeps a beat or becomes a Timer one-shot.
  So does another thread with news for the loop (`LineInput`'s reader on Windows, any later
  worker): unless it signals something in the wait, the loop hears it only at the cap.
- **Windows waits on at most 63 handles beside the message queue,** the timer among them. A Neovim
  pane claims three or four (its output and error reads, a write in flight, its process), so 15 to
  20 panes fill it; past that the wait needs a second thread or a completion port. The trial never
  checks the count. POSIX's `poll` has no such limit.
- **A missed wake** (a reader that forgot to claim, or stopped beating by a wrong rule, 2.4) is a
  lag of up to the cap with one, or a stall until something else wakes the host without one.
- **The handshake.** A reader stops polling only after a `Readable`, so a host without a reactor
  keeps today's behaviour, and the two kinds of host can coexist while hosts move over.
- **Who keeps the list of claims** (decision 2): the host names the reader offices it expects, or
  Loom reads every claim of the `WaitSet` shape. Under (B) the second is Loom's own.
- **Not tried yet:** an SDL window on Linux (X11 or Wayland, the display's fd through SDL's window
  properties), a guest driving the input, Windows' build pipes (the Builder's beat already runs
  only while it builds).
