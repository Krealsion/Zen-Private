# Source research behind the presentation-manager draft

2026-09-11. Supports the [discussion draft](presentation-manager.md); it is not production law.
Static source tracing and architectural review only. No new build, runtime probe, platform
failure injection or performance measurement was performed for this draft. Proposed behavior
is labeled in the draft; observations below describe the inspected code and contracts.

Inspected identities: Zengine `9cbf5a5ac8d4751472dc891371401d93a25e03cc`;
Loom local `eee04550dfbae61638ff84f1c9da1c32ad90f9b0`, whose source tree matches accepted
`f20f32df01e36ae672cef8013ea4499b76e3954c`; Zen report baseline
`d134017b5c11a22239d6de8eedb68b5efce8496a`; private baseline
`c1e7fda5129376b2e4928db425b59b2cde47473b`. No remote state refresh is claimed.

## E1 Unanswered work and existing management

- [Realization law](../../Zengine/agents/realization.md), lines 81–90, 120–151:
  `PlanExecutor` is a host-local owner; `PlanBooter` is its message bridge. An unanswered load
  remains loading indefinitely. Empty queue/turn does not establish refusal or abandonment.
  Host policy decides whether a failed plan should end a process.
- [WeaveManager](../../Loom/include/zen/kernel/manager.hpp), lines 11–33 and 151–209:
  an ordinary replaceable broker to kernel control, without a Kernel pointer or its own
  application policy. Its current public operations include load, swap, reload and list.
  Reaching that broker is meaningful authority, not harmless ordinary messaging by definition.
- [Kernel control](../../Loom/include/zen/kernel/control.hpp), lines 203–222:
  successful load registers the participant and queues activation before answering with its id.
  [Lifecycle law](../../Loom/docs/laws/lifecycle-laws.md) separates activation from health/readiness.

**Inference:** a presentation manager can reuse a proven owner/bridge relationship. Its own
workflow state and policy do not require Loom to make every request eventually settle.

## E2 Where presentation lives now

- [Workshop repaint](../../Zengine/workshop/weave_run.cpp), lines 24–65:
  refreshes room/projections, reads current owners, publishes status/attention and the composed
  picture. It is not a rendering backend.
- [Workshop handlers](../../Zengine/workshop/weave_handlers.cpp), lines 135–162 and 191–222:
  Skin greeting prompts initial composition/restoration; medium extent changes the screen,
  reconciles setup and repaints.
- [Pane content/reveal seam](../../Zengine/workshop/weave_seam.cpp), lines 156–200 and 282–356:
  Workshop admits a pane's content and separately changes setup, selection and keyboard focus.
  The current Editor reveal commitment is the unaccepted mechanism analyzed by the research.
- [External text route](../../Zengine/workshop/weave_external.cpp), lines 169–177:
  Workshop forwards a pane id and text to the provider's role. Document generation is not in
  that current text shape.
- [Presentation decision](../../Zengine/agents/decisions/a-presentation-owns-no-facts.md),
  lines 7–25, and [pane waiting law](../../Zengine/agents/workshop/panes-and-windows.md),
  lines 222–233: a panel presents another owner's facts; an unanswered room request means waiting.

**Inference:** composition, room, focus and semantic routing already form a related ownership
cluster. Extracting that responsibility is distinct from moving tool state into it. The
decision-record title must be read in its build/pane context, not as a prohibition on all
presentation-specific authoritative facts.

## E3 Media, input and resource ownership

- [Skin shell](../../Zengine/surface/skin.hpp), lines 7–60 and 96–110:
  `SkinT<Medium>` is a weave over a native medium that supplies canvas, clipboard, placement,
  extent and pumping. [SDL export](../../Zengine/surface/skin_sdl.cpp), lines 701–705,
  exports the instantiated Skin as a loaded weave.
- [Surface law](../../Zengine/agents/surface.md), clipboard/placement sections and lines 457–469:
  raw input broadcasts are not focus arbitration; multiple canvas publishers overwrite whole
  pictures. A surface arbiter is an explicitly named future seam.
- [SDL medium](../../Zengine/surface/skin_sdl.cpp), lines 117–153 and 273–315:
  Skin and input reader can be independently selected, share SDL subsystem lifetime, and must
  not steal each other's events. The Skin pumps without consuming the reader's queue.
- [Artifact intent](../../Zengine/workshop/load_plan.hpp), lines 9–50:
  mounting an operator-provider surface and loading a weave are separate optional intentions.

**Inference:** a manager should reconcile semantic presentation without absorbing platform
event capture or forcing one artifact per lower-level graphics concept. Candidate resource
coexistence is a real constraint; live native resources cannot be assumed to follow role changes.

## E4 Loaded and ready do not establish working output

- [SurfaceReady](../../Zengine/surface/vocabulary.hpp), lines 572–580, is a once-per-incarnation
  greeting. [SkinT::on(SurfaceCanvas)](../../Zengine/surface/skin.hpp), lines 125–130, calls
  `announce_surface_once` before the void medium call and increments the frame count afterwards.
  The announcement at lines 224–230 does not query output success.
- [SdlMedium](../../Zengine/surface/skin_sdl.cpp), lines 140–153, 210–217 and 608–636:
  SDL initialization may leave `ok_` false; canvas may return without drawing; window/renderer
  creation can fail. `complain` at lines 103–112 writes the operation and SDL reason to stderr.
