# Zen — First-Contact Orientation, v2

**Status:** PRIVATE ORIENTATION ROUTER — the first read for a Vision  
**Refreshed:** 2026-09-06 (v2 written 2026-09-05; v1: 2026-08-29)  
**Why v2 exists:** two Vision sessions in September proposed and drove a direction — an interpreted,
maker-authored weave — that no live authority had selected, and their hand-offs carried it forward
as "Phase 2." A third Vision inherited it and made two architecture errors before the founder
caught the frame. This document is written so that cannot happen quietly again. It bridges the soul
and the technical, states the direction in the founder's words, points at the further reading, and
ends with the questions a Vision must answer from source before it writes a single prompt.

During orientation, do not edit code, documentation, Git state, private strategy, or external
systems. Understand the project before accepting phase shorthand — *especially* shorthand from a
hand-off.

## 0. The soul, in one screen

Zen exists so people can **build, learn, explore, grow, share, teach, and steward** meaningful
digital work. Power is never gatekept — only made honest. The workshop is made of the same stuff
as the things you build with it; the beginner and the veteran do the *same thing* at different
heights. (`zen-vision.md`, "The Workshop".)

The founder's own words, 2026-09-05, which every phase serves:

> I crave coding. Real, C++ coding. I want to do that in an ecosystem that naturally supports
> extensibility and modularity. **Loom is that ecosystem**, and I want **Zengine to be, essentially,
> just an IDE** — one that does things no other IDE can do: reloading the code in place with
> seamless handoffs, using only partial compilation of the specific parts, and swapping it in.
>
> Think of the user first. The code is always built in support of the user's best interests.
> This part of the project is to make development **quick and easy. Not instant and braindead.**
>
> These pieces are able to create a great many things — that is their whole purpose. The important
> part is that we build the *right thing*.

## 1. The three sentences that are law

1. **Loom is the substrate.** Everything else stands on it and nothing else is required to.
2. **Zengine is a default set.** Nothing requires Zengine; it only enhances Loom. A person taking
   five files out of Zengine and using only those is a valid use, by design. Each package is
   independently linkable (`Zengine/README.md`, "The packages").
3. **Workshop is a tool for working within Loom** — the maker's IDE — not the product everything
   must route through. It receives no ambient authority and is built from the material it offers.

Two operational corollaries the September errors violated:

- **The running weave is the truth.** A maker never has to close Workshop for new changes to be
  pulled in. A new version arrives as a live replacement through Loom's handoff protocol: the
  state is converted by an authored migration, or the handoff halts and the incumbent keeps
  serving. Files on disk are for when the process is off. (`Loom/docs/guides/replacing-a-service.md`,
  `Loom/docs/laws/handoff-laws.md`.)
- **The Builder exists.** Workshop's Builder pane starts a real OS process from a named recipe and
  offers the artifact to the realization owner; `f` builds-and-realizes the waiting frontier. A
  maker at the Workshop has a compiler in the loop whenever they point at a header or a
  CMakeLists. (`Zengine/builder/`, `Zengine/docs/reference/builder.md`, `Zengine/agents/realization.md`.)
- **The panes are weaves (2026-09-06, VD-19).** Every pane a maker sees inside Workshop is a
  participating weave from the plan; the host keeps room, focus, realization and roots. Three
  tools already live across the pane protocol (`Zengine/introspection/`, `composer/`, the Pane
  Creator); the built-ins written as C++ inside the host (`workshop/screen.hpp`, `keymap.hpp`)
  are the debt the current arc pays. A prompt that adds host-side C++ where a weave could be is
  the mistake to refuse.

## 2. Read in this order

