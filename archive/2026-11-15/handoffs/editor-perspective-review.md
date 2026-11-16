# The Editor perspective, checked against the source

Vision, 2026-10-20, for Ponder. Checked: `rebuild-scaffold/perspectives/editor.md` as found
(untracked), against Zengine `7cc0ec14`, and for drift against `main` at `8a32a6a4` and the open
#340. Of 100 claims checked by hand, 10 are wrong. The keys, the action counts, the shapes and
their fields, the manuals' lines and the laws hold. Fifteen of the design's proposals meet a key,
a law or a shape that already answers them, and the desk is framed in cells where the window is
now pixels.

## How to correct

- As for the baseline: a **Measured** line copies from the line it names. A value the
  perspective chooses -- a window size, a setting's value -- is **Design** and says why; a
  default is the source's.
- What this list does not name was checked and holds, except the drawing's labels other than
  its keys and titles, which were not checked.

## 1. The desk is drawn in cells

- The window is pixels. "150 columns by 60 rows" is not in the lines it cites: they hold the 78
  by 22 minimum and the 640 by 400 maximum, in cells (`workshop/screen.hpp:52-58`), the reserved
  rows (63, 77) and the right column (69-71). Say the window as the perspective's choice, 1800
  by 720 pixels.
- The bands are the face's lines, not twelve-pixel rows. At `7cc0ec14` and on `main` the OS
  window offers no text measure (Workshop adopts it from cols and rows,
  `workshop/weave_handlers.cpp:271`, 273 on `main`), so the bands are 24 and 48 pixels. #340
  gives the window its face, 8 by 18, which Workshop adopts (`weave_handlers.cpp:276-277` at
  `91d7e002`), and the bands become its lines: the top 2 x 18 plus its insets and boundary, 42
  pixels, the bottom 76 (`workshop/screen.hpp:170-217` there). A 720-pixel window's room is then
  602 pixels tall, and the desk's 636-pixel panes run past it.
- So give the desk against the room, and pixels only as what they come to at a stated face. The
  layout research's revision, running now, changes the words section 5 uses (x, y and amount
  present only where a word uses them; no `right-column`): redraw 2.1, 2.2 and 5 from its report
  once the founder settles it, or mark them to be redrawn. The terminal window's picture is
  derived from the pixel one, floored to cells (BL-WORK-05); a count of cells belongs to that view
  alone.

## 2. Corrections, by section

### 2.1

- The drawing's `[load Shift+B]` is `builder.build-realize`, "load after build"
  (`tests/actions.txt:19`); `load` alone is `builder.load`, `o`.

### 2.2

- The Terminal does not close on `escape` or `ctrl+t`. `escape` is `terminal.back`, which steps
  back through recall, list and line to the desk (`tests/actions/zengine.terminal.txt:6`): the
  keys go back and the pane stays. `ctrl+t` opens or focuses and never toggles (WL-DESK-03,
  `agents/workshop/desktop.md:40-44`). Closing on the key that opened it is UX-02, wanted: say
  so.

### 2.3

- Neovim's `profile` defaults to `clean` (`editor/neovim/launch.hpp:45`, which the row takes,
  `editor/neovim-editor/pane.cpp:308`). If the perspective wants `user`, that is Design.
- Files' `listed-entries` defaults to 2000, its most, and may be kept from 100
  (`files/files.hpp:37-38`, `files/files.cpp:952-955`). 256 is not in the source.
- `workshop.pane-titles` is a flag, on by default (`workshop/prefs_persist.hpp:99`, 139-141);
  `shown` and `hidden` are what an older prefs file wrote (93-94, read at 617-631 and 895).
- `workshop.skin` takes four words, `classic` (the default), `block`, `day` and `night`
  (`workshop/pane_settings.hpp:508-527`).
- A layout's baseline theme is `LayoutTheme` `{name, fingerprint}`
  (`workshop/settings_seam_vocabulary.hpp:256-261`), kept in `workshop-prefs.json` under the
  office `@<layout>`, keys `theme` and `fingerprint` (`workshop/prefs_persist.hpp:210-212`).
  `settings/theme_persist.hpp:82-104` is the theme file itself: `ThemeKey` and `ThemeFile`,
  beside `ThemeSetting` (68).

### 3.1

- `a` opens the chooser and sends nothing (`tests/actions/zengine.files.txt:11`);
  `RecipeAuthorRequested` v2 goes with `files.commit-field` (`return`) and `files.write-recipe`
  (20, 22). Both recipe shapes are Workshop's, `workshop/pane_seam_vocabulary.hpp:60` and 68;
  `files/vocabulary.hpp:25-60` holds the pane's key and its action ids.
