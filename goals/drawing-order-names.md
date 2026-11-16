# Drawing order and names

A goal of *drawing for real-time games* on the [roadmap](../roadmap.md); how this file works:
[README](README.md).

Done when (decided 2026-11-15):

- [ ] paint order is drawing order, in both windows: a drawing read top to bottom shows what is on
  top
- [ ] an optional order number on a node or a group, compared only among its siblings, so groups
  are sub-layers, as in the founder's Quarry engine
- [ ] names are optional: a named node is kept and diffed; an unnamed one is resent with its group
  each time, and what rarely changes (terrain) is sent once and kept, as today
- [ ] a click or an action needs a name; the canvas may name an unnamed node by its place

Tasks:

- [ ] the prompt, built in this order: the order rule, then names, then the number --
  `prompts/unrun/drawing-order-names.md` (warm). Holds on #177.
- [ ] the round run, its pull request reviewed
- [ ] merged

Open:

- Plain numbers or named layers from a declared list. Lean: numbers, the simplest.
- Unnamed shapes as nodes, or as one node of many shapes. Lean: decided by the round; sprites and
  points stay the fast path, unnamed nodes the easy one.
