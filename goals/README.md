# Goals

One file a goal: a feature on the [roadmap](../roadmap.md)'s path, sized to finish in a few
rounds. A goal file is a checklist, not a purpose: the roadmap says why and in what order; the
file says what done means and what is left. Work decided but off the path is in the
[backlog](../backlog.md); what Zen has met and not decided, in [pressure](../pressure.md).

Every goal file has the same parts:

- **Done when**: the requirements, the decided rules among them. A box is checked when `main`
  holds it, and stays checked until the goal is done.
- **Tasks**: the work that gets there, in order, each with its prompt and temperature, and what
  it holds on. A task leaves the file the day it is done; its reviewed report is its record.
- **Open**: calls not yet made, each with Vision's lean.
- **Records**: the reports and research it rests on (paths are Zen's: `reportbacks/` is
  `Zen/reportbacks/`).

A task line says its state, never its story: the story is its reviewed report, which stays in
`reportbacks/` for good. When every "Done when" box is checked, the goal gets one short entry in
`history/<year>-<month>.md` -- what was wanted, what was built and in which pull requests, what it
taught, and which reports hold the record -- and its file moves to `archive/goals/`. A paused goal
keeps its file, its open boxes in view, and the roadmap says it is paused. "Day one" marks a check
still to make; each goes when made.