- The Builder's shapes are not in `builder/vocabulary.hpp:28-116` (the role and the outcomes) or
  `builder/builder-pane/vocabulary.hpp:31-120` (the pane key and the modes). `BuildRequested` v2,
  `BuildOutputRequested` v1, `PromoteArtifact` v1 and `RevertArtifact` v1 are
  `builder/vocabulary.hpp:179`, 319, 405 and 412; `ProjectFrontierRequested`, `PlanRowRequested`
  and `RecipeSourceRequested`, each v1, are `workshop/builder_seam_vocabulary.hpp:26`, 61 and 87.
  `o` sends `PlanNamesRequested` v1 (44), which the list leaves out.

## 3. The design against the source

None of these is wrong to want. Each meets something the source already settles, and needs its
answer in the draft before the walkthrough.

### Keys

1. **`ctrl+f` is the manual's, and a pane cannot take it.** `desktop.manual` is an application
   row above the modes (`workshop/desktop-pane/pane.cpp:645-649`), which meets every pane's
   rows: a pane row on its chord is refused in the collision law's sentence, and Workshop keeps
   the rows it last accepted from that pane (`workshop/keymap_join.hpp:460-473`,
   `workshop/docs/hotkeys.md:267-272`). A pane may stand in for the manual by declaring
   `supersedes`, but the chord is the manual's only key, for the reason at `pane.cpp:624-625`.
   Choose another chord.
2. **`/` is text in the standard Editor.** A row on a printable swallows that character when it
   fires (WL-KEY-12, `agents/workshop/keyboard.md:116-118`), so a slash could no longer be typed
   into source. In the Neovim-backed Editor, `/` is Neovim's own search.
3. **Zengine names no function key.** `input/vocabulary.hpp` has no scancode for one and the key
   grammar no name (`workshop/gesture_grammar.hpp:29-92`), so `f3` and `shift+f3` are refused as
   outside the grammar. From a POSIX terminal, F1 to F4 arrive as Escape and two letters
   (`input/translate.hpp:378-392`) and the rest are dropped (476-483).
4. **`ctrl+tab` is `tab` from a POSIX terminal.** The reader takes the tab byte as `tab` with no
   modifier (`input/translate.hpp:307`) and reads no keyboard protocol that would say ctrl, and
   the standard Editor's `tab` inserts a tab (`tests/actions/zengine.editor.txt:4`). `posix_gap`
   does not name it (`workshop/gesture_grammar.hpp:278-303`), so the row would be accepted and
   type a tab. `ctrl+shift+tab` arrives only where a terminal sends `ESC [ 1 ; 6 Z` (503). A plain
   ctrl+letter is what both windows deliver.
5. **`ctrl+w` removes a layout one mode over.** In command mode it is `layout.remove`
   (`workshop/keymap.hpp:221`, `workshop/docs/setups.md:108`), kept off bare keys because a
   removal cannot be undone (`keymap.hpp:213-214`). A pane row on it does not collide (a pane's
   rows meet no other mode's, WL-KEY-05), but a hand that learns `ctrl+w` closes a file presses it
   once the Editor has given the keys back.
6. **`alt+l` never arrives from a POSIX terminal**: alt arrives only on the editing keys
   (`workshop/gesture_grammar.hpp:282-284`). It is accepted and its gap said once
   (`agents/workshop/keyboard.md:89`). For a key in both windows, take a free ctrl+letter.

### Opening at a line

7. **`builder.output-open`:**
   - the reader has no cursor: `up` and `down` move the page
     (`builder/docs/zengine.builder-pane.md:279-297`). Say which line it reads: a pressed row, or
     a cursor the reader gains;
   - a relative path in a build's output is relative to where the build ran, a CMake recipe's
     build tree or a one-file recipe's workspace (`builder/generate.hpp:305`, 327), not
     `ProjectRoot::project_dir`;
   - MSVC writes `file(line,column)`, and a Windows path's drive letter carries a colon: say which
     forms the parse reads;
   - like `e`, it asks its hand's class `open` before it sends (WL-OPEN-01,
     `agents/workshop/opening.md`; WL-GUEST-03, `agents/workshop/guests.md`).
8. **`OpenSourceRequested` v2's absent values.** Loom's optional fields (a `std::optional<T>`
   member, `include/zen/weave/shape.hpp:19-21` at Loom `3afe9e3`) say "no line" without 0 meaning
   it, as the founder chose for the layout words on 2026-10-20. `kMaxLineText`, 240, is already
   source-transfer's, with its rule for a cut line (`editor/source-transfer/vocabulary.hpp:64-80`):
   use it. `PrepareSourceRequested` has two versions (`workshop/open_seam_vocabulary.hpp:119`, and
   v2 with the canvas room at 170): the widening is of v2.
9. **`zengine.search`** opens a hit the same way, so it too asks class `open` first.

### More than one document

