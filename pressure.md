# Zen Live Pressure Board

**Status:** PRIVATE LIVE AUTHORITY  
**Refreshed:** 2026-08-30  
**Role:** open observed pressure and the evidence/trigger that may justify action  
**Strategy:** `private/zen-strategic-map.md`  
**Known owed work:** `private/backlog.md`

This board keeps only pressure that can still change a decision. Closed phase ledgers remain in
reports and Git history; they are not repeated here.

## 1. Rules

```text
ACT       current evidence supports a bounded near-term packet
WATCH     real pressure exists; more use should shape the answer
PARKED    real pressure exists but a named trigger has not fired
SEED      strategically useful candidate; not current product or architecture law
```

Pressure is not authorization. A known technical seam belongs in repository law; deliberately owed
but deferred work belongs in `private/backlog.md`.

## 2. Current action pressure

### P-ACT-01 — The Editor cannot choose a source

**State:** ACT — EDIT-R1 COMPLETE; EDIT-1 IMPLEMENTATION-READY  
**Evidence:** `reportbacks/EDIT-R1-RB.md`, current `Zengine/docs/workshop/editor.md`

Builder is still the only source-acquisition path. A maker can edit one recipe-named source but
cannot independently navigate the project and open another admitted file.

**Bounded answer:** capture the launch directory once as project root; add Project Files as an
ordinary pane; factor one normalized Editor-owned open-by-path door; make Builder another caller;
refresh on open/navigation/explicit gesture/finished build. Preserve one document, dirty refusal,
and the Editor's byte law.

**Completion witness:** launch with no useful Builder source, navigate and edit/save a source, then
use Builder independently.

### P-ACT-02 — Relative single-source recipes already split edit and build meaning

**State:** ACT WITH EDIT-1 REVIEW  
**Evidence:** EDIT-R1 path trace

The Editor and Builder preflight currently resolve a relative source spelling against the process
CWD, while the generated single-source CMake project resolves it against the generated workspace.
This is pre-existing and means the public sentence “the file you edit is the file the recipe builds”
is only reliable for an absolute authored source today.

**Required disposition:** EDIT-1 must not inherit or restate the false parity quietly. Its production
prompt/review must either give both paths one project-root resolution or retain/refuse the relative
case in explicit current truth. Path normalization at the Editor door alone fixes document identity;
it does not by itself change what generated CMake builds.

## 3. Workshop product pressure

### P-WORK-01 — Default pane height and keyboard resizing are tedious

**State:** WATCH  
**Evidence:** `Zengine/docs/workshop/limitations.md`, ARR-0 recommendation

Pane width responds to the surface; default height remains nine rows. Pointer resize is efficient,
but keyboard resize moves one cell per press and offers no coarse/fill operation.

**Trigger:** repeated real use treats this as the dominant arrangement cost after EDIT-1, or a
surface-aware default can be stated without becoming a layout solver.

### P-WORK-02 — The Pane Editor edits the spatial grammar only, and has no contextual door

**State:** WATCH  
**Evidence:** WUX-13 (`Zen/reportbacks/WUX-13-RB.md`), `Zengine/agents/workshop.md` §"The Pane
Editor has a subject"

The original pressure — Pane Inspect lacked a subject model; Info understood the selected
document object — is answered: the Pane Editor holds an identity-held `PaneRef` subject
independent of `Panels::selected`, lists the picker's inventory, and edits place/size/front/
participation through the existing doors. What remains is narrower:

- it edits only what a `SetupPane` can say today (absolute place, per-axis size, front rank,
  participation) — no anchors, fill, docking, locks or relative placement, because no pane can
  hold them;
- there is no contextual "edit this pane" row seeding the subject from the right-click menu;
  the editor's own list is the acquisition door;
- Info still inspects document objects and is deliberately retained beside it (the document
  editor owns the product's first five minutes and the only typed doors for `Context` and `%`
  shares) — retiring it is a product decision, not an editor decision;
- the default nine-row stack height shows three panes and three rows (P-WORK-01).

