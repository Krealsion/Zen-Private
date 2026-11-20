# Zen's current state

**What it is:** where Zen is now: what runs, what waits and on whom, each lane's next step, and the
calls waiting on the founder. The file changed most, at every phase, review or call. It names a
goal and links its file; what the goal still needs is in that file.  
**Beside it:** [README.md](README.md), the map and the rules; [roadmap.md](roadmap.md), the order;
[goals/](goals/), a checklist a goal.  
**Updated:** 2026-11-19, the documentation's trial reviewed and filed; the law cut's lane fix running.

## Where Zen stands

Zen is two libraries and an application. Loom is the substrate: pieces of code called weaves,
each holding only the authority it was granted, talking only through messages that one gate
checks. Zengine builds on Loom -- windows for a GUI and a terminal, input, a timer, operators --
and holds Workshop, the desk where a maker builds, runs, inspects and changes things while they
run. Both have been public under the AGPL since 2026-11-01, and Zengine publishes a nightly
package.

The two weeks before the rebuild went to Loom's foundation, after a cold audit found Zengine
building around gaps only Loom could close. Loom gained the union (one value of any registered
shape), a weave made with one checked value, a floor under every ask (each followed to its answer
or told how it ended), deadlines in its wait, the turn's time on every delivery, and calls (a
function of its argument alone, answered by a role's holder): ABI 17 at `9f3db68`. Zengine spent
each one: its Timer runs on a deadline, a drawing's operands are one union with their looks said
once, the build runner owes its answer, and the realization owner is a participant of its own
(`main` at `7dfd8690`).

Then drawing for games. Real-time drawing was measured -- in Release a whole area at the bound
takes 26 to 30 ms against a 16 ms frame -- and its causes found, and how people really draw was
audited against what Zen offers. A tile defense built on what that taught (sprites from a sheet
the game draws in code, tiles, particles, in the GUI and the terminal alike) waits as Zengine
#177, green and reviewed.

Workshop still lives inside Zengine; its move to a repository of its own is decided and measured,
and the line between them falls round by round. Security work is open, privately: a contained
weave can hold gigabytes of the host's memory through its waiting messages (its fix reported,
waiting for review); a schema's agreement by structure and the session key's owner-only file
are on `main` since 2026-11-10, both advisories published. The founder's boot drive failed on
2026-11-15; Zen's folder survived on its own drive. A laptop reads and writes Zen since
2026-11-16 and builds nothing; the PC comes back with a new system drive in a couple of days
(2026-11-18), and nothing builds until the restore round has rebuilt the kit there.

## Now

- The instruction audit ran and is reviewed (2026-11-18): its ten calls and 20 diffs wait on
  the founder ([instruction-audit](goals/instruction-audit.md)); the restore round after them.
- The outside audit of 2026-11-09, checked at today's `main`, is reviewed (2026-11-19): eight
  calls wait on the founder ([audit-recheck](goals/audit-recheck.md)). It found the security
  pair finished on 2026-11-10, now in history.
- The law cut and its continuation are reviewed (2026-11-19): Loom #38 waits on the founder's
  merge; Zengine #178, with 64 laws back, merges after #177 and #170, rebased onto both
  ([law-cut](goals/law-cut.md)).
- The documentation's design is tried, reviewed and in its fourth pass (2026-11-19): smaller
  encouraged and never forced, the size caps paused for the rewrite, three passes. Stage 4's
  prompt is next, publishing it ([doc-design](goals/doc-design.md)).
- Nothing builds until the PC is back (a couple of days, 2026-11-18) and the restore round has
  run there; its prompt, written for the laptop, is rewritten for the PC first.
- The founder's Workshop notes of 2026-11-18 (`founder-notes.txt`, here) wait to be filed once
  he approves the plan's layout.
- Waiting on the founder: the PC; the security fix's calls
  ([queue-budget](goals/queue-budget.md), reviewed 2026-11-16); Loom #38's and Zengine #178's
  merges, after their rebase; the calls below.
- Merged 2026-11-19: Loom #34 and #37, Zengine #170, #177 and #179. Zengine's `main` went red at
  `94f0492` on a race in a builder case, proven (its first look can take the line its check
  reads); #179 fixed it (`55d533a`). The law cut's rebase ran: Loom #38 is green; Zengine #178's
  MinGW job met its 60-minute limit on a cold build. Its continuation,
  `prompts/unrun/law-cut-lane-limit.md` (hot), fits the lane's limit first, in a pull request of
  its own, then moves #178 onto it ([law-cut](goals/law-cut.md)).

## The issue lane

- **The issue lane**: Raid, at its weekly cap until about 2026-11-19; the founder weighs moving
  its job to Ponder. Reviewed 2026-11-19, each to merge: Zengine #170 (`PlanWhere` named
  `PlanStatus`), Loom #34 (the text checks named from one list) and #37 (the guide shows a call).
  Filed, no pull request yet: Zengine #173 to #176 (#175 answered: the stand-in host
  withdraws as an ask). A fix pushed by `cursor[bot]` may still wait for a run's approval.

## Each lane's next step

Up to three Ceecee lanes, the issue lane beside them in the cloud, as many as the restored PC
holds. Each step holds until the
one it names has merged. Vision's proposal, for the founder to set:

- **Lane 0, the ways of working and the machine**: #178's last rebase, once #177 and #170 merge;
  doc-design's research, once the founder has marked up the design; instruction-audit's diffs;
  machine-restore once the PC is back. All lanes wait on it.
- **Lane 1, Zengine, the drawing**: tile-defense (#177's merge); drawing-order-names;
  drawing-speed's W1; language-pass's first slice (`graphics/` and the tile defense); ports,
  TheyCameInWaves first. Why: each step works in the files the last one changed, and the ports
  want readable helpers to prove.
- **Lane 2, Loom**: queue-budget's fix; drawing-speed's L1; data-plane and drawing-speed's L2, in
  the order their two reports give (read on day one); then the foundation's goals in the order
  above, with wasm-box's S5 and owned-names' Loom round among them. Why: a defect outranks
  features, and L1 checks messages in the same code the fix changes.
- **Lane 3, Zengine, the second**: pane-contract's round 4; workshop-move's line round 2;
  owned-names' Zengine round; game-time's ZTT and G1, and one-host's ZH1 once its Loom round
  merges; unions-rest's Zengine items, which touch `graphics/implied.hpp`, in a gap between lane
  1's rounds. Why: the split is the founder's baseline, and its files are Workshop's, apart from
  lane 1's.
- **Vision, beside the lanes**: wasm-box's S4b found and reviewed;
  game-time's G2 designed with the founder before lane 1 needs it, since V5 builds on it.

## Calls waiting on the founder

The calls no goal owns, each with Vision's lean:

1. The lanes' order above.
2. Raid's job to Ponder (Agent Two): the founder's own weighing.
3. The three questions of 2026-11-13, night: Loom's run record on Windows (the manager retrying a
   stale record on its own, option a, in a Loom round with the run manager's stamps split); a
   night publishing an older commit after a workflow change (wait, as #166 does); the host's own
   wait set all or nothing (several own sets, each held or refused alone).
4. The older calls, each checked on day one against the two clarify files and the decision-wave
   sheet -- those still open come here or go to their goal, the rest go: the archived backlog's
   section 5, and the drawing operators' word (2026-11-08).

A goal's own calls are in its file's "Open". The near ones: #177's follow-ups (tile-defense); cold
readers in the language pass, once the documentation's trial has tested one (language-pass); what
tells the window to present (game-time); the sandbox's retirement and its scope (sandbox-retired).
