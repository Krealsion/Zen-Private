Source: memory node `zen-companion-maps` (memory store commit 88e7b28); the body below is that node's, verbatim.
Moved from memory 2026-09-03.

# The three companion maps (landed 2026-07-17)

Vision authored three roadmap maps and Josh handed them to me for a codebase pass. They are
**destination-as-compass** documents — the same status as the horizons in [[zen-orientation]]:
held to *weigh* seams, **never** a build queue. They currently live in
`C:\Users\Joshua\Downloads\zen-map-{1,2,3}-*.md` (transient — like `zen-vision.md` before it, they
likely want a committed home in the repo eventually; flagged to Josh, not yet done).

The task Josh gave: pass over the code, flag what will **resist** these goals, bank it "to design
**against** not toward until that phase arrives." The resistances live in [[zen-roadmap-resistances]];
this node is just the anchor for what the maps *are*.

## Map 1 — The Core Tower (the Loom)
The stable substrate, small on purpose, changes only by named seam-pulls. Restates what's built
(L0 gate/value/schema · L1 switchboard · L2 weave authoring + access model · L2b standard_shapes +
relay · the service branches kernel/isolation/bridge) as a **holdable tower**. Introduces the
**known/unknown calling model** (unknown = bus door for strangers; known = `#include` + direct call
for owner/peers — "having a, not being a") and the **helper ladder** (generated → hand-written →
validating, all *caller courtesy over the bus*; the receiving gate is the only truth). Names three
future seam-pulls: the **emit-gate**, the **identity/Weaver phase**, **location-transparent addressing**.

## Map 2 — The Package Atlas (Zengine, the default set)
The shelf *above* the core: **packages** are peers you take/modify/ignore, defined by their
**conversational contract** (shapes spoken + roles expected), not their link graph. Atlas of the
Zengine port targets (Math/Types, Time, Assets, Render, Window, Input, Audio, Scene/Entity,
Animation, Tools) with a **Face** taxonomy (bus-never pure lib / helper-over-bus service / bus-only).
Key decisions: **SDL3** is the port target (new code is SDL2 — a priced swap); the old
`message_bus/` is **REPLACED by the Loom** (do not port — it's the "before" picture); the felt demo
is the **live spawner swap with cooperative handoff** (`enemy_wave_spawner` → `tank_rush`,
mid-wave state carries across), corrected to the demo-litmus (must show new *code*, not new *config*).

## Map 3 — Modding & Composition
How a stranger extends/replaces/shares safely, and what happens when many do at once. Core principle:
**optional participation above a mandatory floor** (latent handlers / speculative hospitality — write
handlers for messages that don't exist yet; the Loom mandatorily makes non-participation a clean
non-event). Splits **schemas (inert data, the REGISTRY) from behaviors (code, packages)** — never
conflate. The **conflict trichotomy** (works / reconciled-invisibly / caught-and-presented-with-the-why;
**reconciliation fails safe** — anti-Postel, irreconcilable is the honest default). The **Weave Manager**
(itself a weave; a small deterministic AI; static+dynamic triage; **bias toward surfacing**; born
*before* triage as the lifecycle steward orchestrating load/swap/handoff). **Multiplicity as a declared
tag** (`singleton` vs `multi`). Still-open: mod-surface declaration, mod-consent model, the commons.

## Map 2 corrections applied to the file (2026-07-20, Vision's rider)
- **The quarry's size.** "cmake junk / ~5k of 17k / real code ~12k" was **wrong and is retired**:
  no CompilerId files and no build dirs were present at import. The quarry is **~9k source lines
  (48 .cpp / 48 .h / 1 .hpp)**; the older figures came from a stale concatenation artifact.
- **The Tools tier correction (dated 2026-07-19).** Filing the console / Poke / **Weave Manager** /
  brokers under the *Zengine* atlas was a map imprecision. They are **substrate default tooling**:
  in the Loom *repo*, outside the exported *core*, replaceable like everything above the law.
  Zengine is the **domain** default set (Time, Render, Assets). **"Replaceable" is a property, not
  an address.**
- **Seam named: broker graduation.** StorageBroker/NetworkBroker are proven system components
  wearing a **test-fixture address** (`tests/weavelib/`); each moves to its real tooling home when
  its first **non-test** consumer arrives (the same named-trigger pattern as the kernel export).

## The tier model the maps introduce
**Loom (mandatory floor) → Loomstd (the small universal middle: the "std lib" of Zen) → Zengine
(default packages) → your packages.** `Ack`/`Refused`/`Result` already belong in Loomstd conceptually;
`Handoff`/lifecycle/save-on-death belong there too. The repo has **no Loomstd tier yet** — the standard
shapes live in `loom::` (core). This tier placement is one of the design-against items.

## How they relate to what exists
The maps are **mostly honest about the current state** — they repeatedly mark things "seeded / named /
built" and cite real seams already in the code (the bridge's schema-fetch-on-unknown as "the registry
in embryo"; `mount_mod`'s contained-stranger hosting; role-addressing; the SDL pixel-brain/skin split;
the reload-in-place lifecycle). The resistances catalog is therefore **not** "the maps are wrong" — it
is "here are the specific current code *shapes* that will need to bend when each phase's trigger fires,
recorded so we stop deepening them by accident." See [[zen-roadmap-resistances]].