**Trigger:** a maker reaches for a pane fact the rows cannot say, wants to seed the subject from
a pointed pane without walking the list, or the document editor's retirement is decided.

### P-WORK-03 — Provider participation is deliberately read-only and host-bounded

**State:** WATCH  
**Evidence:** current pane protocol and Workshop limitations

External panes publish bounded prose and receive no input, contextual rows, arbitrary drawing,
focus, lifecycle, or installation/discovery support. One PaneRef mounts once.

**Trigger:** a second independent provider or a real tool demonstrates one precise missing contract.
Do not infer a plugin framework, generic input protocol, or same-PaneRef multiplicity from the fact
that a provider pane exists.

### P-WORK-04 — Conventional editor expansion should come from use

**State:** WATCH  
**Evidence:** EDIT-0 closeout and editor limitations

Search is the first likely missing ordinary affordance. Unicode, multiple documents, language
tooling, splits, and Vim behavior each have different representation and ownership costs.

**Trigger:** after EDIT-1, actual editing repeatedly hits one of these walls. Unicode requires a
truthful caret/column/glyph model; multiple documents require independent lifecycle pressure; Vim
requires a real backend rather than incremental imitation.

### P-WORK-05 — Attention's compact graphical channel has limited voice and owns no room

**State:** WATCH  
**Evidence:** WUX-4 pressure

The compact Surface text slot carries text but no semantic role, so the SDL chip has one visual
voice. It overlays the top-right of a full canvas because no publisher-declared reservation exists.
The keymap's POSIX-gap statement is also standing truth still carried on an event-shaped row.

**Trigger:** a second semantic slot consumer, repeated obscuring of important content, or a keymap
condition that materially misleads a maker.

### P-WORK-06 — Source provenance is the next self-hosting join

**State:** WATCH — AFTER EDIT-1  
**Evidence:** EDIT-R1 provenance trace, authored load-plan/build-recipe seams

The project can already relate provider/office, load-plan row, artifact stem, recipe, and source by
authored joins. Workshop does not yet expose `pane -> Edit Code`, and Editor correctly knows none of
the topology.

**Trigger:** EDIT-1 is accepted and a real pane can be traced to one source/recipe without guessing.
The host should answer; browser rows and Editor must remain topology-free.

### P-WORK-07 — Live replacement is still a deliberate wall

**State:** PARKED  
**Evidence:** Builder/realization law and `Zengine/docs/workshop/limitations.md`

An already-live artifact refuses realization and tells the maker to restart. Provider overlays are
reversible contributions, not artifact hot reload.

**Trigger:** the pane-to-code loop reaches an already-live artifact and can state provider/weave
custody, continuity, authority, rollback, and failure semantics for that concrete case.

### P-WORK-08 — A hidden pane loses the position it was hidden at

**State:** WATCH
**Evidence:** WUX-7 desk work; current `Zengine/docs/workshop/panes.md`

Removing a pane from the setup and bringing it back through the picker gives it the composition's
default slot rather than the place the maker had arranged it in. Persisting a latent geometry for
a pane that is not in the setup is a new durable fact, so it is not a free repair.

**Trigger:** a maker's arrangement is destroyed by an ordinary hide/show cycle often enough to be
the dominant arrangement cost, or a latent-place representation can be stated without giving the
setup a second population.

### P-WORK-10 — Arrangement has no snapping, locks or collision avoidance

**State:** PARKED
**Evidence:** WUX-5/WUX-6/WUX-7 arrangement work; ARR-0

Three separate wishes keep arriving together and are deliberately unbuilt: edge snapping,
per-pane locks, and refusing to place a pane where another already is. Each is a real convenience
and each adds a durable fact or a solver to a desk whose whole current claim is that what a maker
authored is what is stored.

⚠ **The fourth wish left this entry.** Named layout tabs are shipped (WUX-9) and durable
(WUX-10) — and they cost neither a solver nor a second geometry owner, because a layout is an
ordinary `Setup` and the session already owned machine-local state. That is the shape the
remaining three still have to find.

**Trigger:** arrangement is measured as a repeated cost in real use AND one of the three can be
stated without a layout solver or a second geometry owner.

