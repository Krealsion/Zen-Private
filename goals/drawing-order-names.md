# Drawing order and names

A goal of *drawing for real-time games* on the [roadmap](../roadmap.md); how this file works:
[README](README.md).

Done when (decided 2026-11-15, from the founder's reading of TheyCameInWaves as the first port's
study: every immediate-mode library teaches that what is drawn later is on top, and Zen's
`picture` looks the same but does not behave so):

- [ ] paint order is drawing order, in both windows: a drawing read top to bottom shows what is on
  top, as in Java2D, LOVE or raylib; alike for a whole drawing and a difference (today a node new
  in a difference goes after its siblings, so one picture can stack two ways by its history,
  P-WORK-105)
- [ ] an optional order number on a node or a group: siblings sort by it first, then by drawing
  order, and a number competes only with its siblings, so groups are sub-layers, as in the
  founder's Quarry engine; nothing inside a group sorts past its parent's siblings (an entity
  whose y goes negative stays above the terrain group, and none passes the HUD). It covers a layer
  kept in its place (the HUD's high number), creation order (a spawn count) and y-sorting (an
  entity's y), so there is no third mode; groups follow the same rule, and today's creation order
  is replaced. The window's key is already ancestors' places, then its own
  (`graphics/window/store.hpp` 198): only how each level ranks its children changes
- [ ] names are optional: an unnamed thing is resent with its group whenever any of it changes
  (right for what moves every frame); a named one is kept and compared one by one, alone or as a
  named sub-group with unnamed parts inside; what rarely changes (terrain) is sent once and kept,
  as today
- [ ] a click or an action needs a name: a press reports the name of the thing under it; the
  canvas may name an unnamed node by its place in its group, so the window need not change for it

Tasks:

- [ ] the prompt, built in this order: the order rule (it ends the inconsistency and a port's
  first trap), then names, then the number; one round, before the language pass reaches
  `graphics/` and before the ports -- `prompts/unrun/drawing-order-names.md` (warm). Holds on
  #177.
- [ ] the round run, its pull request reviewed
- [ ] merged

Open:

- Plain numbers or named layers from a declared list. Lean: numbers, the simplest.
- Unnamed shapes as nodes, or as one node of many shapes. Lean: decided by the round; sprites and
  points stay the fast path, unnamed nodes the easy one.

Records: the founder's calls of 2026-11-15 (filed here from the Project's `claude/zen-pending.md`);
TheyCameInWaves, `github.com/Krealsion/TheyCameInWaves` (Java2D).
