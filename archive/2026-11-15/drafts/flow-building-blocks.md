# Flow building blocks, reusable UI pairs and cross-pane authoring

**Status:** founder-selected research direction; contracts below remain design proposals.\
**Updated:** 2026-09-30\
**Accepted 2026-09-30:** [Flow's powers research](../../../../reportbacks/zengine-flow-powers-RB.md)
revises §2 to §5 below.\
**Entry:** [Flow UX plan](flow-ux-research.md).\
**Related:** [UI update research](ui-update-research.md).

The founder wants reusable non-primitive building blocks, explicit storage, operator tags,
native-source traversal and drag-and-drop composition across Workshop panes. A presenter/view
pair, including a recycling list, is the first complex composition to design toward. This page
owns the candidate inventory and architecture; the Flow plan owns screen/gesture choices.

## 1. Make storing a value visible

The high-water example should read:

```text
Reading.value ---------------------+
                                   v
Read highest [owned state slot] --> maximum --> Store highest [same owned slot]
```

Label the state owner, initialization and read/write roles. The Store action is an effect, with
a clear commit boundary, not a mathematical output that mysteriously becomes next time's input.
Do not draw a same-evaluation feedback cycle. The next message sees the committed value.
Initialization must state its domain: zero is a valid seed only when that is the intended floor;
an arbitrary signed high-water tracker needs a first-sample/presence policy instead.

Current maker semantics already have a write: after the complete trigger body succeeds, its
chosen result replaces `On.output` in the owner’s state. Later emitted messages are built using
the updated state. An evaluation refusal leaves that maker state unchanged; previously performed
ambient native effects are not rolled back. An emission failure does not undo committed state.
The existing `On.output` can therefore be presented as an explicit **Store** boundary without
pretending arbitrary state-writing operators already exist. See
[the source findings](../../../../reportbacks/zengine-flow-ux-refinement/state-patterns.md).

Current Store changes the running maker's in-memory state. Restart durability belongs to a
separate snapshot/save policy; do not label this write as saving a file or a durable checkpoint.

The store's on-screen position is presentation. Moving it does not change commit timing. Future
multiple writes, intermediate reads, conditional writes and shared stores need explicit ordering,
consistency and ownership contracts. A remote Store is an authorized request with an observable
outcome; it cannot be displayed as an immediate local assignment.

The small study calculates a proposed write in Draft Try and commits it only in Local live Try.
That is the study's explicit numeric behavior, not a promise that arbitrary native Try is pure.

## 2. Candidate standard library

Names below describe capabilities, not frozen identifiers or already-shipped APIs. Parameterized
notation is shorthand; it does not assert that the current schema system has generic type
constructors. Reuse current Loom/Zengine value kinds and extend their owning codecs deliberately.

| Family | Types / shapes worth supplying | Useful operations or templates | First consumer and ownership |
|---|---|---|---|
| Structured values | Named record, optional value, result with reason, typed list, stable item identity, value revision | Construct/project/update a record; explicit optional default; success/refusal branching; typed conversion | Operation authoring and examples. Immutable values belong to the value/operator owners. |
| Numeric and text transforms | Range, unit-bearing amount, formatted text | Clamp/remap, compare/select, format/join/parse with explicit failure | Clear first graphs and view-model projection. Specify overflow, units and conversion rather than guessing. |
| Collections | Keyed item, keyed sequence, slice/window, change set | Count/find/map/filter/sort/fold; stable-key lookup and diff | Lists and catalogs. Document ordering and callback effects; a data-shaped operator is not necessarily pure. |
| Owned state | State slot, state snapshot, update request/result | Read, Store, Reset; accumulator/high-water; keyed store | Explicit handler state first. Shared/asynchronous stores are stateful participants or assemblies, not hidden globals inside value operators. |
| Messages and time | Typed input/output, request correlation, pending/result state, subscription handle | Send/ask and observe; route/match; timer, debounce, throttle, change notification | Interactive applications. Use Loom's actual delivery/answer/history semantics; policy must say what is delayed, combined or lost. |
| Presentation values | View model, stable action/item identity, logical bounds/units, style tokens, viewport description | Format/project display state; resolve visual layout; map local input into typed intent | Presenter/view contract. Reuse existing geometry conventions and distinguish logical from device coordinates. |
| Reusable UI assemblies | Presenter/view pair; row view; recycling list; tree; schema-directed form; source viewer | Bind model, render, report intent; reuse bounded views; retain keyed edit state; navigate source | First complex consumer is a list of operators that can be dragged into Flow. Every collapsed assembly opens to its owners and connections. |

Begin with the blocks needed by two complete examples: high-water with an explicit Store, and an
operator catalog presented as a recyclable list. Do not implement this whole table speculatively.
Record construction/projection, typed results, collections and state ownership earn attention
before decorative widgets. Timer/debounce and richer collections follow specific examples.

The current finite operator graph does not supply general higher-order map/filter/fold callbacks.
A native collection leaf can be useful with honest source/effect metadata; a general iteration
or callback language needs its own evaluation, bounds and refusal contract.

Value schemas, value operators, stateful participants and assembly templates may share a discovery
library, but keep their kinds visible. This does not put every kind into the existing synchronous
`op::Catalog`. Dragging a template creates an inspectable draft of its participants,
wiring and declared requirements; it does not silently load artifacts or grant authority.

**Accepted 2026-09-30:** the library splits by kind
([power map](../../../../reportbacks/zengine-flow-powers/power-map.md)). Forms that run operators (loop,
choose, map, fold) belong to the operator evaluator; owned state, messages and time belong to
participants, so a Timer or a store is asked, never placed as a block; presentation values and
reusable UI assemblies belong to the view package and the UI builder. Flow's graph holds operators
and evaluator forms only.

## 3. Presenter/view pair

**Accepted 2026-09-30:** the pair is an assembly of two participants made in two tools, a
Flow-made presenter and a builder-made view, joined by shapes; it is not a Flow template. The
recycling list is the view renderer's. The roles and guardrails below still hold for the pair.

Proposed reusable assembly:

```text
data owner / service --> presenter --> typed view-model snapshot or update --> view
                              ^                                           |
                              +--------- typed input intent --------------+
                                                                          |
                                                  presentation commands / hit map
                                                                          v
                                                               presentation backend
```

The presenter holds application/presentation data and processing rules. It receives intents,
validates them against meaningful identities/revisions and asks the true data owner to change
business state. A presenter may own that state when the application deliberately gives it custody;
the pattern does not create a second authoritative copy automatically.

The view receives its view model and reads its own presentation state: viewport, hover, focus,
scroll position, animation progress and local geometry. It draws and reports input intents.
Local formatting/layout arithmetic is part of presentation, not a forbidden business operation.
It does not fetch business data or silently perform application writes when painting.

This refines “only graphical calls and own-state checks” just enough to support interactive
views: reporting `Activate(item_id, seen_revision)` is allowed; deciding its business meaning
belongs to the presenter. A pending operation is displayed from observed state; it is not made
successful by an animation finishing.

Use **presenter** for application/data projection and **view renderer** for the component that
resolves/draws presentation. Earlier UI-update research used presenter for that latter role;
the names must not accidentally assign drawing authority to the application presenter. Roles
need clear contracts, but do not mandate a separate loaded weave for every logical helper.
Message grants apply to participants: helpers sharing one weave share its authority. A colocated
pair can have graph/API rules, but independent grant-based restrictions require separate participants.

### Guardrails for this template

| Rule | How to check or enforce it | Honest limit |
|---|---|---|
| Presenter has no graphical output powers | No drawing nodes in its authored graph; no drawing grants for its participant; inspect transitive dependency requirements | An arbitrary in-process native provider can have ambient effects; tags and signatures alone cannot prove absence of graphics calls. |
| View owns presentation only | Typed view-model inputs, local presentation state and a narrow intent output; disallow direct business-service powers in the template profile | A source/code review is still needed for trusted native leaves. |
| Painting/inspection does not change business state | Separate render from commit/effect paths; explicit state/action boundaries; observe invocation/write counts in the witness | Reading a description is different from executing an unverified native getter. |
| One owner per authoritative state | Name owner and state slot; distinguish view-model snapshot from mutable domain state | Deliberate replication/caching remains possible with its own consistency policy. |
| Updates and input keep their meaning | Carry model/item/view revision where needed; validate stale intents; use the hit map for the shown frame | No global synchronous snapshot across independent hosts is implied. |
| Replacement preserves the rule profile | Recheck the resolved provider's requirements/provenance when it changes; invalidate the claim or refuse an incompatible replacement | A same-signature overlay need not have the same effects. |
| Rules are inspectable and replaceable | Show rule profile, checks, requirements, unknowns and refusal locations; custom assemblies may choose another profile | A declared tag is not a verified fact, and a rule profile is not universal Loom law. |

The template profile supplies useful guardrails for this pattern. A maker can author different
patterns; the UI should name which rules hold, which were deliberately changed and which cannot
be checked. Do not imply a security sandbox for arbitrary native code.

### Recycling list as the first complex pair

Outside, expose an item source, stable key, row-view template, selection/activation intent and
viewport configuration. A consumer can use this as one simple catalog entry. Inside, keep the
following owners traversable:

1. The presenter filters/sorts data and exposes keyed items plus model revision and loading/error
   state. It owns durable selection/edit state only if the application assigns that role.
2. The view's virtualization helper resolves visible indices from scroll/bounds/row metrics,
   acquires a bounded pool of row views and binds each to a stable item key and generation.
   It may compute visual geometry; it does not query or mutate the business model directly.
3. Recycling resets transient hover/animation/gesture state. Any retained edit/selection belongs
   to the item key, never merely to row number or a reused row widget. Old callbacks cannot act
   on whichever item happens to occupy the recycled row now.
4. Input is checked against the item/binding generation and displayed revision before the
   presenter applies its meaning. A stale click either identifies its original item or refuses.
5. Offscreen rows have explicit subscription/timer/resource policies. Bounds are real; an empty
   list, provider loss and partially loaded data still have an intelligible representation.

Start with fixed-height rows and measured bounded reuse, then earn variable heights and async
assets from actual pressure. Hiding these internals is a reading convenience, not a loss of
inspection or source navigation. [Qt's ListView documentation](https://doc.qt.io/qt-6/qml-qtquick-listview.html#reusing-items)
illustrates why recycling requires resetting transient state and treating pooled items as still
potentially alive; it is precedent, not a mandate to adopt Qt. The separation also resembles
[Passive View](https://martinfowler.com/eaaDev/PassiveScreen.html), while keeping Zen's explicit
message and ownership contracts.

## 4. Tags, descriptions and native source

**Accepted 2026-09-30:** prose rides inside each contribution, `zengine.OperatorContribution`
version 2, authored where the operator is authored, so an overlay brings its own words; every
asker reads it through the one [discovery door](../../../../reportbacks/zengine-flow-powers/discovery.md).
The maker's own tags and folders are Inventory's. Source for a provider's native leaf needs
operator → artifact → recipe, which does not exist yet.

Use one owner-supplied metadata projection for GUI search, hover help and terminal discovery.
Separate:

- descriptive tags, aliases, purpose and examples;
- input/output shapes and declared state/effect requirements;
- provider/contribution identity and revision;
- source locator, symbol/range and build/source provenance;
- verified rule-profile results, unknowns and the revision/dependencies they apply to;
- personal/project organization tags that do not rewrite a provider's published claims.

Tags are many-to-many and may cross folders. Neither `pure` nor `view-safe` becomes proof merely
because it was attached as a label. Keep metadata versioned and optional so older/missing
descriptions remain honest. This small common descriptor is a consumer of a wider metadata pass,
not an excuse to build a universal ontology first. The selected
[contract-metadata research](../backlog.md#bl-work-26--load-metadata-researched)
owns the distinction between author declarations and host-attested file, actor and load-time facts.

Entering an authored composite opens its graph. Entering a native primitive opens actual source
when available, including the function and registration that give it its catalog identity.
For the current basic provider, `math.max` is authored in
[`operator/primitives.hpp`](../../../../Zengine/operator/primitives.hpp). Provider overlays mean that
an identity alone is insufficient: show the currently resolved implementation, or the recorded
implementation for a historical invocation. A current lookup cannot establish past resolution;
historical claims require recorded provider/artifact provenance.

Distinguish **source associated with the loaded artifact** from **current editable checkout**.
Show mismatch, missing source, unavailable permission or a remote source boundary explicitly.
Current pane Edit Code already has source acquisition/Editor commitment owners; reuse them after
adding the missing operator-to-provider/artifact/source relation. Do not create a second file
opener or pretend provider-only operators are pane offices. Native providers currently lack an
in-place reload path; opening/editing source does not imply that the running implementation changed.

## 5. Cross-pane drag-and-drop

**Accepted 2026-09-30:** the typed carry exists (Editor transfers, #59). Flow joins it with
receivers for values, shapes, operator references and operations; the tally panel's compose
stage brings the first three.

Flow remains an intended consumer of the Workshop-wide transfer protocol. The accepted
[Editor transfer packet](../../../../reportbacks/zengine-editor-typed-transfers-RB.md) exercises selected text, command
insertion and file locators first, with separate optional C++ generation. Conventional code
editing must remain independently useful: no Flow document or compiler is required to reuse
material across these panes. Let the observed friction inform Flow's conveniences without
turning its representation into a mandatory path for source authors.

The host/input owner tracks the gesture across pane boundaries and resolves the current target
using current grants
and displayed geometry. The source offers a bounded typed payload or resolvable reference; the
destination owns validation and the eventual semantic edit. The
[maker-story section](../goals/workshop.md#complete-maker-stories-and-reusable-information) owns typed inspection and authority across these
routes: acquisition and use are separate actions by the maker or an ELH with granted authority.
Handling the actor's data does not grant a pane that actor's authority. A privileged intermediary
must not turn an ELH gesture into a maker approval. Any ELH permission bypass must be compiled
out of ordinary builds.

Useful first transfers:

| Source | Payload | Flow's deliberate result |
|---|---|---|
| Operator catalog / Info | Definition reference with provider/revision context | Add an occurrence, keeping dependency provenance. |
| Typed value/message library | Value plus schema identity | Fill a compatible constant or save a named input example. |
| Project Files / Editor | Source or artifact reference | Open/associate source, or offer a supported import; arbitrary C++ is not automatically an operator. |
| Assembly library | Presenter/view or list template reference | Instantiate an inspectable draft of the assembly and its requirements. |
| Another Flow graph | Authored selection/definition reference | Copy/import/link with explicit scope and supported boundaries; never silently move running state. |

A candidate protocol could carry a gesture/offer identity, source incarnation, available representations,
copy/link/move intent, payload bounds and expiry. The target previews compatibility without executing
content. On drop it revalidates the target document/version and commits one semantic edit or an
attributable refusal. Source/target replacement, Escape and lost grants cancel appropriately.
Repeated delivery cannot commit twice. A move needs source deletion only after a verified target
commit; begin with copy/reference transfers rather than a distributed move transaction. These mechanics
are research proposals to test against the story, not a frozen wire contract.

A reference is not authority. No drag payload contains borrowed drawing grants, reload powers or
an implicit permission to compile/run. Native-artifact activation and file writes remain separate
authorized actions. Source-provided labels and type claims are checked at the destination owner.

Terminal agents spend the same add/import/bind commands with explicit references, versions
and their own granted authority.
They do not have to synthesize a pointer drag. The corresponding accepted/refused receipt names
the same object the GUI shows. This keeps cross-pane UX and agent participation one capability.

## 6. Dependency order and useful witnesses

1. Correct the interaction study and visible state boundary; collect founder/human feedback.
2. Coordinate with the maker-story preflight on typed information, contract metadata, actor
   provenance and approval authority. Reuse schema/value tools and source owners for tags,
   hover details and explicit semantic targets; do not open a competing reflection project.
3. Deliver an operator or typed-value transfer into Flow through that shared boundary. Prove
   the equivalent terminal/ELH action against the same model, including missing authority.
   Confirm reuse with another subject rather than treating a Flow-specific adapter as general.
4. Extend reusable authoring from value operations to explicit assembly templates. Use one
   presenter/view pair, then a recycling operator list, as the proving consumer.
5. Let that list provide concrete retained-view/update measurements. It shares dependencies with
   UI-update research without making a universal rendering rewrite a prerequisite.

Witnesses should include failed computation with unchanged owner state; failed emit after committed
state; separately authorized presenter/view participants refused graphical/business powers outside
their roles (or explicitly narrower graph/API checks for colocated helpers); unknown native
effect claims; row reuse with pending input; stale cross-pane drop; changed provider/source; cancelled
drop without mutation; and a terminal request that produces the same draft as the GUI transfer.
Keep keyboard/vim movement extensible through semantic movement commands; the default UI supplies
dragging and does not spend space on Move left/right buttons.
