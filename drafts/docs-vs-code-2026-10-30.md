# Docs against code: what the self-test study found (2026-10-30)

Found while writing the founder's self-test from the code: Loom at `bde337e4`, Zengine at
`6004b53c`, and `pass-tools/mcp-elh` as of 2026-10-30. 26 places where a page or a comment says one
thing and the code does another. Each names the question it came from (the self-test artifact's ids)
and the lines on both sides. The code is the side the answers trust. None is filed; they wait for
the next issue sweep to weigh.

## Loom (8)

- **loom-03**, the gate and Unverified: docs/laws/admission-laws.md GATE-02 (line 44) cites
  `include/zen/admission.hpp` for 'Unverified's accessor-free surface', but Unverified is declared
  in include/zen/serialize.hpp:56 (admission.hpp holds Error and Admission). GATE-02 and
  docs/terminology.md also say Unverified has 'no accessors'; it has three claim accessors
  (well_formed, claimed_name, claimed_version, serialize.hpp:61-65) and none for field data.
- **loom-11**, Mail: docs/guides/messaging.md:98 calls `mail.reply(...)` 'an ordinary send back at
  the sender's address', and README.md 'Sixty seconds of weave' (lines 51 and 56) shows
  `mail.reply(Pong{p.seq})` answering `bus.send(id, Message(to_value(Ping{7})))`. Mail::reply
  (include/zen/weave/weave.hpp:78-81) sends only to the inbound reply_to, with no fallback to the
  stamped sender (unlike the substrate replies at weave.hpp:551 and the control door at
  kernel/control.hpp:321), so in the README snippet, where no reply_to is set, the Pong is addressed
  to WeaveId 0 and refused NoSuchTarget. examples/heartbeat_woven.cpp:68 sets reply_to and works.
- **loom-13**, asks and answers: Possible drift (wording): docs/reference/messaging.md:389 ('An
  answer does not earn a second answer') and the comment at include/zen/weave/weave.hpp:556-557 ('An
  answer seeds no answer (ANS-01)') read naturally as 'a delivered answer cannot itself be
  answered'. In code deliver_one gives every non-notice delivery from a weave, an answer included, a
  fresh ReplyAuthority whose requester is the answerer; only the preparation identity is not
  inherited (src/switchboard/switchboard.cpp:2522-2531), and tests/test_kernel.cpp:3214-3250 has a
  coordinator answer a readiness answer. One ask still gets at most one answer.
- **loom-14**, three refusals: include/zen/weave/dispatch_refusal.hpp:23-24 lists the notice's
  reasons as 'CapabilityDenied / NoSuchTarget / TargetUnavailable / NotAccepted / GateRefused';
  notify_dispatch_refusal also sends ApplicationFailed (src/switchboard/switchboard.cpp:570-573), as
  docs/reference/messaging.md 'Sender-visible dispatch refusal' (lines 125-126) says. The header
  comment lags the code.
- **loom-18**, Grant, LiveAuthority, GrantAuthority: Minor, code comment:
  include/zen/switchboard/switchboard.hpp:1151-1152 says delegation refusals are checked 'inert
  capability, foreign or dead board, missing subject, ceiling'; delegate_authority_as also refuses
  DescribeOnly between the board and subject checks (src/switchboard/switchboard.cpp:1988-1993), as
  docs/reference/capabilities.md 'Live delegation' lists.
- **loom-25**, changing a running weave: docs/laws/lifecycle-laws.md LIFE-01 (lines 11-14) says 'ten
  non-meanings are pinned in the header' (not healthy, not ready, not a role-holder, state not
  preserved, no predecessor implied, not graceful, resources not promised, no loop commanded, no
  work re-commanded, system not ready), and docs/reference/lifecycle.md:89 repeats 'LIFE-01 pins ten
  non-meanings'. The header, include/zen/weave/lifecycle.hpp:79-81, names six (healthy, ready, a
  role holder, state kept, a predecessor existed, anything should start); 'not graceful', 'resources
  not promised', 'no work re-commanded' and 'system not ready' appear nowhere in code, and
  tests/test_weave.cpp pins only the one-field minimality.
- **loom-26**, poke, ZEN_EXPOSE, ZEN_HIDE: docs/guides/diagnostics.md:58 says 'A weave that opts in
  (ZEN_EXPOSE) can be inspected and adjusted by message', and docs/reference/messaging.md
  'Observation' (lines 471-472) says the poke doors allow inspect/manipulate 'where a weave opts
  in'. In code every WeaveBase weave answers the poke doors and an untagged scalar field is readable
  by default (include/zen/weave/shape.hpp:307); ZEN_EXPOSE is needed only to write or reset,
  ZEN_HIDE opts a value out of reading, and what a host controls is whether the answers may leave
  (allow_poke_answers).
