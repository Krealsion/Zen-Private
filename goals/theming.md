# Theming

**Status:** designed and decided; nothing built to it yet\
**Decisions:** the founder's

Design answer (Joshua, with Vision), 2026-11-07 and 2026-11-08, reached while reviewing V4 (#117)
through the theme slice of the context map (`../drafts/context-map-themes.md`), then the design
drawn from it (`Zen/reportbacks/theming-design-RB.md`), taken with Vision's amendments on
2026-11-08 for V4's next attempt. These calls bind every theming prompt; the code they reshape is
V4's. This file retires once theming lands.

## The calls

- **A theme is the look alone, and the host's** (Workshop's, where Workshop is the host). Zengine
  keeps only the mechanism: a value declared by name with a default, looked up by that name when
  it is painted.
- **Four tiers.** Roots: colours; sizes, named from tiny to huge; fonts. Styles: header, body and
  the like, each a font, a size and a colour pointing at roots. A pane's own values, declared where
  they are used, with a default that may be a style, a root or an exact colour. One use: an
  override of a single field. A theme sets values at any tier: one piece, or a complete set.
- **Drawn by name, declared where used**, through helper functions: the name a pane sends is the
  name it declared. No pointer crosses a weave.
- **Themes stack**, and the host keeps the stack a layout wears (in Workshop, the layouts' owner).
  A weaver sees one word: theme.
- **A change is an event by kind**: a colour repaints; a size or a font re-measures. Each weave
  handles it in its own `on`, or not at all. No dirty flags.
- **Settings stay mechanical; keys are the keymap's own layers.**
- **The terminal's look is its own file.** A theme is a name with a window file, a terminal file
  or both, each file's `format` saying its medium. A terminal file holds the colour names draws
  already use (`accent` and the rest), each with its ink and fill, and the border characters; no
  sizes, fonts or other window fields. Its defaults are today's terminal colours; a weaver edits
  them by the group a name belongs to.
- **A theme for the other medium is a normal link in the chain**: applied in its place, converted
  as well as it can be (a colour to its nearest ink; an ink to the colour xterm shows it in;
  `terminal default` falling through to the theme below), and marked with a warning in the theme
  manager when it is put in.
- **The theme manager shows a sample**: elements and components wearing a theme fed to it, as the
  look stands or as it would be if applied.
- **`format` stays** for now: it lets a reader refuse the wrong file early, and with
  `format_version` say which rules a file is read by.

## Decided from the design (2026-11-08)

1. **One owner per palette name.** Where the theme weave runs it owns the shipped looks; a host
   without it (`zengine-app`, the snake) offers its own.
2. **A pane's own values are "own values"** in code and pages; Inventory keeps "slot".
3. **"baseline" retires**: a layout wears a stack, bottom first (`LayoutThemes` for
   `LayoutTheme`), and the theme's fingerprint goes with it.
4. **A pane row's theme** is one theme laid over its layout's stack.
5. **Sizes `tiny` to `huge` are roots**; `caption`, `body`, `heading` and `title` become styles,
   weight a style's field.
6. **The terminal's look**: the two calls above, two files paired by name and the other medium's
   theme converted in its place.
7. **No new change shapes**: a size or font change is a new `AreaRoom`, which carries the
   measures; a colour change is the window's own repaint; an owner hears a colour change only once
   a weave computes from one.
8. **A version-1 theme file that carries settings or keys is refused**, saying where they live
   now.
9. **The theme weave is a feature of its own**: `theme/`, role `zengine.theme`.
10. **Includes stay beside the stack**: a file is built from pieces; a layout wears a stack.
