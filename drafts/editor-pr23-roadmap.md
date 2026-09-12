# PR #23 — managed opening and Editor extraction

**Step 3 selected — 2026-09-12.** The
[Workshop Goal Map](../goals/workshop.md#pane-extraction-current-status-and-next-work) owns the
fixed outcome. The [execution prompt](../../prompts/zengine-managed-open-integration.md) is the
self-contained Ceecee handoff. This roadmap explains ownership, sequence and acceptance; it does
not self-accept the implementation.

Loom PR #6 is merged at `a08499f4e445b578b2c4ffcaac6265aa7094b88f`, with the same tree as the
reviewed `1dcf42b` authority correction. Zengine PR #23 remains open and unaccepted at
`9cbf5a5ac8d4751472dc891371401d93a25e03cc`. Refresh live identities at execution.

## The result we are building

Opening B while A is current has one defensible commitment boundary. Before it, A remains the
current readable/editable document and B is only a candidate. At it, B becomes the current
document, its admitted presentation and room agree, and its pane receives the keyboard. The
terminal success answer follows both owners applying the published values. Physical rendering
follows the selected presentation state;
this PR does not need a new renderer acknowledgment protocol.

If opening refuses before publication, A and its legitimate intervening work remain, with no
setup/focus change
attributable to that refused operation. After publication, application failure is an attributed
outcome, not a rollback or a claim that A was preserved. A later independent action stands. Silence
may leave an operation pending; it cannot justify dropping admitted input, falsely reporting
success, or letting an obsolete queued permission change the current desk.

These guarantees remain the acceptance authority. The existing passing suites did not establish
them. See the [integration stop](../../reportbacks/editor-sender-refusal-integration-RB.md) and
the [commitment investigation](../../reportbacks/editor-commit-investigation/DESIGN.md).

## Put the manager pattern to work here

Use a focused Zengine owner for the **open operation**. It coordinates the participating owners
and carries the maker's intent through preparation, commitment and the reported outcome.

| Responsibility | Owns |
|---|---|
| Workshop application authority | Allowed participants, grants, application policy and connections |
| Open-operation manager | The particular request, exact participants, preparation stage, pending attempts, supersession and the outcome it can establish |
| Editor weave | Source admission and document state, including identity, bytes, saved/dirty comparison, editing state and eligibility to replace |
| Current presentation owner | Trial and admitted content/caret, room/setup change, focus and input routing |
| Accepted Loom publication mechanism | Conditional publication of prepared values under explicit authority; no Editor or layout policy |

Keep management in a focused Zengine module with an ordinary participant-facing conversation.
Any required host-only operation gets explicit host wiring. Packaging the manager as a separate
artifact is not itself a prerequisite; the contract and state ownership must allow it to move.
Workshop can remain the presentation implementation during PR #23. Moving every presentation
responsibility into a new weave would add a second extraction to this task.

The manager must not become a second document custodian or receive a mutable native Editor
pointer. It should be possible to inspect which open is pending, who it is waiting on, and
which failure was actually observed. Use existing status/diagnostic surfaces for the selected
path; a general inspector or repair framework is not required.

## Completed prerequisites

Step 1 established the real loaded Editor/Workshop slice and corrected publication/application,
record retention, repair answers and old-door provenance. Its reusable Zengine source is
`76be71f406678b4ea8786f3f823f6924bd274a12`, also preserved as a complete patch in the
[second correction pack](../../reportbacks/editor-managed-open-slice-corrections-2/README.md).

Step 2 landed the generic Loom dependency with ABI v8 and exact-version rejection, loaded
claimants, native coordination, three showing answers and explicit record release. The subsequent
authority correction binds capabilities to exact operator lives/incarnations and refuses foreign
operations without effects. Both were reviewed; PR #6 is merged. Production integration consumes
the accepted installed dependency, not the historical experimental Loom patch.

## Step 3 — finish PR #23 against that contract

Preserve the extraction's useful work and existing semantic repairs. Replace its opening path
as one coherent change across the Editor, operation manager and current presentation owner:

- replace the current host-first reveal followed by later source installation;
- remove the 256-gesture acquisition queue and its drop/replay mechanism;
- preserve A's legitimate paste/input during preparation, with operation invalidation where
  required and no rollback of unrelated newer presentation changes;
- version any required input/content/commit shapes at their actual published boundary, preserving
  ordinary pane-action and separately built legacy-provider compatibility;
- make stale preparation, projection and completion messages harmless to current work across
  real requester, Editor and presentation-owner replacement;
- represent committed, refused and still-pending operations truthfully, including loss of a
  terminal answer. Do not infer standalone mode from a failed enqueue.

Integrate sender-visible dispatch refusal carried by accepted Loom v8 in the relevant
Files/Builder → Editor → presentation chain
and its directly supporting asks. Each operation owner opts in, stores the real send attempt,
authenticates the notice and matches its current request/stage. A forged, duplicate, mismatched
or late notice must not settle another operation. Refusal of dispatch, a failed handler and
delivered silence remain distinct. This is a bounded consumer conversion, not an all-Zengine
settlement campaign.

Include the two bounded integration repairs: retire an older retained repair record whenever
a newer terminal outcome becomes current, including immediate begin refusal; handle recorded
native participant failures at the actual host pump without swallowing unrelated exceptions.
Document fresh host authorization if the manager is replaced. Adapt the non-const snapshot helper
and remove the dead Loom SDL dev override (BL-DEF-04) alongside integration wiring. The execution
prompt carries the reproduction and acceptance details.

**Exit:** PR #23 implements the fixed behavior with the real loaded Editor and installed Loom,
and all remaining acceptance obligations below are supported by evidence.

## Acceptance and merge review

Restage the existing probes at the new protocol's meaningful milestones while preserving their
behavioral expectations. The required core evidence is:

| Case | Required result |
|---|---|
| Successful opening at commitment | Current source/Poke, admitted content, room and focus identify B together |
| Valid A paste during preparation | A receives its legitimate change; conflicting B open refuses; prior setup/focus remains |
| More than the old cap of ordinary events, including several producers | Every admitted event retains its order and subject; unrelated panes remain usable |
| Resize or setup change before/after commitment | Stale preparation cannot commit; later independent changes are not rolled back |
| Real reload/removal with queued preparation, input, projection or answers | Old operations cannot act on a new participant or change current work |
| Authenticated refusal and forged/mismatched/late controls | Only the appropriate current operation settles |
| Silent/failed participant and lost terminal answer | Truthful bounded operation state; preserved work; no fabricated completion or timeout |
| Stale paste after edit and paste bookkeeping across reload | No orphan pending flag; subsequent valid opening remains possible |

Preserve earlier same-path viewport, multiline editing, undo/redo, save, key remapping, document
custody, Files/Builder and legacy-provider witnesses. Add a focused mutation that breaks the
new commitment/input property, prove it reaches the loaded artifact, then restore the control.
Run the official Zengine lane against the pinned installed Loom, applicable sanitizer/Windows
evidence, package checks triggered by the final diff, and affected live TUI/SDL interactions.
Review CI job by job on the final PR head. Name any unverified limitation instead of generalizing
a modeled witness into whole-product acceptance.

Update current law and guides where the implementation changes their meaning: Editor and pane
laws, custody decision, protocol comments and the public Editor guide. Keep reports historical,
keep memory out of the current-fact path, and check the changed opening/refusal interaction's
ceremony. BL-WORK-01 applies; BL-WORK-02's simple external pane remains useful. Broad onboarding,
Flow, service retirement and output-provider coexistence remain outside this PR.

Finally refresh PR #23's title/body around the implemented result, reconcile BL-WORK-03 with
the evidence, and review for founder acceptance before merge. This roadmap does not self-accept
either dependency or extraction.

## Current handoff and next boundary

Send the [Step 3 prompt](../../prompts/zengine-managed-open-integration.md). It carries all selected
guarantees, source inputs, remaining repairs and workflow without requiring this private roadmap
as an attachment. Ceecee returns the production PR and evidence for founder review. Only acceptance
of that result closes the Editor extraction; the IDE loop, Flow and service-retirement work are
not automatically authorized by this handoff.
