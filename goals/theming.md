# Theming

**Status:** design in review; nothing built to it yet\
**Decisions:** the founder's

Design answer (Joshua, with Vision), 2026-11-07 and 2026-11-08, reached while reviewing V4 (#117)
through the theme slice of the context map (`../drafts/context-map-themes.md`). These calls bind
every theming prompt. The design drawn from them is `Zen/unreviewed/theming-design-RB.md` until it
is reviewed, then in `Zen/reportbacks/`; the code it reshapes is V4's. This file retires once
theming lands.

## The calls

- **A theme is the look alone, and Workshop's.** Zengine keeps only the mechanism: a value declared
  by name with a default, looked up by that name when it is painted.
- **Four tiers.** Roots: colours; sizes, named from tiny to huge; fonts. Styles: header, body and
  the like, each a font, a size and a colour pointing at roots. A pane's own values, declared where
  they are used, with a default that may be a style or a root. One use: an override of a single
  field. A theme sets values at any tier: one piece, or a complete set.
- **Drawn by name, declared where used**, through helper functions: the name a pane sends is the
  name it declared. No pointer crosses a weave.
- **Themes stack**, and the layouts' owner keeps the stack a layout wears. A weaver sees one word:
  theme.
- **A change is an event by kind**: a colour repaints; a size or a font re-measures. Each weave
  handles it in its own `on`, or not at all. No dirty flags.
- **Settings stay mechanical; keys are the keymap's own layers; the terminal has a look of its
  own**, not fields on the window's colours.
- **`format` stays** for now: it lets a reader refuse the wrong file early, and with
  `format_version` say which rules a file is read by.