- **loom-30**, the box lives in the kernel: docs/guides/dynamic-weaves.md:8 opens 'What loading it
  in-process means' with '`Kernel::load` is `dlopen`.' In code Kernel::load opens a file beginning
  with \0asm as a WebAssembly module in the box, or refuses it when LOOM_ENABLE_WASM is off, and
  never hands it to dlopen (src/kernel/kernel.cpp:313-329); on Windows it uses the LoadLibrary
  backend (kernel.cpp:49-53). The same page mentions the box later, so this is an overstatement
  rather than a contradiction.

## Zengine (8)

- **zengine-02**, why Workshop keeps few facts: WL-DESK-01 names 'roots' without saying what they
  are; only the code (user_paths.hpp) does. A one-line gloss in the law would close it.
- **zengine-04**, why every pane is a weave: agents/decisions/a-participant-earns-its-place.md
  (Alternatives considered, "Permission as a fifth reason") says the loader's `allow_any` "admits
  every row but one", and the code comment at workshop/pane_doors.hpp:9 says the loader binds
  `allow_any()` "to every library it opens"; in code `artifact_admission()`
  (workshop/admission.hpp:79-96) gives bounded grants to two offices, `zengine.inventory` and
  `zengine.first-run`, and Loom's `trust_every_artifact` (allow_any sends) to every other plan
  artifact.
- **zengine-09**, from offer to pixels: docs/architecture/README.md (Ownership map, row "pointer
  routing") says Workshop's weave routes the pointer "in one place: the `PointerButton` and
  `PointerMoved` handlers"; in code Workshop accepts no `input::PointerButton` or
  `input::PointerMoved` message: the window routes each press to the area it lands in (a pane's area
  hears its own pointer), and Workshop's own area hears `graphics::AreaButtonChanged` and
  `AreaPointerMoved`, which it converts into internal `pointer_button`/`pointer_moved` calls
  (workshop/weave_handlers.cpp:319-349).
- **zengine-10**, input sessions and AttributedInput: README.md:31-32 says one Input weave is "the
  sole producer of key, text and pointer moments, on a POSIX terminal, a Windows console, or an SDL
  window" (README.md:212, docs/README.md:51 and docs/getting-started.md:493 repeat "the sole
  producer"); in code the `zengine-input` weave reads only the terminal and the Win32 console
  (input/input.cpp:4), the OS window empties and translates SDL's queue itself
  (graphics/window/window_sdl_backend.hpp:9), the terminal window takes the terminal's keys and
  presses when it holds the terminal (graphics/window/window_terminal.hpp:9,
  input/terminal_reader.hpp:10), windows hand keys and presses to areas as `graphics::Area*` shapes,
  and a plan naming the old `zengine-input-sdl` is refused as retired
  (workshop/load_execute.hpp:166).
- **zengine-12**, setups, layouts and their owner: workshop/docs/zengine.workshop.md (the opening
  paragraph) says Workshop's weave "holds the desk -- which panes are on it, where each stands and
  in what order ... -- and the files that bring a desk back"; in code the layouts (rows, places,
  order) are held and written by `zengine.layouts` (workshop/layouts/owner.hpp:7-12), Workshop
  presents a copy it never writes (workshop/live_desk.hpp:6-9), its setup save is a `LayoutEdit`
  asked of that owner (workshop/weave_session.cpp:316-318), and the owner writes the session;
  Workshop's weave itself writes only its window file and the keymap file
  (workshop/weave_session.cpp:596-600, workshop/weave_desktop.cpp:710).
- **zengine-13**, the Desktop weave: agents/decisions/the-application-defaults-are-a-participant.md
  ("And the absence of a choice is state") says the chosen pane's keys "now stay, in `DesktopState`
  version 2 with its shape unchanged"; in code `DesktopState` is version 3, with `hotkeys_open`
  added (workshop/desktop-pane/vocabulary.hpp:161-167; tests/shapes.txt:98 pins "DesktopState v3").
- **zengine-16**, a presentation owns no facts: agents/decisions/a-presentation-owns-no-facts.md
  (Consequences) says the recipe catalog the session uses "lives on the `Session` beside the source
  document"; in code `Session` (workshop/screen.hpp:782-894) holds no catalog: the host holds it as
  `CurrentRecipes current_recipes` in `main` (workshop/workshop.cpp:354), changed only through the
  project door (workshop/pane_doors.hpp:143-156), and the source document is the Editor office's
  (workshop/pane_seam_vocabulary.hpp:28).
- **zengine-28**, how the repository keeps itself honest: tests/mutants/README.md (The corpus) says
  the claiming comment reads `// MUTATION (tests/mutants/<suite>.md#<id>): ...`; in code 43 claiming
  comments under tests/ open `// MUTATION (...)` without the mark (for example
  tests/test_launcher.cpp:159), which still counts because the runner reads only the
  `tests/mutants/<file>.md#<id>` pointer (tests/mutants/run.py:43) and no check enforces the mark.

## The ELH (6)