### P-WORK-12 — Renaming a layout rides the setup save

**State:** CLOSED by WUX-11 (`reportbacks/WUX-11-RB.md`)

Renaming is a layout operation and saving is a file operation, and they are two gestures now:
`layout.rename` (double-click a tab, or its contextual menu) writes no file at all, and `s`
writes the active layout's desk and names nothing. The second half of the entry — *a maker with
several layouts has one setup file for all of them* — is also gone: every layout owns its own
optional association, and the top row says which artifact the live one is related to and whether
it still matches it. What survives of the entry is P-WORK-13 below, which is the part WUX-11
deliberately did not build.

### P-WORK-13 — A layout can only ever acquire the one Setup file the command line named

**State:** WATCH
**Evidence:** WUX-11 (`reportbacks/WUX-11-RB.md`); current `Zengine/docs/workshop/limitations.md`

Every layout now has its own optional Setup association, and a run may honestly hold several
different ones — but the only path by which a layout with none can ACQUIRE one is `s` or `r`
against `--setup`. So within a single run, every association a maker makes fresh points at that
same path, and two layouts saved in one sitting necessarily share a file (which the
shared-artifact law then keeps honest rather than hiding). Keeping two arrangements on disk still
means two runs.

The per-layout ownership model is deliberately built so that this can be answered later without
moving anything: a chooser would only ever widen WHICH path an association may be established
with, and would touch neither `SetupLink`, nor the durable shape, nor the three verdicts.

**Trigger:** real use shows makers wanting a second named arrangement inside one run — at which
point the question is a live artifact chooser, and it must not be allowed to become a Setup
library, a project abstraction or a general file dialog.

### P-WORK-11 — Reading past an ellipsis is a window-only gesture

**State:** WATCH
**Evidence:** WUX-7; `Zengine/surface/skin_tui.hpp` (`kTuiPointerOn`), current
`Zengine/docs/workshop/limitations.md`

Hover reveal needs an idle pointer, and the TUI Skin asks terminals for button-event reporting
(`1002`) only, so the gesture exists in the graphical window and not in a terminal. Moving to
`1003` buys one gesture and pays for every idle motion in every session. Separately, no beat
reaches Workshop, so the reveal is driven by the pointer's own position rather than by time --
a timed marquee would need a repaint with nothing behind it.

**Trigger:** terminal makers meet the cut text as a real obstacle, or something else already
justifies a repaint pump Workshop can honestly spend.

## 4. Build and verification pressure

### P-BUILD-01 — Windows parallel CTest has a separate Timer failure

**State:** WATCH / BOUNDED DEFECT  
**Evidence:** ZOOM-P1, current Zengine verification law

Linux/GCC is safely parallel. Windows/MSVC remains serial because the Timer suite intermittently
fails a weave-load assertion under concurrent CTest; this was measured before and after the compile
fixture repair and is not the same defect.

**Trigger:** select a focused Windows concurrency investigation before documenting or enabling
parallel MSVC verification.

### P-BUILD-02 — Zengine's fetched-source cache has no lifecycle owner

**State:** WATCH  
**Evidence:** ZOOM-P1 and LSDL-0

The basename-keyed cache was measured at roughly 13 GB/80 entries, has no eviction, can retain stale
generator identity, and can leave partial population litter. Loom no longer writes it after SDL
removal; the pressure is Zengine-only.

**Trigger:** another stale-cache failure, material disk growth, or a build-system touch that can name
the cache's owner without introducing a general package manager.

### P-BUILD-03 — Mutation practice is stronger than its durable documentation

**State:** WATCH / OWED ROUTE IN BACKLOG  
**Evidence:** repeated recent mutation campaigns

Canary-first, exact mutation application, rebuild, blast-radius prediction, checksum restore, and
artifact separation remain report knowledge rather than one short routed law.

**Trigger:** next substantial mutation campaign or a new executor expected to run one without
reading phase archaeology. See `BL-VER-01` in the backlog.

### P-BUILD-04 — The hosted/advisory MSVC result remains weaker than local evidence

