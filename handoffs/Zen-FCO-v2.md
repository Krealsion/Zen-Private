# Zen — First-Contact Orientation

**Role:** first read for Zen: Vision; a route, not a roadmap or execution prompt  
**Refreshed:** 2026-09-10  
**Continuity:** this path stays stable; earlier versions and their evidence remain in Git

Zen exists to help people build, learn, explore, grow, share, teach, and steward meaningful
digital work. The workshop is made from the same material it offers its makers. Read the
founder's [vision](../../zen-vision.md) for the human promise; do not reduce it to a feature list.

## 1. Start with the question you are here to answer

Read these three owners first:

1. [Vision](../../zen-vision.md): why this exists.
2. [Orientation](../../zen-orientation.md): vocabulary, ownership, evidence, and collaboration.
3. [Strategic map](../zen-strategic-map.md): selected direction and the active goal.

Then read the relevant part of the [Workshop goal map](../goals/workshop.md). Its current
capability and sequence are the place to establish what has landed and what comes next.
An old handoff's proposed next phase never overrides these owners or the founder's current word.

| When you need… | Read |
|---|---|
| repository paths, roles, branches, remotes | [Repository registry](../../REPOSITORIES.md); query Git for live state |
| observed pressure and its wake condition | [Pressure](../pressure.md) |
| work deliberately owed but deferred | [Backlog](../backlog.md) |
| the origin of a strategic decision or an unpromoted candidate | [Vision deltas](../vision-deltas.md) |
| executor workflow, verification, commits, memory | [Executor constitution](../../executor-constitution.md) |
| a fresh executor's entry route | [Executor handoff](current-executor-addendum.md) |
| machine-specific commands and limits | [Machine facts](../machine_facts.md), read only |
| persistent human/author identity design | [Identity design](../goals/identity-phase.md), not a claim of current implementation |
| live/durable forms and Flow | [Two forms](../goals/two-forms.md), a horizon, not an active phase |
| a past result or why a claim changed | the relevant reportback, dated handoff, and Git |

Read a repository's `AGENTS.md` before touching it, then follow its subject router:

- [Zengine](../../Zengine/AGENTS.md): package/Workshop behavior; [README](../../Zengine/README.md)
  inventories the packages.
- [Loom](../../Loom/AGENTS.md): substrate; [CONTEXT](../../Loom/docs/CONTEXT.md) routes exact
  reference, law, and test owners. The [mental model](../../Loom/docs/guides/mental-model.md),
  [weave authoring](../../Loom/docs/guides/writing-a-weave.md), and
  [replacement guide](../../Loom/docs/guides/replacing-a-service.md) introduce the model.

Do not make every historical handoff or every pressure entry mandatory reading. Open the source
that answers the current question. The raw vision capture is an inbox, not default orientation.

## 2. Distinctions to establish before planning

- **Loom is the substrate; Zengine is an optional default set.** Workshop is the maker's IDE,
  not a required route through which every Loom application must pass.
- **The running weave is the live subject.** Same-shape reload and authored changed-shape
  handoff are different operations; a saved state file is not a replacement for the latter.
- **The Builder already runs a compiler.** Generated C++ carries ceremony; authored C++ carries
  meaning. `maker/` exists for interpreted execution and remains paused pending that consumer.
- **Pane ownership is a migration in progress.** A pane's identity and the weave presenting it
  are distinct even when that presentation is a participating weave. Read the goal map for the
  remaining host-owned surfaces instead of treating the destination as today's implementation.
- **The human and `loom::Weaver` are different.** The existing Weaver is a bounded policy
  delegate; it is not persistent human identity. Read the
  [Weaver reference](../../Loom/docs/reference/weaver.md) before designing its Workshop seat.
- **Tracking an ask is not learning its send's fate.** `AskBook` records pending conversations;
  it does not report dispatch refusal, promise an answer, or supply progress. The current order
  and this distinction are recorded at [P-LOOM-02](../pressure.md#p-loom-02--sender-visible-fate-and-unresolved-obligations-are-still-separate-questions).
- **Limits are part of the claim.** In-process grants bound speech, not native memory access;
  bridge reachability does not authenticate a person; abuse containment is not escape resistance.

## 3. Working as Vision

The founder chooses direction and acceptance. Vision investigates, questions premises, reviews
the whole proposed result, and consolidates accepted knowledge into its proper home. Ceecee owns
implementation choices within the task's outcome and boundaries; architectural disagreements
must be surfaced rather than hidden by a prompt's instructions about how to implement them.

The durable workflow and hot/warm/cold prompt definitions live in
[Orientation §8](../../zen-orientation.md#8-working-rhythm). Invoke the executor constitution
when writing an execution prompt; do not copy its standing rules here.

When consolidating, rewrite the answer where the reader first needed it. Keep one current owner
and route other documents there. Preserve founder wording and intent; Git and reports keep the
history. A documentation task may edit the authorized documents during orientation: this router
does not add a separate approval gate to the founder's task.

## 4. Check the whole result, then its premises

Begin with the [architectural-fit review](../../zen-orientation.md#architectural-fit-comes-first):
does the complete result serve the founder's vision and preserve the path for selected next work?
Passing local tests cannot answer that by themselves. Then answer the relevant source questions
in your own words, with a named revision and precise
source/law/test anchors. Ask the founder to spot-check consequential premises; do not require a
ceremonial questionnaire for an unrelated editorial task.

1. What does each layer own, and which parts can an application omit?
2. What can a maker do today, and which exact owner refuses the proposed next step?
3. What happens to the incumbent when a proposed successor lacks an authored migration?
4. Which actor requests, decides, performs, and enforces the operation? What does its grant cover?
5. Does the evidence establish the claimed behavior, or only a narrower observation?
6. Which capability is already present, and which missing consumer behavior actually earns work?

Two recurring mistakes explain this check: earlier handoffs promoted interpreted execution into
direction without approval, and proposals assumed the Builder did not exist. Verify a premise
before researching inside it. Say “I have not read that owner” rather than claiming absence.
