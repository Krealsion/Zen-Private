# The tile defense

A goal of *drawing for real-time games* on the [roadmap](../roadmap.md); how this file works:
[README](README.md).

Done when:

- [ ] Zengine #177 merged: the tile defense in `examples/tile-defense/`, drawn in the GUI and the
  terminal; `sheet`, `tiles`, `sprites` and `points` (`Operands` v2); the helpers `Box`,
  `Group`, `Sheet`, `TileGrid`, `SpriteBatch` and `PointBatch`
- [ ] the painters' handlers named for what they do, one scheme in both: `sprites_to_blits` in
  the GUI's, `sprites_to_cells` in the terminal's, `frame_in` to `blit_frame`, `frame_cells` to
  `frame_to_cells`; each comment the rule in plain words
- [ ] `stage`, the arranger's name, renamed: the workspace and `zengine_stage_sdl` already use it
- [ ] a kept texture no longer copies the pixels it compared
- [ ] the terminal's tile settled: today one cell a tile, square where the GUI is two to one
- [ ] a drawer hears of a left-out node by default, not only when it declares `DrawnRefused`
  (P-WORK-100)
- [ ] a game can start with no host of its own (P-WORK-102)
- [ ] the drawing traps the usability runs found, checked on `main` and sent to the issue lane:
  `Image::set_tint` doing nothing for a pool colour; a `WindowShaped` before its arranger is
  known dropped (`window.hpp` 458); an owner's group at a presented element's path refused at a
  reload; a field added to a drawer's state refused at a reload in place; the two traps the
  drawing guide does not say

Tasks:

- [ ] the founder merges #177 (green on ten of ten and Package at `a3f5153d`, clean beside #170)
- [ ] the names and the arranger's rename go with the language pass's first slice; the rest with
  the next drawing round
- [ ] the traps checked on `main` once #177 is in, then filed for the issue lane

Open:

- #177 merged as is, its follow-ups placed as the tasks say. Lean: yes; the founder's call.
- From the usability run's six (2026-11-14), unless #177 settled them (day one: check): an
  example host, and `zengine-app` taking a drawing weave; the helpers in a package of their own;
  a drawing's refusal said as a notice.

Records: `reportbacks/zengine-game-drawing-RB.md`, `drawing-usability-research-RB.md`,
`drawing-usability-research-second-RB.md`.
