Source: memory node `zen-roadmap-resistances` (memory store commit 88e7b28); the body below is that node's, verbatim.
Moved from memory 2026-09-03.

# Roadmap resistances — design AGAINST these, not toward them

Josh's framing (2026-07-17): "flag anything that will resist the docs' goals … bank them as
memories to design against not towards until that phase arrives. Purely roadmap items to keep the
coding on an honest track." So this is **not** a build list and **not** a bug list. Each item is a
current code shape that is *correct for today* but points the wrong way for a named future phase —
recorded so we **stop deepening it by accident** and recognize the trigger when it fires. The maps
themselves are [[zen-companion-maps]]. Everything here was read by hand in one thread
([[no-subagents-on-zen]]); verify file/line against current code before acting (staleness rule).

> **Standing caution:** most of these are *already* named seams (in [[zen-orientation]]'s trigger
> map, in `DESIGN.md`'s "named successors", in [[wsl-bridge-phase]] and [[identity-phase-design]]).
> This catalog does not invent them — it points each one at the **exact code that resists** and at
> the **map goal** it resists, so the design-against is concrete. Do not treat any of these as a
> reason to build ahead; the honest default stays "build less, hook the seam, let the trigger pull."

---

## R1 — Addressing is WeaveId + singleton-role → resists replacement, handoff, location-transparency, `multi`
**The single biggest cluster; Maps 1, 2, and 3 all pull on it.**

- **The shape:** a `WeaveId` (`switchboard/message.hpp`) is an **opaque, bus-local `uint64`** —
  meaningless across any bus boundary. Contract-directed reach is **role addressing**
  (`send_to_role` / `Grant::allow_to_role`), but a role is **singleton by construction**:
  `Switchboard::roles_` is `map<string, WeaveId>` (one holder), and binding a role already held
  **throws** (`switchboard.cpp` ~line 104, "roles are singletons in this phase"). A role rebinds to
  a *new* holder only via unregister-then-register — **not atomic**, and there is **no op that
  rebinds a WeaveId behind a new participant** (already named in [[wsl-bridge-phase]]'s relocation
  litmus: "one new primitive, not zero").
- **Resists (Map 2 felt demo):** `enemy_wave_spawner → tank_rush` swap. If callers address the
  spawner by `WeaveId`, the successor's *different* id breaks them; if by role, the swap needs an
  **atomic role rebind to a different holder** that today throws.
- **Resists (Map 3):** "swap any weave for another that speaks the same shapes"; **`multi`
  multiplicity** (`roles_` can hold exactly one — there is no many-holder path; `DESIGN.md` names
  "the concurrent-instance version resolver … all brokers stay singletons" as unbuilt).
- **Resists (Map 1):** location-transparent addressing (a contract-address resolving to a different
  host) — `WeaveId` is the opposite of that.
- **Trigger:** relocation / the felt-demo swap / distributed Zen / the third broker's `multi` need.
  Certain that *one* of these fires.
- **Design against, not toward:** keep addressing **role-first** wherever a consumer must survive a
  swap (the UI `Presenter.source_role` already models this correctly — copy that instinct). Do **not**
  hand out raw `WeaveId`s as durable references, and do **not** deepen the singleton assumption into
  new call sites without noting it. When a swap/handoff phase arrives it wants **atomic role rebind**
  and (eventually) a **multi-holder role** — leave `roles_` shaped so that becomes `map<string,
  vector<WeaveId>>` + a resolver, not a rewrite. The singleton *is right for the brokers* (storage
  must be exactly one) — the tag `singleton`/`multi` is what's missing, not the singleton itself.

## R2 — All reload paths are same-identity/same-state-schema → resists the cooperative handoff
- **The shape:** every "swap" today is **snapshot → revive against the same state schema, same
  WeaveId**: `Switchboard::reload`/`swap_state` (gate the candidate against *the* state schema),
  `Kernel::reload_from` ("swap the library behind the same WeaveId … a state-schema **version
  mismatch is a clean refusal**"), `IsolationHost::reload` ("re-spawn from **the same .so**, keep
  the SAME WeaveId/grant/role"). The `Weave` contract's lifecycle is `snapshot()/revive()/policy()`
  (`weave_contract.hpp`) — **no handoff hook, no `wake_messages[]`.**
- **Resists (Map 2 / Map 3):** the felt demo's **cooperative handoff** — `PrepareShutdown →
  {state, wake_messages[]} → the successor (a DIFFERENT weave with a DIFFERENT state shape) revives`.
  Current `reload_from` would **refuse `tank_rush` as a version/shape mismatch**; there is no path to
  hand a state *bundle* to a differently-shaped successor, and nothing carries pending outbound
  intent (`wake_messages[]`) across the swap. Map 3's "augmentation composes; replacement arbitrates"
  replacement half has no mechanism.
- **Already named:** `DESIGN.md` → "**Authority-transfer** — promoting a *different* Weave into a
  role (loud, user-gated, with a **state handoff + transition-window quiescing**). P1/P2 ship
  reload-in-place only." This IS that seam.
- **Trigger:** the Manager/handoff phase (the felt demo carries it).
- **Design against, not toward:** treat the current reload as **reload-in-place only** and say so;
  do not let "reload" quietly grow into "replace-with-different-weave" without the handoff protocol.
  The handoff is a **cooperative message protocol** (the outgoing weave *produces* the bundle), not
  an extension of host-side snapshot/revive — keep it out of the `Weave` vtable (the contract is
  deliberately minimal) and shape it as gated messages.

## R3 — Lifecycle orchestration is host-only C++ API → resists "the Weave Manager is itself a weave"
- **The shape:** load/reload/unmount/kill/swap/`record_grant_delta`/role-bind are **host process
  authority**, not reachable by a participant: `Kernel` methods, `IsolationHost` methods, and the
  Switchboard **root** authority (`send`/`publish`/`send_to_role` ungated, `register_weave`,
  `unregister_weave`, `kill`, `reload`, `swap_state`). The host "holds the pen" by design
  (`record_grant_delta` comment: "the host, never a Weave, decides").
- **Resists (Map 3):** the Weave Manager is, on-thesis, **itself a weave** — "a participant holding
  a job, inspectable, replaceable, non-privileged." Born *before* triage as the **lifecycle steward
  orchestrating load / swap / cooperative-handoff**. But a weave cannot drive any of the above today
  — those powers are not projected onto the message boundary.
- **The precedent to follow:** [[wsl-bridge-phase]] already did exactly this move for a *different*
  power set — it turned discovery/tap/send into an **operator-protocol of gated messages** and
  stamped the sender from the connection. The Manager needs the same: a **lifecycle-operator
  protocol** (load/swap/handoff/grant-delta as messages), gated, with the host as the authority the
  protocol is checked against. (Note the tension to resolve honestly: a message-driven Manager still
  bottoms out in *host* authority — the "born as a weave" claim must not smuggle root powers into an
  ordinary grant. This is the same authority-transfer wall as R2.)
- **Trigger:** the Manager phase (Map 3 birth-order: Manager first, small, demo as its consumer).
- **Design against, not toward:** when the Manager arrives, **do not** give it a privileged C++
  handle to the Kernel/Host — give it a **message protocol** and keep the host holding the pen.
  Meanwhile, don't add new lifecycle powers *only* as host C++ methods without noting they'll want a
  message face. Keep conflict/lifecycle outcomes as **structured values** (see R4/R5), because a
  weave-Manager can only triage what arrives as data.

## R4 — Schema namespace is flat `(name, version)` with a hard global throw → resists multi-author modding + cross-language sharing
- **The shape:** the `Registry` keys on `(name, version)` and **throws `SchemaConflict`** when the
  same key is registered with different content (`registry.hpp`; spine invariant 3: "a frozen
  `(name, version)`, a content-id over the shape"). Shapes are shared between weaves by
  **`#include`-ing the same C++ header** — fine for same-codebase weaves.
- **Resists (Map 3):** the modding case is *exactly* two strangers publishing different shapes under
  the same `(name, version)` — today that's a **hard throw at registration**, and one mod simply
  can't load. Map 3 wants the **third namespace coordinate `(author, name, version)`** so different
  authors' same-named shapes are distinct, not colliding. And "a mod written later, by someone else,
  in another language … can't include your header" → contracts must be shareable **as data**, which
  `#include` is not.
- **The embryo that's right:** `kernel/schema_codec.hpp` already encodes a `Schema` **as a gated
  Value** (`zen.SchemaDesc` meta-schema, `encode_schema`/`decode_schema`) — Map 3's "registry in
  embryo." It captures name/version/fields/types **only** — not author, access tags
  (`ZEN_EXPOSE`/`ZEN_HIDE`), emit-set, or multiplicity — so it speaks the *shape* but not the
  *mod-surface*.
- **Trigger:** first cross-author trust decision (= the identity/Weaver phase; see
  [[identity-phase-design]]) and/or first non-C++ weave.
- **Design against, not toward:** hold `(name, version)` as **provisional two-thirds of the real
  key** — do not assume it is globally unique forever, and do not add logic that *depends* on
  `SchemaConflict`-as-a-throw for correctness in a way that a `(author,...)` coordinate would break.
  Keep **schemas (inert data) and behaviors (code) separate** (Map 3's cardinal split) — resist any
  convenience where "import a message type" drags in behavior. Promote the schema-as-Value codec
  toward canonical only when a real cross-language/cross-author consumer pulls it (not before).

## R5 — Composition conflicts are exceptions, not triageable values → resists the trichotomy
- **The shape:** conflicts today are a **mix** of thrown exceptions (`SchemaConflict`; role-already-held
  `throw std::invalid_argument`) and clean-refusal structs (`ReloadResult.version_mismatch`,
  `RefusalReason`/`Refusal`, `ReviveOutcome`). The version-mismatch path is the well-shaped one — a
  *value* the caller inspects, old code keeps running.
- **Resists (Map 3):** the conflict trichotomy needs every conflict to be a **detectable,
  explainable value** a Manager can triage (works / reconcile / **surface-with-the-why + confidence**).
  A `throw` is a crude fail-safe: safe (no silent wrong-merge — good, it honors the cardinal law) but
  **not surfaced with a why and a wheel**. Map 3's "version mismatch is a *warning*, not a break —
  knowable only by running it" maps directly onto making these **static-triage values**, not throws.
- **Trigger:** the Manager phase / first real multi-mod load.
- **Design against, not toward:** the honest default (refuse rather than silently merge) is
  **correct — keep it**. But prefer **structured refusals over thrown exceptions** for anything that
  is a *composition* event rather than a *programming* bug, so a future Manager can attach a "why"
  and a confidence instead of catching an exception. `ReloadResult`/`Refusal` are the good pattern;
  the registration-time `SchemaConflict` throw is the one most likely to need to become a surfaced,
  triageable event when modding arrives.

## R6 — Known, lighter-weight items (fold-ins, not their own phase)

- **The emit-gate carve-out (Map 1 seam-pull).** `Mail::send/reply/publish` is the reserved
  chokepoint for gating emitted shapes against declared `Emit<...>`, deliberately **not enforced**
  (`weave.hpp` Mail comment) because not every weave's emit-set is statically enumerable; grant-level
  emit-enforcement exists (`emit_default_grant`) but the **standard-reply ride-along** (poke answers
  / `Ack`/`Refused`/`Result` emitted without an `Emit<>` declaration) is a **pinned known carve-out**.
  Map 3 sharpens the principle: *participation is optional, **honesty is mandatory**.* Design-against:
  don't let the carve-out widen; when "undeclared emit of a standard reply shape" must close, that's
  the named pull.
- **No Loomstd tier (Map 3).** `Ack`/`Refused`/`Result` live in `loom::` (core), not a distinct
  optional middle tier; `Handoff`/lifecycle/save-on-death have **no home**. Design-against: when the
  handoff/lifecycle helpers arrive (R2), give them a **Loomstd** home (optional, universal), not the
  mandatory core — resist dumping domain-flavored behavior into `loom::`.
- **SDL2, target is SDL3 (Map 2, decided).** `zen-ui-sdl` uses SDL2 (2.30.11 + SDL2_ttf via pinned
  FetchContent, `CMakeLists.txt`; `#include <SDL.h>` in `sdl_ui.hpp`). The Phase-B audit already
  **priced** the SDL3 swap (a new executor for four draw ops + one text-width fn + one event mapper,
  enforced by the build graph). Design-against: keep **all `SDL_` quarantined to the skin** — the
  pixel-brain (`zen-ui-pixel`) stays SDL-free — so the migration stays a priced swap, not a rewrite.
  Do **not** inherit the original Zengine's `rttr` runtime reflection without a reason (the new code
  deliberately avoided reflection; C++26 reflection is the eventual answer).
- **Packages are libraries, not conversational contracts yet (Map 2).** The repo is organized as
  link-target libraries (`zen-core`, `zen-switchboard`, `zen-ui`, …); Map 2 defines a package by its
  **conversational contract** (shapes spoken + roles expected), swappable for anything that speaks the
  same shapes. Design-against: as Zengine ports land, resist deepening **link-graph** coupling where a
  **conversational-contract** boundary is what the map wants (the SDL skin's four-op replaceability is
  the model). Minor today; matters when the first real package port happens.

## What did NOT resist (recorded so the catalog is honest, not alarmist)

- **Optional participation / clean non-event floor** — **satisfied.** A directed send to a
  non-accepter is a clean `RefusalReason::NotAccepted` (never a crash); publish to zero accepters is
  a legal 0-count; `WeaveBase::handle`'s no-match throw is guarded-impossible for a *delivered*
  message (accept-set == handler-set by construction). Latent handlers work. The **one caveat**:
  pre-handling a *foreign/future* shape needs the C++ struct to exist → that's the R4 schemas-as-data
  gap, not a floor gap.
- **Contained-stranger hosting** — **built** (`IsolationHost::mount_mod`: floor authority, identity =
  `.so` content-hash, host-recorded deltas on top). Map 3's "run a stranger's mod contained" — the
  hard one most modding systems lack — is real.
- **Schema-as-Value codec, role-addressing, the pixel-brain/skin split, reload-in-place, provenance
  (bus-stamped sender)** — all real and correctly shaped; the maps cite them accurately as seeds.
- **UI primitive vocabulary is a closed enum** (`WidgetKind`, per-kind arity in `tree_of`) — judged
  **mostly aligned, not a resistance**: the intent vocabulary is deliberately closed at the primitive
  level and **open at the component level** (compose schematics from existing kinds). A stranger
  extends by *composing components*, not by adding primitives. Watch only if a mod ever genuinely
  needs a new primitive rendering intent — then Map 3's mod-surface-declaration tension is real.

## Since written

Added 2026-09-03, when this file moved out of memory. Nothing above this heading was rewritten. Each line names its owner; verify there before relying on it.

- **R2 fired.** The cooperative handoff is a message protocol, as designed against: the Weave Manager's `SwapWeave` composite and the handoff letter (`zen.PrepareShutdown` → `zen.Bequest` / `zen.ClaimBequest`, Loom `docs/reference/lifecycle.md`), then prepared replacement (Loom `docs/laws/replacement-laws.md`, PR-01..09: a sealed candidate, an authenticated readiness answer, commit at one admission dispatch, and it preserves nothing) and authored handoff (`docs/laws/handoff-laws.md`, HANDOFF-01..03: a temporary migrator weave carries a value across schema identities, and no Loom API was added for it); reload-in-place and swap stay two ops.
- **R3 fired.** The Manager is an ordinary weave and lifecycle orchestration has a message face: Loom `include/zen/kernel/manager.hpp` drives load / swap / reload / list by gated messages to the kernel's control door, holds exactly `load_capability` and no privilege, answers in `zen.Result` / `zen.Ack` / `zen.Refused`, and the host keeps the pen (lifecycle authority is host-minted and board-relative, LIFE-04 in `docs/laws/lifecycle-laws.md`).
- **R1 moved in part.** Prepared replacement admits a verified successor into the role with no window; `SwapWeave` keeps its unheld window at floor tier and names an atomic rebind as a refinement; the Manager's own rule is role-first addressing. The `singleton` / `multi` tag was not re-measured.
- **R5 moved at one boundary.** Every outcome crosses the Manager as a value, never a throw (`manager.hpp`: a composition event is data a steward can triage); the registration-time `SchemaConflict` throw was not re-measured.
- R4 and R6 were not re-measured on 2026-09-03.
