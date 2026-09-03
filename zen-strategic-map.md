# Zen Strategic Map

**Status:** PRIVATE LIVE AUTHORITY  
**Refreshed:** 2026-08-29  
**Role:** concise global direction, goal registry, and strategy/process router  
**Current major goal:** Workshop  
**Current product direction:** EDIT-1 — Choose What to Edit  
**Current execution state:** EDIT-R1 is accepted research and implementation-ready; no production packet is selected by this map

This file states current strategy. It is not a phase chronicle. Accepted reports and Git history
retain how the project arrived here.

## 1. Why Zen exists

Zen exists to put meaningful creative power in people's hands so they can:

> **Build. Learn. Explore. Grow. Share. Teach. Steward.**

The safety spine is an enabling condition, not the product's purpose.

> **Power is never gatekept — only made honest.**

Zen's present technical bet is native code at native speed, with explicit authority at semantic
boundaries and a machine-checkable account of the containment the host actually imposed. The
current security claim is abuse-tier containment on Linux, not kernel-escape resistance.

## 2. The strategic spine

```text
credible substrate
    -> maker-facing Workshop
    -> legible, buildable projects
    -> stranger-legible ecosystem
    -> hosted Weaves and operational services
    -> multi-author trust and continuity
    -> Zen-native teaching, building, and stewardship

north star across the path:
    playing and making become the same honest act
```

The path is pressure-ordered, not a guaranteed schedule. Goals may overlap when a live consumer
demonstrates a more important missing truth.

## 3. Architectural laws to carry forward

Repository laws and current source own exact mechanics. These are the strategic laws whose loss
would change future decisions.

- **No privilege by default.** A system component, debugger, Workshop surface, provider, or
  operator receives no special authority merely because Zen supplied it.
- **Loom holds grammar, not answers.** Domain policy stays with the host or participant that owns
  the fact.
- **The actor remains the actor.** A policy delegate may change a Session's authority; it does not
  perform the Session's work or launder authorship through itself.
- **One fact, one owner.** Discovery and enforcement should read the same store; presentation must
  not become a duplicate policy engine.
- **Different questions keep different owners, lifetimes, and authorities.** Composable,
  accepted, semantically meaningful, presently applicable, authorized, delivered, and successful
  are not one generic `valid` fact.
- **Authored intent and resolved observation stay separate.** Persist intent; derive current
  placement, availability, capability, and presentation from live owners.
- **Identity and provenance are distinct.** Identity says what should be resolved; provenance says
  which concrete incarnation supplied it. Paths, hashes, handles, indices, and function pointers
  are not durable semantic identity.
- **Saved intent resolves implementation at spend.** Retain stable references; hold the current
  provider while invoking; never persist a native callable.
- **Composition consumes existing power.** Native code should introduce only power Zen cannot
  already express. Generated code may carry ceremony; authored code carries meaning.
- **A source may suggest a document; the Editor owns opening and editing it.** Builder is one
  referrer, not the Editor's source authority.
- **Build intent and load intent are separate authored truths.** They join by artifact identity;
  neither silently absorbs the other's policy.
- **A presentation owns meaning inside its grant; the host owns room and spatial conflict.** Paint,
  hit-testing, ordering, clipping, and granted pane room spend the same resolved geometry.
- **Pointing names a subject for one request; selection is a state the maker entered.** Context
  remembers identity and re-asks the owner when the action is spent.
- **Refuse rather than pretend.** Unsupported bytes, units, authority, lifecycle, or platform
  claims remain visible and unchanged rather than being guessed, clamped, normalized, or dropped.
- **The same gesture may have different meanings only when its active contexts are mutually
  exclusive and explicit.** Dispatch, help, and remapping spend one action truth.
- **Evidence is proportional to the claim.** A green is not proof of everything; package,
  sanitizer, native-platform, live-interaction, and mutation evidence are used when their distinct
  failure classes matter.

## 4. Current system position

### Loom

Loom is a credible installed substrate for schema-governed values, messaging, senses, history,
capabilities, isolation, dynamic weaves, lifecycle, replacement, and host-owned authority policy.
Message acceptance discovery reads the same registered shape truth delivery enforcement reads.
Ask provenance and bounded host turns are explicit. SDL has been removed from Loom: the portable
pixel-layout brain remains, while Zengine owns the active graphical product medium.