- [Exported construction](../../Loom/include/zen/kernel/export.hpp), lines 334–340,
  reduces a thrown constructor to null; [Kernel load](../../Loom/src/kernel/kernel.cpp),
  lines 1045–1047, reports that create returned null. Detailed reasons are not uniformly retained.

**Source-derived conclusion:** current load success, greeting and counters cannot establish
successful platform output. A scoped readiness/failure conversation must define its evidence.
No failed-display run was performed here. This does not retroactively redefine the existing
greeting as a promised renderer health check.

## E5 Lifecycle boundaries and continuity

- [Prepared replacement](../../Loom/docs/reference/prepared-replacement.md), lines 44–105:
  exact-participant preparation/admission is available. The coordinator interprets the domain
  answer; Loom authenticates the conversation. It does not supply incumbent state continuity,
  infallible application handlers, or a transaction over device effects.
- [Kernel reload](../../Loom/src/kernel/kernel.cpp), lines 1176–1240:
  early shape/manifest refusal precedes replacement, but late revive refusal occurs after the
  incumbent instance was destroyed and can leave the weave unavailable. Blanket rollback
  promises for every unsuccessful reload would be false.
- [Manager swap](../../Loom/include/zen/kernel/manager.hpp), the legacy swap contract near
  line 53, unloads then loads. A failed successor does not preserve the old participant.
- [Kernel role unload/query](../../Loom/src/kernel/kernel.cpp), lines 1274–1328:
  a native registered holder is not a Kernel-owned artifact to unload through that path.
  [Control](../../Loom/include/zen/kernel/control.hpp), lines 245–260, has unload operations;
  the current Manager vocabulary has no standalone unload command.

**Design obligations:** choose the exact supported transition, source of active-binding truth,
and cleanup authority. Candidate preparation must respect the incumbent's native resources.
The presentation manager's own failure/replacement also needs reconstruction of current
knowledge; restoring an id or a pending flag does not restore an expired authority/right.

## E6 Evidence and attribution

- [Messaging reference](../../Loom/docs/reference/messaging.md), lines 83–158:
  `DispatchRefused` is an authenticated, opt-in, best-effort report about an exact pre-handler
  refusal. It is not an answer or a report of every later failure.
- The same reference, lines 370–394: host observers see delivery/refusal/lifecycle information;
  `HandlerFailed` says an entered handler did not complete, with no reason field or journal
  outcome. The bounded journal cannot distinguish an expired record from an unknown/pending
  ticket merely through `outcome`. `dispatch_parent` is not application causality. Payload
  references in observer callbacks are not durable storage.
- [Loaded failure reporting](../../Loom/src/kernel/kernel.cpp), lines 807–826:
  loaded ABI handler failure reaches the host observation path. The messaging reference's
  opening section describes native exceptions propagating after dispatch state restoration.
- [Workshop journal](../../Zengine/workshop/workshop.cpp), lines 664–696:
  selected facts can be recorded with `--log`; specific build/realization results are retained
  in full. Existing stderr survives failure of the surface itself. No universal presentation
  operation inspector or manager-facing observer projection is claimed present.

**Inference:** existing evidence can support a narrow application-owned operation view. It does
not supply a causal graph automatically or give an ordinary loaded manager host observer powers.
Runtime observations, participant reports and absent evidence should remain distinguishable.

## E7 Editor commitment and the research limit

The [commitment research](../../reportbacks/editor-commit-investigation-RB.md) and its
[design](../../reportbacks/editor-commit-investigation/DESIGN.md) demonstrate hypothetical
publication of owner-prepared roots in real loaded research participants. They explicitly
leave full Editor/Workshop integration and production SDK/root lifecycle unimplemented.

The independent [Vision review](C:/Users/Joshua/Documents/Codex/2026-09-08/https-github-com-krealsion-loom-https/work/editor-commit-review/review.md)
reran those experiments and identified a pending-paste flag outliving its local request state.
That is prior review evidence, not a new run during this draft. The fixed Editor outcome remains
in the [Goal Map](../goals/workshop.md#pane-extraction-current-status-and-next-work).

**Inference:** a presentation manager may consolidate presentation decisions, but it does not
by itself synchronize Editor-owned current source with the admitted view. The publication
candidate should be assessed against that remaining boundary, with no unspoken weakening of
the selected outcome and no universal progress guarantee.

## Review and backlog disposition

Six of six planned review areas completed: owner mapping; actual output/readiness paths;
lifecycle/authority and resource limits; failure attribution; input/Editor interaction;
reader scope and architectural fit. A bounded independent source trace supplemented this review.
No runtime test result, current remote status, final API or seamless-switch guarantee is claimed.

BL-WORK-01 applies to tracing a concrete failed/stuck intent; BL-WORK-02 favors keeping ordinary
pane authoring simple; BL-WORK-03 remains unresolved implementation/acceptance work.
BL-ADOPT-03 requires measurement when performance claims or actual bottlenecks arise; this draft
makes none. BL-ARCH-01's public include debt is not triggered by source changes, and BL-ARCH-02
supports keeping this proposal outside mandatory current law. No closed ABI item is reopened,
and no new backlog item or production phase is selected by a discussion draft.
