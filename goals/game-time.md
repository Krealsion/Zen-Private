# Game time and the frame clock

A goal of *drawing for real-time games* on the [roadmap](../roadmap.md); how this file works:
[README](README.md).

Done when (the game-time research's rounds, taken 2026-11-13):

- [x] the turn's time and date on every delivery (TT, Loom #32); Neovim on the wait's time (G3,
  #164)
- [ ] Zengine reads the turn's time that Loom puts on every delivery (ZTT); the Neovim bound's
  extra wake among its uses
- [ ] a world's time is a Zengine world clock serving the Timer's shapes (G1); real time stays the
  wait's, the date its second reading, and nothing schedules on a date
- [ ] the frame clock is the window's own claim, a frame's time its due time, its beat 16 ms, a
  change outside a look presented at once (G2, also V5's first stage)

Tasks:

- [ ] ZTT -- ready
- [ ] G1 -- ready
- [ ] G2's design settled with the founder
- [ ] G2

Open:

- What tells the window to present. Lean: a frame clock's beat.

Records: `reportbacks/game-time-research-RB.md`, `loom-turn-time-RB.md`.