10. **The buffer shelf:**
    - a switch hands over one document (`EditorTransfer`,
      `workshop/editor_handoff_vocabulary.hpp:23-44`), and Neovim to standard already needs
      consent for unsaved changes in other buffers (`editor/docs/editor-switch.md:50`): say what
      a switch does with the other seven;
    - a reload in place carries one `EditorPaneState` and its undo (WL-EDIT-15,
      `editor/editor-pane/vocabulary.hpp:83-124`);
    - the 8 MiB undo budget and the 4 MiB file ceiling are one document's
      (`editor/editor-pane/editor.hpp:37`, 42-44): say whether a shelf multiplies them or shares
      them;
    - Neovim already opens a second file beside an unsaved one
      (`editor/docs/zengine.editor.md:222`), so the gap and option B are the standard Editor's
      alone.
11. **`editor.2`**: the opening publishes one `EditorDocument` for the office
    (`workshop/open_seam_vocabulary.hpp:29-41`), and a switch carries one. A second seat is a
    second document in both, far more than `info.2`'s value views: price it in call 1, or keep it
    out of the recommendation.

### What the perspective asks of others

12. **Focus per perspective** (2.4, and section 4's first ask): the selection and the keyboard are
    one Workshop-global truth that a layout switch does not copy, clear or revalidate
    (WL-LAYOUT-06, `agents/workshop/layouts.md:52-63`). Restoring focus per perspective changes
    that law: say so, and the change is the founder's to take.
13. **A holder per perspective** (section 4's fourth ask): the office has one holder at a time,
    so a perspective preferring the other makes every move between them a switch. Standard to
    Neovim resets the standard Editor's undo history, and Neovim to standard can need consent
    (`editor/docs/editor-switch.md:49-50`). Say whether that is the ask, or a hint read only when
    a session starts.
14. **A switch from the Editor's menu** (Missing 4): the act classes are `build`, `write` and
    `open` (WL-GUEST-03), and none names a switch; only the Terminal is granted the switch's
    commands (`editor/docs/zengine.editor-switch.md:38-39`). Say whether the menu's office is
    granted them as the Terminal is, or a class is added.
15. **Flow to the Editor** (2.4): `a` offers a folder only once it holds a configured CMake tree,
    a `CMakeCache.txt` (`files/docs/zengine.files.md:202-205`), and `ask-generate` writes a
    `CMakeLists.txt` (`flow/docs/zengine.flow.md:113-116`). Say how the generated directory
    reaches the Builder.

## 4. Drift since `7cc0ec14`

Eight merges, #330 to #339; `main` is `8a32a6a4`.

- `editor/docs/zengine.editor.md:291` is now 316: #333 gave the Editor the window's pointer in
  its own area (`AreaButtonChanged`, `AreaPointerMoved`, `AreaWheelTurned`, `AreaHoldEnded`).
  Section 3.1 can say that presses, sweeps and the wheel now reach the Editor in a window.
- #338: the default plans load the windows.
- #339 set text a character a cell in the windows, the stopgap #340 (open) replaces with the
  face's measure: `WindowOffered` v3 `{window, width, height, epoch, cell_px, text_advance_px,
  text_line_px}`, and each owner paints its own ground. Section 1 above is what this moves.
- Every other line the draft cites holds on `main`.

## 5. What holds

- The six moments, and every key and action id in them, `o`, `return` and `f` included (the
  Builder tutorial's own sequence).
- The counts: the Editor 6 and Neovim 4, the one unbound row; Files 23; the Builder 33 over four
  modes, output's 10, none of which opens a diagnostic.
- The shapes and their fields: the switch's six answers, `EditorDocument`, the opening's trial,
  preparation and admission, `SourceText`, `SourceSelection`, `SourceLocation` and its context,
  `OpenSourceRequested` v1 and `SourceOpened`, `EditorPaneState`, `ProjectRoot`.
- The Editor's and Files' settings keys, bounds and wheel values; the band keys; the pane
  references; the v5 file's envelope, its settings' spelling and the Layouts row as the shipped
  desks write it.
- The manuals' lines; WL-LAYOUT-06 and 07 for the document across a detour; WL-OPEN-01; the UX
  items; `info.2`; `editor-materials`; the Terminal's `send` and `ask`.
- The four open calls are well posed. Calls 1 and 4 need the costs in section 3 beside them
  before the founder answers.

## 6. Before the walkthrough

1. Correct section 2's ten.
2. Answer section 3's fifteen in the draft: a chord both windows deliver where a key is taken or
   does not arrive; the shelf's and the second seat's costs in call 1; the law each ask changes.
3. Redraw 2.1, 2.2 and 5 against the room in pixels, or mark them to be redrawn once #340 merges
   and the layout words settle.

Then the draft is ready for the founder.
