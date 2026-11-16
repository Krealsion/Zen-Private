# Zen roadmap

**What it is:** the plan Zen follows -- where it stands, where it goes and why, the goals being
pursued and their order. The most changed file here: it moves the same day direction moves or a
goal's task lands, and nothing is work until a goal it names says so.  
**Beside it:** [goals/](goals/), one checklist a goal: what done means and what is left, with its
drafted prompts and holds; [backlog.md](backlog.md), work decided but off this path, each item
with what brings it back;
[pressure.md](pressure.md), what Zen has met and not decided; [history/](history/), what
finished, told as short stories; [archive/2026-11-15/](archive/2026-11-15/), the old plan, whole.  
**Updated:** 2026-11-16, installed at the rebuild (drafted 2026-11-15, while the founder's
machine was down).

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
waiting for review), and a schema's id is to be checked by structure before the release. The
founder's boot drive failed on 2026-11-15; Zen's folder survived on its own drive. Its
replacement, a laptop running Ubuntu 22.04 with 15 GB and 8 threads, is up since 2026-11-16, and
nothing builds until the restore round has rebuilt the kit there.

## Where it goes, and why

The long road is the spine: a credible substrate, then a Workshop makers enjoy, then projects
anyone can build, a Zen strangers can read, hosted weaves, trust across many authors, and at its
end Zen teaching, building and stewarding beside the people in it. The north star across all of
it: playing and making become the same honest act.

The founder's direction of 2026-11-08 sets the near road: finish what is already decided,
through Workshop's move to its own repository, stopping only for detours that are plainly right,
with concerns marked for the end. Three directions joined it since: Loom's gaps closed so that
Zengine's files shrink rather than grow around them (2026-11-10); drawing that fits a real-time
frame and reads naturally to the person writing it (2026-11-14); and readability as a pillar
beside modularity, in the code and in the docs (2026-11-15). The release comes after them.

Why games: a game is the hardest everyday test of a drawing design -- many moving things, every
frame, in two media. If a tower defense is pleasant to write in Zen and fast to run, the design
holds for the panes too, and Zen's first ports, two of the founder's own games, will show where it
does not. Why readability: Zen is for people who want to build without a private course first.
Code that reads plainly keeps the substrate honest with them, and with the agents beside them.

The long goals, as the strategic map registered them: Workshop is the current one; a Zen
strangers can read is underway through two standing tasks; hosted weaves are not selected (they
get a goal map of their own before any hosting work); trust across many authors is a required
long path, unbuilt; Tutor, Builder and Steward are a horizon, three roles kept distinct.

## The goals

Each direction below, with why it matters, and its goals in order; each goal is a checklist in
[goals/](goals/).

Now:

1. **The machine.** Every lane waits on it.
   [machine-restore](goals/machine-restore.md).
2. **Drawing for real-time games.** A game is the hardest everyday test of a drawing design; the
   founder wants drawing that fits a 16 ms frame and reads naturally to the person writing it.
   [tile-defense](goals/tile-defense.md), [drawing-order-names](goals/drawing-order-names.md),
   [drawing-speed](goals/drawing-speed.md), [game-time](goals/game-time.md),
   [ports](goals/ports.md).
3. **Security** (private). A defect outranks features. [queue-budget](goals/queue-budget.md),
   [security-pair](goals/security-pair.md).
4. **Loom's foundation.** Close the gaps Zengine builds around, so its files shrink and no
   god-file grows back. [data-plane](goals/data-plane.md), [takeover](goals/takeover.md),
   [one-host](goals/one-host.md), [schema-evolution](goals/schema-evolution.md),
   [unions-rest](goals/unions-rest.md), [calls-in-zengine](goals/calls-in-zengine.md).

Next:

5. **Untrusted code.** One home for it that holds on every platform; recovered 2026-11-15, after
   it fell off the plan. [wasm-box](goals/wasm-box.md),
   [sandbox-retired](goals/sandbox-retired.md).
6. **The Workshop split.** The founder's baseline runs through it.
   [pane-contract](goals/pane-contract.md), [owned-names](goals/owned-names.md) (decided
   2026-11-09, never built), [workshop-move](goals/workshop-move.md).
7. **The visual foundation.** "High quality components means higher quality composites" (the
   founder, 2026-10-29). [looks-in-time](goals/looks-in-time.md),
   [keys-and-presses](goals/keys-and-presses.md), [element-set](goals/element-set.md),
   [view-cost](goals/view-cost.md).
