# The perspectives baseline, checked against the source

Vision, 2026-10-19, for Ponder. Checked: `rebuild-scaffold/perspectives/BASELINE.md` and
`README.md` as found (untracked), against Zengine `7cc0ec14`. Of 57 claims checked by hand, 31 are
wrong. The counts read off the action census hold; most names, keys, settings, bounds and file
names do not. Correct BASELINE.md from this list before drawing any perspective.

## How to correct

- A **Measured** line names the file and line it was read from, at `7cc0ec14`, and copies the
  name or number from there; nothing is composed. A number taken from a report is **by report**,
  and says which, or is counted again.
- A name that cannot be found in the source is not written.
- What this list does not name was not checked. Check it the same way: the shortfalls ("where it
  falls short") were not checked, except where a line below says so.

## 1. The definition

- BASELINE makes a perspective a layout ("called a layout or setup in parts of the code today").
  The founder's notes keep them apart (`private/backlog.md`, section 1b, theme 6): "a workspace
  arranges tools and material; a perspective presents them for a task and may span workspaces".
  Today's nearest thing to a perspective is a layout and what it holds; it is not one.
- README's `ready` says "ready to hand to `layouts/`". Which owner holds a perspective is not
  decided: the desk's owner is named `zengine.layouts` so that theme 6 is not decided by a name
  (the desk split's decision 3, taken 2026-10-19). Say "ready for the founder" instead.

## 2. Corrections, by section

### 1.1 The desk

- The bounds are `workshop/setup.hpp`'s: `kMaxSetupNameLen` 32 (line 37), `kMaxSetupPanes` 96
  (45), `kMaxLayouts` 8 (49), `kMaxPaneSettingsPerDesk` 512 (59).
- No `kMaxPaneRefLen`, `SetupPlaceMode` or `SetupSizeMode` exists. A place is `default`,
  `right-column` or `pixels` (`setup.hpp:285`).
- A setting's key is at most 32 bytes and its text 64: `kMaxPaneSettingKeyLen` and
  `kMaxPaneSettingTextLen` (`workshop/pane_settings.hpp:26-27`).
- `SetupLink` holds `path` and `known` (`workshop/layout_shelf.hpp:35`): no stem, no `dirty()`.
  The dot is `link_status`: none, current or modified (`layout_shelf.hpp:55`).
- `put_live` counts the desks put live (`layout_shelf.hpp:88`); it is not a mode. No
  `workshop.put-live` exists, `Shift+P` is the Builder's `builder.promote`, and WL-LAYOUT-11 is
  the shared-artifact law (`adopt_known_setup`).

### 1.2 The files

- The keymap file is version 2 (`workshop/keymap_persist.hpp:33`).
- Themes (`settings/theme_persist.hpp`): `kMaxThemeDepth` is 4 (line 57; 16 is
  `kMaxThemesResolved`). A `ThemeSetting` is `{target, key, flag, number, text, clear}` (line 68),
  its target `*`, `<office>` or `<office>/<pane>`.
- Eight offices declare pane settings, each in its `vocabulary.hpp`: Attention (`detail`), the
  Editor (`status`, `tab-width`, `undo-depth`, `wheel-lines`), Neovim (`profile`, `status`), Files
  (`listed-entries`, `wheel-rows`), Introspection (`composite-columns`, `gap`, `view-columns`),
  the Terminal (`legend`, `prompt`, `wheel-rows`), the View Builder (`new-height`, `new-width`,
  `snap-reach`) and the desktop (`help`). "32 across 11 offices" is a report's count.
- `kMaxLocks` is 128 (`workshop/prefs_persist.hpp:55`); no `kMaxSettingLocks` exists.
- `SettingsWriteRequested` is `{revision, writes, baselines, cause}`, each `SettingWrite` naming
  one layout by position, `-1` the live one (`workshop/settings_seam_vocabulary.hpp:311-339`). No
  `target_all_layouts` exists.

### 1.3 The load plans

- Each window plan holds 21 rows (`workshop/window-load-plan.json`,
  `workshop/sdl-window-load-plan.json`). Required: `zengine-operators-basic`,
  `zengine-workshop-session-history`, `zengine-graphics`, the window (`zengine-window-terminal`
  with `zengine-input`, or `zengine-window-sdl` with `zengine-input-sdl`) and `zengine-timer`.
  Optional, each `zengine-<name>`: `introspection`, `composer`, `desktop-pane`, `files`,
  `builder-pane`, `attention-pane`, `connections-pane`, `info-pane`, `terminal-pane`,
  `editor-pane`, `menu-presenter`, `flow-pane`, `view-builder`, `inventory`, `inventory-pane`.
- No row is `zengine-Builder`, `zengine-workshop` (Workshop is the host), `zengine-opening`,
  `zengine-editor-switch`, `zengine-view-host` or `zengine-flow-host`.

### Task 1, Flow

- The 39 actions are `tests/actions/zengine.flow.txt`'s, ids with no `flow.` prefix: `ask-save`,
  `ask-open`, `run`, `ask-generate`, `ask-discard`, `ask-new`, `ask-import`, `ask-export`,
  `apply`, `stop`, `inspect`, `catalog`, `page-graph` to `page-events`, `fit`, `zoom-in`,
  `zoom-out`, `ask-trigger`, `ask-emit`, `add-fold`, the state, message, library and preset asks,
  `send`, four `drop-*`, `dialog-confirm` and `dialog-cancel`.
- None of the others BASELINE names exists anywhere in `flow/` (`connect`, `add-operator`,
  `add-hub`, `extract-subflow`, `bind-state`, `add-handler`, `add-publish`, `edit-expression`,
  `add-local-operator`, `select-event`, `clear-events` and the rest). Read the pages again in
  `flow/docs/zengine.flow.md`.
- Five are bound (`ctrl+s`, `ctrl+o`, `ctrl+r`, `ctrl+g`, `return`), so 34 are unbound, not 35.
- Flow declares no settings: `snap-reach`, `new-width` and `new-height` are the View Builder's,
  and no `event-limit` exists. No `flow-pane.json` exists.
- Run, apply, send and stop are the Flow pane's `run`, `apply`, `send` and `stop`; no
  `flow.ask-run` family exists. No `powers.carry` exists.

### Task 2, the Editor

- Neovim's rows are in `tests/actions/zengine.editor.txt`, beside the standard Editor's.
- The marks file is `workshop-marks.json` (`workshop/pane_seam_vocabulary.hpp:21`).
- The Builder's 33 rows are in `tests/actions.txt`, and the Builder declares no settings.
- Only the Terminal is granted `EditorSwitchRequested`, not Compose
  (`editor/docs/zengine.editor-switch.md`, Use). Checked and holding: neither Editor has a find
  or search.

### Task 4, UI

- The View Builder's pane is `view-builder` (`view/view-builder/vocabulary.hpp:19`), and the
  elements are in `graphics/elements/`.
- "this session already runs a view" is not in the source.
- UX-11 is navigation gestures, UX-13 a component's events as triggers, UX-14 notes on an element
  and UX-16 closing a view with unsaved work (`private/ux-batch.md`); none says what BASELINE
  cites it for. Give each View Builder defect its source, or drop it.

### Task 5, exploration

- Powers is `zengine.introspection/powers`, its 7 actions in
  `tests/actions/zengine.introspection.txt`; Loaded and Project have no rows there.
- Compose's keys: `compose.submit` `ctrl+return`, `compose.store` `ctrl+s`, `compose.preset`
  `ctrl+b`.
- Info has 30 distinct actions over 68 rows (`tests/actions/zengine.info.txt`); unset is
  `ctrl+u`, not Delete.
- Inventory holds up to 36 portable views, named `inventory.<n>` (`kMaxPortableViews`,
  `inventory/inventory-pane/slots.hpp:12`).
- The Terminal has 9 actions (`tests/actions/zengine.terminal.txt`).
- Compose, Info, Inventory and Powers declare no settings; Introspection's and the Terminal's are
  in 1.2 above.
- UX-31 is an item's full schema on hover and Inspect, not a Preset/Value toggle.

### Task 6

- Attention has three actions: `attention.up`, `attention.down` and `attention.dismiss` (`d`).
- `GuideRequested`'s law is `agents/workshop/guide.md`, not `workshop/docs/zengine.desktop.md`.
- Arranging has no `Shift+P` put-live (1.1 above).

## 3. What holds

- The tasks, and the three you added: triage, pairing and tailoring.
- Every perspective drawn for the two windows, never the Skin.
- The action counts: Flow 39, the Editor 6 and Neovim 4, Files 23, the Builder 33, the View
  Builder 7, Powers 7, Compose 9, Inventory 21, Hotkeys 8. The Editor's, Neovim's, Files' and
  the View Builder's settings.
- Workshop's 11 office settings and its four skins; the file names; the layout keys `.` and `,`;
  the eight demo setups; Info's four views; the View Builder's three elements; the eight element
  headers; `Panes::selected` and `Panes::keyboard`; `activate_layout`; Flow's dialog sentence.

## 4. Second check, after the corrections (2026-10-19)

BASELINE.md and README.md as corrected, checked again at Zengine `7cc0ec14`: 87 claims, 83 hold,
and the name checker finds nothing the source lacks. The baseline can be drawn on. Four small
fixes, to fold in with the first drawing:

1. 6b: the guests file has no default name. It is passed with `--guests`, and the pages call it
   `guests.json`; no `workshop-guests.json` exists.
2. 1.3: "32 of 44" is not in G1's report. It is a count of `census.md`'s rows that are wrong in
   both windows, and Vision's count agrees; say it is counted from the census, not by report.
3. Task 3: "Handoff Rule 5" is the handoff's section 5 (what not to do), its credential line.
4. 3.5: the desk's owner is the part `workshop/layouts/`, not `layouts/`.
