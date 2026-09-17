# Zen Live Pressure Board

**Status:** PRIVATE LIVE AUTHORITY  
**Refreshed:** 2026-09-17
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

The founder's hands-on Neovim use has supplied concrete interaction and presentation pressure.
The [Workshop Goal Map](goals/workshop.md#7-the-next-maker-loop-after-edit-1) owns the newly selected
roadmap and exact Terminal history-key behavior. Part 1 is everyday interaction; expressive
editor presentation follows, with local inspectability/control brought forward. PR #33 is
merged; the next prompt starts from main containing that editor implementation.

The accepted Files action-identity, pane-to-source, Workshop development-launch and standalone
host/admission arcs are predecessors, not still-selected tasks. BL-WORK-04 remains owed and
conditional on its stated wake. New notes are roadmap direction, not a blanket backlog expansion.
Progress/closing answers, general picture provenance and service retirement keep their own bounds.

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

### P-WORK-03 — The pane protocol is what a provider can say, and the built-ins need more

**State:** SELECTED EXTRACTION ARC CLOSED (2026-09-13); remaining surfaces parked pending a consumer

Files, Builder, Attention, Info, Terminal and Editor are pane weaves. The accepted
[PR #23 result](goals/workshop.md#pane-extraction-current-status-and-next-work) closes the Editor
migration. Layouts, Pane Manager and the maker pane remain host-owned under the selected boundary.
The pane protocol's current contract belongs in `Zengine/agents/panes.md`.

**Trigger:** a selected remaining migration or a real provider demonstrates a missing contract.
Preserve the component's undo, normalization, selection and fallback behavior with its owner.
`marks_persist.hpp` pulling `persist.hpp` into the weave image remains a separate follow-on hook.

### P-WORK-23 — Pane notices must agree with actions and hit-testing

**State:** CLOSED / ACCEPTED (2026-09-14), through PR #27

The selected audit and interaction cleanup are accepted. Ignored input preserves notices,
consumed actions publish their removal, Info maps its notice-bearing rows, commit answers
preserve later edits and newer drafts, and cancellation claims no prior write away. Builder/Files
ignored ids and Attention's hidden-condition wording are repaired. BL-DEF-02 and the enumerated
BL-DOC-01 work are closed. Document binding/refusal work is now accepted under P-WORK-26; Files'
cross-mode intent identity is BL-DEF-05, and general queued-picture provenance remains P-WORK-25.

**Evidence:** [corrections report](../reportbacks/zengine-pane-interaction-cleanup-corrections-RB.md),
Vision's independent ordinary lane and loaded-pane reproductions at `407ca15`, the same-tree
merge `b42fe35`, and founder acceptance. Current sequence belongs in the Goal Map.

### P-WORK-26 — Info commits lack document subject binding and known-refusal settlement

**State:** CLOSED / ACCEPTED (2026-09-14), through merged PR #28

Workshop judges a host-issued subject before applying a commit. Selection changes, successful
file loads (identical bytes included) and detected identity re-minting invalidate applicability;
legacy unbound commits are refused. Info releases an invalid-ticket or authenticated exact-attempt
dispatch refusal while preserving the draft. Delivered silence remains valid pending work.
BL-DOC-02 and the follow-up sender-fate paragraph are corrected.

Arbitrary host revival to another document's bytes can still retain the subject. This disclosed
limitation remains deferred until a real Workshop state-replacement consumer is selected; it
does not extend the current repair sequence. The new Info image on a v1-only host remains an
explicitly unsupported pairing. The current boundaries live in the document law and decision record.

**Evidence:** [implementation report](../reportbacks/zengine-info-targeted-commits-RB.md),
[documentation follow-up](../reportbacks/zengine-info-targeted-commits-doc-followup-RB.md),
Vision's independent official lane and state-swap probe, reviewed `c012085`, and same-tree merge
`afdc242`. Current sequence belongs in the Goal Map.

### P-WORK-24 — Files cannot infer whether it already held the keyboard

**State:** CLOSED / ACCEPTED (2026-09-13), PR #25 merged as `968a257`

The merge tree equals reviewed `9c4242c`. Workshop supplies prior ordinary-key routing on a v2
press; Files owns activation, and v1 remains conservative. Hidden-title hit-testing and selection
through the resulting room grant are repaired, and the keyboard band follows actual routing.
Version inspection remains an observation: a later incompatible holder can refuse the press,
attributed on the tap, without a retry. No new Loom mechanism was needed.

**Evidence:** [implementation report](../reportbacks/zengine-files-focus-implementation-RB.md),
Vision's independent official run and settled hidden-title Editor drag probe, and founder merge
confirmation. Its enumerated wording/count corrections (BL-DOC-01) were accepted in PR #27.
The limitations-page residue (BL-DOC-02) is accepted and closed in PR #28.
Queued-picture provenance remains P-WORK-25; it does not reopen this accepted repair.

### P-WORK-25 — Queued presses do not identify the picture they targeted

**State:** WATCH / REPRODUCED; deliberately separate from the selected Files focus repair

Two queued presses on the row painted as `entry-03` can end with `entry-04` selected after the first
press moves Files' listing window. This reproduced on accepted main `3c8d6bc` and the focus prototype.
The press names a row but no published-picture identity. Correct prior-focus context and the
hidden-title repair do not establish correctness across arbitrary intervening pictures.

Preserve a route to solve this later without selecting a general revision/history protocol now.
Terminal's second-press memory is only an analogy, not a reproduced instance of this defect.

**Evidence:** [Files focus investigation](../reportbacks/zengine-files-focus-investigation-RB.md),
P10 and its adjacent probe/evidence pack; Vision independently reproduced the same result.
**Trigger:** the next selected pointer/presentation provenance investigation, or ordinary use showing
repeated queued clicks selecting or activating a subject the maker did not aim at.

### P-WORK-22 — An authored load plan is all-or-nothing, and core panes now ride it

**State:** OPEN — named by the witness, 2026-09-08  
**Evidence:** `reportbacks/pane-weaves-remaining-RB6.md` ("What the work found", 2); `agents/realization.md` LOAD-0/BOOT-0 (the boot walk stops at a refused row and the host exits, code 4)

A tree without `zengine-info-pane.so` does not open a Workshop with a row saying so: the boot
walk refuses the row, says "the authored plan was not completed; 10 artifact(s) participated
before it stopped. Exiting." and exits — as it does for any of the rows ahead of it. Before this
arc that list held tools; it now holds the pane a maker meets first. The shape this wants is a
plan whose rows can say whether the host can run without them — realization law and plan
grammar, Zengine's (`agents/realization.md`), not Loom's; the Loom loads one weave at a time and
has no plan. Plan grammar is also where P-WORK-18's request lands; the two should be read
together before either moves.

**Trigger:** the first maker whose pane image fails to build; or the founder's word.

### P-WORK-04 — Conventional editor expansion should come from use

**State:** TRIGGERED BY FOUNDER USE — staged in the Goal Map, not all in Part 1
**Evidence:** founder's 2026-09-17 notes after live Neovim switching

Terminal interaction, Neovim profile discoverability, editor highlighting/caret presentation,
standard-editor tabs/navigation/Git marks and reversible hidden comments now have a real consumer.
The [roadmap](goals/workshop.md#7-the-next-maker-loop-after-edit-1) owns their sequence and limits.
Editors may serve different audiences. Unicode/column geometry, document lifecycle and native
write authority remain distinct questions; this entry does not collapse them into visual polish.

### P-WORK-05 — Attention's compact graphical channel has limited voice and owns no room

**State:** WATCH  
**Evidence:** WUX-4 pressure

The compact Surface text slot carries text but no semantic role, so the SDL chip has one visual
voice. It overlays the top-right of a full canvas because no publisher-declared reservation exists.
The keymap's POSIX-gap statement is also standing truth still carried on an event-shaped row.

**Trigger:** a second semantic slot consumer, repeated obscuring of important content, or a keymap
condition that materially misleads a maker.

### P-WORK-06 — Source provenance is the next self-hosting join

**State:** CLOSED — founder accepted and merged the pane-to-source loop
**Evidence:** [final correction report](../reportbacks/zengine-pane-to-source-loop-corrections-RB.md)

The authored pane/office-to-source/recipe join is now a starting capability. Editor retains
document custody and Files remains a navigator; current law belongs to Zengine's Workshop code
and opening owners. Further provenance needs should name their new consumer.

<a id="p-work-07--live-replacement-the-same-shape-rung-is-built-the-changed-shape-rung-is-the-wall"></a>

### P-WORK-07 — Live replacement: generic migration remains beyond the editor proof

**State:** SAME-SHAPE RUNG LANDED; EDITOR HANDOFF IMPLEMENTED; GENERAL DEVELOPMENT MIGRATION PARKED
**Evidence:** Zengine realization laws and [Neovim live-switch report](../reportbacks/zengine-neovim-live-switch-RB.md)

Same-shape build/reload, explicit promotion and revert remain available. Neovim PR #33 now uses
Loom prepared replacement and an authored editor handoff; the founder has exercised it successfully.
The founder has merged that PR. It does not make arbitrary changed-shape builds migratable.

**Trigger:** a concrete changed-shape development task beyond the editor-specific handoff, with
authored migration, custody, refusal and activation behavior. Preserve the seam without requiring
a general migration framework or overlapping incumbent retirement in the interaction phase.

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

### P-WORK-14 — Refusals are kept but not readable

**State:** ACT (VD-20 — before the arc's first shape collision, so it arrives as a sentence)  
**Evidence:** `reportbacks/three-small-things-RB.md` Doc gaps and Pressure; `pick-and-load-repairs-RB.md`

A realize refusal is cut on the realize row and on the notice; `--log <path>` now keeps it whole,
but the journal has no reader a maker can run (`loom::Logger::read` is the only door, and a
Zengine page may not name it). The boot walk's own refusals ride no selected shape and are
journaled nowhere. Every fact added to the journal widens the gap between kept and readable.

**Trigger:** the first maker who needs the whole sentence; the answer is a reader (a tool), then a
place to read a refusal whole — the same seam as the Terminal overlay's reach.

### P-WORK-15 — Promotion is explicit; two roads wait on it

**State:** ACT for the modal (VD-21 — the approval modal is the general modal's second consumer); the timed auto-revert stays a road  
**Evidence:** `reportbacks/build-then-load-RB.md` Choices; `prompts/build-then-load.md` STEP 2 approval

A reloaded image is not the default until promoted, and revert exists. Two roads: a timed
auto-revert ("reverting in 10") once keep and revert are habitual — an explicit keep, a rule for a
second reload during the window; and a modal that warns on closing without promoting, which the
founder wants as the pressure for a general popup/modal feature.

**Trigger:** a reload that breaks input or UI in practice; or the first maker who quits with an
unpromoted image and did not know.

### P-WORK-16 — `config` is named, not asked

**State:** HOOKED  
**Evidence:** `Zengine/docs/workshop/builder.md`; `reportbacks/pick-and-load-repairs-RB.md` Pressure 1

A `cmake_target` row's `config` is empty and right under single-config generators and must be
authored under multi-config ones; the chooser does not ask it. `load_cache()` already reads the
generator, so the chooser could ask exactly when it matters.

**Trigger:** a maker on MSVC pressing `a` on a Visual Studio tree.

### P-WORK-17 — The weave you just loaded is a late row behind `... N more`

**State:** OPEN (a sharper case of P-WORK-11)  
**Evidence:** `reportbacks/build-then-load-RB.md` stage b witness

The Project pane cannot scroll; a row authored by "load it" is a late row and hides behind the
ellipsis. The pane protocol has keys and a wheel; the introspection pane spends neither.

**Trigger:** the pane protocol work that gives the Project pane a viewport.

<a id="p-work-18--every-loaded-artifact-may-say-anything"></a>

### P-WORK-18 — Loaded participation needs explicit authority

**State:** INITIAL HOST/ADMISSION CONSUMER LANDED; FURTHER UX FOLLOWS CONSUMERS
**Evidence:** founder confirmed Loom/Zengine standalone/admission work merged;
[final host correction report](../reportbacks/loom-standalone-usability-corrections-3-RB.md)

The earlier application allow-any baseline is not the current execution starting point. Further
authority work should inspect the supplied host and Zengine admission policy, keeping native
execution trust, message grants, human identity and OS file access distinct. Protected drafts,
dependency installation and micro-console control are concrete future consumers; their phases
must specify what boundary actually enforces each promise.

**Trigger:** one of those consumers needs a missing authority decision or operator explanation.
Do not infer a universal grant store, modal system or remote identity from the completed host arc.

### P-WORK-19 — The keymap is a closed catalog in one header

**State:** LANDED for pane rows (Zengine PR #15, 2026-09-06): `PaneActions` joins under the collision law at admission, the file wins in both load orders, a Workshop id is refused, dispatch sends the resolved id; BL-DEF-03 rode along  
**Evidence:** `workshop/keymap.hpp` (`join_pane_rows`), `agents/workshop/keyboard.md`, `agents/decisions/a-pane-declares-its-actions.md`

What stands: `Act` and `KeyContext` are still closed for the host's own rows, and shrink as panes
leave (`kFiles`, `kRecipeChooser`, `kAuthoring` left with Files). The prose still argues in the
header; it moves to `agents/decisions/` when the file is next touched for a reason of its own.

The founder now requires a provider to be able to learn when Workshop rejects its action
declaration, so that it can recover under its own policy. The bounded follow-up, current gap
and wake condition belong to [BL-WORK-04](backlog.md#bl-work-04--a-pane-can-learn-that-its-action-declaration-was-rejected).



### P-WORK-21 — The Composer still matches raw keys

**State:** OPEN — QR-sized  
**Evidence:** `Zengine/composer/composer.cpp`; `reportbacks/pane-actions-and-files-RB.md` Pressure 3 and 4

The Composer answers Up/Down/Return/Escape/Tab from raw `PaneKey`, so its keys are in no legend
and no maker's file moves them — the state Powers was in before PR #15. Declaring them is the
same change Powers took. Companion of the same size: a pane row's authored gesture gets no
`posix_gap` note at admission (a maker who moves `powers.view` onto `shift+1` is not told a
terminal cannot press it) — one sentence in `join_pane_rows`.

**Trigger:** a maker reaches for the Composer's keys in the band or in a keymap file; or the next
touch of `composer.cpp`.

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



### P-BUILD-04 — MSVC support claims follow hosted evidence

**State:** WATCH  
**Evidence:** the hosted lane remains advisory; the historical unexplained failure is resolved

Vision read the original [failed run](https://github.com/Krealsion/Zengine/actions/runs/31271991320):
test-time compilations lacked the Visual Studio environment and could not find `cstdint`.
[Commit 24a4fdd](https://github.com/Krealsion/Zengine/commit/24a4fdd2a618d53810eb2093cc713b2f0a2fb530)
repaired that step and is in accepted main. The MSVC jobs passed on
[main e593894](https://github.com/Krealsion/Zengine/actions/runs/34445632720) and
[Editor 9cbf5a5](https://github.com/Krealsion/Zengine/actions/runs/34535147227), checked individually.
BL-VER-02's reconciliation is complete. Keep future support-policy decisions separate: local
success or these particular hosted successes do not by themselves change the advisory policy.

### P-BUILD-05 — Three more spin-bound loops in the builder suite

**State:** OPEN — a one-line quick repair each  
**Evidence:** `reportbacks/three-small-things-RB.md` Pressure 1; `Zengine/tests/test_builder.cpp` 519, 587, 985

`drain` was bounded by two million looks and reddened CI three times in two days on a fast runner
before it got a wall clock. `beat_until_idle`, `carry_until_over` and an inline guard are the same
defect under three names. They have not reddened; the drain had not either, until it did.

**Trigger:** the next red on this suite — or sooner, at the founder's word.

### P-BUILD-06 — Quoted refusals are pinned nowhere

**State:** OPEN  
**Evidence:** `reportbacks/three-small-things-RB.md` Doc gaps 2, Pressure 5

Loom's guide and a Zengine case both quote `conflict_what`'s sentence from `src/registry.cpp`;
`doc_links` checks links, not quotations. A reword leaves both stale silently. A
`law_register`-style rule for quoted refusals is the shape, if wanted.

### P-BUILD-07 — Two ownership gaps the repairs exposed

**State:** OPEN  
**Evidence:** `reportbacks/three-small-things-RB.md` Doc gaps 3, Pressure 2; `pick-and-load-repairs-RB.md` Doc gaps

VM-MUT-09 ("hash the artifact the mutation lands in") has no clause for a case that reads a source
file at run time. And nothing under `agents/` states which shapes the Workshop host keeps durably —
the host's journal selection lives inside `main()` and is pinned by reading `workshop.cpp` as text,
now from two suites; a named seam (a function returning the selection) would let cases assert the
object. Also owed from the documentation arc: the four routed documents over budget (`operators`,
`panes`, `realization`, `surface`) each want a register phase in the family-table shape.

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

**State:** PARTLY SUPPLIED — scoped dispatch refusal merged; unresolved obligations remain
separate selected work (VD-20), requiring their own consumer-grounded scope.

**Evidence:** [merged dispatch-refusal contract](../Loom/docs/reference/messaging.md#sender-visible-dispatch-refusal),
[remaining seams](../Loom/docs/reference/known-seams.md),
[Editor integration preflight](../reportbacks/editor-sender-refusal-integration-RB.md).

Loom now offers explicit acceptors authenticated notice of selected pre-handler dispatch
refusals, returned to the exact sending life and incarnation. TerminalSession consumes it;
the scoped Zengine opening-chain integration is accepted with PR #23. The notice is best effort,
not proof of delivery, semantic success or eventual settlement. It cannot make separate
application facts commit together.

`AskBook` remains conversation bookkeeping. Its attempt matching supports the notice consumer;
it does not itself supply provenance, terminal answers or progress. Exact mechanics belong
in the Loom messaging and answer-authority contracts, not a second pressure-board specification.

Delivered-but-unanswered work, handler failure and invalidated answer rights remain distinct
progress questions. Builder progress, the Weaver's pending approval and realization's waiting
row supply the consumer pressure (VD-20). Scope further obligation work from those needs;
do not infer timeout, cancellation, retry or a general transaction system from vocabulary.
The accepted Editor manager demonstrates application-specific commitment and attributable pending
state; it does not by itself supply the remaining progress/closing-answer contract.

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

### P-LOOM-06 — Two sentences Loom's documentation owes, and one witness

**State:** OPEN — documentation, a later Loom phase  
**Evidence:** `reportbacks/build-then-load-RB.md` stage a Pressure 8′; `three-small-things-RB.md` Pressure 6

`Kernel::load_from` uses a bare `LoadLibraryA` and inherits the host's error mode; on the CI
runner's Windows a staged non-image raised a modal hard error inside the call and hung a suite until
the job timed out, where a desktop Windows 11 turned it into error 193. Zengine's hosts now set the
error mode; `dynamic-weaves.md` should say a host decides it. The copier's shape-name collision is
now documented in the weave guide and demonstrated by no Loom case at the guide's altitude.

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

- **Two forms bridged by Flow** (`private/goals/two-forms.md`, 2026-09-05): a live interpreted form
  (the paused `maker/` package is its runtime) and a generated durable C++ form, with Flow reading
  code into its world through the Loom ABI's handles and drawing raw nodes for what it does not
  understand — under the constraint above: let the C++ compiler parse C++. "A raw node is an
  operator iff it has no bus access, transitively" is the founder's hypothesis, not law.

These candidates influence completeness tests only. They require their own current consumers and
authorized phases before they become architecture.
