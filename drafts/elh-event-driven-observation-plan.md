# Event-driven ELH observation and reusable monitors

**Selected:** founder discussion, 2026-09-24.\
**Owner:** [Workshop goal map](../goals/workshop.md#near-term-order-and-purpose).\
**Order:** after the [tower-defense #60 corrections](../../prompts/zengine-tower-defense-creation-story-corrections.md)
and acceptance of that repaired baseline. This is selected direction, not an implementation packet.

## Outcome

Let an ELH subscribe to authorized application events and state, run reusable Python monitors,
and return a meaningful outcome to its supervising agent when work completes, deviates from its
expectation, or needs a decision. Ordinary progress should not need an LLM turn or repeated
screenshots. A test can inhabit an explicit play state: act, evaluate events, keep evidence,
and advance or request attention according to its own authored policy.

The first proof follows a Builder operation through build and realization. The second extends
the tower-defense story: observe an enemy crossing a chosen boundary or a count passing a
threshold, then capture/report the relevant state and causal evidence. Policies, predicates and
game knowledge live in ordinary ELH packages; the Loom host must not acquire a game-test engine.
These capabilities should also support later debugging, reusable task packages and watchers.

## What the research established

At the reviewed #60 baseline (`2656235`, Loom `0c655c0`), Builder already publishes BuildStatus
with an operation number and separate build/realization facts. The helper waits on formatted pane
rows. Screenshots mostly retain milestone evidence; image recognition is not its completion
oracle. The first consumer can therefore use existing application meaning rather than create a
second Builder state model.

Loom already has ordinary messages, latest claims through Senses, and Recorder/Logger history.
The link records incoming ordinary messages as Crossed evidence but deliberately does not pass
them off as answers to an ask. Operator bus observation is broader than an ordinary guest
subscription; Workshop guests are admitted without the whole-bus tap. Research the smallest
supported subscription path through the link and Python tool runtime, preserving these facts.
Do not infer that an existing payload arriving or being recorded already grants a useful,
scoped subscription contract. Rebaseline the source before implementation.

Source routes: Loom `docs/guides/observing.md`, `docs/reference/senses.md`, history and bridge
references, `include/zen/bridge/link.hpp`, `src/host/link.hpp`, and `python/loom_session/`;
Zengine `builder/vocabulary.hpp`, `builder/weave.hpp`, `workshop/guests.cpp`, and the maintained
`external-host/tools/workshop/` package. Resolve live repositories from the registry.

## Three different observations

| Kind | Meaning | Example and consequence |
|---|---|---|
| Latest claim/state view | What its owner most recently exposed, with provenance and freshness | Game phase, remaining lives, latest Builder status. A Sense is a latest claim, not a journal or an exact snapshot of all pending work. |
| Event | A particular occurrence attributable to its producer | Enemy crossed checkpoint; a particular build ended. Sampling only the latest state can miss an occurrence that was superseded. |
| History | Retained evidence about earlier traffic and outcomes | Explain a deviation using the existing Recorder and Logger; identify what was retained, omitted or forgotten. |

A subscription must not turn an ordinary event into an authenticated answer, an admission into
completion, or a local record of remote speech into a local witness of the far execution.
Build completion and successful realization remain separate. Silence and an exhausted wait
can leave work pending; they do not prove refusal, cancellation or failure.

## Required properties of the first useful implementation

- **Scoped authority:** request and grant observation deliberately. Knowing a shape, connecting,
  or holding input permission does not approve a bus-wide feed or command execution. The ELH
  cannot approve itself. Authorization is enforced before forwarding protected data.
- **Attributable identity:** retain the source host/session, producer identity and relevant
  operation/sequence provenance. Make replacement, reconnect and stale readings visible; do not
  join unrelated lifetimes because their numeric operation IDs match.
- **No missed-start race:** establish and acknowledge the subscription before triggering the
  action. Define how a late observer obtains a baseline and follows later events without a
  silent gap. Snapshot/stream ordering is an explicit contract, not a delay chosen by the tool.
- **Honest bounded delivery:** declare limits and ordering scope. Latest-state updates may be
  coalesced when that is their contract; occurrence-sensitive tests cannot silently lose events.
  Expose overflow, history gaps and interruptions, with a recovery or inconclusive-test route.
- **Owned lifetime:** name subscriptions and associate them with a task/session. They remain
  actionable across a client's wait timeout and end/revoke visibly. Task cancellation releases
  the appropriate subscriptions; a disconnected client does not prove remote work stopped.
- **Separate mechanism and policy:** keep generic transport, routing and evidence with Loom;
  application facts with their Zengine/game owners; predicates, expectations, state transitions,
  time limits and reporting policy with the ELH package. Arbitrary Python executes in the ELH,
  not as a new remote-host subscription language.

Research should resolve broadcast participation versus scoped observation/relay, receiver/filter
authorization, subscription ownership, and the baseline/cursor contract. Choose the least
mechanism that provides the stated guarantees. A full federation, durable process identity
redesign or arbitrary retrospective bus access is not implied.

## Delivery arc

1. **Trace and establish the mechanism with Builder.** Follow the actual existing publications,
   bridge policy and Python delivery loop. Land any necessary general Loom surface and its
   installed-consumer proof before Zengine consumes it. Subscribe, trigger a specific build,
   distinguish its terminal build and realization outcomes, and fetch diagnostics/capture only
   when the monitor's policy calls for them. Exercise refusal, late results, reconnect, gaps and
   cancellation. This is one coherent outcome, not an invitation to split every step into a PR.
2. **Consume it in the tower-defense play story.** Expose a small owner-defined gameplay surface;
   do not scrape rendered glyphs or assume arbitrary private state is observable. A reusable
   Python monitor follows prepare/build/load/play/finished-or-needs-attention states. Demonstrate
   an expected path and a deliberate deviation such as a checkpoint threshold, with attributable
   events and an evidence bundle. An automated response such as pause needs its own authority.
3. **Make it easy to reuse.** Maintain capability/help entries and a compact example at the
   generic Loom session and Zengine ELH documentation owners. Save useful configurations/setup
   material in an existing toolbox where appropriate; restoration grants no new authority and
   executes nothing. Show task reuse/cancellation without reconstructing the whole environment.

An agent-facing notification/await route is part of the consumer proof: distinguish the monitor
producing an outcome from a particular agent harness actually resuming the LLM. Do not promise
automatic wakeups that the supervising harness has not implemented or exercised.

## Captures and measurement

Use structured application observations for semantic conditions. Pane text or TUI cells are
inexpensive routine presentation evidence, including structured pane inspection while Workshop
remains graphical. Retain graphical captures at meaningful visual milestones and deviations.
TUI success cannot establish graphical geometry, pointer or drag behavior; those retain their
own witnesses. Do not remove useful visual evidence merely to lower a screenshot count.

Compare against the repaired tower-defense baseline: agent turns/calls, ELH runs/requests,
attributable host traffic, capture count/bytes, end-to-end latency, event loss/gaps and setup/reset
cost. Separate changed observation strategy from different game speed or presentation pacing.
Success is a simpler, trustworthy reusable story, not a claimed universal speedup.

## Adjacent work stays bounded

#60's unsaved-buffer, truthful completion, file selection, cancellation and shutdown repairs are
prerequisites and remain required without subscriptions. P-WORK-30's layout/selection ceremony
is related pressure, not automatic authorization to redesign the desktop in this phase.
Pane placement, broad authority UX, remote discovery, Flow UX and Editor work keep their own
owners and sequencing. Reuse Recorder/Logger; do not build a competing history subsystem.