```text
private/handoffs/Zen-FCO-v2.md              this file
zen-vision.md                               why Zen exists; its human promise
zen-orientation.md                          vocabulary, spine invariants, honesty doctrine, rhythm
REPOSITORIES.md                             repository registry: path, role, branch, remote — never a HEAD board

private/zen-strategic-map.md                global direction and laws  (refreshed 09-06)
private/goals/workshop.md                   Workshop product authority (refreshed 09-06)
private/pressure.md                         open pressure and wake conditions
private/backlog.md                          work knowingly owed, not now
private/vision-deltas.md                    incorporated decisions; seeded candidates NOT promoted
private/goals/identity-phase.md             the settled design for author identity — a road
private/goals/two-forms.md                  live form / durable form / Flow as bridge — a HORIZON, not direction
private/handoffs/handoff-2026-09-06.md      repository state after the build-then-load arc; working with the founder; debts
private/handoffs/current-executor-addendum.md
                                            (STALE: an 08-29 card naming EDIT-1 as current — read §6–§8 for its laws, not its state)
private/machine_facts.md                    the founder's machine (read, never edit)

Zengine/AGENTS.md                           the one mandatory read; then its router
Zengine/README.md                           the package table — what exists
Loom/AGENTS.md                              the one mandatory read; then docs/CONTEXT.md
Loom/docs/README.md → guides/mental-model.md → guides/writing-a-weave.md → guides/replacing-a-service.md
```

Then the routed owner of whatever the task touches — and nothing before that. Do not read
`private/raw-vision-deltas.md` by default.

## 3. Zengine, as a flowchart

Derived from every package's `CMakeLists.txt` at Zengine `1ed28d1` (2026-09-05). Arrows read
"links".

```text
                         LOOM   core · kernel · switchboard · history · terminal
                           ▲   find_package(loom) against an INSTALLED prefix — Zengine is a stranger
   ┌───────────────────────┼─────────────────────────────────────────────────────────┐
   │ EXPORTED (zengine::…) — header-only vocabularies plus one loadable weave each     │
   │   ui                                                                             │
   │   activation                                                                     │
   │   operator                                                                       │
   │   component                                                                      │
   │   timer        → activation, operator                                            │
   │   surface      → activation, timer-vocabulary                    (+ SDL medium)  │
   │   input        → activation, timer- and surface-vocabulary       (+ SDL medium)  │
   ├─ NOT EXPORTED ──────────────────────────────────────────────────────────────────┤
   │   builder      → activation, timer-vocabulary        a recipe → an OS process    │
   │   introspection→ activation, component, input/surface-vocabulary                 │
   │   maker        → operator                            a weave from data — PAUSED  │
   │   snake        → input, surface skins, timer         the worked example          │
   │   workshop     → builder-, composer-, ui-, surface-, input-, timer-vocabulary,   │
   │                  component, introspection-view, operator (+basic);               │
   │                  loom history, terminal              THE IDE                     │
   └─────────────────────────────────────────────────────────────────────────────────┘
```

The maker's path through the IDE, as it exists today (`private/goals/workshop.md` §2, §3):

```text
PROJECT TRUTH   object document · pane setups · load plan · build recipes · source files
                (build intent and load intent are separate; they join only by artifact stem)

   Project Files ─┐
   Builder ───────┼─► Editor.open(path) ─► edit ─► save (atomic; dirty refuses)
                  │
                  └─► Builder: recipe ─► OS process ─► artifact
                          └─► realization owner: waiting frontier ─► realize ─► live weave
                                     live artifact, same shapes  ─► RELOAD IN PLACE (state kept) ─► promote | revert
                                     live artifact, shape changed ─► REFUSED in the maker's words   ◄── THE WALL
   inspect: Powers (operator stack) · Introspection · Message Composer (a message from the
            target's own accepted shapes, to the weave you just made)
```

The wall's first rung fell on 2026-09-05: a rebuilt same-shape artifact reloads in place through
Loom's `zen.ReloadWeave`, and the maker promotes or reverts it (Zengine PRs #11–#14). The second
rung stands: a changed shape is refused and not replaced. Loom already has prepared replacement and
the authored handoff (PR-01..09, HANDOFF-01..03); Workshop does not drive them yet (P-WORK-07,
second rung). Join 1 — a source reached from the pane that draws it — is not built (P-WORK-06).

## 4. The direction — 2026-09-05, in the founder's words

The IDE loop, quick and easy:

```text
schema builder                 author a ZEN_SHAPE without writing the macro by hand
instance authoring             fill an instance of a schema — initial or test data
generated boilerplate          the class, the handlers' skeleton, the CMake target — generated ceremony
build                          Builder, as it exists
messages from Workshop         Message Composer, as it exists — talk to the weave you just made
reload in place                partial compilation of the specific part, seamless handoff, swap in
```