- **elh-06**, the guest door row and its powers: workshop/guest_door.hpp:193 says the decision seam
  `decide()` is 'Called by the host (a console command, a suite, tomorrow a popup)', and
  external-host/docs/external-host.md:94-95 (section 1) says of an `"admit": "ask"` row that 'today
  the decision is a suite's or a host's'. In the code the only caller of `GuestDoor::decide` is
  tests/test_workshop_guests.cpp:743: workshop/workshop.cpp wires no console command and the
  Connections pane 'decides nothing' (external-host/connections-pane/pane.cpp:9), so in a shipped
  Workshop an ask row's connection stays awaiting-decision until the peer leaves.
  (external-host.md's 'What this does not do yet' does say no per-connection prompt exists.)
- **elh-08**, attenuation: what a worker may say: Loom's docs/guides/sessions.md:329-330 (section 6)
  says a worker is admitted 'under the rules its package asks for ("asks" in loom-tool.json)' and
  that 'A package that asks for more is refused whole'; python/loom_session/tool.py:16 likewise says
  'the rules its package ``asks`` for'. In the code `asks` is per tool (src/runs/catalog.hpp
  ToolSpec::asks, read per tool by read_tool in catalog.cpp), and run_manager.hpp:420 registers only
  `tool->asks`, so what is refused whole is that one run's registration, not the package: another
  tool of the same package that asks less still runs (Zengine's `workshop/act` asks only
  `loom.link.Ask`, while `workshop/connections` also asks `loom.link.StatusRequested`).
- **elh-09**, a package's name says its reach: external-host/README.md:44 (after the 'What is in
  this folder' table) says 'both tool packages are under `share/zengine/loom-tools/`', but
  cmake/ZengineInstall.cmake:262-266 installs five packages there (workshop, workshop-machine, desk,
  desk-machine, accounts-machine), as external-host/AGENTS.md ('the five tool packages') says.
- **elh-11**, one participant per link; giving input back:
  external-host/docs/external-host.md:603-604 and :622-623 (section 3, 'What a person meets on this
  route' and 'Giving Workshop's input session back') say the busy refusal names the run holding the
  session ('opened for "loom session run <name>"', 'the purpose naming the run that holds it'). Only
  external-host/tools/workshop/inspect_capture.py:118 opens with that purpose; hand.py:214, which
  workshop/act, drag, place, builder and the demo tools use, opens with the fixed purpose 'inventory
  composition demo', so a busy refusal caused by one of those runs does not name the run.
- **elh-15**, the desk as text; guide; resolve: external-host/tools/desk/resolve.py's docstring
  (line 11) says the candidates' parts are read at `PaneView` v6; the code reads them through
  desk_asks.read_pane, which asks at PANE_VIEW_VERSION = 7
  (external-host/tools/desk/desk_asks.py:80), as the tool's manifest description and
  external-host.md say.
- **elh-16**, setups, walks and demo.py: workshop/docs/demo-setups.md:113-115 ('Prepare once, come
  back to it') says starting a setup authorizes 'the shipped Python packages -- `workshop`, `desk`
  ... and those the setup names'; external-host/demo.py:301-302 also approves `workshop-machine` and
  `desk-machine` (any-revision), the two packages whose tools reach the machine as the session's
  user. external-host.md ('The desk written as text for an agent') says it correctly: a setup
  approves all four.

## The MCP server (4)

- **mcp-02**, only verified outputs: README (What an answer holds.) says structuredContent's
  artifacts rows carry, 'for an output not inlined, not_inlined with the reason'. In code only a
  text or picture output that could not be inlined gets not_inlined: an output of any other type (a
  .bin, say), and a .bmp whose .png twin sits beside it, is skipped before any reason is recorded
  (mcp_elh.py lines 496-499), so its row lists name, path, size, digest and state and nothing more.
- **mcp-03**, its own three tools: README says the three tools 'ask no other office' (the
  session__runs description in code says the same). Strictly, each request first attaches, and
  Session.attach asks the session door's office loom.session to Describe itself to confirm the
  lifetime (Loom python/loom_session/session.py line 78); only then do the operations go to
  loom.runs alone. Minor, but it is a second office.
- **mcp-06**, its bounds: Not README drift but an adapter comment that Loom's code contradicts:
  make_room's docstring (mcp_elh.py lines 314-315) says a released run's record is forgotten and
  'loom-session runs <dir> --past still lists it'. Loom's Past handler skips every record of the
  current lifetime (src/runs/run_manager.hpp line 867, past->lifetime == lifetime_), so a run
  released now is listed by --past only from the host's next lifetime; until then only its directory
  and run.json on disk remain.
- **mcp-08**, why it adds no power: README (Prerequisites.) says the session's key and its link
  credentials 'are read only to keep them out of every answer and log line'. That holds for the link
  credentials and for mcp_elh.py's own read (session_secrets), but the key is also what admits the
  server: every attach goes through loom_session's read_session_file, which reads session.key, and
  Session.attach presents it to the door, which is why the server holds the owner's client grant at
  all.
