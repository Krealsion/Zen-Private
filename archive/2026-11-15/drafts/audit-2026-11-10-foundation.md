# The audit of 2026-11-10: Loom's foundation, so Zengine shrinks

A cold reviewer the founder contracted read Loom, then Zengine, in separate steps, in the
primary's checkouts (2026-11-10). Its text is below whole. Vision checked its claims in the source
the same day, at Loom `0faba926` and Zengine `4865cf8c`.

## Vision's check

Held, in the source:

- Loom's kinds are seven (`include/zen/kind.hpp`), none a union; a field a door does not declare
  is refused (`UnknownField`). `InjectedEvent` (`input/vocabulary.hpp`) is fourteen fields and a
  `kind` string standing in for one.
- `graphics/implied.hpp` writes Loom's private wire envelope by hand (format bytes, the name, the
  version, the content id) to carry a value whose shape its receiver already knows.
- An image rides a node's operands, bounded at `kMaxArgsBytes` (64 KiB, `graphics/vocabulary.hpp`):
  128 by 128 pixels at most.
- A loaded weave is handed the host's table only inside `handle`; `create` takes a refusal sink and
  nothing else (`include/zen/kernel/abi.h`). Zengine carries four C ABIs of its own
  (`flow/native_abi.h`, `graphics/element_abi.h`, `operator/host_abi.h`,
  `operator/provider_abi.h`), and `OperatorOffer` (`operator/host_surface.hpp`) opens an artifact a
  second time to hand it a host surface.
- `HostContext` (`workshop/weave.hpp`) carries about twenty `std::function` hooks, "what the weave
  needs from the host and cannot get by message".
- `app/` includes `workshop/` headers (`app/main.cpp`, `app/host.hpp`, `app/folder.hpp`).
- A menu's record is kept until a `WithdrawalFence` "has come round twice" (`agents/panes.md`):
  Loom tells nobody an ask ended.
- `view/description.hpp` bounds a view at 64 elements; Flow's C++ generator refuses a fold, for
  the evaluator's budget (`flow/generate.hpp`).

Overstated, or already moving:

- Loom has a synchronous read: Sense (`sense_observe`), a weave reading another's latest claim in
  its own turn. Some of `HostContext`'s hooks could be claims today; the gap is synchronous
  computation.
- In motion: the floor of the replacement research (asks get an ending) ends the menu fences;
  Loom#18 makes a nested value read-only; Loom compares a schema's structure where its id decides
  agreement. Zengine's operator catalog and Flow's generated C++ still compare by the 64-bit id
  alone: a finding for the private round, never a public word.
- The version cascades are half the founder's rule (every change a version) and half the strict
  reader; the release resets every version to 1.
- Its time estimates are guesses.

## The audit, as it was given

> Analyzed value.hpp:L1-114
> Analyzing abi.h:L1-120
> Analyzed switchboard.hpp:L1-120
> Analyzing zen-vision.md:L1-120
> Analyzed abi.h:L1-120
> Analyzed kind.hpp:L1-57

That feeling you’ve had — pushing back against complexity in Zengine only to watch it bulge out somewhere else — makes complete sense once you look at both repos side by side. You haven't been failing to keep Zengine clean; **Zengine is being forced to solve problems in user-space that only Loom can solve at the kernel boundary.**

And knowing that **Workshop is splitting into a third repo** makes this exact moment the highest-leverage inflection point you will ever have. If you extract Workshop *before* fixing Loom's seams, you will freeze Zengine's current workarounds into permanent cross-repo contracts. If you fix Loom's seams *first*, the 3-repo split (`Loom` → `Zengine` → `Workshop`) becomes remarkably clean.

Here is how I see the whole system, why the internal fight is happening, and how I would guide it from here.

---

### 1. The Whole Picture: Why Zengine Is Fighting Loom