Loom's current live HEAD is discoverable from Git. `REPOSITORIES.md` records repository location,
role, branch, and remote only; it does not record an accepted HEAD.

### Zengine

Zengine now has an installable stranger package and application-facing services built on an
installed Loom. It also owns:

- typed operator catalogs and host-resolved provider overlays;
- explicit provider provenance and reversible contribution stacks;
- authored load plans and build-recipe catalogs, joined only by artifact stem;
- a living realization owner whose frontier can wait, refuse, resume, and be inspected;
- generic message composition from a target's declared accepted shapes;
- a Surface/Input path with TUI and SDL media over one application meaning;
- verification lanes whose Linux CTest population is safely parallel and whose Workshop tests are
  split by semantic ownership.

The package is installable; Workshop itself remains a build-tree application because its current
Builder custody and graphical artifacts are not an installed product contract.

### Workshop

Workshop has crossed from application scaffolding into a place where ordinary development can
happen. A maker can load an authored project arrangement, inspect powers and realization state,
arrange a persistent desk, ask pointed things what can be done, edit one real source file, save,
build, realize a waiting artifact, inspect the result, and return to editing.

The latest accepted product arc includes:

- WUX: graphical voice, fine-grained pane geometry, independent-axis settlement, per-user
  config/state roots and isolation, restored desktop placement, and an attention surface for
  standing conditions;
- the build/test optimization sequence: compile proofs no longer mutate the main build tree,
  concurrent builds use distinct trees, and Workshop's monolithic test entry became six semantic
  suites;
- Loom SDL removal after portable proportional-layout and medium-agnostic outline coverage landed;
- CTX: contextual actions reference the one action truth and spend explicit subjects without
  turning pointing into selection;
- ARR: pane and whole-desk arrangement became two scopes over one vocabulary;
- EDIT-0: one ordinary multiline source document with exact byte/line-ending custody, atomic save,
  dirty refusal, deferred-paste sequencing, and the full save/build/realize/inspect loop.

## 5. Current direction: EDIT-1

The immediate product problem is architectural:

> **The Editor can edit a source, but it cannot choose a source.**

EDIT-R1 established the implementation-ready shape:

```text
Builder -----------+
Project Files -----+----> Editor.open(path)
future Edit Code --+
```

The host captures the launch directory once as the project root. A fourth catalog pane presents a
bounded, refreshable directory view inside that root. Builder keeps recipe discovery and calls the
same Editor-owned open-by-path door. Every entrant receives one normalized absolute spelling;
dirty-document refusal and the Editor's representation law remain authoritative.

EDIT-1 succeeds when Workshop can launch with no useful Builder selection and a maker can open
Project Files, navigate to a source, open it, edit it, save it, then use Builder independently.

The production prompt still owns a few product choices exposed by research: ordering, hidden-file
presentation, link-directory policy, pointer activation, whether the write-only recipe field is
removed, and whether an explicit project-root override is earned now. Those are bounded choices,
not a reason for another research phase.

EDIT-1 deliberately does not include tabs, search, file mutation, a VFS, a watcher, a provider file
protocol, language tooling, source-to-artifact inference, rebuild/reload, or hot replacement.

## 6. What follows EDIT-1

The next compelling maker loop is:

```text
point at a pane
    -> Edit Code
    -> resolve its source through the host's authored provenance
    -> Editor.open(path)
    -> save
    -> build the owning artifact
    -> realize or replace it under lifecycle law
```

Do not implement it as one guessed shortcut. It contains three separately owned joins:

1. pane/provider identity -> source or recipe provenance;
2. source/recipe -> build artifact;
3. artifact -> eligibility for initial realization or live replacement.

The first two can reuse existing authored project truth. The third is intentionally still a wall:
already-live artifacts are refused and tell the maker to restart. Live replacement becomes work only
when the loop reaches that wall with a real artifact and can preserve provider, weave, authority,
state, and failure ownership honestly.

Nearer follow-ons that remain pressure-driven include pane Inspect, source search/Unicode/multiple
documents, provider-contributed contextual actions, better default pane height/coarse arrangement,
and a graphical Flow projection over facts, values, operators, actions, and authority. None is
automatically next merely because its seam is visible.

## 7. Goal registry

