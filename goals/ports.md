# The first ports

A goal of *drawing for real-time games* on the [roadmap](../roadmap.md); how this file works:
[README](README.md).

Done when:

- [ ] TheyCameInWaves runs in Zen, in the GUI and the terminal
- [ ] RunCantHide the same
- [ ] each port has a side-by-side: what Zen made easier, what it made harder, and the helper or
  design change each gap wants
- [ ] the helpers they asked for exist: a box around a centre, words centred in a box, a line
  width (`LineArgs` has none)

Tasks:

- [ ] TheyCameInWaves (Java2D, 29 files; `Draw(Graphics g)` each frame, a camera offset subtracted
  by hand 90 times, `Size / 2` 32 times). Holds on the language pass's first slice.
- [ ] RunCantHide (`github.com/Krealsion/RunCantHide`, Java, 2017, the same skeleton). Holds on
  TheyCameInWaves.

Open:

- Where a port lives: an example in Zengine, or a repository of its own. No lean yet; asked
  before the prompt.