Right now, Loom offers **one universal primitive**: asynchronous, queued, serialized-by-value actor messages validated against rigid record schemas ([`Switchboard`](file:///g:/programming/cpp/Zen/primary/Loom/include/zen/switchboard/switchboard.hpp), [`Value`](file:///g:/programming/cpp/Zen/primary/Loom/include/zen/value.hpp#L75-L100), [`Kind`](file:///g:/programming/cpp/Zen/primary/Loom/include/zen/kind.hpp#L23-L31)), loaded behind a closed `create(void)` C ABI ([`abi.h`](file:///g:/programming/cpp/Zen/primary/Loom/include/zen/kernel/abi.h#L25)).

That primitive is great for **low-frequency control-plane coordination**. Virtually everything admirable in your stack — explicit capability grants, deterministic turn logs, survivorship across crashes/reloads, stranger-mode packaging — comes from taking that model seriously.

The internal fight starts because an interactive engine (`Zengine`) and an IDE (`Workshop`) actually have **four distinct kinds of work**, and Loom currently forces the other three through that single control-plane keyhole:

1. **Algebraic domain data & evolving plugin contracts** → Loom has no sum types (`Variant`) and rejects additive fields (`UnknownField`). So Zengine contorts into 14-field sparse structs ([`InjectedEvent`](file:///g:/programming/cpp/Zen/primary/Zengine/input/vocabulary.hpp#L274-L293)), 4-field optional constant bags ([`field_source_schema`](file:///g:/programming/cpp/Zen/primary/Zengine/maker/definition.hpp#L60-L70)), `Bytes` type-erasure, and `v1`..`v9` version cascades ([`graphics/vocabulary.hpp`](file:///g:/programming/cpp/Zen/primary/Zengine/graphics/vocabulary.hpp)).
2. **Bulk media / frame-rate data planes** → Loom copies everything through boxed `Cell` heaps and serialized envelopes. So `graphics` had to forge Loom's private wire header in [`implied.hpp`](file:///g:/programming/cpp/Zen/primary/Zengine/graphics/implied.hpp#L26-L64) and copy RGBA pixels into `64 KiB` `Node::args` ([`image.hpp`](file:///g:/programming/cpp/Zen/primary/Zengine/graphics/elements/image.hpp#L87-L135)), hitting a `128x128` image ceiling.
3. **Synchronous, bounded local calls & capabilities** → Evaluating a pure operator or reading a host fact is synchronous call-stack work, not an async queue turn. Because [`ZenHostApi`](file:///g:/programming/cpp/Zen/primary/Loom/include/zen/kernel/abi.h#L97-L120) can only send/publish/sense async messages and `create(void)` takes nothing, Zengine was trapped between two bad choices:
   - **Obey *"Write Loom, not host code"*** → Simple local actions explode into distributed-systems ceremony: 8-message 2PC `JointPublication` flows (`zengine.opening`) just to open a file and seat a pane, 2-hop [`WithdrawalFence`](file:///g:/programming/cpp/Zen/primary/Zengine/agents/panes.md#L387-L409) dances to close a menu, and [`TimerServiceT`](file:///g:/programming/cpp/Zen/primary/Zengine/timer/timer_weave.hpp) messaging itself forever because the bus has no clock deadline.
   - **Bypass Loom to stay synchronous** → [`OperatorOffer`](file:///g:/programming/cpp/Zen/primary/Zengine/operator/host_surface.hpp#L164-L249) `dlopen`s the library a second time and stuffs a raw pointer into a mutable global static across async turns; [`HostContext`](file:///g:/programming/cpp/Zen/primary/Zengine/workshop/weave.hpp#L91-L334) injects 20+ `std::function` backdoors into Workshop. That immediately forfeits Wasm/process isolation, grant auditing, and hot-reload!
4. **End-user expressiveness vs. meta-machinery** → Because so much engineering budget went into fighting those three mismatches (fences, 2PC, version bridges, side-channel ABIs), the actual creative layer (`Maker` writing only one state field per trigger, `Flow` refusing `fold` in [`generate_cpp`](file:///g:/programming/cpp/Zen/primary/Zengine/flow/generate.hpp#L50-L56), `View` capped at 64 fixed-pixel labels/ints/buttons) remained starved.

---

### 2. What Loom Needs to Become for Zengine to Breathe

Loom does **not** need to become bigger or absorb UI/engine concepts — in fact, `Switchboard` should probably get *smaller*. Instead, Loom needs **four foundational upgrades** so Zengine never has to tunnel around it again:

#### A. Complete the Value Algebra: `Kind::Variant` + Immutable Flat `Value`
- **Add `Kind::Variant` (tagged unions)** to [`Kind`](file:///g:/programming/cpp/Zen/primary/Loom/include/zen/kind.hpp#L23-L31) (which you already designed as append-only). Every variant carries a named case tag + case payload validated directly by `Gate::admit`.
  - *Immediate payoff in Zengine*: [`implied.hpp`](file:///g:/programming/cpp/Zen/primary/Zengine/graphics/implied.hpp)'s hardcoded wire-header surgery disappears; `CanvasDrawing` nodes, `InjectedEvent`, `Maker` field bindings, and optional sub-records become natively typed and gate-checked.
- **Make admitted `Value`s genuinely immutable & flat** (arena or contiguous byte-backed buffer with indexed offsets rather than mutable `std::shared_ptr<Value>` cells and `O(F^2)` name lookups in [`Value`](file:///g:/programming/cpp/Zen/primary/Loom/include/zen/value.hpp#L75-L100)), add DAG visit budgets to `admit()`/`serialize()`, and replace 64-bit FNV-1a `content_id()` trust (`gate.cpp`, [`Catalog::walk`](file:///g:/programming/cpp/Zen/primary/Zengine/operator/catalog.hpp#L394-L395), [`generate_cpp`](file:///g:/programming/cpp/Zen/primary/Zengine/flow/generate.hpp#L80-L81)) with real structural identity (cached by schema pointer pair in-process, or 128-bit/SHA-256 digest on wire).

#### B. Separate Control Plane from Data Plane: Capability-Governed `Blob` / `Resource` Handles
- Keep `Switchboard` messages small and fast, and add a **host-owned immutable Blob / Resource store** to Loom (`Kind::Resource` or unforgeable `ResourceHandle` tokens in [`ZenHostApi`](file:///g:/programming/cpp/Zen/primary/Loom/include/zen/kernel/abi.h#L97-L120)).
- A weave creates/commits an immutable byte buffer (pixels, audio, mesh, large document snapshot) once and receives a lightweight capability token `(id, generation, content_hash, byte_len)`.
- Control messages carry the 16–32 byte handle across the bus in `O(1)`:
  - In-process SDL windows borrow `std::span<const uint8_t>` with **zero copies** (and can cache GPU `SDL_Texture*` keyed directly by `(id, generation)`!).
  - `wasm_box` and `IsolationHost` weaves read slices across `ZenHostApi` / shared memory.
  - Replay logs deduplicate blobs by hash instead of copying megabytes through every turn.

#### C. Add Synchronous, Grant-Checked `Port` Calls to `ZenHostApi` & `create(ctx)`
- Replace `create(void)` with `create(const ZenInitApi*)` and add **synchronous capability-checked `call_port(role_or_host, port_name, req_bytes, resp_sink)`** to [`ZenHostApi`](file:///g:/programming/cpp/Zen/primary/Loom/include/zen/kernel/abi.h#L97-L120) and `loom::Mail`.
- A port handler is strictly **bounded, non-yielding, and side-effect-isolated** (it cannot pump the bus; it computes an answer from an immutable catalog or read-only host projection and returns synchronously).
- *Immediate payoff in Zengine*:
  1. [`OperatorOffer`](file:///g:/programming/cpp/Zen/primary/Zengine/operator/host_surface.hpp#L164-L249), `ImageShare` double-`dlopen`, and shared-library global mutable statics **disappear completely**.
  2. Zengine's 4 custom C ABIs collapse back into Loom's single ABI.
  3. **Wasm (`wasm_box`) and process-isolated weaves can now evaluate operators natively** through `ZenHostApi`, governed by Loom's `Grant` table and logged deterministically if desired!
  4. Most of [`HostContext`](file:///g:/programming/cpp/Zen/primary/Zengine/workshop/weave.hpp#L91-L334)'s 20+ `std::function` lambdas become clean, grant-checked host ports or `Sense` claims.

#### D. Native Deadlines in `Reactor` + Additive Schema Evolution
1. **First-class monotonic deadlines in `loom::host::Reactor`**: Give Loom's reactor/switchboard a min-heap of wake deadlines (with deterministic `advance_to(ms)` in tests). When no timer is armed, **0 messages sit on the bus** (`drain_until_idle()` works again, [`timer::Rest`](file:///g:/programming/cpp/Zen/primary/Zengine/timer/rest.hpp) and [`TimerServiceT`](file:///g:/programming/cpp/Zen/primary/Zengine/timer/timer_weave.hpp)'s perpetual self-`Drive` loop vanish).
2. **Tolerant additive projection within a major version + load-time contract verification**: Allow schemas to mark new optional/defaulted fields as *additive* so v1.1 emitters don't force `v1`..`v9` handler duplication across every reader, while keeping unknown-field rejection on strict authoring files. And verify required `Ask`/`Sense` dependencies at plan realization so incompatible panes refuse cleanly instead of hanging forever at `OBJECTS (waiting)`.

---

### 3. How I Would Sequence & Guide the Project Forward

With you as sole author right now, your biggest advantage is **zero legacy external users**: breaking `ZEN_ABI_VERSION` from `11` to `12` costs you days today, whereas after splitting Workshop and publishing SDKs it will cost months.

I would sequence the work in **four deliberate phases**:

#### Phase 1: Untangle the `Zengine` ↔ `Workshop` Upward Coupling (Prep, ~1 week)
Before touching Loom or moving repos, sever the places where non-Workshop Zengine secretly reaches up into `workshop/`:
- Right now, [`app/main.cpp`](file:///g:/programming/cpp/Zen/primary/Zengine/app/main.cpp#L13) and `app/host.hpp` `#include "workshop/bus_tally.hpp"` and rely on `zengine::workshop::load::PlanExecutor` ([`load_execute.hpp`](file:///g:/programming/cpp/Zen/primary/Zengine/workshop/load_execute.hpp)).
- Move load-plan representation, `PlanExecutor`, and `BusTally` down into a neutral Zengine package (e.g., `realization/`), enforcing a strict one-way DAG: `Zengine packages` → `app`, and `Zengine packages` → `workshop`, never `app` → `workshop`.

#### Phase 2: Loom Foundation Upgrade ("Loom 2.0" Pass)
Stay focused inside Loom until the kernel truly matches Zengine's needs:
1. Fix the 3 core Gate/Value invariants (immutable flat `Value`, DAG visit bounds, structural schema identity).
2. Ship `Kind::Variant` (`ZEN_VARIANT`) + additive schema field rules.
3. Ship `ZenHostApi` synchronous `call_port` + `create(init_ctx)` + immutable `Blob` resource handles.
4. Put monotonic deadline wakeups into `Reactor` and trim `Switchboard`'s responsibilities (extracting 2PC `JointPublication` out of the hot dispatch core if Zengine barely needs it once variants/ports exist).

#### Phase 3: Pay Down Zengine's Workarounds & Prove Expressiveness With One Real App
Before splitting Workshop out, refactor Zengine onto the new Loom primitives and **build one non-trivial standalone application** launched by `zengine-app`:
- Delete `OperatorOffer`'s double-`dlopen` hack, delete [`implied.hpp`](file:///g:/programming/cpp/Zen/primary/Zengine/graphics/implied.hpp)'s wire-header surgery, move `Image` to `Blob` handles (unlocking real textures/sprites), and put `Timer` onto `Reactor` deadlines.
- Let a real target app (e.g., a small 2D interactive tool, synth/sequencer, or game) force `Maker`/`Flow` and `View` past toy constraints: multi-field state updates per trigger, full `fold` parity in [`generate_cpp`](file:///g:/programming/cpp/Zen/primary/Zengine/flow/generate.hpp#L50-L56), and `View` consuming the actual `graphics/elements/` controls with basic layout.
- Fix the packaging split so `zengine-app` exports self-contained runnable bundles that don't break if a downloaded folder moves.

#### Phase 4: Extract `Workshop` Into Repo #3 as a True Stranger
Once `Zengine` can build and run a real app via `find_package(zengine)` (including `zengine-window-sdl`!), move `workshop/` into its own repository:
- Workshop consumes Zengine **strictly via `find_package(zengine)`** (`ZEN_ZENGINE_DEV=OFF` by default), replicating the exact stranger-by-default discipline between Zengine and Loom.
- Decompose `workshop/weave.hpp` and `workshop/screen.hpp` so Workshop is just a well-factored Zengine host + panes, rather than a privileged monolith with 20+ host lambdas.

---

### Where Would You Like to Dig In First?

Since you're using me as a sounding board, we can drill down into whichever piece feels highest-friction or most controversial to your mental model of Zen:
1. **Synchronous `Port` calls vs. pure async `Mail` in Loom** (how to give weaves synchronous operator/host capabilities without violating determinism, replayability, or containment).
2. **`Kind::Variant` + `Blob` handles** (how to evolve Loom's value & wire format so `graphics/` and domain vocabularies become clean and fast).
3. **Simplifying `Switchboard` & UI coordination** (whether 2PC `JointPublication` and multi-turn fences are even the right tool for things like `zengine.opening` and menus).
4. **The `Zengine` vs. `Workshop` repo boundary** (what belongs in Zengine's core runtime vs. Workshop, and what Zengine's target "product" actually is).
