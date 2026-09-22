# Inspect, keep and reuse a live subject

**Status:** proposed next phase; source-informed plan, not an implementation report\
**Drafted:** 2026-09-22\
**Product owner:** [Workshop Goal Map](../goals/workshop.md#near-term-order-and-purpose)\
**Direction:** [complete maker stories](maker-story-development.md)

## Goal and why this comes next

A maker can point at a loaded weave, obtain information from its actual owner, keep an
independent typed copy, and use a selected value in a permitted operation. An ELH can perform
the same story through supported messages with its own granted authority. The result or refusal
remains connected to the subject, request and actor that caused it.

The last phase established a reusable route for agents to improve Workshop and prove the result.
This phase lets Workshop explain its own objects in a form makers and agents can use. It supplies
the common foundation for contextual inspection, cross-pane reuse, later drag-and-drop and Flow
arguments. The product result is a complete useful interaction; the architectural result is a
repeatable owner-to-inspector-to-consumer path.

## Accepted starting point

Founder-confirmed merges were checked on 2026-09-22. Their trees match the reviewed candidates.

| Repository | Merged baseline | Accepted result |
|---|---|---|
| Loom #11 | `4b4667904888c26cda862fcce6725549c97d7141` | Compact session/tool reader entry and documentation routes, on the reusable session support delivered by #10. |
| Zengine #44 | `8048c058ca6b2f245017921b3a3f78e3de8308c4` | Complete recipe-authoring journey, maintained tool checks, native interaction evidence, loaded-module identity and continued same-session context. |

The [completion report](../../reportbacks/zengine-elh-workshop-improvement-completion-RB.md)
owns evidence. The public [recipe journey](https://github.com/Krealsion/Zengine/blob/main/docs/workshop/elh-recipe-journey.md)
owns the reusable route. The merged multi-config form also resolves P-WORK-16, which leaves the
live pressure board. Refresh source, installed artifacts and parallel work before execution;
the canonical local checkouts were behind these merges during this planning review.

## The first story

1. Open Loaded and explicitly inspect the Introspection weave's entry. Resolve the selection
   through the loader/runtime owner to the actual participant. Show which subject answered and
   whether this is a current observation, a saved copy or an unavailable source.
2. Inspect its supported public contract and state structure in a generic typed information view.
   Follow a nested field path without scraping painted labels. Keep an independent copy and save
   it with the schema definitions needed to reopen it after the supplier disappears.
3. Select the exposed state field `selections` from that structure and use its name to fill the
   `field` argument of a `zen.PokeRead` draft. Explicitly select/confirm the target and operation;
   choosing a value alone does not send anything or confer permission.
4. Perform the authorized read and display the actual reply beside its request/subject context.
   Refused or unanswered requests remain attributable. Reopen the saved information and make
   clear why historical data is still readable while its old runtime target may no longer exist.
5. Repeat the operation through the maintained ELH route using ordinary bounded grants. Retain
   results and relevant crossings in the existing run/history facilities.

This is grounded in existing behavior: `IntrospectionState.selections` is exposed, `PokeDescribe`
returns structured field descriptions, and `PokeRead` can read that field. Its scalar result is
currently text; display it honestly rather than claiming arbitrary nested-state access. The
generic inspector still handles typed observations such as the nested `PokeStructure` value.
The counter is a first concrete consumer, not a special editor or hard-coded inspector model.

A different equally concrete consumer may replace this example if current source makes it more
useful. It must preserve the whole acquisition, retained value, compatible argument, explicit
destination and authorized result loop. Flow integration is welcome when its current owner can
consume the same transfer contract without conflicting with parallel UX work.

## Source findings that shape the work

| Existing facility | Consequence for this phase |
|---|---|
| `message-draft::Draft` and `Library` already support nested paths, independent copies, schema closure, persistence and admission. | Reuse them. Keep provenance and runtime routing separate from reusable values and authority. |
| Composer already discovers `DescribeAccepted` after `LoadedSelected`, but has an older draft implementation. | Reuse the discovery path where sound; choose one shared value model for new work. Do not require a wholesale Composer rewrite. |
| `LoadedSelected` carries a library name and observed role. Existing `ListLoaded` is text and its consumer accepts correlation-matching results. | Treat the current row as a selection hint. Resolve and authenticate owner facts; it supplies neither a trustworthy WeaveId nor current liveness. |
| Loom's kernel knows loaded name, participant ID, status and role; its loaded record does not retain the complete file/actor/time history requested for metadata. | A narrow typed owner query is a plausible Loom change. Research missing metadata at its source; never infer or backfill it from display text. |
| Workshop's `ResolvedArtifact` and source associations already connect running images, promotion history and recipe editing entries. | Reuse those owners. An editing entry, requested library path and loaded image identity are different facts. |
| Existing Info presents layout properties through string rows. | A general typed view needs a real value/owner seam. Its home may be an evolved Info weave or another replaceable participant, not new permanent Workshop behavior. |
| Guest admission is bounded, but Input republishes injected events without their initiator; the bus stamps immediate authorship. | Admission alone cannot establish authority for downstream inspection or execution. Preserve trusted interaction context through the complete new path. |

These observations were checked in the reviewed trees matching the merges above. Useful source
entry points are Loom `include/zen/kernel/{kernel,control}.hpp`, `include/zen/weave/{describe,poke}.hpp`
and Zengine `introspection/{vocabulary.hpp,introspection.cpp}`, `composer/composer.cpp`,
`message-draft/`, `input/input_weave.hpp` and `workshop/weave_external.cpp`.

## Work sequence within one warm session

**1. Trace the complete route before selecting mechanisms.** Establish the real subject, owner,
getter, schema/value transport, consumer, response attribution and actor path. Compare the
current metadata sources: author declarations, loader records, source associations, schema
discovery, exposed state and recorder history. For each proposed fact name its owner, lifetime,
availability and required permission. Record important findings and the exploration timeline.

**2. Establish the subject and authority boundaries.** Supply the smallest public owner query
needed for the story. Preserve the initiator across input, menu/getter continuations, inspector
and final send, with validation at semantic owners. Investigate a host-owned scoped interaction
context before assuming Loom needs a new global provenance field or ABI. If a public substrate
primitive is actually missing, define it in Loom with its Zengine consumer and independent proof.

Acquiring information and applying it are separate authorized operations. A copied value,
target ID, role name or reopened library grants nothing. Local input and ELH input may share
presentation while retaining their own established authority. A self-authored actor payload or
a privileged component's immediate sender stamp is not proof of the originating actor.
Missing context must not silently mean maker authority. Existing guest `inspect` permission
covers specific discovery operations; it is not permission for arbitrary state reads or sends.

**3. Complete the maker interaction.** Provide the discoverable inspect action, typed traversal,
retained copy/save/reopen, argument transfer, explicit execution and attributable result. Use
current Draft/Library mechanisms and owned operation surfaces. A contextual action may begin
the story; full dragging is not required. Keep selection and inspection distinct from activation.

**4. Prove and package the same story.** Exercise the native graphical interaction as well as
structured ELH operations. Carry the key failures through the real boundaries. Add a maintained
reusable journey/tool beside existing ELH packages, using the session recorder and logger rather
than a second history system. Reuse TUI presentations where supported and state any differences;
a complete new TUI inspector is not a prerequisite for this first phase.

**5. Check architectural reuse and publish the reader route.** Use a small second subject such
as a Files location when this can be done through the same boundary. If that needs another
architectural decision, record the concrete missing consumer seam instead of inventing a generic
framework. Update the public owner references and compact ELH capability map where readers first
need the answers. Report ceremony, important discoveries and any context compaction.

These are work dependencies, not five executor prompts or mandatory PRs. Continue through
research, implementation and proof unless a genuine decision blocks the next step.

## Completion evidence and limits

- A maker can complete the first story from documented setup; the visible controls themselves
  work, and the ELH reaches the same semantic owners under its own grants.
- The observation has an authenticated supplier and unambiguous runtime subject. Missing,
  replaced or unloaded subjects do not silently retarget an old operation to a successor.
- Nested data and its schema closure survive copy/save/reopen independently of the supplier.
  Incompatible assignment preserves the previous draft. Reopening does not imply sendability.
- Denied inspection and denied execution are distinguishable. A granted input session cannot
  borrow greater authority through the touched menu, inspector or sender path. Missing replies
  remain visibly pending
  or unavailable according to their owner; the harness bounds its wait without inventing success.
- Cancelling inspection or an unfinished draft does not perform the operation. Late replies
  cannot attach themselves to a different subject or resurrect a cancelled action.
- Exercise forged/replayed interaction context and mismatched replies at the actual boundary.
  Establish the lifecycle limits of any delegated authority; do not claim continuous revocation
  if the mechanism grants a durable capability.
- ELHs cannot approve or enlarge their own permissions. Test actual approval routes that exist;
  GuestDoor currently has host-callable admission but no approval-message or popup route. Do not
  build an approval UI solely to test it. If one is introduced, injected input must not approve it.
- Default builds enforce the normal path. Ordinary pre-approved bounded grants support unattended
  proof. No bypass is needed for this story; any bypass introduced must be compiled out by default.
- Use repository-required checks appropriate to changes, plus an installed Loom consumer witness
  for a new public substrate contract. Tie live evidence to the tested source/artifacts and keep
  the successful session's retained context inspectable.

Document the metadata result even where implementation stays narrow. Source file, content/build
identity, direct loader, requesting actor, approver and distinct times are different facts.
Unknown stays unknown. Host observations do not change immutable schema identity; saved provenance
does not authenticate a present actor. Full crash-recovery browsing and durable cross-host identity
remain separate work. No message grant scheme here sandboxes arbitrary trusted native code.
Workshop still uses `trust_every_artifact` for plan-loaded code; enforce the new story's actor
boundary without claiming that this phase hardens the whole application's artifact policy.

## Decisions, coordination and following work

The exact inspector home, typed observation envelope and trusted actor mechanism need execution
preflight. Routine implementation choices belong to Ceecee. Bring back a concrete choice if
completion would require a new authority delegation model, durable runtime-reference promise,
incompatible public contract or change to another active owner's design. Source evidence must
justify those changes; the visual demo must not determine them by accident.
Changing the meaning of an existing guest `input` or `inspect` grant is an authority decision,
not a routine UI choice.

Coordinate shared pointer/menu/input vocabulary, `message-draft`, Flow forms and any Composer
changes with parallel UX work. Use isolated source/work/run locations and current merged bases.
Preserve the warm session and existing ELH lifetime when useful, while distinguishing retained
history from proof about newly built artifacts. The founder continues to perform PR merges.

P-WORK-02 (contextual inspection), P-WORK-18 (explicit authority) and BL-WORK-01 (learning/ceremony)
are directly relevant. Other backlog entries stay parked unless the chosen implementation
actually touches their owner. P-WORK-16 is closed by the accepted predecessor.

After this story works, the next consumers are a second domain subject and cross-pane/Flow reuse,
then drag-and-drop and richer follow/pin presentations. Their shared transport and authority
rules should already have a home. Full UI authoring, protected source publication, a universal
metadata catalog, general delegation policy, dependency installation and service retirement
retain their separate triggers. The end goal is for each maker story to improve Workshop through
the same inspectable, authorized and reusable capabilities available to its users.
