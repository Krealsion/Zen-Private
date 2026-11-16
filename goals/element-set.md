# The element set (V9 to V11)

A goal of *the visual foundation* on the [roadmap](../roadmap.md); how this file works:
[README](README.md).

Done when (the founder's calls of 2026-11-02 and 11-03):

- [ ] proportional text first, after V3 and before V9: a pane writes one layout for both media
- [ ] the elements: button (once `control`), field, list, collapsible, text area, hint
- [ ] a collapsible is one fold, and a group of them an accordion: the code's `Accordion` and
  `IndependentAccordions` renamed to match
- [ ] search is the list's filter: filters and a sort chained in order, by the list's type and
  parameters
- [ ] a choice is a rule, not an element: a group over elements that have an on state, wherever
  they sit, saying how many may be on; tabs are toggle buttons under a one-of rule,
  `tab_strip` their strip's layout
- [ ] groups are a pane's layers, painted and hit in tree order; a move puts a node before or after
  a sibling; a raise flag lifts one until lowered, never across groups
- [ ] the old drawn classes retired as faces supersede them (Image and Grid kept until then); a
  menu row's key and submenu mark as fields; every key a hint names read from the keymap;
  Workshop's panes on a shared piece wherever one fits
- [ ] each stage reviewed for feel, its faces in both media and a pane's code using them, before
  it merges
- [ ] the gates first (the Grinch's, taken): door-level authored migration edges, and roles on
  every element

Tasks:

- [ ] proportional text
- [ ] V9, V10 and V11 (day one: what each holds, from `stages.md`)

Open:

- The raise flag (2026-11-03) beside drawing order and names (2026-11-15): one ordering rule for a
  pane's layers and a drawing's nodes. Lean: the drawing's order number, settled before V9.
- Forms (a form greyed until its box is checked, a field required or checked): rules of the
  choice's family, his linked-field logic, designed as one when the set reaches forms.

Records: `reportbacks/visual-foundation-research/design.md` and `stages.md`,
`reportbacks/ui-census-RB.md`.
