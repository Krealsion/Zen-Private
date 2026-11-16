# Context map: the theme slice

Vision, 2026-11-07. The first slice of Zen's context map (Domain-Driven Design): the parts that
bring a theme to the screen, as V4 (#117) builds them, and the words each part uses. Read from V4's
branch at `1a4655c7` and `main` at `4dba5cb2`.

## The parts

Each is an office with its own model; its shapes are the language it speaks to the others.

- **Settings** (`zengine.settings`, the `zengine-settings` weave): reads theme files, judges a theme
  whole, applies it, and builds a palette for each theme it knows.
- **Layouts' owner** (`zengine.layouts`): keeps the layouts -- each one's rows, settings and locks,
  and one theme name (`LayoutTheme`).
- **Workshop** (`zengine.workshop`): the desk and the keymap. Chooses which palette each area wears,
  offers the compiled shipped palettes, and tells Settings where the themes are.
- **Graphics** (`zengine.graphics`, the directory): keeps every offered palette by name at its
  latest revision, and which palette each area wears; passes both to the windows.
- **Windows** (SDL, terminal): paint each area from the palette it wears.
- **Flow**, and any pane with slots: says which colours it lets themes set.

## What crosses

- Workshop -> Settings: where the theme folders are, the offices the plan names, Workshop's own
  theme (`ThemesPlaced`).
- Settings -> Layouts' owner: reads the layouts (`LayoutSettingsRequested`); writes their settings
  and theme names (`SettingsWriteRequested`, its `LayoutThemeWrite`s).
- Settings -> Workshop: reads the keymap and edits it (`KeymapRequested`, `KeymapEditRequested`).
- Settings -> Graphics: a palette under each theme's name (`PaletteOffered`).
- Workshop -> Graphics: the compiled `night`, `day` and `block` (`PaletteOffered`), and which
  palette each area wears (`PaletteChosen`).
- Graphics -> Windows: the palettes, and each area's choice.
- Flow -> Settings: its slots (`SlotsDeclared`); Settings -> anyone: say them again (`SlotsAsked`).
- Settings -> anyone: entries skipped once their office declared (`ThemeSkipsSaid`), which Workshop
  says on its band.

## The words

What each word means in each part. Two meanings or two owners is a decision.

- **theme**, five meanings:
  - Settings: a file of settings, keys and a look (`ThemeFile` v2), which may include others.
  - Layouts' owner: one name a layout keeps, with that theme's fingerprint (`LayoutTheme`, "a
    layout's baseline").
  - Workshop: `workshop.theme`, a choice of `night`, `day` or `block` (`classic` for `night`), on a
    pane's row and for Workshop's own areas.
  - Graphics: the shipped looks, `graphics/themes/*.json`, compiled into palettes.
  - The snake: its `theme` button, which switches between two palettes.
- **palette**, three meanings and two owners of one name:
  - Graphics: what a window paints with, kept by name at its latest revision (`PaletteOffered`).
  - Settings: a theme's look, kept under the theme's name (`HeldPalette`).
  - Workshop: the name an area wears (`PaletteChosen`).
  - `night` is offered twice: compiled, by Workshop, and from its file, by Settings. Graphics keeps
    whichever revision is higher, and nothing relates Workshop's revisions to Settings'.
- **baseline**, one idea in three places: the flag on an apply (`ThemeApplyRequested.baseline`), a
  layout's theme (`LayoutTheme`), and Workshop's `worn_theme()` (the live layout's, else its own).
- **slot**, two meanings:
  - Settings, Flow, Graphics: a colour or text size an office lets themes set (`SlotsDeclared`,
    `PaletteSlots`, a theme file's `slots`).
  - Inventory: an item's place in a view, and its key (`SlotView`, `SlotBinding`).
- **skin**, retired and still read: `workshop.skin` is read as `workshop.theme`; `app.json` says
  `window.skin`; comments still name the retired Skin seam ("the Skin's answer to a paste").
- One meaning each, nothing to decide: **look**, **pool**, **wear**, **merge**, **reset** (the
  keymap's `reset` means the same: back to the default), **waiting**, **lock**, **outline**.

## Decisions

Decided (the founder, 2026-11-07):

1. **The Layouts' owner keeps what a layout wears: its stack of themes**, saved with the layout.
   Settings builds the palette from the stack; Workshop picks it by name.

Surfaced by the words, open:

2. **One owner per palette name.** Lean: Workshop offers the compiled palettes only while no weave
   holds `zengine.settings`; with Settings there, it alone offers palettes.
3. **A weaver sees one word, theme** (the founder's call, 2026-11-04). Inside, two words keep two
   things apart: a *theme* is a file; a *palette* is what Graphics paints with, built from a
   layout's themes. Open: `workshop.theme` on a pane's row -- a theme laid over the layout's stack
   for that pane's area (lean), or a stack of its own.
4. **"baseline" retires into the stack**: the bottom of a layout's themes, and the apply's flag
   becomes "add to the layout's themes".
5. **"slot" keeps one meaning.** Lean: Inventory keeps it, the game meaning; the theme side takes
   another word (theming elsewhere says "token"). Cheapest before V4 merges, since V4 brings
   `SlotsDeclared` and the theme file's `slots`; `PaletteSlots` and Flow's `slots.json` are on
   `main` already.
6. **"skin" goes**: `window.skin` renamed with the next app file change (V4 asked), and the
   comments naming the Skin seam say what answers now.
