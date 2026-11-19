# Zen's private plan

**What it is:** the founder's own plan for Zen, and this page its way in: what each file here
holds, the order to read them, and what to change after a phase or a review. A git repository of
its own, its remote the private `Krealsion/Zen-Private`, committed as the founder with a
pathspec. This page changes only when a file's job changes.

## Read first

1. [current_state.md](current_state.md): where Zen is now, what runs and what waits, on whom.
2. [roadmap.md](roadmap.md): the order, the directions and each one's goals.
3. In [goals/](goals/), the file of each goal in hand.

Then, as a question needs them: [backlog.md](backlog.md), [pressure.md](pressure.md),
[history/](history/). How to reason about Zen is outside this folder: `Zen/zen-orientation.md`,
shared by Vision and the executor; how each of them works is `Zen/vision-constitution.md` and
`Zen/executor-constitution.md`.

## The document map

| File | Holds | Changes when | Edited by |
|---|---|---|---|
| `README.md` | this map, the read order, what to change after a phase | a file's job changes | Vision, on the founder's word |
| `current_state.md` | where Zen stands; what runs, what waits and on whom; each lane's next step; the calls waiting on the founder | every phase, review or call | Vision |
| `roadmap.md` | the long road; the directions in order, each with why and its goals; standing duties; what is marked for the end; the horizons and what stays out | the direction or the order changes | Vision, on the founder's word |
| `goals/<goal>.md` | one goal's checklist: done when, tasks, open calls, records ([how](goals/README.md)) | a task lands or a call is made | Vision |
| `backlog.md` | work decided and not pursued, each with what brings it back | an item is decided or comes back | Vision |
| `pressure.md` | what Zen has met and not decided | a seam is met, or a goal or the backlog takes one | Vision |
| `history/<year>-<month>.md` | one short entry a finished goal, pointing at its pull requests and reports | a goal finishes | Vision |
| `archive/` | the old files, kept whole ([what](archive/README.md)) | a goal finishes | Vision |
| `machine_facts.md` | the founder's machine | the machine changes | the executor, when a prompt hands it over |
| `relicense/` | the maps of the MPL-era rewrite and of this repository's own; the bundles themselves on this drive, outside Git | never | nobody |

The executor reads here and edits only a file its prompt hands over (its constitution, section a).

## After a phase or a review

The same day, in this order:

1. The report moves from `Zen/unreviewed/` to `Zen/reportbacks/` with its evidence, committed in
   Zen and pushed to its private remote, `Krealsion/Zen-Core`. The reviewed report is the
   record, for good.
2. The goal's file: a box is checked when `main` holds it; a done task leaves; new tasks and calls
   are added, each call with its lean.
3. `current_state.md`: what runs, what waits, each lane's next step, the calls.
4. `roadmap.md`, only if the direction or the order changed.
5. `pressure.md` and `backlog.md`, as items arrive or move.
6. A goal whose every box is checked: one entry in `history/<year>-<month>.md`, and its file moved
   to `archive/goals/` with `git mv`, its links mended (`Zen/pass-tools/private-archive/`).
7. Commit here with a pathspec, as `Krealsion <krealsion@gmail.com>`, and push.

## Rules that hold

- A goal leaves the roadmap only finished (to history), paused (its file kept, the roadmap saying
  so), parked (to the backlog), or dropped on the founder's word: never by silence.
- One fact, one file: `current_state.md` names a goal and links its file; it never repeats the
  goal's tasks.
- Nothing is work until a goal names it, and nothing in pressure is owed.
