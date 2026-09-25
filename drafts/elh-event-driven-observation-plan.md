# Event-driven ELH observation and reusable monitors

**Selected:** founder discussion, 2026-09-24; rebaselined 2026-09-25.\
**Owner:** [Workshop goal map](../goals/workshop.md#near-term-order-and-purpose).\
**Baseline:** Zengine #60 accepted and merged as `c02b88a463e6c937e0a1416a989149742aeaedf1`;
its tree matches reviewed `bcf85b2`. Loom main is `0c655c06d5585d984a16d681993d1179d3dabdeb`.
Recheck live main before implementation. This is the next phase's draft, not an executor prompt
or authorization to implement it during planning.

## Outcome

An agent starts a reusable ELH monitor that subscribes with explicit authority, performs an
authorized action, follows attributable application outcomes and returns useful evidence when
the task finishes, deviates or needs a decision. Routine progress does not need an LLM turn.
The session and unresolved run remain available when its supervising client stops waiting.

The first consumer follows one Builder operation through build and realization. The second uses
the same mechanism to monitor tower defense: observe enemies crossing a chosen checkpoint,
count a threshold, and report a completed playthrough or a deliberate deviation. Python packages
own those policies. Loom supplies reusable mechanisms, not a game-test engine.

## Why this comes next

#60 established the complete creation loop: editor authoring, build, live reload, play, saved
workspace/toolbox, promotion and repeatable replay. Its corrections exposed the next structural
cost: ELH tools infer application outcomes from a sequence of painted rows. That couples a tool
to wording, clipping and pane visibility, and can miss transitions between observations. Retaining
operation identity repaired a concrete bug; receiving typed owner observations is the next step.

This is primarily about trustworthy observation, not replacing image recognition: the accepted
replay already uses pane text for most semantic checks. Captures remain valuable visual evidence.
The aim is to let an agent delegate a whole interval of work to a reusable program and return to
an attributable result, with enough evidence to investigate an exception.

Builder earns the mechanism against an existing owner with separate build and realization
outcomes. Gameplay then proves that the result generalizes beyond build tooling. A programmable
threshold or expectation belongs in an ordinary editable package, rather than a new host feature
for each test. This supports later story testing, debugging and reusable automation while keeping
ordinary coding and UI interaction first-class. Flow can consume the same observations later.

## What is already present, and what is missing

Source-traced against the baseline above:

- Builder publishes `BuildStatus` v4 with its request counter, operation, build outcome and
  realization outcome. The repaired `workshop/builder` keeps that identity through its wait,
  but obtains facts by parsing pane rows.
- Loom distinguishes messages for occurrences, Senses for latest claims, and Recorder/Logger
  for retained evidence. A Sense is not an event journal or an exact snapshot of pending work.
- The host link records ordinary incoming speech as `Crossed` evidence; it deliberately does
  not satisfy an ask with that speech. Python's direct connection also keeps unsolicited
  messages in a bounded 64-entry deque. Neither is a complete scoped subscription contract.
- Workshop grants named guest capabilities. Input, capture, inspection or knowledge of a schema
  must not silently become permission to observe all participants or execute their commands.

Source routes: Loom `docs/guides/observing.md`, `docs/reference/senses.md`, bridge/history
references, `include/zen/bridge/link.hpp`, `src/host/link.hpp`, and `python/loom_session/`;
Zengine `builder/vocabulary.hpp`, `builder/weave.hpp`, `workshop/guests.cpp` and
`external-host/tools/workshop/builder.py`. These are investigation entry points; current public
contracts stay at their repository owners.

## Delivery arc

One goal-oriented assignment may carry the following checkpoints through research, implementation
and proof. They are useful acceptance boundaries, not mandatory session breaks or arbitrary PR
counts. Separate worktrees start from current main and preserve parallel comment, Flow and UX
work. If Loom changes are needed, prove Zengine against an installed candidate package and make
the dependency explicit. The founder merges; final integration must use an accepted dependency.

### 1. Establish an authorized observation path with Builder

Trace ordinary publication, scoped observation/relay, the link and the Python worker. Choose the
least mechanism that lets an admitted consumer subscribe, establish readiness, receive typed
observations, wait and release its subscription. Do not begin by adding a blanket bus tap.

Subscribe before triggering a build through an already authorized action path. Associate the
initiating intent with the accepted request and eventual operation, including the interval before
an operation number exists. A convenient next event is not proof that it belongs to this action.
Keep build completion and realization completion separate. A successful build with pending or
refused realization must remain distinguishable.

Have the existing Builder helper consume this route. A pane may be covered, closed or resized
without breaking its outcome observation. UI interaction can still require a visible control;
the delivery must distinguish that action requirement from an observation requirement. Reading
events grants no new action permission. Existing pane text remains useful presentation evidence.

### 2. Reuse it for a programmable play monitor

Expose a small owner-defined game state/event surface, with game/run identity and enough
meaning to express a checkpoint count and play outcome. Use occurrences when every crossing
matters; do not infer them from whichever enemy positions survived the last snapshot.

A reusable Python package runs through prepare, build/load, play and finished/needs-attention
states. Demonstrate both a normal completion and a deliberate deviation. At the deviation, keep
the relevant typed observations, state, causal history references and a screenshot or pane view.
If policy also pauses the game, that is a separately authorized command whose outcome is tracked.
Observation alone does not authorize intervention.

Use the existing game, workspace, toolbox and reset path. Preserve the complete creation replay;
add the monitoring route without replacing its authoring or UI proof with pre-seeded game files.
Thresholds and expectations should be editable without recompiling Loom or Workshop.

### 3. Leave an agent-usable, repeatable tool

Make the capabilities discoverable through the existing manifest/help and compact ELH guides.
An agent can start a monitor, obtain a run handle, await or reattach, inspect evidence and cancel
without rebuilding the environment. A second run in the same session does not inherit the first
run's events, counters or leaked subscription. Reuse and improve the maintained demo/toolbox
where it helps; restoration executes nothing and grants no authority.

The tool returning an outcome and a supervising harness waking an LLM are different capabilities.
Prove the available await/resume handoff. Claim automatic LLM wakeup only if a concrete harness
integration is implemented and exercised; do not make a new agent scheduler a prerequisite.

## Contracts the implementation must settle

| Boundary | Required result |
|---|---|
| Authority | Observation is explicitly scoped and checked before protected data crosses the boundary. Denial and revocation are visible. The ELH cannot approve itself; existing development exceptions remain explicit and off by default. |
| Identity | Preserve host/session lifetime, producer and operation provenance. Distinguish a role's current holder from an earlier incarnation; reconnect must not make a reused numeric ID look continuous. |
| Start and late attachment | Define when a subscription is active and how an initial baseline joins later events. An event immediately after readiness must be observable. A late observer gets retained evidence or an explicit gap, not an invented uninterrupted past. |
| Delivery bounds | Declare ordering scope and bounded storage. Coalescing is allowed for latest-state contracts, not silent loss of occurrences. Overflow, disconnect or history eviction is visible and leads to explicit recovery or an inconclusive result. An observer must not indefinitely stall the producer. |
| Lifetime and cancellation | A client wait timeout does not erase a running monitor. Release/cancel/revoke ends observation visibly; it does not imply that an independently running build stopped. Define reattachment and host-loss behavior without promising process migration. |
| Meaning | An event is not an authenticated answer; admission is not completion. Silence may be valid pending behavior. Domain policy decides what a deadline means and reports what it actually knows. |
| Evidence | Reuse Recorder/Logger, with deliberate retention for relevant payloads and gaps named. An ELH record of remote speech is not a local witness of every far-side effect. |

Resolve the transport/relay placement, authority granularity, baseline/cursor ordering and
subscription custody during preflight, with small executable probes. These implementation
choices remain open; the desired behavior is settled. Bring a consequential authority or
application-contract tradeoff back to the founder rather than weakening it to obtain a green.

## Acceptance and measurement

The phase is ready when both consumers work through the same maintained observation mechanism:

- Builder follows its own request and operation to the correct build/realization outcomes with
  no recurring pane capture needed to learn completion. Exercise immediate completion, failure,
  pending realization and a competing build; another operation never becomes this one's result.
- Gameplay reports the configured crossing threshold and normal finish from typed observations.
  Deliberate deviation produces an attributable, traversable evidence bundle.
- Two real hosts and the installed-package boundary prove authority refusal/revocation,
  subscribe-before-act, late attachment, bounded overflow/gaps, disconnect/reconnect and cleanup.
  Test forged/wrong-source observations and preserve the answer-authentication boundary.
- A client wait expires while the monitor remains reachable; a later client inspects or cancels
  it. Repeat a task in the existing session and prove prior subscription/state isolation.
- The normal creation replay, relevant UI witnesses and repository verification still pass.
  Event observation must not hide a broken visible interaction.

Compare the same work and pacing against merged #60. Its accepted correction report records a
long-root replay at 18/18, 58 ELH runs, 3,428 asks and 379.8 seconds; these describe that run,
not a performance target. Measure agent-facing calls/turns, ELH runs and requests, attributable
host traffic, capture count/bytes, completion-detection latency, gaps and setup/reset cost.
Separate fewer observations from faster simulation or omitted creation steps.

Prefer one useful monitor invocation over making the agent orchestrate every event. Do not
promise that subscriptions remove desk arrangement or text-editing cost: P-WORK-30 records
separate input ceremony. Retain selective graphical captures for visible outcomes; TUI/state
checks cannot establish pointer geometry or graphical rendering.

## Adjacent work stays bounded

Inventory currently loses the game's `zen.Result` reply after delivering a stored command
([P-WORK-33](../pressure.md#p-work-33--stored-commands-can-lose-their-domain-reply)). Preserve
this as a following consumer of truthful command outcomes. It is not a reason to make every
answer a subscription event or build a universal command manager inside this phase.

P-WORK-29's toolchain authoring, P-WORK-30's arrangement cost, P-WORK-31's presentation choice
and P-WORK-32's command discovery remain separate. Full federation/discovery, host migration,
arbitrary retrospective bus access, a new scheduler, game polish and Flow UX are not prerequisites.
Use the existing Recorder/Logger rather than creating a competing history subsystem.

Acceptance evidence for the prerequisite: [second correction report](../../reportbacks/zengine-tower-defense-creation-story-corrections-2-RB.md)
and [its evidence](../../reportbacks/zengine-tower-defense-creation-story-corrections-2-evidence.md).
The original experiment's recorded boundary deviations remain history; acceptance does not
recast them as an uninterrupted ELH-only authoring run.