### Goal 0 — Credibility detour

**Complete.** CI, population honesty, installed-package witnesses, containment truth, and current
law were repaired enough for application pressure to resume. Remaining defects belong to the live
backlog or repository seams; they do not reopen the goal.

### Goal 1 — Workshop

**Current.** Make Zen tangible, legible, authorable, and useful to a maker without giving the
environment unexplained privilege. Detailed current authority: `private/goals/workshop.md`.

### Goal 2 — Stranger-legible Zen

**Partially underway, not the current primary goal.** Zengine now has an installed package and
external-reader documentation. A real stranger build, human contributor front door, release
identity, and stability promise remain evidence-triggered work rather than maturity theater.

### Goal 3 — Hosted Weaves

**Not selected.** Create a dedicated Goal Map before the first hosting implementation. Bridge
reachability is not authentication; abuse-tier containment is not an escape-tier claim; operational
identity, signing, revocation, quotas, and supervision require live hosting pressure.

### Goal 4 — Multi-author continuity and trust

**Required long path, unbuilt as a product.** Runtime sender/role provenance exists. Durable human
authorship, artifact integrity, consent, trust policy, and continuity across authors do not.

### Goal 5 — Tutor, Builder, and Steward

**Horizon family.** Keep three roles distinct: Tutor teaches; Builder helps create and produce;
Steward observes, diagnoses, and helps maintain. AI strengthens intention and learning rather than
substituting for either.

## 8. Horizons and firewall

Committed horizons remain live debugging, a scalable kernel, replaceable weaves, and the north star
that modders are players. Possible synthesis remains a semantic computing environment in which
project declaration, visual presentation, live runtime, source, terminal, and failure are navigable
representations of meaningful things.

A horizon defines a completeness test. It does not authorize a demo-driven implementation. If a
horizon starts specifying framework details, move those details back behind current consumer
pressure or discard them.

## 9. Process doctrine

### Source and acceptance

- The phase prompt is scope authority.
- Current source and load-bearing tests decide what exists; reports are evidence and navigation.
- A report landing begins review. Founder acceptance decides disposition.
- Live Git answers current identity. A prompt states expected heads or names the accepted
  predecessor whose END is its baseline. `REPOSITORIES.md` is not a moving HEAD board.
- Private consolidation rewrites the smallest correct authority after acceptance; executors do not
  self-accept or edit private strategy.

### Prompt Contract v1

1. A substantial prompt has one authoritative stop-condition list. Body, verification, and report
   sections reference it rather than re-enumerating requirements.
2. Standing execution rules are referenced; only phase exceptions are repeated.
3. The baseline is stated in the prompt or inherited explicitly from the accepted predecessor.
4. Local understood repairs use compact QR prompts. Ownership, authority, lifecycle, public
   architecture, cross-subsystem contracts, and new maker capability use the production lane. A
   large production prompt without fresh research receives a source preflight before final authorship.
5. Substantial reports arrive as `<PHASE>-RB.md` plus `<PHASE>-evidence.md`. Review the decision
   layer first; open evidence when a claim needs audit. Small QRs use one compact report.

### Carrying-cost law

Current-facing law is rewritten in place and organized by subject, not phase. Phase codes and full
proof belong in reports and Git history. Raw capture is an inbox, not default reading. Closed pressure
does not stay in the live board merely to preserve a chronicle.

## 10. Private authority map

```text
zen-vision.md                         public purpose and human promise
zen-orientation.md                    broad architecture and working rhythm
REPOSITORIES.md                       stable repository registry; no HEAD custody

private/zen-strategic-map.md          global current direction (this file)
private/goals/workshop.md             current Workshop product authority
private/pressure.md                   open observed pressure and triggers
private/backlog.md                    work knowingly owed but not current
private/vision-deltas.md              compact routed decision/candidate index
private/raw-vision-deltas.md          raw source archive/inbox; not current authority
private/handoffs/current-executor-addendum.md
                                      current execution card
private/handoffs/Zen-FCO-v1.md        first-contact route

repository laws/references            exact current semantics
phase reports/evidence + Git history  proof and chronology
```

Refresh this map only when current direction, a goal's status, a strategic law, a horizon, or a
process doctrine changes. Routine phase closure belongs in the Goal Map; routine evidence belongs in
the report.
