# To the Night Lab Orchestrator: today's baseline, and the triggers

From Vision, the Zen thread, 2026-10-09, after `night-lab-handoff.md`. Read that first.

## Where Zen stands (2026-10-09, evening)

- Zengine `main` at `ffde139`: the agent's desk stage 0 (#150) and stage 1 (#151) merged, with two
  of #151's three review fixes (#155, #157). The third, #156, is being rebased.
- Stage 2 is in build: notices (`DeskStamps`, `desk/watch`), and a pane's stamp naming its picture
  by a fingerprint of what the pane sent.
- The founder's order: the desk's stages 1 to 3b ahead of BL-WORK-09, the desk's later stages,
  then the documentation rewrite (not yet planned), then the lab. Loom `main` is at `b664311`.
- In the plans (`Zen/private/backlog.md`): BL-LAB-01 (era 2, with today's seeds), BL-WORK-38 (the
  desk), BL-WORK-41 and BL-WORK-42 (the Data Conversion Mapper, the Black Box Reader).

## 1. The go: when runs may start

- Only the founder's word starts era 2's runs. Watch for readiness and report it; never start a run
  on readiness alone.
- Readiness, and where to read it:
  - the desk: BL-WORK-38's State line, and Zengine `main`'s merges (read them in a clone of your
    own, outside the Zen folder, or on the pull request pages). The question needs at least stage
    3b; the founder's order is the whole desk, then the docs;
  - the documentation rewrite: it enters the plans (Goal 2) when it is planned;
  - the wall: verified by you with the founder, by the handoff's checks.
- GitHub: the API refused this thread's sessions (403). Use git and the public pages.

## 2. A run: how it starts and ends

- The executor runs inside the wall, and Cowork cannot reach in: a Cowork scheduled task runs in
  Cowork's own VM or in the cloud, never in a WSL distribution. A nightly run starts from a Windows
  scheduled task the founder makes, one line that starts the executor in the distribution with the
  standing prompt, or from the founder's own hand.
- Unattended means no one answers the executor's permission prompts. How it runs unattended inside
  the wall is the founder's decision; the wall, and a token that reaches one repository, are what
  make it safe.
- A run ends by pushing to `github.com/Krealsion/zen-night-lab`. You hear it there: fetch the
  repository, or keep a morning check-in of your own (a Cowork scheduled task can do that part).
- One full build at a time on the machine: a run goes when Ceecee's lanes are idle, until the
  desk's stage 7d gives a build slot.

## 3. Inside an experiment: listening, not polling

The founder's design: an application runs and is acted on by messages, with no agent in the loop,
and an unexpected occurrence calls the agent in to review. The parts exist:

- **Loom's observation relay** (`Loom/docs/reference/observation.md`). A subscriber asks the relay's
  office (`loom.observe`) for one producer's publications of named shapes, and is told each one in
  order, numbered. A `Gap` is a loss the relay counted. Nothing from before the subscription is
  replayed. Observing is its own authority and grants nothing: a guests file row names what it may
  observe (`observe`), apart from its powers.
- **Workshop's monitor** (`external-host/tools/workshop/monitor.py`, with the `observe` tool beside
  it). A policy names the producer and its shapes, plays the application through the run's own
  input, sees every observation, and ends FINISHED, NEEDS ATTENTION or INCONCLUSIVE, its evidence
  in `monitor.json` (with `attention.png` on attention). Running out of time is INCONCLUSIVE, never
  proof that the owner failed.
- **The example**: `examples/tower-defense/monitor/td_policy.py` plays the game from the game's own
  typed events, counts the enemies crossing a checkpoint, and pauses the game on attention.
- **The desk's notices** (stage 2, landing now): `DeskStamps` says when the desk changes, and
  `desk/watch` writes what moved. They follow what a pane shows, not an application's meaning.
- NEEDS ATTENTION is the trigger for an agent's review, and its evidence is the review's input.
  Polling is a named mistake.
- Read in Zengine: `docs/workshop/external-host.md` ("Following what an owner says, instead of
  reading its pane"; "The desk written as text for an agent") and `agents/workshop/desk-read.md`;
  in Zen: `reportbacks/elh-event-driven-observation-RB.md`.

## Seeds for era 2

From the "Perspectives" proposals (the founder, 2026-10-09): setups as perspectives on one truth.

- **A Codex**: a pane that reads what a weave accepts (`zen.DescribeAccepted`, live), each pane's
  declared words and the refusals (`Refused`). Never prose in `zen.SchemaDesc`: that is a named
  mistake (the desk research's decision 12).
- **A Data Conversion Mapper**: a Flow view that authors a migration operator, two versions side by
  side (`zengine.migrate.<family>.v<from>-to-v<to>`, Zengine's `operator/migration.hpp`).
- **The Proving Grounds**, after the desk's stage 7: a weave run out of process against a scripted
  sequence of messages, graded by a monitor. A crash is caught only out of process.
- **The Autopsy Table and the Conductor**: lab ideas only.
- **Not the Cartographer**: Loom enumerates no participants, and `zen.QueryRole` cannot tell an
  unheld role from one held where the kernel cannot see, so a map of the bus would invent facts.

The Codex and the Mapper are on Zen's roadmap too (stage 4b's form, BL-WORK-41). A lab prototype
informs them and never replaces them; what it finds reaches Zen through the founder.

## What you carry into the wall

The executor inside cannot read `Zen/`. Whatever it needs goes into the lab repository: the house
rules and the question in its README, the observation and monitor contracts above, its short
constitution, the report's form, and the standing prompt.
