# Easier interaction authoring

**Status:** selected 2026-09-23; implementation follows the merge of Zengine #52.\
**Purpose:** reduce the work and opportunities for error involved in adding an ordinary,
correctly authorized interaction, while preserving the ownership that makes tools composable.\
**Execution packet:** [zen-interaction-authoring.md](../../prompts/zen-interaction-authoring.md).\
**Roadmap owner:** [Workshop goal map](../goals/workshop.md#near-term-order-and-purpose).

## Why this phase comes next

Terminal acquisition lets an existing Inventory, Info and Compose reuse a new source of typed
material. That demonstrates the architecture's benefit. Implementing the source still required
repeated tracking of attempts, correlations, answer provenance, refusal identity and operation
stages. One missed native reply grant left pickup pending despite its declared reply vocabulary.
The report and exploration log for [Terminal capture](../../reportbacks/zengine-terminal-inventory-capture-RB.md)
own the observed evidence, including executor mistakes that were not API defects.

Before adding more independent views and interactions, make that ordinary authoring path easier.
This is one bounded phase with research, implementation and proof in the same executor session.
Its stages are working checkpoints, not mandatory separate prompts or PRs. Flow and unrelated UX
work continue independently; shared contracts need coordination.

## Source-grounded starting points

- Loom already owns `include/zen/weave/ask_book.hpp`, authenticated answer provenance and
  sender-visible dispatch refusal. `AskBook` tracks conversations; it does not authenticate
  an answer. In particular, its role-addressed mode cannot identify the respondent by itself.
- Zengine already has `inventory/pane_client.hpp` and `workshop/pane_operation.hpp`. Compare
  these with Terminal capture, Info field pickup and `inventory-pane/command.hpp` before
  choosing a common mechanism. Gesture identity, request correlation and queued-attempt identity
  serve different purposes, even where a particular protocol uses the same scalar.
- `workshop/workshop.cpp` and `tests/workshop_support.hpp` maintain native host grants.
  Declaring an emitted shape does not authorize sending it, and Emit is not an exhaustive send
  list. An intentionally denied operation is valid policy. Zengine's architecture overview still
  says there is no undeclared emission; reconcile that author-facing explanation with current
  Loom contracts along the touched documentation route.
- `docs/guides/make-a-workshop-tool.md` in Zengine still leads through historical built-in panel
  examples that its warning says will not compile. The loaded Tally example and current pane
  walkthrough offer a better starting point. Check current source before rewriting this route.
- Broad seam and fixture headers caused costly Windows rebuilds in the last phase. Measure
  actual dependencies before choosing a build change; the observed cost does not establish a
  particular fix.

These locations refer to the reviewed product trees, not permanent paths that an executor may
assume still own the behavior. Rebaseline on current main after the predecessor lands.

## Work and completion target

1. **Trace and measure two real operations.** Start with Terminal capture and Inventory's
   permission-then-owner path, using Info as an existing consumer. Record where the developer
   must edit, what is repeated, how failures are found, and the current focused build/test route.
   Choose the smallest common mechanism supported by their actual differences.
2. **Simplify the production code.** Reuse or improve existing helpers and migrate at least two
   real operations. Keep application stages, payload validation and result meaning visible.
   Prefer explicit operation state over loosely related flags where it improves comprehension.
   No automatic retry, timeout settlement, authority grant or hidden global conversation state.
3. **Make a missing grant diagnosable.** Deliberately remove a necessary reply grant in a
   controlled witness. From the ordinary supported diagnostic route, identify the refused
   sender, destination, shape/version and reason, and associate it with the operation as far as
   existing provenance permits. Distinguish observed refusal from unanswered work. Reuse Loom's
   Recorder/Logger and existing refusal records. Share approved policy definitions only where
   justified, with independent evidence that absence of authority still denies the effect.
4. **Make the learning and edit/build path usable.** Repair the existing contributor route around
   a maintained loaded example, show the new request pattern and how to find a refusal, and
   separate current instructions from obsolete mechanics. Compare a local implementation edit
   and a shared-header edit before/after. Apply a bounded dependency improvement if the measured
   graph supports it; otherwise report the cause and a concrete follow-on rather than claiming
   a speedup or broadening this into a build-system rewrite.

Completion requires simpler real call sites, an attributable missing-grant witness, an exercised
public authoring route, and measured build findings. Code length alone is not an acceptance test.
The complete Terminal-to-Inventory-to-Info/Compose story must retain its behavior and authority.

## Ownership and proof

Place generally useful message bookkeeping in Loom only when it belongs there and works without
Zengine. Pane gestures and Workshop policy remain in Zengine. A Loom change is conditional on
the investigation, not a required second PR. Preserve installed-package use and loaded-weave
behavior; prefer changes that do not require a new wire schema or ABI.

Evidence follows changed guarantees: genuine answers and refusals, forged or unrelated arrivals,
stale/duplicate work, two operations active at once, bounded capacity and delivered silence.
Keep validation before settlement, preserve exact-incarnation and role-addressing meaning, and
do not infer remote cancellation from forgetting a local record. Exercise the actual host grant
path rather than proving only a fixture's reconstruction. Use focused checks, required official
lanes and installed consumers where applicable; preserve a meaningful negative control and
restore sources before acceptance builds. Replay the maintained SDL/TUI story for changed pane
paths and attach current screenshots when there is a visible result.

Measure files and independently maintained facts needed per operation, contributor reading and
navigation, rebuild fan-out and elapsed time under a named configuration. Record ELH command
counts if the story changes; transport optimization is not selected. Keep important discoveries,
wrong assumptions and context-compaction costs in the exploration log.

## Backlog and following work

This phase serves BL-WORK-01 and the authoring portion of BL-ADOPT-01. Preserve BL-WORK-02's simple
learning example. Reconcile current-law friction under BL-ARCH-02 only in the touched route.
BL-ADOPT-03 governs any build-speed claim. Reassess BL-ARCH-01 if the measured include boundary is
involved; large fan-out alone does not prove an ownership defect. Builder verification, isolation,
release promises and unrelated framework horizons remain parked. This does not close the broader
onboarding items automatically.

After acceptance, return to a concrete maker story: multiple independent Info views if comparing
and combining saved values needs them, or inventory organization against an actual task. This
phase should let that work use fewer independently maintained protocol facts. It does not select
persistence, a general task scheduler, a coroutine framework, automatic grants, or a new pane SDK.
