# PR #23 — managed opening and Editor extraction

**Vision's proposed implementation roadmap — 2026-09-11.** The
[Workshop Goal Map](../goals/workshop.md#pane-extraction-current-status-and-next-work) owns the
fixed outcome. This roadmap makes the next work concrete; it is not an executor prompt,
approval of a production Loom facility, or acceptance of the PR.

[PR #23](https://github.com/Krealsion/Zengine/pull/23) was checked on GitHub for this roadmap:
open, head `9cbf5a5ac8d4751472dc891371401d93a25e03cc`, targeting `main`; the local Zengine
checkout matches and is clean. Loom's clean local `eee04550dfbae61638ff84f1c9da1c32ad90f9b0`
has the accepted `f20f32df01e36ae672cef8013ea4499b76e3954c` source tree. Private START is
`699682ddddc0fc4dd1ac06c07e28bf696769f593`, clean. Refresh identities when execution begins.

## The result we are building

Opening B while A is current has one defensible commitment boundary. Before it, A remains the
current readable/editable document and B is only a candidate. At it, B becomes the current
document, its admitted presentation and room agree, and its pane receives the keyboard. The
terminal answer follows that fact. Physical rendering follows the selected presentation state;
this PR does not need a new renderer acknowledgment protocol.

If opening refuses, A and its legitimate intervening work remain, with no setup/focus change
attributable to that failed operation. A later independent action remains independent. Silence
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
| Protected publication mechanism, if adopted | Conditional publication of prepared values under explicit authority; no Editor or layout policy |

Keep management in a focused Zengine module with an ordinary participant-facing conversation.
Any required host-only operation gets explicit host wiring. Packaging the manager as a separate
artifact is not itself a prerequisite; the contract and state ownership must allow it to move.
Workshop can remain the presentation implementation during PR #23. Moving every presentation
responsibility into a new weave would add a second extraction to this task.

The manager must not become a second document custodian or receive a mutable native Editor
pointer. It should be possible to inspect which open is pending, who it is waiting on, and
which failure was actually observed. Use existing status/diagnostic surfaces for the selected
path; a general inspector or repair framework is not required.

## Packet A — close the real managed-open design

**First implementation slice:** carry the protected-publication candidate into a witness using
the actual Editor state and Workshop presentation/input paths. Reuse the existing investigation
and failing controls. The preferred candidate remains owner-prepared values published together
after final validation; adding a manager does not by itself make separate writes atomic.

The design should implement this sequence:

1. Establish an identifiable open intent and bounded preparation resources. Bind the exact
   participating instances and relevant revisions. Editor judges source/dirty/paste eligibility.
2. Prepare B and a trial presentation without making either current. Editor authors document
   values; presentation authors its own values. Retain the current owners' truth throughout.
3. Keep admitted A input working on A. Relevant document, presentation or input-admission changes
   invalidate the candidate operation before it can publish. Avoid an open-owned gesture queue.
4. Revalidate and publish the participating facts at one observable boundary. The protected
   exchange invokes no participant handler, renderer or file operation between state changes.
5. Report the established outcome. Losing the terminal answer cannot undo commitment; a stale
   answer or old queued command cannot commit a different operation.

Resolve four concrete adoption questions in this slice:

- **One truthful state view.** Normal reads, editing, snapshot/revive and Poke must read the same
  committed document. Full caret, selection, viewport, saved comparison and undo/redo behavior
  must survive. Refreshing a cached mirror after Poke has already read it is too late.
- **The real presentation/input boundary.** Use actual room/focus decisions and actual routing,
  not a supplied target or a string standing in for focus. Account for A input already routed
  but awaiting delivery. Prevent old content/caret messages from repainting A over committed B.
- **Lifecycle and resources.** Define current-value ownership, operation invalidation, candidate
  release, owner removal, compatible reload and bounded retained state. Recover actual committed
  facts without pretending that restored bookkeeping recreates an expired answer right.
- **Editing cost and authoring cost.** Preserve supported source bounds and ordinary edit behavior.
  The prototype's full serialized root copies are not a production cost model. Demonstrate a
  sensible representation and measure relevant changed paths; keep ordinary panes free of this
  coordination machinery.

The [Vision review](C:/Users/Joshua/Documents/Codex/2026-09-08/https-github-com-krealsion-loom-https/work/editor-commit-review/review.md)
already identifies two necessary corrections to the next witness: consuming a valid but stale
clipboard answer must clear the outstanding-operation bookkeeping, and reload must not leave
an orphan pending-paste flag blocking fresh opens. Use a fresh, correct evidence inventory;
the old report's stale `baseline-identity.py` hash is not a mechanism defect to rediscover.

**Exit:** a working slice demonstrates the fixed boundary with real state/routing, and a short
contract identifies the minimal production support it needs, its lifetime/access rules and its
costs. Review the whole result before fixing the public API. This packet should not reopen the
broad search for managers, continuity policies or general transaction frameworks.

The existing provisional-install alternative exposes B before presentation agrees and relies
on additional fencing/recovery. It is not the current recommendation under the fixed contract.
If this slice reveals a material obstacle, return that specific obstacle and the smallest
choice needed; do not quietly weaken opening or add another speculative subsystem.

## Packet B — land only the justified Loom dependency

If Packet A confirms the need for production protected publication, give that work its own
bounded Loom change and review. Its contract stays generic: owned prepared values, exact
participants/revisions, scoped publication authority, truthful outcomes and explicit resource
lifetime. Document opening, pane geometry, retry policy and UX stay in Zengine.

Participation must be optional. Define how a participating weave accesses its authoritative
state through its normal SDK, including Poke and snapshot; do not make every existing weave
adopt a new state model. Decide the ABI extension/version and supported compatibility policy
explicitly after the contract is sound. Unchanged pane protocols and binary ABI compatibility
are different promises; preserve the former and state exactly what is earned for the latter.

Exercise the actual loaded boundary, failure sensitivity and relevant package/lifecycle lanes.
If public-header changes make BL-ARCH-01's ownership debt material, scope that related repair
there. Check the live backlog again before an ABI change; the previous ABI reassessment item
is closed and is not automatically owed again.

**Exit:** accepted, installed Loom support at an exact published commit, with the shipped images'
build/compatibility route clear. PR #23 may be developed against an explicit experimental prefix
while preparing the dependency, but final acceptance must use the accepted installed dependency.
If Packet A earns the fixed contract with existing public Loom, omit this packet and explain
the actual mechanism. No new Loom capability is authorized solely by this roadmap.

## Packet C — finish PR #23 against that contract

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

Integrate ABI-v7 dispatch refusal in the relevant Files/Builder → Editor → presentation chain
and its directly supporting asks. Each operation owner opts in, stores the real send attempt,
authenticates the notice and matches its current request/stage. A forged, duplicate, mismatched
or late notice must not settle another operation. Refusal of dispatch, a failed handler and
delivered silence remain distinct. This is a bounded consumer conversion, not an all-Zengine
settlement campaign.

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

## Next handoff

The next Ceecee prompt should cover **Packet A only**, with the fixed outcome and concrete
adoption questions above. It should authorize a bounded implementation slice and return a
working artifact plus the proposed production contract. Packet B, if needed, and Packet C get
their own execution scopes after that review. This keeps the public API choice reviewable
while concentrating effort on the already demonstrated Editor blocker.

Roadmap review: four of four areas checked — current PR/dependency identity; fixed guarantees
and investigation limits; manager/custody fit; backlog and acceptance sequence. No new runtime
test was needed or run for this planning update; previous results are linked as prior evidence.
