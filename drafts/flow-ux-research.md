# Flow UX: discover, compose, inspect, and reuse

**Status:** initial source/live/prototype research complete; human validation and production decisions remain. Interaction and delivery details below are proposals.\
**Updated:** 2026-09-30\
**Accepted 2026-09-30:** [Flow's powers research](../../reportbacks/zengine-flow-powers-RB.md)
revises §3, §4, §7 and §10 below; the 2026-09-20 selections stand.\
**Authority:** [Workshop roadmap](../goals/workshop.md#flow-ux-research-and-hierarchical-authoring).\
**Companions:** [UI update research](ui-update-research.md) and
[building blocks, presenter/view pairs and cross-pane authoring](flow-building-blocks.md).
**Founder refinement:** [2026-09-20 evidence](../../reportbacks/zengine-flow-ux-refinement-RB.md).
**Research result:** [recommendation and evidence](../../reportbacks/zengine-flow-ux-research/research-result.md),
with separate [agent contract](../../reportbacks/zengine-flow-ux-research/agent-interface.md),
[semantic options](../../reportbacks/zengine-flow-ux-research/semantic-options.md) and
[human task protocol](../../reportbacks/zengine-flow-ux-research/human-patterns.md).
The isolated walkthrough completed a running high-water example; the interactive study remains
a local simulation. No novice-human study or production redesign has been completed.

## 1. Outcome and scope

A maker should be able to find a useful operation, drag it into a graph, connect meaningful
inputs and outputs, exercise it, understand the result, and package useful work for reuse.
Complexity can be hidden behind a small interface while its available implementation remains
traversable. A novice and an expert spend the same underlying commands and runtime contracts.

The founder tried the current Flow pane and found it confusing. Selected direction: serious UX
research, direct manipulation wherever useful, a default folder-like palette with input/output
previews, movable nodes, and inspectable nested composites. The old box workspace is interaction
lineage worth evaluating. This does not select restoration of its retired document model.

This plan is an end-to-end destination with a research/delivery sequence, not a claim that every
proposed control or semantic capability already exists. No implementation is authorized merely
by a sketch here. Research should converge on a coherent execution packet, with meaningful
milestones rather than a mandatory prompt or PR per feature.

## 2. Current baseline and the consequential gaps

Source baseline: Zengine main `e561418fc031065c51ab362c3d6f40e34651fbf0` (PR #42), inspected
2026-09-19. PR #40 added standalone authoring/generation; #41 added the graphical pane and
reusable typed drafts. The founder's confusion is hands-on evidence. The initial research subsequently
completed a source/guide-informed isolated live walkthrough and a local interaction study;
these are agent evidence, not unassisted human usability validation. The report owns its exact
build provenance and limits.

| Present capability | Research pressure |
|---|---|
| Header dragging, panning, zoom and persisted layout | Make them apparent and consistent; add selection/movement affordances instead of claiming dragging is wholly absent. |
| Flat catalog list, click-to-add, source-click then destination-click wiring | Searchable palette, drag-out creation and drag-to-connect, with useful non-drag alternatives. |
| Canvas motion currently follows held gestures | Hover previews need an owner-appropriate pointer/focus seam, including leave/invalidation and queue cost; pinned/click/focus previews can work earlier. |
| Separate State, Messages and Graph pages | A newcomer currently needs state and a message before the first trigger; make the starting task legible without learning index-based bookkeeping. |
| Graph draft separate from running participant; Run, Apply and Stop | Show which revision is being edited and which is running, with outcomes beside their cause. |
| Existing operator composites | FlowCatalog exposes signatures, not composite bodies; recursive inspection needs an owner-supplied description seam. |
| Single-output graph nodes and one selected composite result | Plural exposed outputs and extraction of arbitrary selections require a capability decision, not merely more ports painted on a box. |
| Each trigger selects one state field; emission mappings lack a visual editor | Include input/schema, state and output authoring in the completeness audit; a better operation canvas alone does not complete the weave-authoring loop. |
| Authored node vector is execution order; forward links are refused; every node executes | Spatial movement and grouping must not silently reorder, omit or duplicate execution. |

Routes: [pane guide](../../Zengine/docs/workshop/flow.md),
[Flow reference](../../Zengine/docs/reference/flow.md),
[host boundary](../../Zengine/docs/reference/flow-runtime.md),
[graph edits](../../Zengine/flow/graph_edit.hpp),
[pane view](../../Zengine/flow-pane/view.hpp),
[catalog replies](../../Zengine/flow-host/runtime.hpp),
[operator model](../../Zengine/operator/operator.hpp), and
[contribution descriptions](../../Zengine/operator/provider.hpp). Refresh live source before
execution; these routes identify owners, not permission to copy their contracts into the pane.

## 3. One workspace with discoverable supporting surfaces

Design for a landscape 1920×1080 Workshop first, while keeping a smaller Flow pane usable
beside other panes. The composition adapts to available room; it does not shrink every label
to fit a miniature desktop. Candidate arrangement:

```text
Project / Trigger / Composite / Nested composite       Draft r7 | Running r5
+------------------+------------------------------------------------------+
| Search           | Graph                                                |
| In scope         | message + read state -> operations -> explicit Store |
| For this port    |                                                      |
| Kept (Inventory) | hover/focus details; Open enters                     |
| All, by kind     |                                                      |
+------------------+------------------------------------------------------+
| Try an input / Diagnostics / Events (expand when needed)                 |
+-------------------------------------------------------------------------+
```

Supplementary operator information belongs in hover/focus tooltips, not a permanent inspector.
Keep editable constants, required bindings, errors and navigation reachable without hover.
Contextual editing and optional companion Info/Editor panes can expose deeper tasks. Collapse
the palette/observations when room is limited; keep Flow's internal hierarchy distinct from
Workshop's pane hierarchy. No essential action requires keeping another pane open.

**Accepted 2026-09-30:** the palette's sections are what is in scope (the message's fields and the
state the body reads, which today's pane calls "Sources"), suggestions for the selected port, kept
powers (an Inventory folder of references) and all powers by kind. Saved examples leave for
Inventory (§7).

The recommended entry offers examples and two intents: **Compose an operation** and
**React to a message**. The existing high-water tracker remains a useful stateful starter:
incoming reading, Read highest, comparison, explicit Store highest into the same owned state
slot, and a test message. Storage commits after the complete handler body succeeds and before
emissions are constructed; it is not a same-evaluation feedback wire. The
[storage contract](flow-building-blocks.md#1-make-storing-a-value-visible) distinguishes current
in-memory behavior from future durable/shared storage. A reusable calculation
should not require invented state/trigger ceremony. Source research established that current
maker triggers require a state output, while independent operation composition can use the
existing catalog/evaluator. The new operation draft and managed publication still need explicit
contracts; this is a design recommendation, not a shipped capability.

## 4. Discovery and direct manipulation

### Palette

- Search asks the [discovery door](../../reportbacks/zengine-flow-powers/discovery.md#the-door)
  across names, prose, tags and input/output signatures; categories are provider-authored tags, and
  the sections are §3's (accepted 2026-09-30). The maker's own folders are Inventory folders of kept
  references; they organize, and never rename operators or change authority.
- Hover or keyboard focus shows a small port map, purpose, types, defaults/required values,
  provider, availability and a short example. Make the tooltip dismissible and reachable while
  inspecting it, with a focus/touch route; essential information and actions remain available
  without hover or colour discrimination. Selection alone does not open a permanent side panel.
- Drag a result onto the canvas with a placement preview; commit on drop. Escape cancels.
  Add by click/keyboard is an equivalent semantic operation. Filtering retains the user's place.
- Opening a port's picker or dragging its wire into empty space filters compatible candidates.
  Explain unavailable/incompatible items; an empty list must not conceal why nothing fits.
- Sources that require sampling remain explicit. A preview displays declared metadata and
  already observed values; hovering must not invoke arbitrary operators or send messages.

### Canvas and wiring

- Clear header/grip for movement; visible named ports; generous measured hit areas; drag threshold
  distinguishes selecting from moving. Wheel/zoom/pan behavior is visible and consistent.
- Drag wire to a port, preview compatibility and the exact resulting binding, then commit.
  Support click-source/click-target and keyboard connection for precision and accessibility.
- Show required/unconnected, constant-bound, connected and unavailable ports distinctly.
  Inline constant editing should coexist with the common schema/value editor, not invent types.
- A refused connection explains type, scope, execution-order or lifecycle constraints at the
  destination. Offer a deliberate visible conversion when supported; no hidden casts.
- Reconnect and remove a wire, duplicate/delete nodes, multi-select/move, frame selection,
  fit graph, and undo/redo. One completed drag is one undoable edit, not hundreds of motions.
- Useful organization includes labels, optional snap/alignment and manual reroute points.
  Automatic layout is an explicit presentation action and never reorders execution.
- Preserve incomplete work. Unfinished drafts within the workspace's admitted structure and
  bounds can be saved, navigated and repaired; Run/Apply
  explains the remaining admission problems without destroying the draft or incumbent.

Quarry the old workspace for hit/drag geometry, selection, authored-versus-resolved separation,
and persistence patterns. Review code against current device coordinates and ownership before
reuse. Do not revive `WorkshopDoc`, a second graph authority, or the retired canvas as host UI.

Candidate gesture map to test in graph context (text fields keep their editing behavior):

| Intent | Proposed gesture and discoverable alternative |
|---|---|
| Select / inspect | Click selects; hover/focus reveals supplementary operator details. |
| Move selected nodes | Drag header after a small threshold; no Move left/right buttons. Semantic movement leaves room for later user-defined keyboard/vim bindings. |
| Select a region | Left-drag empty canvas for marquee; modifiers extend selection. |
| Pan | Middle-drag or Space + left-drag; visible pan tool for devices lacking a middle button. |
| Navigate / zoom | Wheel pans; explicit zoom controls, with a modifier-wheel candidate centred at pointer. |
| Connect | Drag from port, or select source then destination; drop on empty room opens compatible search. |
| Inspect / enter a composite | Click selects; double-click, Enter or visible Open enters when no text field owns the key. |
| Cancel / leave | Escape cancels the current gesture/edit first; explicit Up/breadcrumb leaves a composite. |

This deliberately revisits current blank-drag panning to make room for marquee selection.
Research may keep panning as default and expose selection through a visible tool instead. Resolve
the conflict explicitly and test it with trackpad/keyboard users. Parent/desktop Escape fallback
must use the existing consumption contract, not infer non-consumption from a quiet pane. Gestures
inside the graph must remain distinct from Workshop's outer pane move/resize controls.

## 5. Organization, nesting and reuse are different acts

| Concept | Meaning | Editing consequence |
|---|---|---|
| Palette folder/tag | Organizes discoverable definitions and examples | Changes where something is found. |
| Visual group/frame | Names and optionally folds a region of this graph | Changes presentation only; execution is unchanged. |
| Composite definition | Named interface backed by an authored composition | Changes reusable behavior when explicitly published/applied. |
| Composite occurrence | One use of that definition with bindings/configuration | Changes this occurrence's inputs or local presentation. |

Proposed default: selection inspects; double-click or a visible **Open** action enters a
composite. Breadcrumbs, back/forward and Up return to the exact occurrence, restoring selection,
pan and zoom at each level. Search can reveal a nested node through its path. Wires crossing a
boundary terminate at named interface ports, and those ports lead to their internal bindings.
The same definition may be used many times: navigation retains the occurrence path as well as
the definition identity.

**Grouping first, extraction when honest.** A presentation-only fold may hide arbitrary selected
nodes while preserving their original execution positions. Extracting a callable composite is a
semantic edit: identify boundary values, preserve execution order and effects, show the proposed
interface, and refuse unsupported selections with a remedy. Noncontiguous selections can have
interleaved effects; a new function call cannot simply replace them at one position. Do not infer
purity because an operator's arguments omit bus access, or skip unused nodes.

Expose named inputs, defaults, result(s), documentation and observed failure paths. Audit the
single-result model and contribution codec before selecting support for multiple outputs or
additional constant kinds. Do not quietly pack an arbitrary interface into a special UI-only
object or create a second evaluator to make the picture look complete.

**Reuse needs visible edit scope.** A definition view should say where it is used. Editing a
shared definition changes a draft; show affected uses before deliberate publication. Provide
"make independent copy" for a local variation. Folder movement, opening a box and editing an
occurrence's constant must never silently change every use. Research which identities/revisions
the current catalog can honestly resolve before selecting version pinning or automatic updates.

Keep composite evaluation separate from stateful weave/message boundaries. State ownership,
initialization, reset, message emission, asynchronous pending work and authority need explicit
owners. An ordinary operation group must not acquire those semantics just because it is boxed.
The first reusable-composite proof should use existing operation semantics; any richer boundary
is separately declared and explained in the graph. A reusable presenter/view pair is an assembly
of participants and connections, not a value operator with hidden state/authority. The
[building-block plan](flow-building-blocks.md) owns that inventory and its rule profile.

**Traversable means all available meaning is reachable.** Authored composites open to their
graphs. Entering a native leaf opens its actual available implementation through the source/Editor
owners, including registration and resolved-provider provenance. Distinguish loaded-artifact
source from the editable checkout; the [source contract](flow-building-blocks.md#4-tags-descriptions-and-native-source)
names the missing metadata and historical evidence requirements. Missing bodies, sources or
permission are named boundaries, not fabricated subgraphs or an implied native decompiler. Unavailable providers leave inspectable authored intent.

## 6. Make behavior understandable while it runs

- Distinguish message arrival, value dependencies, evaluation order, state updates and emitted
  messages. Use labels/port shapes as well as colour; explain execution order without requiring
  makers to memorize vector indices. Dragging a node never changes behavior.
- Keep draft revision, applied revision, initial-state edits and observed running state distinct.
  Apply is deliberate; unsupported contract changes say whether a fresh run or authored migration
  is required. Undoing a draft edit does not undo effects already produced by a running weave.
- Make accepted message schemas, state fields and emitted message mappings discoverable and
  editable through their actual owners. Identify which schema-directed forms can be reused and
  which operations the current graphical surface cannot yet express.
- Show validation and runtime problems at the owning node/port and in a navigable list.
  Nested errors include a path back through composite occurrences. Queued, delivered, refused,
  pending and observed output remain separate facts. Application completion can remain unknown
  or pending after dispatch settles; a silent participant does not itself keep a dispatch fence open.
- Reusable test messages are ordinary typed drafts. Select an example, send deliberately,
  inspect state/output and follow its correlation. No side-effectful auto-run on hover or typing.
- Port values and execution highlighting require real observations with revision/run identity.
  If the current runtime exposes only trigger outcomes, say so; research per-node observation
  as a separate capability. Never re-execute the graph to invent a debug preview.
- Reuse Loom Recorder/Logger and the host's authorized observations. Replay, stepping, breakpoints,
  and resumed native continuations are later capabilities, not consequences of adding animation.

## 7. Persistence, commands and replaceability

Graph meaning remains under the definition/operator owners; workspace layout, folders, groups
and navigation remain presentation metadata. Reusable definitions and their occurrences need
stable identity; renaming/reordering must not retarget a binding. Define what the project carries
and what remains an external dependency. Importing a Flow workspace/composition package admits
data; any native-artifact load remains a separate host policy/execution action. Neither grants
authority merely through its presence.

**Accepted 2026-09-30:** examples are Inventory's typed values, carried in and out; a saved
workspace stops carrying named examples, and its retained forms stay.

Preserve workspace save/reopen, incomplete forms, historical schemas and explicit dirty handling.
Version any changed durable format with an honest migration/refusal path. Saving authored work
does not save pending queues or process continuations. Provider/pane replacement ends or explicitly
transfers active gestures; it must not commit the wrong node from stale hit maps.

GUI, keyboard and messages should use the same semantic edit model. Research found that
FlowEdit exists but default Terminal/ELH direct semantic authoring is not end-to-end usable:
vocabulary/grants and structured payload composition are missing; reads can cancel a drag and
commands depend on active UI context. The [agent audit](../../reportbacks/zengine-flow-ux-research/agent-interface.md)
owns the proposed harmless queries, explicit object/version targets, later runtime results and
shared terminal payload route. Prove both Workshop TerminalSession and loom-host ConsoleEngine,
including actual ELH transport; input injection is useful evidence but is not semantic parity.
Cross-pane drag/drop uses Workshop's shared offer/preview/commit/cancel ownership with typed
references; Flow consumes it through the same semantic add/import/bind commands agents use.
See [the transfer contract](flow-building-blocks.md#5-cross-pane-drag-and-drop). Coordinate with the
parallel pane-UX work around menu, pointer, focus and form ownership. Research composition-level
transactions and undo at the semantic owner rather than building a GUI-only command history.

## 8. Research and delivery sequence

| Milestone | Work and evidence | Boundary |
|---|---|---|
| A. Observe and design | Run real newcomer/returning-maker tasks, log assumptions, compare low-fidelity layouts and gesture maps, trace missing semantics. | Select the screen vocabulary and resolve high-consequence forks before production contracts change. |
| B. Direct authoring loop | Palette/search/previews, placement and connection gestures, navigation, hover/focus details, contextual edits, errors and undo; finish a useful graph and exercise it. | Keep current operator/runtime meaning; a graphical demonstration alone does not prove learnability. |
| C. Hierarchy and reuse | Visual groups, inspect existing composite bodies, extract/name/reuse supported compositions, traverse occurrences and show edit impact. | Description transport, outputs, identity and ordering changes require explicit design and evidence. |
| D. Live understanding | Connect diagnostics/examples/available observations to the graph, including nested failures and draft/applied divergence. | Richer per-node observation is earned here if the existing host cannot supply it. |
| Parallel research | Retained descriptions, live bindings and invalidation using actual Flow workloads. | [UI update research](ui-update-research.md); no global rendering rewrite as prerequisite for B. |

These milestones describe dependencies and reviewable outcomes, not compulsory separate sessions.
Research may prototype across them to discover the right model. Implementation can complete the
whole selected packet when its premises hold; record significant discoveries and context handoffs.

## 9. Tasks that judge the result

1. Starting from an empty pane, create and run a small message-to-state flow without consulting
   private implementation docs. Identify what starts it, what data it needs and what it changes.
2. Find an unfamiliar compatible operation by purpose/type, preview it, drag it in, connect it,
   correct a bad connection, and undo an accidental move/deletion without losing work.
3. Fold a visual group without changing execution. Separately extract a useful sequence into a
   composite, expose its supported interface, save it to the palette, use it twice, enter one
   occurrence through two nested levels, trace a port inside, return, and distinguish editing the shared definition
   from making an independent variation. Verify identical runtime behavior before/after extraction.
4. Change a draft while an older revision runs; send an example; explain which revision produced
   the result. Locate a nested refusal or missing provider without inventing unavailable evidence.
5. Save/reopen and replace a pane/provider, retaining authored work and honest unresolved state.
   Repeat key tasks at a small viewport and with keyboard/non-drag controls.
6. Drag/pan/resize a populated graph while input and observations arrive. Measure input-to-present
   latency, queue growth, publications and layout/paint work; check capture after settled input.

Record intended action, first attempted action, actual outcome, recovery, external knowledge,
important "aha" moments and time spent finding owners. Count decisions and context switches as
well as clicks. Agent exploration and reproducible ELH journeys support the audit; a founder or
new human's first encounter is distinct evidence. Set performance targets from measured baselines
and the desired interaction, not an arbitrary benchmark score.

## 10. Proposed defaults and decisions research must settle

Initial research recommends first-class operation authoring, a typed return binding for direct
input/constant results, conservative extraction of contiguous single-result intervals, and local
shared drafts activated through explicit project-scoped application. The
[decision table](../../reportbacks/zengine-flow-ux-research/research-result.md#decisions-recommended-before-production-contracts-freeze)
explains the owner-level changes. These are not yet founder-approved semantics. Keep arbitrary
visual grouping distinct; no lazy evaluation, general multi-output model or global replacement
policy is implied. Actual human task observation remains outstanding.

- **Proposed:** folders organize; groups simplify a drawing; composites define reusable behavior.
  Select-to-inspect and Open-to-enter avoid making every click navigate away.
- **Founder selected:** landscape-first composition, default dragging without Move buttons,
  supplementary operator details on hover, explicit storage, tags, native-source traversal,
  non-primitive building blocks and cross-pane composition. The companion plan separates
  selected outcomes from proposed protocols and enforcement limits.
- **Accepted 2026-09-30** ([Flow's powers research](../../reportbacks/zengine-flow-powers-RB.md)):
  a loop is an evaluator-owned fold over an operator reference resolved through the one catalog,
  fold first and collect later. It counts first and runs by count, refuses a step of 0, takes its
  direction from the step's sign and excludes the limit by default; Flow binds the default step of
  1 at placement. Each loop has a count bound, and a per-evaluation spend budget in the catalog
  lands first, bounding nested loops and call cycles too. UI building belongs to a UI builder
  beside Flow, joined to it by shapes. The 2026-09-20 selections stand; the
  [building blocks plan](flow-building-blocks.md) says where each block now lives.
- **Proposed:** contextual palette and editing replace much routine modal/index entry;
  modal decisions remain for genuine destructive or authority-bearing transitions.
- **Proposed:** visible execution order first; changing ordering semantics is an explicit language
  decision. Multiple outputs need a deliberate owner-level capability choice.
- **Open:** the exact first-screen vocabulary and small-pane arrangement; test competing sketches.
- **Open:** supported extraction shapes, shared-definition update policy, and whether the first
  reusable artifact can use the current contribution representation without extending it.
- **Open:** which runtime observations are available cheaply and which demand new instrumentation.
- **Open:** how much old workspace code survives current coordinate/ownership contracts; reuse
  proven mechanisms and interaction ideas, not its obsolete subject model.

## 11. Prior art to examine without importing its semantics

[Unreal's node editor](https://dev.epicgames.com/documentation/en-us/unreal-engine/nodes-in-unreal-engine)
offers drag-from-pin contextual discovery and visibly differentiated execution/data connections.
These are useful interaction references, not a mandate to adopt Blueprint execution or implicit casts.

[Node-RED subflows](https://nodered.org/docs/user-guide/editor/workspace/subflows) demonstrate
reusable palette entries, instances and an editable interior with exposed boundaries. Their own
interface and selection restrictions illustrate why extraction must respect the underlying model.
Do not import those restrictions or message semantics into Flow by analogy.
