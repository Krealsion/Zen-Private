# UI update research: retained descriptions and observable dependencies

**Status:** selected side research; no production renderer architecture selected.\
**Updated:** 2026-09-19\
**Authority:** [Workshop roadmap](../goals/workshop.md#ui-update-optimization-research).\
**First consumer:** [Flow UX](flow-ux-research.md), alongside ordinary pane movement/resizing.

## 1. Question and useful result

Can a pane publish how its view is represented once, then let a replaceable presenter respond
to changing dimensions and subscribed data without repeatedly asking the pane to rebuild the
same description? Measure the benefit while keeping failures, dependency ownership and the
relationship between displayed geometry and input understandable.

The founder's proposal combines static/percentage-based geometry, stable drawing descriptions,
dirty updates and variable-like access to live data. Separate the costs it could avoid:
description construction/publication, layout resolution, text measurement, drawing preparation,
rasterization and composition/presentation. A stable tree does not imply every later stage is free.

## 2. Existing pieces and evidence

Source baseline for Zengine: main `e561418fc031065c51ab362c3d6f40e34651fbf0`, 2026-09-19.
Refresh live source before experiments; the references below identify owners rather than frozen
line numbers.

- [Zengine UI](../../Zengine/docs/reference/ui.md) already separates authored extents/context
  from resolved geometry; its result is currently cached nowhere. Its cell-lattice document
  semantics do not automatically become the right representation for pane interiors.
- [Loom component vocabulary](../../Loom/include/zen/ui/component.hpp) declares field bindings,
  slots and presenters. It explicitly lacks a live binding/presenter runtime. Loom's
  [pixel layout](../../Loom/include/zen/ui/pixel.hpp) produces drawing commands and hit targets
  from a widget tree; it is another useful seed, not a required universal UI model.
- [Pane canvas](../../Zengine/workshop/pane_canvas_vocabulary.hpp) carries replacement pictures.
  [Room refresh](../../Zengine/workshop/weave_canvas.cpp) currently regrants on geometry changes.
  A retained view would need to separate description lifetime from resolved-frame/input validity.
- [Drag research](../../reportbacks/zengine-flow-presentation/drag-research.md) found repeated
  room/picture work under changed motions and explains why a generic queued paint marker can
  break causal settlement/capture. Its counts are not physical latency measurements. Reproduce
  the relevant workload before comparing designs; preserve the no-op and safe-preview repairs.
- Historical VarStorage lives in `G:/programming/cpp/DDnD/Zen/src/message_bus/var_storage.h` and
  `examples/var_storage_examples.cpp`. Conversion invokes a deferred getter, including functions
  over live objects. It has no change notification, dependency tracking, caching or snapshot
  contract. Preserve the ergonomic idea; do not treat captured pointers as portable bindings.

The observed drag pressure meets the wake condition of
[BL-ADOPT-03](../backlog.md#bl-adopt-03--performance-evidence-before-performance-claims) for a
bounded measurement effort. The backlog's wider maturity work stays parked; this research does
not create a general benchmark campaign or justify an unmeasured speed claim.

## 3. Candidate ownership model

```text
pane / view author -- description and binding intent --> presenter
data owners       -- authorized updates -------------> presenter-held values
viewport / metrics / input context ------------------> dependency evaluation
dependency evaluation --> resolved scene --> draw + hit map for that presented revision
```

The pane owns authored meaning; data providers own their values; the presenter owns evaluation
and resolved geometry within its grant; the medium owns font/device facts and physical drawing.
Application policy still owns room, focus and authority. Exact extraction/package boundaries are
a research result. Do not make Workshop's current ownership location permanent or require a new
Loom primitive without showing why an ordinary participant contract is insufficient.

The retained description should be inspectable and reloadable. Treat caches and native callables
as disposable implementation state, not durable authored identity. A future presentation weave,
UI-editing overlay and alternate medium should be able to consume the meaning without preserving
the old renderer's private objects.

## 4. Invalidation and data access

| Change | Candidate work; verify rather than assume |
|---|---|
| Pane translation | Placement, clipping/composition and input transform; retain interior layout where independent. |
| Bounds change with fixed content | Reconsider clipping/visibility; retain unaffected interior geometry. |
| Percentage extent changes | Reevaluate dependent geometry and downstream constraints only. |
| Wrapped text width or font metrics change | Remeasure/reflow affected text and dependent layout. |
| Colour/status changes | Paint invalidation if no size/ordering dependency changes. |
| Node/port added | Update description and relevant dependency structure. |
| Data provider replaced/revoked | Reconsider dependent bindings and expose stale/unresolved state; input changes only where the affected interaction policy requires it. |
| View/presenter owner or room grant lost | Revoke its input authority and end or explicitly transfer gestures. |

Track dependencies explicitly or through observable reads; compare those approaches for
introspection, dynamic/conditional dependencies, cycle handling and authoring ceremony. A getter
over arbitrary mutable state does not announce when it changes. Non-observable sources need an
explicit polling/sampling policy, never an assumption of permanent validity.

Cross-weave updates remain asynchronous. Reads during layout/drawing use presenter-held values;
they do not secretly block on messages or invoke an unloaded provider. Each frame evaluates a
defined snapshot of source revisions. Related values need an explicit publication boundary when
their consistency matters; do not imply a global atomic snapshot across independent hosts.

Separate persistent state from event streams. A newer state may supersede an older unpresented
state only where the contract permits it. Input edges, ordered actions and recorded events must
not be silently discarded. Time, animation and blinking are dependencies with explicit sampling,
not reasons to continuously rebuild every unrelated subtree.

## 5. Correctness that the optimization must preserve

- Paint and hit testing refer to the same resolved presentation; a cached picture is not current
  authority merely because it looks plausible. Define how input reaches the semantic owner.
- Geometry changes, lost grants, modal transitions and replacement still invalidate gestures at
  the correct time. Deferring physical paint must not erase an intermediate semantic transition.
- External input settlement and subsequent capture retain their causal ordering. A shared flush
  scheduled by an earlier input cannot silently stand in for later separately fenced work.
- Pending/error/cycle/stale bindings name their owner and cause. Last-known-value display is an
  explicit policy, not evidence that a provider answered. Makers may supply imperfect weaves.
- Descriptions and subscriptions are bounded/admitted, with honest refusals and retained authored
  intent. Hidden/offscreen views need defined subscription and resource-lifetime policies.
- TUI and SDL may project differently while preserving meaning. Backends must support any claimed
  partial redraw; retained layout alone does not promise the window system never repaints.

## 6. Small discriminating experiment

Use one pane with fixed text, percentage geometry, wrapped text, a colour/status binding and
one subscribed changing value. Compare the current picture route with a retained-description
prototype under movement, resize, text updates, rapid mixed input and provider replacement.
Include a denser Flow graph after the simple cases distinguish the costs.

Record description publications, room grants, source updates, dependency/layout evaluations,
text measurement, canvas submissions, actual presents, queue high-water and input-to-present
latency distributions. Identify hardware, build, workload and source revision. Do not reduce
success to fewer messages if retained dependencies or renderer work cost more overall.

Prove equivalent visible result and hit targets, ordered input, attributable failure, and capture
after settlement. Inspect the reason each part became dirty. Measure static and changing cases;
a colour-only update, wrapped resize, provider loss and replaced presenter should differ for
reasons the tool can explain.

Compare retaining whole descriptions first with finer patches; add patch identity and recovery
only if measured cost earns their protocol complexity. Compare scheduling improvements separately
from representation changes so one improvement is not credited to the other.

## 7. Deliverable and decision

Produce a reproducible baseline, prototype results, ownership/protocol sketch, failure and
replacement analysis, and a recommended smallest production consumer (or a reason to defer).
Name which existing vocabularies can be reused and which cannot. Research may reject an approach.

Flow UX research proceeds alongside this work. A minimal gesture/affordance repair does not wait
for a retained renderer; a large new graph presentation should use these findings before fixing
a difficult-to-replace protocol. General constraint solving, GPU replacement and universal native
reflection are not prerequisites.

## 8. Primary references

- [Qt retained scene graph](https://doc.qt.io/qt-6/qtquick-visualcanvas-scenegraph.html): retained
  graphical structure and opportunities for batching/reuse.
- [Qt bindable properties](https://doc.qt.io/qt-6/bindableproperties.html): dependency registration
  through observable reads, and the constraints on getters and intermediate writes.
- [Flutter repaint boundaries](https://api.flutter.dev/flutter/widgets/RepaintBoundary-class.html):
  separate display lists and limits on propagation of paint work.

These demonstrate mechanisms to study, not a recommendation to adopt a framework or copy its
threading, ownership or execution model into Loom.
