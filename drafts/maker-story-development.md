# Complete maker stories, typed inspection and authorized reuse

**Status:** selected direction and research arc; proposed mechanisms require source preflight\
**Selected:** 2026-09-21, founder discussion\
**Product owner:** [Workshop Goal Map](../goals/workshop.md#complete-maker-stories-and-reusable-information)\
**Scope:** the next shared foundations for improving Workshop through its own capabilities

## Outcome and working unit

A maker or an agent starts from a stated baseline, sets up what is needed, creates something
useful, inspects it and leaves a reproducible route another person can use. This is the founder's
**0-to-demo story**. Setup may use a supplied installation; the story names that prerequisite
rather than claiming to start from an empty machine. A working result, its route and verifiable
evidence belong together.

One session may research, implement and prove the complete story. Break the work at meaningful
decision or ownership boundaries, not arbitrary investigation/implementation prompts. Keep a
short exploration timeline: important discoveries, wrong assumptions, backtracking, missing
documentation, tool changes, recovery and any context compaction. Move durable answers to the
place the reader first needed them. Ceremony includes finding and understanding an operation,
not just the number of clicks used once the route is known.

Press the same story from graphical, terminal/TUI and structured ELH routes where supported.
These use the same application operation owners; different presentations may suit different
audiences. A direct command proves its semantic route, while a visible control needs its own
interaction evidence. When a presumed click/action does not exist, investigate whether the
missing capability, the presentation or the expectation should change.

The end goal is a Workshop people and agents can understand, extend and improve using the same
materials and explicit authority available to other makers. A story can earn a new pane,
cross-pane operation, reduced pane or simpler workflow. It need not result in more interface.

## Typed information as reusable material

The central object is owned, schema-described information with an optional relationship to its
source. The first selected storage home is inventory; a temporary info box is a future view.
A selected visual subject must resolve to the participant or host-owned service that actually
knows its data, and an authorized retrieval method. A painted label, row index or menu callback
does not establish that relationship alone.

Keep presentation subjects (button, effective background color) and domain subjects (the row's
represented item, its location or participant reference) connected without assuming one tree
owns both. Standard components can supply common inspection; a weave can expose additional
getters and relationships. Typed answers let an unfamiliar inspector traverse fields and lists.
Pending, refused, unavailable and changed subjects remain attributable outcomes.

| Maker operation | Intended meaning |
|---|---|
| Follow source | Revisit an owner through its supported inspection method; show freshness or disconnection. This does not assume a subscription already exists. |
| Pin as a pane | Keep an inspection visible independently of its originating menu; another view may share the same subject. |
| Make an independent copy | Own an editable typed value; changing it does not change the source. |
| Save | Keep the value and the schema definitions needed to reopen it without the original process; retain useful provenance separately. |
| Reuse | Fill a compatible argument, bind a supported reference or request a named operation, with explicit destination meaning and authority. |

Reusing a copy never revives the original sender, grants, answer rights or process. A saved
reference needs explicit resolution and unavailability behavior; it cannot treat an old WeaveId
as identity across hosts or restarts. Applying a change to the original goes through that
owner's operation. Dropping into an argument may only fill it; a drop advertised as execution
can request execution. Avoid imposing an extra confirmation on every ordinary action.

Reuse the existing [message-draft](../../Zengine/docs/reference/message-drafts.md) traversal,
independent snapshots and libraries. Their saved files carry schema closure and values.
Research the missing subject-to-data connection before inventing another schema store, form
engine or persistence format. Sharing this model with Info, Flow and terminal/ELH consumers
should remove duplicate work, not make the inspector depend on a particular pane.

## Inventory as the first home for captured material

The founder selected inventory on 2026-09-22 and narrowed its first phase to one storage slot.
Capture the pure typed data a maker wants together with a separate auto-generated list of typed
metadata. Metadata entries may contain nested structures, such as actual start-command data
when available. Each part retains the schema definitions it needs; the item must remain decodable
without optional provenance. Capture code collects observations from their owners and labels
unknowns, claims and inference honestly. Inventory stores the pair together without certifying
every recorded claim or inheriting the original actor's authority.

The [inventory capture plan](inventory-capture-plan.md) bounds the immediate Set/Get proof:
independent nested ownership, generic decoding, truthful replacement/refusal and current-instance
storage. A message-only weave suffices. The earlier Loaded-to-state-read demonstration is no
longer the first acceptance story. General inspection, UI actor propagation and drag-out follow
when those paths are touched.

The longer-term inventory can organize data, schemas, code and action descriptions into bags;
show unavailable sources; and help resolve/build/load dependencies. Saved buttons can represent
opening a workstation or playing music. Retrieving a description does not execute it. Dragging
from inventory should use the same value-transfer meaning as dragging from a pane, with explicit
authority at the operation boundary. These are consumers of the first slot, not required now.

## Metadata in the weave contract: selected research

The founder selected research into discoverable metadata associated with a weave's contract:
the file it was loaded from, who loaded it, when it was loaded, and other useful context.
Research both the public description and the owning record behind it. This is a selected
consumer for metadata work, not authorization for a universal metadata framework.
The first [inventory phase](inventory-capture-plan.md) collects available capture facts; it does
not require completing this wider metadata inventory or adding missing load history.

Separate the facts before choosing their storage:

- **Author declarations:** purpose, documentation, source/build locators, tags and other
  descriptions supplied with the artifact or vocabulary. Existing structural schema metadata
  does not imply all of these fields exist.
- **Host-observed load facts:** requested and actually opened artifact path where known,
  content/build identity, host and participant incarnation, lifecycle outcome and the point
  at which loading or activation occurred. A path does not prove which bytes are now on disk.
- **Actor and decision attribution:** the direct loader, requesting participant, original
  maker/ELH and approving policy can be different. Record what the host can establish; absent
  attribution stays unknown rather than being promoted into a human identity.
- **Time and lifetime:** define whether a value describes request, load commit, activation or
  snapshot capture; name the clock/host or ordering basis. Do not invent a trustworthy global
  time or user identity from local sequence numbers or roles.

"In the contract" means readers have a supported way to discover these facts. Research whether
author declarations belong in a manifest/schema annotation and runtime facts in a host-owned
load record, linked by the actual artifact/incarnation. Do not bake a particular load's time or
actor into immutable schema identity merely to make it inspectable. The exact layout, ABI impact
and public retrieval protocol remain research questions.

The preflight should inventory existing manifests, loaded records, source associations,
accepted-shape discovery, state inspection, Senses and history. For every proposed field, name
the owner, source, availability, retention and reader permission. Explain behavior across reload,
candidate activation, provider changes, child failure and host restart. Prototype the smallest
useful answer in a generic info box and verify an unfamiliar consumer can read it. Descriptive
metadata never grants permission to load, inspect private state, change code or invoke an action.

## Recovery material is another inspectable source

Public contract discovery describes shapes; values require their own owner. Current
`DescribeAccepted` carries accepted roots and nested dependencies. `PokeDescribe` describes
state fields; `PokeRead` currently reads scalar text and is not a general nested typed snapshot.
Determine whether a typed retrieval extension or existing domain answers best serve the story.

Offer retained recovery material through the owner that still has it when the original weave
cannot answer. An isolation host retains admitted child snapshots and their schemas with the
mount; that can survive child death, but is not automatic durability across parent-host death.
Native `last_known_good` is not a continuously refreshed journal. A saved value, a retained
recovery snapshot, a current reply and a published observation must identify which they are.

Use Loom's existing Recorder and Logger for observed history under their retention policies.
Neither promises arbitrary private state, replay or a full process checkpoint. Preserve the
schema closure needed to interpret retained values after the supplier disappears. Viewing or
copying such material does not restore or execute it; recovery is an explicit owned operation.

## Maker actions and external authority

Inspection, grabbing a value and using it elsewhere are actions by the initiating maker, or an
ELH acting under granted authority. The source supplies facts; the destination owns validation
and the operation. Acquiring information and applying it are separately authorized. Source panes
do not need permanent destination powers, and a data reference carries no borrowed grant.

Preserve the initiator and applicable authority through input, gesture, menu/getter continuation
and the final semantic action. Establish them at the trusted boundary, not from a self-authored
payload claim. Raw input and direct ELH commands must not widen authority through Workshop.
Receiving Workshop decides ELH grants. Its ordinary policy must prevent an ELH from approving or
enlarging its own authority, including by clicking a privileged popup.

Approval is a separately authorized operation. In Loom's existing Weaver model the configured
operator decides, the Weaver delegates within its host-minted ceiling, and the session acts.
A popup can present that decision, but must not substitute its own privileged identity for an
unprivileged originating click. Weaver/operator authority is distinct from merely drawing the
popup or holding the `loom.weaver` role. Research both injected events and local artifact policy.

**Any ELH permission-bypass capability must be compiled out of ordinary builds.** An explicit development
build may include it; no runtime flag, configuration or message can enable an absent bypass.
Governed ELH control remains supported in ordinary builds. Many unattended tests can use bounded,
explicitly pre-approved authority and exercise normal enforcement; bypass evidence alone cannot
prove the normal boundary. Test self-approval refusal through actual authority-decision paths;
if an interactive approval path is introduced, exercise it with injected input too.
These are message-authority promises; they do not sandbox arbitrary trusted in-process code.

Source observations refreshed 2026-09-22 against the tree merged as
Zengine `8048c058ca6b2f245017921b3a3f78e3de8308c4`: it has receiving-side guest grants,
but Input republishes platform and injected events without
downstream origin distinction, and Workshop calls `trust_every_artifact` for plan artifacts.
Loom's tree merged as `4b4667904888c26cda862fcce6725549c97d7141` supplies Weaver's separate operator and
bounded delegation. Refresh actual execution heads and these paths before implementation;
the selected authority rule above is not a claim that Workshop already enforces it.

## Delivery arc and acceleration

**Current sequence (2026-09-24):** capture, Compose reuse, timed dragging, comfortable setups,
command presets, portable views, Terminal acquisition, interaction authoring, persistence and
independent Info are accepted; named folders merged as #58. The founder selected a
[complete tower-defense creation story through ELH](tower-defense-creation-story-plan.md): use
Workshop to author the game, preserve useful tools and reconstruct the creation in a paced demo.
Eligible Zengine changes reload into the running Workshop; foundational changes need a separate
decision. Tools, durable learning and repeatability govern success. The numbered arc below
describes the broader progression, not an instruction to redo completed capture work.

1. **Reuse the accepted ELH experiment.** Loom #10/#11 and Zengine #39/#44 are merged by founder
   confirmation. Its reusable setup/journey, maintained tool checks, native interaction proof and
   retained session context form the starting point; the [completion report](../../reportbacks/zengine-elh-workshop-improvement-completion-RB.md)
   owns the evidence.
2. **Deliver one-slot inventory capture.** Preflight, implement and prove a real typed item paired
   with automatically captured typed metadata, through a generic Set/Get contract. The
   [selected plan](inventory-capture-plan.md) and [executor prompt](../../prompts/zengine-inventory-capture.md)
   bound the phase. Preserve independent data/schema custody and ordinary message authority;
   this is one complete session, not a mandatory research/implementation handoff.
3. **Acquire from pane subjects and drag out for use.** Trace the subject to its actual owner,
   preserve actor authority and reuse the inventory pair/transfer contract. Research richer
   metadata only where the consumer needs it. Current Loaded selection does not supply a
   trustworthy current WeaveId. A copied reference confers no authority, and source disappearance
   cannot silently select a replacement. Full approval UI or global metadata remains unselected.
4. **Repeat with another subject and presentation.** A button property or document location
   should reuse the same tools. Prove cross-pane/Flow reuse and its structured counterpart
   against the same owner, exposing special-case glue before it spreads. Bags, richer views,
   dependency resolution and persistence follow their actual consumers.
5. **Package the demonstrated routes and broaden bounded stories.** Turn setup, fixtures,
   journeys and semantic assertions into reusable ELH packages. Each next story can then spend
   its effort creating and improving something, instead of rebuilding its harness.

The [Flow building-block direction](flow-building-blocks.md#5-cross-pane-drag-and-drop) consumes
the shared transfer boundary. Independent Flow UX, retained-view research and editor/pane work
continue; this arc is not a gate on every repair. General schema migration, service retirement,
full UI authoring, a package manager and distributed move transactions retain their own triggers.

For parallel work, name a source base, work location, experiment/runtime instance and intended
publication target. Use current Git/workspace mechanisms first; modularity does not eliminate
conflicts in shared contracts or runtime authority. Deliberate publication and founder-performed
PR merges remain separate from successful experimentation. Durable host sessions may retain
context while running; saved packages/results have their own durability and stale-lifetime rules.
The earlier [ELH Experiment 3](../../reportbacks/elh-workshop-improvement-arc.md#experiment-3--integrate-without-overwriting-another-tasks-reality)
remains the later parallel-adoption witness: two work contexts produce compatible candidates,
and a deliberate source/contract/destination change exposes a real adoption conflict. Schedule
it when the stories need parallel publication; it is not a prerequisite for typed inspection.

Keep the [ELH documentation route](../goals/workshop.md#elh-usability-and-extension-documentation)
small: capability, authority, invocation, result/failure and a link to the owner. Generic session,
run/history and package guidance belongs in Loom; Workshop extensions belong in Zengine; tool
help belongs with its package. Every relevant report includes ELH improvements and ceremony.

Success is less repeated setup and discovery, fewer tool/context transitions, clearer refusals,
reusable evidence and a result another maker can reproduce. Tests still verify behavior and
authority; human use judges understandability. Autonomous story work becomes appropriate where
scope and proof are clear, while foundational architectural choices remain founder-directed.
