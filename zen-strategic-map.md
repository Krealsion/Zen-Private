# Zen Strategic Map

**Status:** PRIVATE LIVE AUTHORITY  
**Refreshed:** 2026-09-17\
**Role:** concise global direction, goal registry, and strategy/process router  
**Current major goal:** Workshop  
**Current product direction:** make the working development environment comfortable, expressive, inspectable and recoverable, with replaceable application behavior (§6)
**Current execution state:** founder has exercised the Neovim live switch; PR #33 remains open. The [Workshop Goal Map](goals/workshop.md#part-1--everyday-interaction-selected-for-execution) selects everyday interaction as Part 1; service retirement remains parked.

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
- **A presentation owns meaning inside its grant; application authority governs room and
  spatial conflict.** Workshop currently implements the presentation owner; keeping that owner
  movable into a weave is part of the selected replaceable-shell direction; each extraction
  still needs a concrete consumer and execution scope. See the
  [ownership distinction](goals/workshop.md#application-authority-and-presentation-ownership).
  Paint, hit-testing, ordering, clipping, and granted pane room spend the same resolved geometry.
- **Continuity and repair are authored choices.** Zengine supplies useful starting policies;
  makers may replace them. The [Workshop ownership model](goals/workshop.md#authored-continuity-and-repair)
  owns the direction on pending work, evidence, replacement and alternative repair paths.
- **Pointing names a subject for one request; selection is a state the maker entered.** Context
  remembers identity and re-asks the owner when the action is spent.
- **Refuse rather than pretend.** Unsupported bytes, units, authority, lifecycle, or platform
  claims remain visible and unchanged rather than being guessed, clamped, normalized, or dropped.
- **The same gesture may have different meanings only when its active contexts are mutually
  exclusive and explicit.** Dispatch, help, and remapping spend one action truth.
- **Evidence is proportional to the claim.** A green is not proof of everything; package,
  sanitizer, native-platform, live-interaction, and mutation evidence are used when their distinct
  failure classes matter.
- **Workshop's panes become weaves.** Participating pane weaves are the selected direction;
  remaining built-ins are migration debt. The host keeps room, focus, realization and roots
  (VD-19); the Goal Map names the current exceptions.
- **A plan row asks for authority; it never confers it.** Editing a file gives no power. The
  host's policy — the Weaver, set by the maker — decides what a loaded artifact may say, may
  refuse, and the refused weave is told (VD-21, VD-20).

## 4. Current system position

### Loom

Loom is a credible installed substrate for schema-governed values, messaging, senses, history,
capabilities, isolation, dynamic weaves, lifecycle, replacement, and host-owned authority policy.
Message acceptance discovery reads the same registered shape truth delivery enforcement reads.
Ask provenance and bounded host turns are explicit. Opted-in senders receive authenticated
dispatch refusals for exact attempts; delivered silence is not settled by that facility. Joint
publication and attributed application facts are shipped in ABI v8. Progress/closing answers
remain separate selected work (VD-20). The standalone host and explicit admission-policy
consumer are merged; further authority UX starts there. SDL has been removed from Loom: the portable pixel-layout
brain remains, while Zengine owns the active graphical product medium.

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

Workshop supports the source/edit/build/realize loop, pane-to-source acquisition and development
of its own participating application behind a separate host. The founder has now exercised the
Neovim/standard-editor live handoff successfully. Its report also records baseline Loom use;
PR #33 remains open at this refresh. The Goal Map distinguishes these observations from a merge
or an independent full review and routes the accepted predecessors' evidence.

The next pressure comes from inhabiting that environment: interaction, richer editor display,
discoverability, protected drafts and useful control. The [Goal Map](goals/workshop.md) is the
owner of that product sequence, not a repeated list here.

## 5. EDIT-1 — landed

The Editor can choose a source. The host captures the launch directory once as the project root;
Project Files presents a bounded, refreshable view inside it; Builder and Project Files call one
Editor-owned `open(path)` door with one normalized absolute spelling; dirty-document refusal and
the Editor's representation law remain authoritative. Surviving law: `Zengine/agents/workshop/project.md`
and `editor.md`; the compressed result belongs in `private/goals/workshop.md` §5.

## 6. The IDE loop — what follows

The maker should be able to reach a running tool's implementation, change it, see the result and
keep or revert it through ordinary Workshop tools. Pane-to-source and Workshop self-development
are now the starting point. Neovim is a concrete editor-replacement consumer; generic changed-shape
development remains a separate capability.

The founder selected the next direction on 2026-09-17:

1. Everyday interaction: Terminal transcript navigation, command-history/completion behavior,
   real destination discovery, pane deselection and existing configuration guidance.
2. Expressive editor presentation, with local introspection, screenshots and authorized control
   brought forward to support development and testing.
3. Protected experimentation and deliberate publication of drafts; deeper configuration/setup,
   reusable GUI behavior, Python participation, GPU and multi-host capabilities follow consumers.

The [Workshop roadmap](goals/workshop.md#7-the-next-maker-loop-after-edit-1) owns exact items,
the founder's Terminal key semantics, and phase boundaries. "Gut the shell" means make fixed
application behavior replaceable while retaining a minimal hosting/authority root outside
application-controlled replacement. It is a design direction across the work, not a mandate to
extract every subsystem before improving the next tool.

Ceremony is audited throughout: actions, decisions, discovery, recovery and the documents/code a
maker must read. Editors should have distinct strengths for different audiences. Live editor
switching proves interchangeability; frequent swapping is not the assumed workflow.

Progress/closing answers remain separate from dispatch refusal. Authority work continues from
the merged standalone/admission consumer; no roadmap item implies universal filesystem protection
or authenticated multi-host identity. Service retirement stays parked under its
[disposition](goals/workshop.md#roadmap-disposition-of-service-retirement).

New-weave production and Flow remain larger capability directions without a new production packet.
The schema-builder direction still authors C++; interpreted execution is pressure-driven. Local
success must keep these future consumers reachable without forcing their implementation now.

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
representations of meaningful things. One-shot authority — a weave asking to do a thing once and
being granted it once — is a horizon Loom has not earned (known-seams: "allow once is not
claimed"); VD-21 notes it and builds nothing.

A horizon defines a completeness test. It does not authorize a demo-driven implementation. If a
horizon starts specifying framework details, move those details back behind current consumer
pressure or discard them. `private/goals/two-forms.md` — a live interpreted form and a generated
durable form bridged by Flow — is a horizon in exactly this sense; it authorizes nothing.

## 9. Process doctrine

[Orientation §8](../zen-orientation.md#8-working-rhythm) owns prompt construction, temperature,
review, acceptance, and consolidation. The [executor constitution](../executor-constitution.md)
owns execution. Reference those owners rather than maintaining a second Prompt Contract here.

The founder chooses direction and acceptance. Vision updates the smallest current authority
after acceptance; a report does not accept itself. This map changes when strategy changes,
not to record every phase. Raw capture is an inbox; proof and chronology stay in reports and Git.

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
                                      executor entry route; no phase selected here
private/handoffs/Zen-FCO-v2.md        first-contact route — the first read for a Vision

repository laws/references            exact current semantics
phase reports/evidence + Git history  proof and chronology
```

Refresh this map only when current direction, a goal's status, a strategic law, a horizon, or a
process doctrine changes. Routine phase closure belongs in the Goal Map; routine evidence belongs in
the report.