8. **The makeovers.** The panes rebuilt on the new pieces, Flow's way: the design taken whole.
   [flow-next](goals/flow-next.md), [view-builder-makeover](goals/view-builder-makeover.md),
   [operator-suite](goals/operator-suite.md).
9. **Readability.** Code pleasant to write, docs plain first.
   [language-pass](goals/language-pass.md), [front-doors](goals/front-doors.md).
10. **The release.** Zen in people's hands, after Workshop's move. [release](goals/release.md).

## Standing lanes and duties

- **The issue lane**: Raid, at its weekly cap until about 2026-11-19; the founder weighs moving
  its job to Ponder. Open for review: Zengine #170 (`PlanWhere` named `PlanStatus`), Loom #34 and
  #37. Filed, no pull request yet: Zengine #173 to #176 (#175 answered: the stand-in host
  withdraws as an ask). A fix pushed by `cursor[bot]` may still wait for a run's approval.
- **Reviews and filing** (Vision): every report in `unreviewed/` reviewed and filed, and this file
  and the goal's file changed the same day.
- **A Zen strangers can read** (the founder, 2026-09-25): a plain first-read path; no private
  information in documents or comments.
- **The drawing door's full set** (BL-WORK-37): ovals, polygons, images, shaders and whole
  widgets, built for the design rather than as consumers ask.
- **Grow with use**: Workshop and onboarding together (BL-WORK-01); a front door for contributors
  before asking for any (BL-ADOPT-01); current law cheap to carry (BL-ARCH-02).

## Now

- Nothing builds until the restore round, `prompts/unrun/machine-restore.md` (cold), written
  2026-11-16.
- Waiting on the founder: the restore round started; the security fix's calls
  ([queue-budget](goals/queue-budget.md), reviewed 2026-11-16); #177's merge; the calls below.
- Waiting on Vision: Raid's three pull requests.

## Next, in order

Up to three Ceecee lanes, the issue lane beside them in the cloud; the laptop's 15 GB may hold
one building lane at a time, and the restore round measures how many. Each step holds until the
one it names has merged. Vision's proposal, for the founder to set:

- **Lane 0, the machine**: machine-restore. All lanes wait on it.
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
- **Vision, beside the lanes**: wasm-box's S4b found and reviewed; security-pair's day-one check;
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

A goal's own calls are in its file's "Open". The near ones: #177's merge and its follow-ups
(tile-defense); cold readers, an exception to Ceecee's rule 11 (language-pass); what tells the
window to present (game-time); the sandbox's retirement and its scope (sandbox-retired).

## Marked for the end

The concerns the baseline set aside, readdressed when the Workshop split is done:

- `PaneRefusalRequested` (#126) lets any seated pane have Workshop say a sentence as its own
  refusal notice; the notice should say whose refusal it is.
- The issue lane posts none of the comments `taking-an-issue.md` asks for.
- The security pair's one-way doors and its structure.
- #18's quoted red cannot come from its final case; #136's catalog counts four text documents
  where there are five.
- Office to role's leftovers: the code's multi-word names (a census of identifiers first) and the
  13 console pictures; once both are in, the kit's version-1 grants of `Run` and `RunList` go.

## Horizons, and what stays out

A horizon defines a completeness test; it never authorizes a demo-driven build.

- **Horizons**: live debugging; a scalable kernel; replaceable weaves; modders are players; a
  semantic computing environment where declaration, presentation, runtime, source and failure
  are navigable views of meaningful things; one-shot authority, which Loom has not earned;
  Zenscript's return; scouting threads that prepare answers for the main thread to check and
  apply; a compile-down to a standalone app with no Loom in it; a small 3D third-person action
  game with procedural animation as Workshop's final test.
- **Stays out** (not owed work): tabs, Vim emulation, syntax highlighting, a VFS, a file watcher
  or a Flow editor inside the built-in Editor (a differently shaped editor arrives as a pane
  weave); one pane shown several times, and plugin discovery; live artifact replacement before a
  concrete owner and continuity case; general obligation, consensus, metadata or persistence
  frameworks; multithreaded dispatch (not built, and nothing may assume it never will); Windows
  native containment (the box runs everywhere instead); production hardening of the bridge
  before hosted or remote use; a replacement SDL executor for Loom's portable pixel layout.