**Interpreted execution is useful only because it runs with no compilation.** The `maker/`
package — a weave interpreted from a data definition — is merged (Zengine PR #10) and **PAUSED**:
kept in the default set as a library, no further phases, until interpreted execution is actually
needed. The founder keeps it as a pressure point: the day a maker needs a weave that runs with no
compilation, the consumer exists and the seam is already cut. It is not easier than writing the code when the
boilerplate can be generated, and less necessary still when the schema builder, instance authoring
and the Message Composer exist.

`private/goals/two-forms.md` (live form / durable form / Flow as the bridge) is a **horizon**: a
completeness test that helps judge a seam, never an authorization to build one. The orientation's
rule stands — "do not use the destination to authorize work ahead of a real consumer."

**2026-09-06, evening — the arc that enters the loop.** Reading `keymap.hpp` and `screen.hpp`
whole, the founder named the material as the problem: an AI wrote C++ inside the host where Loom
asked for weaves. Direction, in his words: split, split, split, until splitting would make a thing
too small to be useful — and even then those become operators, and compose into the thing. Every
pane a maker sees is a participating weave; make new, previously-unspeakable panes, load them and
see them work without closing Workshop. Preconditions he set: send fate, then an ask that can be
answered with progress before it closes (Loom); the plan row as a request for authority that the
Weaver, set by the maker, grants or refuses — a refused weave is told and may declare itself
broken or ask to be unloaded. Shape collisions wait for their first instance. VD-19..21 hold it;
the maps carry it.

## 5. Ideas to carry (from v1, still true)

- Loom holds grammar, not answers. No privilege by default is the keystone.
- The actor remains the actor; policy does not launder authorship.
- Authored intent and resolved observation are different truths. Identity says what should be
  resolved; provenance says which incarnation supplied it.
- Composition consumes existing power; native code introduces only missing power. Generated code
  carries ceremony; authored code carries meaning.
- A grant bounds speech, not what in-process native code can touch. Abuse-tier containment is not
  escape resistance. Bridge reachability is not authenticated identity.
- Refusal beats a false success, fallback, normalization, or platform claim. "Proven" names the
  evidence and configuration that proved it. Green means nothing complained.
- Build intent and load intent are separate truths joined by artifact stem. Initial realization and
  in-place reload are two acts of one owner; changed-shape replacement is not yet driven by
  Workshop. Provider overlay is not artifact hot reload. Nothing is upgraded silently.
- TUI and SDL are media over one application meaning.

## 6. Where things stand — 2026-09-06

| repository | main | note |
|---|---|---|
| Loom | `b296032` | PR #4, one documentation paragraph (the copier's shape-name collision); before it `0a66374`, the doc sweep. No Loom source changed in September |
| Zengine | `406ea57` | PR #14 (drain clock; refusal journaled); #13 repairs; #12 pick-and-load; #11 reload in place; #10 `maker/`; #9 family table; #8 methods; #7 residues; #6 the split |

Landed since the maps' previous refresh (08-29), consolidated into them on 2026-09-06:

- **EDIT-1** — Project Files, the one `Editor.open(path)` door, project root captured
  (`agents/workshop/project.md`, `editor.md`; tests `"EDIT-1: …"`). P-ACT-01 is closed in fact.
- **WUX-R14** — research: pane interiors have no durable representation (report only).
- **The documentation arc** — the Workshop compiled once (`workshop/<subject>.cpp` under
  `zengine-workshop-logic`); 30 `WL-` registers under `agents/workshop/`; 12 `VM-` method
  registers under `agents/verification/`; `agents/verification.md` a router; `AGENTS.md` ≤ 20 KB.
- **The law-register family table** — one row per family per directory (`WL`, `MW`); the seam the
  four over-budget documents (`operators`, `panes`, `realization`, `surface`) will use as registers.
- **`maker/`** — the interpreted weave, its three `MW` registers, three decision records, 26 pinned
  cases. Paused (§4).
- **Build, then load** (PRs #11–#14, 2026-09-05–06) — a rebuilt same-shape weave reloads in place,
  state kept, on the same `WeaveId`; the new image is not the default until promoted; revert;
  "pick buildable" authors a recipe row; "load it" authors a plan row; a project catalog and plan
  at the project root are in force at launch; the `builder` suite's drain has a clock; a realize
  refusal is kept whole in `--log`.

**Consolidated 2026-09-06** by Vision on the founder's word: `zen-strategic-map.md` (§5 landed,
§6 the IDE loop with join status, §8 two-forms as horizon), `goals/workshop.md` (§2, §6, §7, §11),
`pressure.md` (P-ACT-01 closed; P-WORK-07 first rung closed; P-WORK-14..17, P-BUILD-05..07,
P-LOOM-06 added; two-forms seeded), `vision-deltas.md` (VD-15..17, VS-05). Not touched:
`backlog.md` (refreshed 08-29; read it with that date in mind).

**Not selected by this document.** Candidates the live authority names, for the founder to choose
among: a source reached from the pane that draws it (P-WORK-06, goal map §7 joins 1–2); the
changed-shape rung of live replacement (P-WORK-07); the IDE flow of §4 — the schema builder,
instance authoring, generated boilerplate — of which the Message Composer, the Builder, reload in
place and promotion already exist; and, cheap and owed, the three remaining spin-bound loops
(P-BUILD-05).

**Selected 2026-09-06, by the founder,** from those candidates: the head of §4 — a new weave
authored from Workshop (generated boilerplate carrying the smallest schema builder it needs),
research first: `prompts/new-weave-research.md`. Generated C++ is the default form; the definition
document stays a horizon and `maker/` stays paused (VD-18). Second consolidation pass the same
day, by the Vision that inherited: VD-18 and the delta ledger, this file's §2 flags, the strategic
map's §10 route to this file, the executor addendum marked stale. The addendum still owes a rewrite.
The same evening the founder selected the pane-weave arc ahead of new-weave production (VD-19..21);
§1's third corollary and §4 carry his words, and `pressure.md` gained P-WORK-18 and P-WORK-19.
**2026-09-07:** Zengine PR #15 (`PaneActions`, Powers the consumer, BL-DEF-03 closed) and PR #16
(Files as a weave: three doors, per-mode rows, the conversion, the built-in gone) merged — the
arc's first migration. Heads: Zengine `main` past `d4815cc`'s merge; Loom `b296032`. Next: the
Builder migration with `RecipeCatalog` v2 (P-WORK-20); the Composer is the next `PaneActions`
consumer (P-WORK-21). `Zen/private` committed at `d36cf7f` and again after this pass.

## 7. How a Vision fooled the founder — and how to tell

What it looked like, so it is recognizable:

- A hand-off proposed a direction ("the missing layer is the interpreted, stateful, maker-authored
  one") as if it were the tree's fact. No live authority had selected it; VS-01 and VS-04 were
  explicitly *not promoted*. The next Vision inherited the frame and researched inside it.
- Package prose claimed "every weave in this repository so far is C++" and "a maker has no compiler
  in the loop" — false, because `builder/` and the Builder pane exist. Nobody had read them,
  because nobody's grep was aimed at them.
- A review proposed converting a stale state *file* in a loader, when Loom's model is that the
  running weave is the truth and a new version is a live replacement with an authored handoff.
- Every one of these sounded fluent and confident. None carried a file anchor to the tree.

The standing rules for a Vision, the way the executor constitution is for Ceecee:

1. **Read §2 before anything.** A Vision that has not is not yet a Vision.
2. **Every architectural claim carries `file:line` at a named head.** In a prompt, a review, or a
   chat answer. "I believe" without an anchor is a flag, not a finding.
3. **A prompt's premises are traced by the Vision, not inherited.** Hand-offs carry state, evidence
   routes, and lessons. **They never carry direction.** Direction lives in the maps; a hand-off that
   proposes one is a candidate for `vision-deltas.md`, not a phase.
4. **Say "I have not read X."** Never "X does not exist" or "so far" about a tree you have not
   measured. The Builder was invisible to three sessions for exactly this reason.
5. **Before proposing anything, answer §8 in your own words with anchors**, and let the founder
   spot-check two. One wrong anchor ends the benefit of the doubt.
6. **Ceecee has final say on architecture, from the actual code in motion** (the founder,
   2026-09-06). A prompt states the outcome, the fence and what not to do; where it says HOW, that
   is a guess made before the code was read at the heads, and the executor overrides it and records
   the divergence. Nearly every failure so far had a Vision's or the founder's condition at its
   root; the fewer conditions forced, the fewer of our misconceptions reach the tree. **A STOP is
   honored, never routed around**: when the executor stops on a false premise, the phase ends there
   and the premise is fixed — time lost now, much more saved later.
7. **The review gate is the whole architecture, not decision-by-decision** (the founder,
   2026-09-06): the proposed architecture as a whole if every recommendation is applied, sample
   code where technical specificity is warranted, what the decisions are trying to accomplish,
   where there is room to diverge, and which choices would be mistakes. Verified on the branch,
   not the report's account of it.
8. **Every prompt and every CONTINUE is handed to the founder with its temperature named** — in
   the Vision's message beside the path, never as a line inside the prompt: the executor already
   knows what it is, and a label it cannot act on is noise at best and wrong at worst. The
   temperature is a fact about how the prompt was WRITTEN — what it assumes of the mind that reads
   it — so the founder runs it on the right Ceecee (the founder's vocabulary, 2026-09-07). **Hot**:
   written for a Ceecee that has already run prompts in this thread; carries only what changed and
   dies in a fresh session. **Warm**: written for a fresh Ceecee session with its memory store
   intact — the standard phase prompt: heads, routes, the fence, the not-to-do list. **Cold**:
   written for a Ceecee with no memory of any kind, acting only on the prompt,
   `Zen/executor-constitution.md` and the repositories' `AGENTS.md`; it needs everything a warm
   prompt has plus where to begin and how to find its way, and it is what a cold audit is thrown
   at. The label existed as `warm executor` / `cold executor` on the surrounding prose in
   `private/history/Vision-Handoff-8-3-26.md` and was never defined in a live authority;
   `zen-orientation.md` §8's "cold start" is, in this vocabulary, a warm one — the founder's
   public sentence to fix.

## 8. First-contact response — answer these before you propose anything

1. Why does Zen exist, in one sentence of your own, and which line of `zen-vision.md` is it from?
2. What do Loom, Zengine, Workshop, Night Lab, and Arena each own? Which of them is required?
3. Draw the maker's path through the IDE today and name the wall. Which package refuses it, and
   which pressure entry parks it?
4. State the three laws of §1 and one place in source each is enforced.
5. What does Loom do when a v2 weave arrives over a live v1 whose migration is not authored?
   Cite the law.
6. What is explicitly *not* claimed — containment tier, bridge identity, grant scope?
7. Which source answers a disputed fact — and in which order do prose, law, source, and tests rank?
8. Name two things a previous Vision got wrong, and the file that would have prevented each.
9. When every pane is a weave, what does the host keep — and where does a loaded pane's authority
   come from? Cite the plan row's grammar, `Kernel::load`'s two overloads, GATE-05 and the Weaver.

Do not propose implementation until those answers agree with current source and the live
strategy documents. If they do, propose one phase, in the founder's direction (§4), at the smallest
correct consumer — and ask whether he wants the begged questions answered before answering them.

## 9. What this document's author did and did not read

Read whole at the heads in §6: `zen-vision.md` (the Workshop block), `zen-orientation.md`,
`REPOSITORIES.md`, `zen-strategic-map.md`, `goals/workshop.md`, `Zen-FCO-v1.md`,
`executor-constitution.md`, both September hand-offs, `Zengine/AGENTS.md`, `Loom/AGENTS.md`,
`Loom/docs/README.md`, the `maker/` package and its report-backs, every package's `CMakeLists.txt`.
Read in part: `pressure.md` (headings, P-WORK-07), `vision-deltas.md` (headings, VS-04),
`Loom/docs/guides/mental-model.md` (opening), `replacing-a-service.md` (skim), Loom's kernel,
schema, gate, handoff and switchboard sources at the lines cited in the maker reports.
**Not read:** `Zengine/workshop/` source, `agents/workshop/*` registers beyond grep,
`agents/realization.md` and `agents/operators.md` beyond grep, `docs/workshop/*`, Loom's
`docs/reference/*` and `docs/laws/*` in full, `machine_facts.md`, Night Lab, Arena. A Vision who
needs any of those reads them before speaking about them.