**State:** WATCH  
**Evidence:** current CI is advisory; local MSVC lanes pass

Do not widen the continuous-support claim from local/native evidence alone. Read authenticated
hosted failure evidence before changing diagnostics or claiming the advisory lane is stable.

## 5. Loom and architecture pressure

### P-LOOM-01 — The portable pixel layout brain has no executor consumer

**State:** WATCH  
**Evidence:** LSDL-0

`zen-ui-pixel` still proves layout commands under uniform and proportional metrics, but no current
workspace skin executes `PxScene`. The commands are proven correct, not yet proven sufficient as a
renderer contract.

**Trigger:** the first real host tries to execute the pixel projection. Do not create a demo merely
to keep the abstraction warm.

### P-LOOM-02 — Sender-visible fate and unresolved obligations are still separate questions

**State:** WATCH / SEED  
**Evidence:** Loom messaging/answer law, recent raw architecture synthesis

Ordinary senders are not told whether a send was delivered. AskBook records authenticated answer
conversations, but Loom has no general promise that an accepted request creates an obligation that
must eventually settle as answered/refused/abandoned/expired/cancelled.

**Trigger:** two real async domains need the same outstanding-work truth and cannot express it with
their own protocol. Do not build a generic obligation framework from vocabulary alone.

### P-LOOM-03 — A policy delegate can die while its installed authority survives

**State:** WATCH  
**Evidence:** Weaver/LiveAuthority law

A grant is not a lease. If the Weaver/policy delegate dies, delegated authority remains while the
ordinary user-facing revocation route may disappear.

**Trigger:** long-lived or remote Sessions, supervision, or a product promise of continuously
available revocation.

### P-LOOM-04 — Authority correctness and operator legibility are different powers

**State:** WATCH  
**Evidence:** live-authority and observation work

The Kernel may enforce the correct current authority while an operator cannot observe changes made
by another capability holder. Participant-local conversation, Sense observation, authority-change
notification, and whole-bus tap are distinct.

**Trigger:** Workshop or a hosted operator needs one precise visibility guarantee. Do not hand every
terminal a host-wide tap.

### P-LOOM-05 — Bridge reachability is not authenticated human identity

**State:** PARKED UNTIL HOSTING/REMOTE CONTROL  
**Evidence:** Bridge reference and current threat tier

Bridge authenticates no person; reachability and socket policy are the current boundary. A trusted
WeaveId is not a durable human identity.

**Trigger:** external terminal/executor, public hosting, remote control, or multi-author trust.

## 6. Adoption pressure

### P-ADOPT-01 — Package truth is ahead of product distribution

**State:** WATCH  
**Evidence:** PKG-0, current Workshop limitations

Zengine has an installed stranger package, but Workshop, graphical artifacts, and the external pane
vocabulary are not an installed third-party product path. This is honest today.

**Trigger:** an outside maker needs Workshop or an external pane from an installed prefix. Do not
turn current build-tree custody into a support promise by documentation alone.

### P-ADOPT-02 — Human onboarding must grow from tested maker friction

**State:** WATCH / GOAL-COUPLED  
**Evidence:** external-reader documentation and Workshop use

The public docs are substantially better and the executor law is routed, but a full human
contributor front door, release identity, and stability promise are not complete.

**Trigger:** actively invite outside contributors or dependents. Simplify accidental ceremony;
teach concepts that are real.

## 7. Seeded strategic candidates — not current work

- **Flow as projection:** facts/events, values, operators, observations/requests, effects, and
  authority may form a maker-facing composition language. A graphical editor is one projection over
  authored semantic structure, not the sole representation.
- **Metadata as inspectable evidence:** identity/provenance facts may accumulate under clear
  claimant domains, but metadata must never become behavioral authority. A final living-system
  snapshot and History/Logger answer different questions.
- **Generated ceremony:** provider/schema/ABI/build glue may be generated while authored primitive
  code carries meaning. Let the C++ compiler parse C++; do not build an arbitrary-C++ parser.

These candidates influence completeness tests only. They require their own current consumers and
authorized phases before they become architecture.
