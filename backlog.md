# Zen Standing Backlog

**Status:** PRIVATE LIVE AUTHORITY  
**Refreshed:** 2026-10-19  
**Role:** work Zen knowingly owes but is deliberately not doing now  
**Pressure:** `private/pressure.md`

An item here is not authorized work and does not imply urgency. Closed items have been removed from
the live file; their evidence remains in reports and Git history.

## 1. Rules

An item belongs here only when Zen has decided work is owed. A possibility, known seam, or observed
pressure stays outside until that decision exists. Every item names its wake condition and source.

**Bounded work moves to GitHub issues** (the founder, 2026-10-09). Defects, review leftovers, doc
fixes, and parked or later ideas are filed as issues on the public repositories, each written as a
small prompt with its fences, so any executor can take one, ship it as its own pull request and
merge it when it is ready. An issue's pull request merges first, and an open phase branch rebases
onto it. A security defect is never a public issue: it goes into a draft private security advisory.
Deep review filed them, from [the handoff](handoffs/issues-handoff.md), until it went (the founder,
2026-10-14). Since then Vision prompts the filing, under `UnknownWorkers` with the labels set in the
founder's name, and reviews the issues' pull requests, beside the deep-review lite the founder runs
now and then. A filed item leaves this file for its issue link. The ordered arcs, research items and
direction stay here and move by phases.

## 1a. The order now

**Close what is open, then the roadmap** (the founder, 2026-10-14). First: #219, the readability
pass, merged as it stands (`aab5177`); Zengine's twelve `ready` issues and the grow frame found in
#219's review, taken in one batch ([prompt](../prompts/ready-issues-batch.md)), started by the
founder; these plans current; every arc resting where it is merged, its next step written in its
item. Both reported and reviewed (Vision, 2026-10-15): the batch as #220 to #233, thirteen pull
requests green on their own heads and #228 the grow frame, filed; the manuals as #234 to #249,
sixteen green, 33 pages in all. The merge train ([prompt](../prompts/merge-train.md)) brought the
remaining branches onto `main` and raised the suite floors (`#250`, `d86ee70`): round one (#220,
#221, #222, #223, #225, #227, #229, and #234–#249 except #238, #240, #243), round two (#226
`65338a6`, #230 `bbe202e`, #231 `524d453`, #232 `98fd5c3`, #233 `a48edc7`, #238 `f9eba7d`, #240
`aae4010`, #243 `09c2d1f`, and #250 `d86ee70`), and the final batch items (#251 `0ea9441` manual
ASCII check, #257 `41336b2` plan booter realization asks, #258 `f06d64d` Flow node placed with no
trigger refused in words, #259 `200f302` refused pane caret said on the notice band, and #224 / #270
`8d5c5d0` `zengine.project`) all **CLOSED and merged** on `main` (2026-10-15 to 2026-10-16).

**Path 1 — Spine-Cutting & Readability Arc (Phases 1A–3B, CLOSED 2026-10-16):**
- **Phase 1A (`#265`, `8b26fd7`, [prompt](../prompts/phase-1a-facets.md), [MSVC follow-up](../prompts/phase-1a-facets-msvc.md)):** Composable weave facets (`zengine/weave_facets.hpp` — `WeaveWith<State, Facets...>`, `DrawingFacet`, `RoomFacet`, `PaneFacet`, `PaneRowsFacet`, `AskFacet`, `ManualFacet`), an end-of-delivery chain (closing P-WORK-72), room resizes reaching drawers (closing P-WORK-73), and `ProbeBase` retired in `activation/` in favor of facet `Activated` handlers over `TimedWeave`.
- **Phase 1B (`#266`, `54d8cc0`, [prompt](../prompts/phase-1b-actions.md)):** Every shipped pane declares what its presses send (`v3::PaneActionRow` causes across all remaining panes, wrapping `Answers` lines at page width), and single-pane offices answer their manual through `ManualFacet`.
- **Phase 1C (`#267`, `c2f2a5a`, [prompt](../prompts/phase-1c-window-clicks.md)):** A press nothing drawn takes is silent unless its area asks for the pointer (`wants_area_pointer`), a press given to an area's owner says it is in the area's pixels, and a facet weave's claim reaches the weave's own handler.
- **Phase 1D (`#269`, `5575476`, [prompt](../prompts/phase-1d-pane-facets.md)):** Pane offices compose their offer, room, rows, and asks as facets (`PaneFacet`, `PaneRowsFacet`, `AskFacet`), and Files keeps the row a reload carried (P-WORK-74 in part).
- **Phase 1E (`#268`, `60a41e5`, [prompt](../prompts/phase-1e-reload-and-manuals.md)):** Reload-in-place state preservation for four offices (P-WORK-74 in part) and the remaining multi-pane offices answer their manual through `ManualFacet`.
- **Phase 2A (`#270`, `8d5c5d0`, [prompt](../prompts/phase-2a-hub-doors.md)):** One project office (`zengine.project`) for the project's readings, recipes, and plan rows (#139 / #224), merged alongside #251, #257, #258, and #259.
- **Phase 2B (`#271`, `a09da96`, [prompt](../prompts/phase-2b-panes-and-reload.md)):** Remaining pane facets (`View Builder`, `Connections`, `Demo`), reload-in-place preservation (`Compose` target and form, `Editor` bounded undo history, `Info` value views, `View Builder` re-asking the view host — closing P-WORK-74), and three pane fixes (`Inventory` naming the removed entry, `Info` `info.value.*` action ids, `View Builder` `view.*` action ids).
- **Phase 3A (`#272`, `b26630b`, [prompt](../prompts/phase-3a-host-manuals.md)):** The Flow host (`zengine.flow.host`), the view host (`zengine.view.host`), and the build runner (`zengine.builder.runner`) carry their manuals and answer what each shape they accept does (closing BL-ADOPT-05 B2 across host offices).
- **Phase 3B (`#273`, `7e9183b`, [prompt](../prompts/phase-3b-surface-timer-and-act.md)):** `zengine-skin-tui-block` built as a second library and documented in `surface/`, timer suite skin swap and timed pokes bounded on their answers, and `workshop/act` boundedly re-reading a moved picture when a press aimed at a word meets a moved picture.

**Godfile / Structural Health Split Arc (Waves 1–5, Phases 4A–8C, CLOSED 2026-10-16):**
Executed to enforce a ~1,000-line ceiling per translation unit and header across Zengine so every subsystem has bite-sized, single-responsibility files before the next roadmap spine themes (every product `.hpp` and `.cpp` now stands under 1,900 lines, down from 6,541):
- **Wave 1 (CLOSED — `#274` `af210e4`, `#275` `8189c0c`, `#276` `32f4e45`):**
  - **Phase 4A (`#275`, [prompt](../prompts/phase-4a-workshop-weave-split.md)):** `workshop/weave.hpp` composes its terminal door and its page as facets.
  - **Phase 4B (`#274`, [prompt](../prompts/phase-4b-info-value-view-split.md)):** `info/value_view.hpp` hands its watch (`info/value_view_watch.hpp` / `value_view_tree.hpp`) and its picture (`info/value_view_edit.hpp`) to headers of their own.
  - **Phase 4C (`#276`, [prompt](../prompts/phase-4c-graphics-elements-split.md)):** `graphics/elements.hpp` split into focused part headers (`graphics/element_*.hpp` — button, checkbox, list, grid, icon, image, scroll view, text box).
- **Wave 2 (CLOSED — `#277` `504ecf4`, `#278` `1b8462a`, `#279` `34c6dfd`):**
  - **Phase 5A (`#278`, [prompt](../prompts/phase-5a-mirror-panes-and-introspection.md)):** Mirror panes (`Attention`, `Connections`) compose directly on `PaneRowsFacet`; `Powers` splits `powers_detail.hpp`; `Introspection` splits its three seats (`introspection/seats.hpp`) and detail helpers.
  - **Phase 5B (`#279`, [prompt](../prompts/phase-5b-terminal-door-and-guest-judge.md)):** The Terminal's host side moves from `workshop/` to `terminal/` (`terminal/door.hpp`, completer, record picture); `GuestDoor` (`workshop/guest_judge.hpp`) answers `ActorScopeRequested` for Workshop's office.
  - **Phase 5C (`#277`, [prompt](../prompts/phase-5c-examples-graphics.md)):** `examples/snake` draws new-game and operator buttons with `gfx::Button` and tracks operator asks with `AskBook`.
- **Wave 3 (CLOSED — `#280` `cf0d85c`, `#281` `de3268d`, `#282` `ee126f9`):**
  - **Phase 6A (`#282`, [prompt](../prompts/phase-6a-info-property-view.md)):** `info/pane.cpp` (2,422 → 995 lines) extracts `info/property_view.hpp` (showing one pane's properties in one list) and deletes the dead 1,291-line uncompiled `workshop/panes.cpp`.
  - **Phase 6B (`#280`, [prompt](../prompts/phase-6b-workshop-desk-read-split.md)):** `workshop/weave.hpp` (2,718 → 1,872 lines) and `workshop/weave_inspection.cpp` (1,073 → 339 lines) extract `workshop/desk_read.hpp` and `workshop/weave_desk_read.cpp`.
  - **Phase 6C (`#281`, [prompt](../prompts/phase-6c-desktop-pane-views-split.md)):** `workshop/desktop-pane/pane.cpp` (1,924 → 675 lines) extracts `panes_view.hpp`, `hotkeys_view.hpp`, and `manual_view.hpp`.
- **Wave 4 (CLOSED — `#283` `968e8bb`, `#284` `5d75fef`, `#285` `289f50c`):**
  - **Phase 7A (`#285`, [prompt](../prompts/phase-7a-neovim-editor-split.md)):** `editor/neovim-editor/pane.cpp` (2,340 → 1,038 lines) extracts `handoff.hpp` and `view.hpp`.
  - **Phase 7B (`#283`, [prompt](../prompts/phase-7b-standard-editor-split.md)):** `editor/editor-pane/pane.cpp` (2,213 → 1,045 lines) extracts `common.hpp`, `opening_switch.hpp`, and `transfers.hpp`.
  - **Phase 7C (`#284`, [prompt](../prompts/phase-7c-files-pane-split.md)):** `files/files.cpp` (2,211 → 996 lines) extracts `recipe_authoring.hpp` and `browser_view.hpp`.
- **Wave 5 (CLOSED — `#286` `5491a0d`, `#287` `b6ba800`, `#288` `0c094ab`):**
  - **Phase 8A (`#287`, `b6ba800`, [prompt](../prompts/phase-8a-builder-pane-split.md), [report](../reportbacks/phase-8a-builder-pane-split-RB.md)):** `builder/builder-pane/pane.cpp` (2,788 → 1,789 lines) extracts `output_reader.hpp` (255), `modes.hpp` (331), and `view.hpp` (582).
  - **Phase 8B (`#288`, `0c094ab`, [prompt](../prompts/phase-8b-terminal-pane-split.md), [report](../reportbacks/phase-8b-terminal-pane-split-RB.md)):** `terminal/pane.cpp` (1,489 → 904 lines) extracts `view.hpp` (447) and `history_and_completion.hpp` (264).
  - **Phase 8C (`#286`, `5491a0d`, [prompt](../prompts/phase-8c-workshop-keymap-and-setup-split.md), [report](../reportbacks/phase-8c-workshop-keymap-and-setup-split-RB.md)):** `workshop/keymap.hpp` (1,683 → 724 lines) extracts `gesture_grammar.hpp` (358) and `keymap_join.hpp` (664); `workshop/setup.hpp` (1,561 → 813 lines) extracts `setup_reconcile.hpp` (519) and `layout_shelf.hpp` (286).
  - **CI Test Order (`#289`, `ab78b10`, [prompt](../prompts/test-order-longest-first.md), [report](../reportbacks/test-order-longest-first-RB.md)):** Explicit `COST` properties on the 37 longest CTest entries in `tests/CMakeLists.txt` (verified against `tests/test_population.txt`) so `workshop_panes`, `neovim_journey`, `workshop_desk`, and `story_journey` start immediately on fresh parallel runners.

**Wave 6 — Meaningful Abstractions Arc, Part 1 (Phases 9A–9C, CLOSED 2026-10-17 — `#290` `7f32082`, `#291` `f0b7b34`, `#292` `8daa8af`):**
- **Phase 9A (`#291`, `f0b7b34`, [prompt](../prompts/phase-9a-control-strip-and-list-rows.md), [report](../reportbacks/phase-9a-control-strip-and-list-rows-RB.md)):** `component/control_strip.hpp` (`kMaxStripRows`, `strip_budget`, typed `pack_controls`, `strip_rows_for`), `component/list_window.hpp` (`earlier_marker`, `more_marker`, `take_wheel_notches`), and `workshop/pane_facets.hpp` (`PaneRowsFacet::strip_rows`, `push_controls`, `push_window`) adopted across `files/` (−76 lines) and `builder/builder-pane/` (−59 lines).
- **Phase 9B (`#292`, `8daa8af`, [prompt](../prompts/phase-9b-composer-and-powers-facets.md), [report](../reportbacks/phase-9b-composer-and-powers-facets-RB.md)):** Value-door bridge (`zengine::ValueDoor`, `zengine::RawValueDoor`, `ZENGINE_VALUE_DOOR`) in `activation/activation.hpp` letting hand-built schemas stand in `loom::Accept<...>` on `loom::WeaveBase` and `zengine::With`; `ComposerWeave` (`composer/composer.cpp` 1,088 → 905 lines, −183) and `PowersDoor` (`workshop/powers_door.hpp`, class body 67 → 38 lines) migrated off raw `loom::Weave` onto `zengine::With`.
- **Phase 9C (`#290`, `7f32082`, [prompt](../prompts/phase-9c-editor-office-seam.md), [report](../reportbacks/phase-9c-editor-office-seam-RB.md)):** Shared header-only `editor/office_seam.hpp` (`namespace zengine::editor_office`, 518 lines) unifying the office seam shared by `editor/editor-pane/` and `editor/neovim-editor/` (`Relay`, `Holding`, `Take`, `Pickup`, `LocateOf<Snapshot>`, relayed open, hold counter, value-carry permission/settle, dropped-location open, and material insertion prose), shrinking the two Editor weave trees by 540 lines (7,930 → 7,390).

**Wave 7 — Meaningful Abstractions Arc, Part 2 (Phases 10A–10C, CLOSED 2026-10-17 — `#293` `a4ff004`, `#294` `ebadfcf`, `#295` `3153b5d`):**
- **Phase 10A (`#294`, `ebadfcf`, [prompt](../prompts/phase-10a-multi-pane-seats-and-windows.md)):** `workshop/pane_seat.hpp` (`PaneCanvasSeat` owning per-seat room, rows, canvas, and `show` / `strip_rows` / `push_controls` / `push_window`; `MultiPaneFacet` routing `PaneProviderReady`, `PaneRoomChanged`, and `PaneControlPressed` by `pane_id`) adopted across all four multi-pane weaves (`DesktopWeave`, `IntrospectionWeave`, `InfoWeave`, `EditorWeave`), plus `component::earlier_marker` / `more_marker` / `take_wheel_notches` adopted across `Desktop`, `Introspection`, `Info`, and `Inventory`.
- **Phase 10B (`#295`, `3153b5d`, [prompt](../prompts/phase-10b-host-managers-and-presenters.md)):** `flow_host::Manager` (`flow/host_manager.cpp`) and `view::Manager` (`view/manager.hpp` / `view/manager.cpp`) migrated off raw `loom::Weave` onto `zengine::With<manual::ManualFacet<...>>::Weave` via `ZENGINE_VALUE_DOOR`; shared menu-presenter seam helpers (`menu_presenter_offer`, `presenter_manual_answer`, `claim_menu_room`, `release_menu_room`, `publish_menu_picture`, `choose_menu_row`) extracted in `workshop/presenter_vocabulary.hpp` and adopted across `MenuPresenter` and `NumberedPresenter`.
- **Phase 10C (`#293`, `a4ff004`, [prompt](../prompts/phase-10c-one-action-path.md)):** `PaneActionFacet`, `PaneMenuFacet`, and `PaneRowsFacet::spend_notice` in `workshop/pane_facets.hpp` adopted across all eight action-bearing single-pane weaves (`Files`, `Terminal`, `Builder`, `Inventory`, `Powers`, `Flow`, `ViewBuilder`, `Demo`), and `graphics::ActionFacet` in `graphics/drawing.hpp` adopted across `SnakeWorld` and `OperatorWeave`, giving pane actions and graphics window actions one `on_action(id, mail)` owner signature.

**Wave 8 — BL-WORK-37 Stages 2 & 3 (CLOSED 2026-10-17 — `#296` `bf3981e`, `#297` `7457af1`, `#298` `f75cc13`, `#299` `aad758c`):**
- **Stage 2 (`#296`, `bf3981e`, [prompt](../prompts/graphics-stage-2-panes-and-actions.md), [report](../reportbacks/graphics-stage-2-panes-and-actions-RB.md)):** `PaneDrawingFacet` (`workshop/pane_facets.hpp`) and `drawn_rows` (`workshop/pane_drawing.hpp`), plus `Attention` (`attention/pane.cpp`) and `Connections` (`external-host/connections-pane/pane.cpp`) rebuilt on `graphics/`.
- **Stage 3A (`#297`, `7457af1`, [prompt](../prompts/graphics-stage-3a-single-panes.md), [report](../reportbacks/graphics-stage-3a-single-panes-RB.md)):** Single-pane suite (`Demo Control`, `Terminal`, `Builder`, `Files`, `Composer`) on `graphics/` via `PaneDrawingFacet` and `PaneRowsFacet` (`rows_sketch` + `RowPress{.window = true}`).
- **Stage 3B (`#298`, `f75cc13`, [prompt](../prompts/graphics-stage-3b-multi-panes.md), [report](../reportbacks/graphics-stage-3b-multi-panes-RB.md)):** Multi-pane seat suite (`Desktop` — `launcher`, `hotkeys`, `manual`; `Introspection` — `loaded`, `arrangement`, `powers`; `Info` — `info`..`info.4`; `Inventory` — `inventory`..`inventory.N`) on `graphics/` via `PaneCanvasSeat` and `MultiPaneFacet`.
- **Stage 3C (`#299`, `aad758c`, [prompt](../prompts/graphics-stage-3c-data-ui-presenter.md), [report](../reportbacks/graphics-stage-3c-data-ui-presenter-RB.md)):** Data-as-UI (`view::View` + `view::Host` in `view/view.hpp` and `view/host.hpp`) on `graphics/` via `view::sketch`, plus `view::Presenter` (`Host::pair(name, presenter)`).

**Wave 9 — BL-WORK-37 Stage 4: Remaining Authoring/Editor Panes & Seam Unification (CLOSED 2026-10-17 — `#300` `e43c45d`, `#301` `99a08ea`, `#302` `91b9b21`):**
- **Stage 4A (`#302`, `91b9b21`, [prompt](../prompts/graphics-stage-4a-canvas-panes.md), [report](../reportbacks/graphics-stage-4a-canvas-panes-RB.md)):** Canvas-picture authoring panes (`FlowPane` in `flow/flow-pane/` and `ViewBuilderPane` in `view/view-builder/`) on `graphics/` via shared `workshop::canvas_sketch` (`workshop/pane_canvas_drawing.hpp`).
- **Stage 4B (`#301`, `99a08ea`, [prompt](../prompts/graphics-stage-4b-editors.md), [report](../reportbacks/graphics-stage-4b-editors-RB.md)):** Both Editors (`EditorPaneWeave` in `editor/editor-pane/` and `NeovimEditorWeave` in `editor/neovim-editor/`) on `graphics/` via a shared `editor_office::EditorWindow` seam in `editor/office_seam.hpp` (drawing caret and selection over rows).
- **Stage 4C (`#300`, `e43c45d`, [prompt](../prompts/graphics-stage-4c-projection-and-standin-unification.md), [report](../reportbacks/graphics-stage-4c-projection-and-standin-unification-RB.md)):** Unifying `rows_drawing` and `WindowDrawing` (two-state `DrawnRefused` recovery) in `workshop/pane_drawing.hpp` across `PaneCanvasSeat`, `PaneRowsFacet`, and `PaneDrawingFacet`, consolidating `tests/window_stand_in.hpp` into `tests/pane_window.hpp`, and teaching `external-host/tools/workshop/act.py` (`aimed`) to wait through `"no settled picture"`.

**Wave 10 — BL-WORK-37 Stage 5: Workshop Window Arranger, Unified `WindowDrawing` + Caret, and `Hand` Unsettled Retry (CLOSED 2026-10-17 — `#303` `44a8bc2`, `#304` `a9d5c99`, `#305` `2ab3de0`):**
- **Stage 5A (`#304`, `a9d5c99`, [prompt](../prompts/graphics-stage-5a-workshop-arranger.md), [report](../reportbacks/graphics-stage-5a-workshop-arranger-RB.md)):** Workshop as `zengine.graphics` arranger (`pane_window_area`, `AreaPlaced`, `SkinOffered`, `SkinChosen` with no-refusal bus guard when `zengine.graphics` is absent) and desk chrome drawer (`workshop_window_drawing` in `workshop/screen_compose.cpp` projecting the same planes `paint` composes — `Layouts`, external pane borders/headers with `*`/`?` actions and waiting/refused fallback, arrangement rings, menus, and bottom band — onto `"zengine.workshop"` via `WindowDrawing`).
- **Stage 5B (`#303`, `44a8bc2`, [prompt](../prompts/graphics-stage-5b-window-drawing-and-caret.md), [report](../reportbacks/graphics-stage-5b-window-drawing-and-caret-RB.md)):** Moving caret bar (`"caret"`) and selection highlight runs (`"sel<r>.<run>"`) into `ws::rows_drawing` (`workshop/pane_drawing.hpp`), passing `caret_` from `PaneRowsFacet::send` so `Terminal` and `Composer` draw their caret and selection in a graphics window, and folding `EditorWindow` (`editor/office_seam.hpp`, 720 → 595 lines), `FlowPane` (`flow/flow-pane/pane.cpp`), and `ViewBuilderPane` (`view/view-builder/pane.cpp`) onto `ws::WindowDrawing`.
- **Stage 5C (`#305`, `2ab3de0`, [prompt](../prompts/graphics-stage-5c-point-reader-unsettled-and-story-journey.md), [report](../reportbacks/graphics-stage-5c-point-reader-unsettled-and-story-journey-RB.md)):** Teaching `Hand.row`, `Hand.pointed`, and `Hand.lattice_point` (`external-host/tools/workshop/hand.py` via shared `Hand.aimed` and `no_settled_picture`, covering both canvas `"no settled picture"` and text `"no settled text picture"`) to wait through unsettled pictures alongside `"picture moved"`, and fixing the `tests/session/story_journey.py` U2 (`unresolved_runs`) startup status race on slow Windows runners.

**Wave 11 — BL-WORK-37 Stage 6: Live Window Extent & Text Input, Seat Caret & `view::View` on `WindowDrawing`, and `builder`/`monitor` Aimed Retry (CLOSED 2026-10-18 — `#306` `1d11677`, `#307` `7b1ab14`, `#308` `238bb70`):**
- **Stage 6A (`#308`, `238bb70`, [prompt](../prompts/graphics-stage-6a-window-extent-text-and-overlays.md), [report](../reportbacks/graphics-stage-6a-window-extent-text-and-overlays-RB.md)):** Staging `zengine-graphics`, `zengine-window-terminal`, `zengine-paint-classic`, and `zengine-paint-block` in `workshop/CMakeLists.txt` and `cmake/ZengineInstall.cmake` (verified by `tests/package/CMakeLists.txt`); emitting `TextEntered` from `graphics::window::WindowBase` (`graphics/window/window.hpp`), forwarding `TextEntered` in `WindowT::on_pump` via `to_keys` to areas with `keys == true`, and publishing `WindowOffered` as `office()` in `WindowT::offer`; teaching `WorkshopWeave` (`workshop/weave_handlers.cpp`) to accept `WindowOffered` for session startup and cell-grid resize when no skin is mounted, keeping `keys = true` on `kWorkshopProvider` and `keys = false` on pane areas in `arrange_graphics`, and projecting the `[value]` drag pill and guest `guide_layer` overlay in `workshop_window_drawing` (`workshop/screen_compose.cpp`) with `kWorkshopProvider` raised in front while an overlay stands.
- **Stage 6B (`#307`, `7b1ab14`, [prompt](../prompts/graphics-stage-6b-seat-caret-and-view-window-drawing.md), [report](../reportbacks/graphics-stage-6b-seat-caret-and-view-window-drawing-RB.md)):** Teaching `PaneCanvasSeat` (`workshop/pane_seat.hpp`) to retain `said_caret_` in `say` and pass it to `ws::rows_drawing` in `redraw` so multi-pane seats draw their caret and selection in a graphics window; teaching `view::sketch` (`view/view.hpp`) to draw the `"caret"` line node for a focused number field; and replacing `view::View`'s hand-rolled `graphics::Canvas` + `whole_next_`/`last_whole_` state with `ws::WindowDrawing`.
- **Stage 6C (`#306`, `1d11677`, [prompt](../prompts/graphics-stage-6c-builder-monitor-aimed.md), [report](../reportbacks/graphics-stage-6c-builder-monitor-aimed-RB.md)):** Routing `builder.calm`, `builder.keys_into` (`external-host/tools/workshop/builder.py`), and `Monitor.press_at` (`external-host/tools/workshop/monitor.py`) through `Hand.aimed` so `"no settled picture"` and `"no settled text picture"` are waited through alongside `"picture moved"`.

**Wave 12 — BL-WORK-37 Stage 7 Wrap-Up: Shipped Window Load Plan & SDK Install, Live Terminal Resize, and `builder.choose`/`Monitor.rows`/`act.aimed` Unification (CLOSED 2026-10-18 — `#309` `7ed868c`, `#310` `5918a4b`, `#311` `5926167`):**
- **Stage 7A (`#311`, `5926167`, [prompt](../prompts/graphics-stage-7a-window-load-plan-and-sdk-install.md), [report](../reportbacks/graphics-stage-7a-window-load-plan-and-sdk-install-RB.md)):** Shipped `workshop/window-load-plan.json` (`zengine-graphics` + `zengine-window-terminal`, `kWindowLoadPlanName`, staged in `workshop/CMakeLists.txt`, documented in `workshop/README.md`, `workshop/docs/load-plans.md`, and `workshop/docs/load-plan.md`, and proven in `tests/test_workshop_load.cpp`), plus exporting `zengine::graphics` (`zengine-graphics-vocabulary` and the 20 public `graphics/` and `graphics/elements/` headers) in `graphics/CMakeLists.txt`, `cmake/ZengineInstall.cmake`, `agents/packaging.md`, `tests/package/CMakeLists.txt`, and `tests/package/public_surface.cpp`.
- **Stage 7B (`#310`, `5918a4b`, [prompt](../prompts/graphics-stage-7b-window-terminal-resize.md), [report](../reportbacks/graphics-stage-7b-window-terminal-resize-RB.md)):** Live terminal resize detection on `zengine.window.pump` in `zengine.window.terminal` (`graphics/window/window.hpp` and `graphics/docs/zengine.window.terminal.md`), marking the resized window dirty and re-publishing `WindowOffered` with the new `cols` and `rows` under the same `epoch`, proven in `tests/test_graphics.cpp`.
- **Stage 7C (`#309`, `7ed868c`, [prompt](../prompts/graphics-stage-7c-builder-choose-monitor-rows-and-act-aimed.md), [report](../reportbacks/graphics-stage-7c-builder-choose-monitor-rows-and-act-aimed-RB.md)):** Routing `builder.choose` (`external-host/tools/workshop/builder.py`) through `pressing(ctx, hand)` and `Monitor.rows` (`external-host/tools/workshop/monitor.py`) through `DeskStamps` settled-picture waiting (both with an open `Hand` and as a watching-only `_Asker`), plus deduplicating `act.aimed` (`external-host/tools/workshop/act.py`) onto `hand.aimed`, proven in `tests/session/workshop_tool_checks.py`.

**Wave 13 — BL-WORK-37 Stage 7 Follow-Up Polish: Settled `stdout` Banner Suppression Over Terminal Media & Guest Input Sessions Under `window-load-plan.json` (CLOSED 2026-10-18 — `#312` `bd8e31c`, `#313` `5b180eb`):**
- **Stage 7D (`#312`, `bd8e31c`, [prompt](../prompts/graphics-stage-7d-settled-banner-and-window-plan.md), [report](../reportbacks/graphics-stage-7d-settled-banner-and-window-plan-RB.md)):** Suppressing the settled `stdout` arrangement banner (`load::medium_holds_terminal` in `workshop/load_execute.hpp` and `workshop/workshop.cpp`) when a terminal medium holds a measured terminal so `loaded:` lines do not scroll or smear `zengine-window-terminal`, adding `zengine-input` (`zengine.input`) to `workshop/window-load-plan.json` for guest input sessions, and closing the doc gaps in `workshop/docs/load-plans.md`, `workshop/docs/load-plan.md`, `workshop/docs/getting-started.md`, and `cheat_sheet.md`.
- **Stage 7E (`#313`, `5b180eb`, [prompt](../prompts/graphics-stage-7e-window-terminal-input-yield.md), [report](../reportbacks/graphics-stage-7e-window-terminal-input-yield-RB.md)):** Process-scoped PID+refcount terminal-input claim (`claim_window_terminal_input`, `release_window_terminal_input`, `window_holds_terminal_input`, `terminal_reader_may_use_terminal` in `input/terminal_reader.hpp` and `ProcessTerminal` in `graphics/window/window.cpp`) so `zengine-input` yields `stdin` when `zengine-window-terminal` holds the terminal while still serving guest input sessions, plus closing the `WindowOffered` resize doc gap in `graphics/docs/zengine.graphics.md`.

**Wave 14 — BL-WORK-36 Stage 2A, Keyboard Focus, & `surface/` Retirement Stage S1 (`zengine-window-sdl` + Severing `graphics/` from `surface/`) (CLOSED 2026-10-18 — `#314` `93376b1`, `#315` `ef07fb1`, `#316` `681abe6`):**
- **Lane 14A (`#315`, `ef07fb1`, [prompt](../prompts/settings-stage-2-doors.md), [report](../reportbacks/settings-stage-2-doors-RB.md)):** `v2::PaneSettingRow` (`tags`, `pinned`, `summary`), `v2::PaneSettingsDeclared`, `v2::PaneSettings` (`revision`), `workshop/settings_seam_vocabulary.hpp` (`PaneSettingsRequested`, `PaneSettingsShown`, `PaneSettingCommitRequested`, `PaneSettingActed`, `PaneSettingUnused`, `SettingLockShown`), `P-WORK-61` incarnation-based reload settings reset in `accept_pane_offer`, `"settings"` guest power in `workshop-guests.json`, `act.py settings` CLI step, and `Terminal` upgraded to `v2::PaneSettingsDeclared` & `v2::PaneSettings` (`legend`, `wheel-rows`, `prompt`).
- **Lane 14B (`#314`, `93376b1`, [prompt](../prompts/keyboard-focus.md), [report](../reportbacks/keyboard-focus-RB.md)):** Eight remappable `focus.*` actions in `workshop/keymap.hpp` (`focus.leave` `ctrl+q` in `KeyContext::kGlobal`, and `focus.next` `tab`, `focus.previous` `shift+tab`, `focus.left`/`right`/`up`/`down` arrows, and `focus.enter` `return` in `KeyContext::kCommand`), pure `selectable_panes`, `cycle_pane`, and `spatial_neighbour` helpers in `workshop/screen.hpp` / `workshop/screen_arrange.cpp`, medium-aware command-mode selection highlight in `workshop/screen_compose.cpp`, and keyboard-only pane entry (`WL-FOCUS-04`) and trap-free exit closing WCAG 2.1.1 G1 and 2.1.2 G2.
- **Lane 14C (`#316`, `681abe6`, [prompt](../prompts/surface-retire-s1-window-sdl.md), [report](../reportbacks/surface-retire-s1-window-sdl-RB.md)):** Severs `graphics/` completely from `surface/` (moving canonical `role` constants into `graphics/role.hpp` and terminal I/O + size into `graphics/window/terminal_io.hpp`, removing `zengine-surface-vocabulary` from `zengine-graphics-vocabulary` with `VM-WALL-11` tripwire), unifies `Window<Medium>` over `TerminalMedium` and `LightMedium`, ships the pixel/light painter (`graphics/light_paint.hpp`) and light skins (`zengine-paint-day` and `zengine-paint-night`) over `ZenginePainterV1` with zero new `ZEN_SHAPE`s, and ships `zengine-window-sdl` (`zengine.window.sdl` in `graphics/window/window_sdl.hpp` and `graphics/window/window_sdl.cpp` with `graphics/docs/zengine.window.sdl.md`).

**Wave 15 — BL-WORK-36 Stage 2B (Tags, Pins & Office Settings), Stage 2C (Pane Setting Promotions), & `surface/` Retirement Stages S2 & S3A (CLOSED 2026-10-18 — `#317` `8581d35`, `#318` `d1f6adf`, `#319` `6e5a130`, `#320` `4f96d69`):**
- **Lane 15A (`#319`, `6e5a130`, [prompt](../prompts/settings-stage-2b-tags-and-pins.md), [follow-up](../prompts/settings-stage-2b-drop-info.md), [report](../reportbacks/settings-stage-2b-tags-and-pins-RB.md)):** `WorkshopPrefs` v3 (`offices`, `pins`, `locks` with corrupt-file and two-hands byte guard), `OfficeSettings*` and `PaneSettingPin*` doors in `workshop/settings_seam_vocabulary.hpp` / `workshop/weave_settings.cpp`, Workshop's 5 office settings (`workshop.pane-titles`, `workshop.band-keys`, `workshop.hotkeys-keys`, `workshop.pinned-scope`, `workshop.focus.ring`), and pure `component/tab_strip.hpp` (with `Info` untouched so settings editing lives in the Gear Overlay and Settings Studio).
- **Lane 15B (`#318`, `d1f6adf`, [prompt](../prompts/settings-stage-2c-pane-promotions.md), [report](../reportbacks/settings-stage-2c-pane-promotions-RB.md)):** Promotes the scraped per-pane constants across seven pane weaves (`Desktop/Hotkeys` `help`; `Editor` `tab-width`, `status`, `wheel-lines`, `undo-depth`; `Neovim` `profile`, `status`; `Files` `wheel-rows`, `listed-entries`; `Attention` `detail`; `Introspection/Powers` `view-columns`, `composite-columns`, `gap`; `View Builder` `snap-reach`, `new-width`, `new-height`) onto `v2::PaneSettingsDeclared`, `v2::PaneSettings`, and `PaneSettingUnused` via shared `workshop/pane_settings_taken.hpp`.
- **Lane 15C (`#317`, `8581d35`, [prompt](../prompts/surface-retire-s2-window-input-and-close.md), [report](../reportbacks/surface-retire-s2-window-input-and-close-RB.md)):** Completes `KeyReleased`, `PointerButton` (buttons 1/2/3 press and release), `PointerMoved`, `PointerWheel`, and close-request tracking across `Window<Medium>` (`graphics/window/window.hpp`), `zengine-window-sdl` (`graphics/window/window_sdl.cpp` via `input/translate_sdl_core.hpp`), and `zengine-window-terminal`, plus process-scoped `ZENGINE_WINDOW_SDL_INPUT_PID` queue yield in `input/window_claim.hpp` and `input/input_sdl.cpp` with zero new `ZEN_SHAPE`s.
- **Stage S3A (`#320`, `4f96d69`, [prompt](../prompts/surface-retire-s3a-window-medium-parity.md), [report](../reportbacks/surface-retire-s3a-window-medium-parity-RB.md)):** Desktop window placement & display clamping (`WindowPlacementValue`, `DesktopSpan`, `DesktopPoint`, `placement_within`, `centred_within`, `grown_within`, `placement()`, `place()`), clipboard copy & paste (`terminal_base64`, `terminal_clipboard_sequence` OSC 52, `SDL_SetClipboardText`, `SDL_HasClipboardText`/`SDL_GetClipboardText`, `clipboard_copy()`, `clipboard_text()`), and presented picture capture (`CapturedWindowPicture`, `text/cells` on `TerminalMedium`, 24-bit bottom-up BMP `bmp_of_bgr24` via `SDL_RenderReadPixels` + `SDL_ConvertSurface` on `LightMedium` / `ProcessSdlBackend`).

**Wave 16 — `surface/` Retirement Stage S3B (Window Bus Doors) & BL-WORK-36 Stage 2D (Workshop Setting Promotions) (CLOSED 2026-10-19 — `#321` `a7b7aa1`, `#322` `98672c4`):**
- **Lane 16A (`#322`, `98672c4`, [prompt](../prompts/surface-retire-s3b-window-bus-doors.md), [report](../reportbacks/surface-retire-s3b-window-bus-doors-RB.md)):** Moves `ClipboardCopy`, `ClipboardTextRequested`, `ClipboardText`, `SurfaceCloseRequested`, `SurfacePlacement`, `SurfacePlacementRemembered`, `SurfaceCaptureRequested`, `SurfaceCaptured`, `SurfaceCaptureChunkRequested`, `SurfaceCaptureChunk`, `PumpSurface`, `kCaptureChunkBytes`, and `kMaxCaptureBytes` into `graphics/vocabulary.hpp` (`namespace zengine::graphics`) with `using` aliases in `surface/vocabulary.hpp` (zero `ZEN_SHAPE` changes in `tests/shapes.txt`), and wires all of those bus doors into `Window<Medium>` (`graphics/window/window.hpp`) for both `zengine.window.terminal` and `zengine.window.sdl`.
- **Lane 16B (`#321`, `a7b7aa1`, [prompt](../prompts/settings-stage-2d-workshop-promotions.md), [report](../reportbacks/settings-stage-2d-workshop-promotions-RB.md)):** Promotes the 6 Workshop settings in `workshop_office_rows()` (`workshop/prefs_persist.hpp`): `workshop.skin` (`"classic"` or `"block"`, both Workshop-wide in `prefs_` and per-pane on `SetupPane::settings` for `arrange_graphics`, with `row_setting_absence` keeping `"classic"` explicitly on a pane row so a pane can wear `"classic"` under a Workshop-wide `"block"`), `workshop.completion-order` (`"declared"` or `"required-first"`, closing the Terminal completion line of `P-LOOM-10` in `terminal/complete.hpp` & `terminal/door.hpp`), `workshop.arrange-step` (`2..16` cells), `workshop.snap-reach` (`6..11` px), `workshop.side-columns` (`16..64` cells), and `workshop.stack-rows` (`5..40` rows, narrowing `P-WORK-01`).

**Wave 17 — `surface/` Retirement Stage S4A (Window Routing & SDL Window Plan) & BL-WORK-36 Stage 3A (Theme Files, Composite DAG Resolution & Settings Vocabulary) (CLOSED 2026-10-19 — `#323` `5c06cfd`, `#324` `6ebc035`):**
- **Lane 17A (`#324`, `6ebc035`, [prompt](../prompts/surface-retire-s4a-window-routing-and-sdl-plan.md), [report](../reportbacks/surface-retire-s4a-window-routing-and-sdl-plan-RB.md)):** Accepts `zengine.window.sdl` in `WorkshopWeave::on(const graphics::WindowOffered&)` and places areas on `window_name_`; offers all four painter skins (`"classic"`, `"block"`, `"day"`, `"night"`) and widens `workshop.skin` choices; ships `workshop/sdl-window-load-plan.json` (loading `zengine-window-sdl` + `zengine-input-sdl`); routes `ClipboardTextRequested` and `SurfacePlacementRemembered` in Workshop (`medium_office()`) and 5 pasting panes (`Editor`, `Neovim`, `Terminal`, `Composer`, `Info` via `WindowDrawing::clipboard_office()`) to the active window or Skin; and widens `kPowerCapture` and `external-host/tools/workshop/` (`workshop_steps.py`, `inspect_capture.py`) to capture from `zengine.window.sdl` and `zengine.window.terminal` as well as `zengine.skin`.
- **Lane 17B (`#323`, `5c06cfd`, [prompt](../prompts/settings-stage-3a-theme-files-and-resolution.md), [report](../reportbacks/settings-stage-3a-theme-files-and-resolution-RB.md)):** Establishes `settings/` (`settings/theme_persist.hpp`, `settings/vocabulary.hpp`, `zengine-settings-vocabulary`): `zengine-theme` v1 durable format (`ThemeSetting`, `ThemeKey`, `ThemeFile`) with envelope-first admission, entry/target validation, canonical sorting, atomic `save_file` with two-hands `expected_bytes` + `replace` guard, `list_themes` (surfacing broken files by their refusal), deterministic 64-bit FNV-1a `theme_fingerprint`, composite DAG `resolve_theme` with cycle/depth/visited/entry bounds and `"later wins"` `from_theme` provenance, and all 20 `zengine.settings` v1 shapes (`settings_themes` suite, 18/18 cases, 26/26 mutants).

**Wave 18 — `surface/` Retirement Stage S4B (Remaining Paste Panes & Workshop Probe Capture Fallback) & BL-WORK-36 Stage 3B (Setting Locks & Cross-Layout Doors) (CLOSED 2026-10-19 -- `#325` `a50d6be`, `#326` `7cc0ec1`):**
- **Lane 18A ([prompt](../prompts/surface-retire-s4b-remaining-paste-panes-and-probe.md)):** Routes the remaining 4 clipboard-pasting panes (`BuilderPaneWeave::begin_paste` in `builder/builder-pane/pane.cpp`, `FilesWeave::begin_paste` in `files/files.cpp`, `PowersSeat::begin_clipboard_paste` in `introspection/seats.hpp`, and `HotkeysView::begin_paste`/`ask_refused` in `workshop/desktop-pane/hotkeys_view.hpp`) through `room().clipboard_office()` / `keys_canvas_.clipboard_office()` instead of hardcoded `surface::kSkinRole`, and teaches `examples/workshop-probe/probe.hpp` (`Step::Capture`) to try `zengine.skin`, `zengine.window.sdl`, and `zengine.window.terminal` in order on `kOutcomeDispatchRefused` so the probe captures cleanly under both legacy Skin and window plans.
- **Lane 18B ([prompt](../prompts/settings-stage-3b-locks-and-cross-layout-doors.md)):** Adds the 13 cross-layout and lock `ZEN_SHAPE`s in `workshop/settings_seam_vocabulary.hpp` (`PaneSettingLockRequested`, `PaneSettingLockActed`, `LayoutSettingsRequested`, `LayoutTheme`, `LayoutPaneSettings`, `LayoutSettings`, `DeclaredSettings`, `LayoutSettingsShown`, `SettingWrite`, `LayoutThemeWrite`, `SettingsWriteRequested`, `SettingWriteResult`, `SettingsWritten`); persists per-layout locks (`<office>/<pane>@<layout_name>` in `prefs_.locks`) and per-layout `LayoutTheme` baselines (`@<layout_name>` in `prefs_.offices`) in `WorkshopPrefs` v3 without bumping `WorkshopSetup` v5 or `WorkshopSession` v8; enforces layout and everywhere locks (and weaver-only unlock) across `PaneSettingCommitRequested`, `PaneCommitRequested`, `PaneSettingsShown`, and `SettingsWriteRequested`; implements `LayoutSettingsRequested` and whole-batch-validated `SettingsWriteRequested`; and widens Terminal + `"settings"` guest power.
- **Reviewed by Vision and merged (2026-10-19):** `#325` (18A) and `#326` (18B). The founder took
  18B's storage as a stopgap (2026-10-19): a layout's locks, pins and baseline stay in Workshop's
  settings file under the layout's name until the desk split moves them into the layout.

**The goal** (the founder, 2026-10-14): Zen legible, and good to use as a human weaver.
Documentation first; then the split, which should simplify the documentation, not expand it; then
the UX improvements, as one batch of `enhancement` issues; complete stories last, on a well-formed
architecture. No timeline: a day or two for the manuals, he says, with minor work beside them. His
notes are kept by item, not as a file: their themes in section 1b, their UX items as issue drafts in
[ux-batch.md](ux-batch.md).

**The alpha release** (the founder, 2026-10-21): a soft release at the end of the week. In order:
- the package on GitHub, one version held at a time: a nightly job packages when `main` has moved
  and tags the next `v0.1.N`, `v0.1.0` first, the version read from the tag rather than written in
  code (BL-ADOPT-06's stages cut to that). The week's most important deliverable (the founder,
  2026-10-22), so researched now rather than after G2, beside both lanes
  ([prompt](../prompts/alpha-package-research.md)): what a stranger downloads per platform, the
  nightly job, a probe package walked, and stages the issue lane builds after the quick setup.
  Reported ([report](../reportbacks/alpha-package-research-RB.md)) and reviewed by Vision
  (2026-10-23, 11 of 11 checks): `main` makes the package today, about 160 lines of install rules;
  Workshop started from the extracted folder with nothing installed, and an exported app ran from
  it and outlived Workshop; stages N0 to N10, the alpha's share N0 to N4 and N6. Decisions A to F
  asked, recommended as the report has them, with B's app finding its host through a line the
  launcher writes in the project, and the images stripped (Vision's scan found MSYS2's own build
  paths in the static runtime's debug sections, none of this machine's). Known for the alpha: an
  exported app asks five consent lines at its first start; the Builder refuses from a package;
  the demos stay out (N7). The founder (2026-10-23): A to F and Vision's two additions, taken;
  D overturns the 10-10 decision 8 (only he pushing `v*` tags), which he had taken with the other
  fourteen at once and does not stand by: his merge is now the package's gate. The issue lane's
  continuation ([prompt](../prompts/issue-lane-alpha-package.md)): N1 to N4, N6 beside N2, N5
  if the week has room; his three settings before N4 merges. Overnight
  ([report](../reportbacks/issue-lane-alpha-package-RB.md)), reviewed by Vision (2026-10-23,
  14 of 14 checks), each green at its first attempt and clean in sequence: #375 (the flake: a
  story root waits for Workshop's plan at rest before its first key, the race, not a longer
  wait), #377 (N1: `ZENGINE_PACKAGE`, the project in `%USERPROFILE%\Zengine`, the app's host
  line, `--version`, stripped and started so) and #379 (N2: the four judges, self-testing). A
  delete waiting on permission held the lane for hours: the constitution's rule 12 (the
  founder, 2026-10-23), deletes only at a session's end. The founder merged #375, #377 and #379
  (`main` `75e56193`). G2's stage 6, #380 (221 files), rebased and green, ASan + UBSan 54:07
  (`main`'s own ran 20.6 to 61.6 minutes that day), reviewed by Vision (2026-10-23, 12 of 12
  checks, the press path read, not all 221 files): ready once its body's kind count says 86 and
  90; two decisions asked, Vision recommending (a) for both as G2's next pull request before
  stage 7 -- a drawing's number on each press, and the window telling the arranger a drawing
  settled -- restoring the stale-press guards the stage dropped (the Builder's four, Info
  views' save copy) with the eight expected failures; its doc gap, the demo readiness note's
  `KeyError`, a line for the demo tools. N6, the front door, #384, green and ready (9 of 9
  checks); N3, #382, building. The founder merged all three (`main` `ccd7f5d5`) and took both
  decisions as (a), each with a condition: a press refused only where an entirely new element
  stands under the hand, never for a picture merely updated; the notice barring no threading
  later. G2's follow-up ([prompt](../prompts/graphics-only-g2-s6b-press-and-notice.md))
  carries both, with BL-WORK-46's first step. N4, #386, open: the founder's three settings
  before it merges. Then BL-WORK-46's second step in the issue lane once the package's share
  is in;
- code a stranger can read; G2 finished in the main lane, its stages chained on the open parent's
  branch, the issue lane beside it, and G2 no gate for the rest;
- the first five minutes researched beside both lanes, building nothing: a first-run setup, the
  story as a checklist, a command palette, a wire let go on empty space
  ([prompt](../prompts/first-five-minutes-research.md), 2026-10-22). Reported
  ([report](../reportbacks/first-five-minutes-research-RB.md)) and reviewed by Vision
  (2026-10-22, 6 of 6 checks): `zengine-palette` and `zengine-first-run`, each drawing in an area of
  its own; Workshop's one new door, `PaletteRunRequested`, running an entry by its key's path for
  the hand that chose it; Flow's wire let go asking `takes`; ten stages, W1, P1, P2, F0, F1, V1,
  L1, P3, F2, T1. The founder (2026-10-22): the palette grows toward JetBrains' search -- files,
  message formats and the rest, each choice acted on or opened in the window that performs it --
  this design a fine start; its shapes named for the command, never the palette
  (`CommandRunRequested`, `OpenFileRequested`, more kinds later), so any presenter may send them;
  no Shift+Space: double Shift in the OS window and Ctrl+Space where a terminal can say it (T1 for
  POSIX), the same action; one written form, `ctrl+p`, the band's default, the quick setup asking
  no scheme; a helper spelling keys for a global setting after the full story. Kept: Shift's
  release (P2) and the editor remembered (F0). His idea: a small launcher, Loom or not, that
  opens the right Loom environment before Workshop -- for the package's research, not L1, which
  is A3's in-Workshop launcher answering what it can start.
  Its stages are the issue lane's, beside G2's stage 6
  ([continuation](../prompts/issue-lane-first-five-minutes.md), 2026-10-22), each an issue and a
  pull request, a report section each as its run turns green: W1; T1, a POSIX terminal's byte 0
  read as Ctrl+Space (no row binds it today; #341's unsaid gap); P1, its door `CommandRunRequested`
  from the palette's office alone, on `ctrl+space`; P2 on P1's branch; the band in full; F0; F1
  on F0's branch, with no scheme block. Not this round: L1, P3, V1, F2.
  Reviewed mid-lane by Vision (2026-10-22, 12 of 13 checks; the failed attempts' logs need admin
  rights): `main`'s runs after #359 and #354 green (ASan 60:09); #353 (`d20a51a1`, the population
  alone changed), #358 (`52c131ce`, stacked, `app_host` 9) and #364 (T1, `df9004d7`) ready, clean
  in that order; #362 (W1, `625ba999`) ready, one population line against #358 for the lane to
  rebase. W1's list draws its right edge just outside the graph's room near the pane's edge (a
  nit). `neovim_journey` failed the sanitizer job's first attempt on #358 and #362 and passed on
  the rerun: a flake that costs a rerun each time.
  All four merged (`2878bd1d`, 2026-10-22). #368 (P1, `f645c9f9`) reviewed by Vision (14 of 14
  checks): the door takes the palette's office alone, under the palette's own row's number,
  spent once, run as that hand down the path its key or press takes; Neovim alone keeps
  `ctrl+space`; ready, its body's "T1" out first. The Windows console's space typed with
  Ctrl+Space is swallowed by `expected_text_of`, but no case types it (the surviving mutant): a
  case for P2's pull request. `neovim_journey` failed `main`'s run after #353 too, the third time.
  #368 merged (`5a32d858`). The lane's report whole
  ([report](../reportbacks/issue-lane-first-five-minutes-RB.md)), reviewed by Vision (2026-10-23,
  13 of 13 checks): #369 (P2 with the console's space case,
  `78e3bbcc`), #370 (the band in full, `02b0087a`) and #371 (F0, `4bd07a83`) ready, clean in any
  order. #373 (F1, `2de525c0`) waits on one change (private): on a weaver's host a guest reaches
  none of the editor office, the Terminal and the Hotkeys pane, yet a guest's press or key on the
  quick setup switched the weaver's editor, confirmed its losses and wrote the settings file; the
  setup becomes the weaver's hand's alone there, as the Terminal is; then its rebase over #368's
  appends in nine files. `neovim_journey`: the story's `ctrl+t` step waits 5 s; read what a failed
  run saw, then raise it, a pull request before N1. Both open the lane's package continuation.
  #369, #370 and #371 merged (`96e08f53`). #373 closed out (`26d224eb`), reviewed by Vision
  (2026-10-23, 8 of 8 checks): rebased with the palette's and the setup's rows side by side; the
  setup the weaver's hand's alone on a weaver's host in `weaver_only_pane`, so its area is placed
  so and a guest's key or press is refused in words, a case red before green on both hosts; its
  run green at the first attempt (ASan 60:07); its body says the rule, not the hole. Ready.
  Its "if the founder cuts them" read Vision's word "cut" below as dropped: G2 stays whole. The
  other researches Vision weighed, for the founder to choose among: the release package refreshed
  (once G2 reaches stage 7); G2's stages 6 and 7 split across both lanes; where the suites' time
  goes (ASan back at 60); Zenscript; the snake demo finalized. Step 7 (C1, L2, C2) and Loom's three
  small follow-ups need prompts, not research;
- the full story, satisfying within the first five minutes: a view made, its inputs wired, its
  logic authored in Flow, its outputs wired back, the view detached into a window of its own,
  Workshop closed and the view still running, Workshop opened and connected to the authored host's
  window (merging it back as a pane a bonus); a first-run screen (control scheme, a Vim checkbox, a
  way to the setups). Walked on `main` by Vision ([handoff](handoffs/alpha-story-walk.md),
  2026-10-21): steps 1 to 4 work today; the view in a window of its own is what is missing.
  The export, its window and the way back researched beside G2, building nothing
  ([prompt](../prompts/app-export-research.md), 2026-10-21); reported
  ([report](../reportbacks/app-export-research-RB.md)) and reviewed by Vision (2026-10-21, 8 of 8
  checks): the app opened by a small Zengine host of its own, `zengine-app`, after Loom installs
  its consent half (L1); a view that hears its own window; steps 5 and 6 are L1, A1 and A2, about
  four days of a lane; step 7 (C1, L2, C2) after the release; the take-back an authored
  hand-over, no Loom change for a view or a flow. The founder took the 14 decisions as
  recommended (2026-10-21): the app host owns the host's setup and its cycle, game-engine
  states for that cycle much later; a closed second window puts its layout back on the shelf,
  a way to restore the window later. L1 is the issue lane's
  ([prompt](../prompts/issue-lane-loom-consent.md)): Loom #58, taken as #59 (`84151bf`),
  reviewed by Vision (2026-10-22, 8 of 8 checks): `loom::host-policy` installed, the command
  moved word for word behind `AuthorityDesk`, its run's 10 jobs green; merged (`02779d7`,
  2026-10-22). Its report leaves A1 the console's seat (about 60 lines over `AuthorityDesk`, as
  the witness's) and where adoption happens when Zengine's plan executor loads; `authority
  pending` lists a refused artifact without the command that answers it (the refusal names it),
  a grammar change only if the founder wants one. The package waits until G2 is done. A1 is the
  issue lane's next ([prompt](../prompts/issue-lane-app-host.md), 2026-10-22): `zengine-app`,
  its console on Loom's store, the app's own weave, a view that hears its window, the probe
  `examples/tally-app/`; it meets G2's stage 4 in `view/view.hpp`. A1 is Zengine #347
  (`a952914e`, fixes #346, [report](../reportbacks/issue-lane-app-host-RB.md)), reviewed by
  Vision (2026-10-22, 12 of 12 checks): its run's 8 jobs green; merged (`4dbffd3a`). A view takes
  its window's keys and text, not its pointer, so a field is focused by Tab, not a click: the
  founder wants it clicked into too (2026-10-22), a small issue once stage 4's pointer shapes
  land. Overnight the lane takes A2, A4, then A3 on A2's branch
  ([continuation](../prompts/issue-lane-app-export-and-start.md), 2026-10-22). Loom, after the
  alpha: an installed `AuthorityDesk` seat (a second host now writes one) and `authority trust`'s
  reply naming a host's baseline. Reviewed by Vision (2026-10-22): #350 (A2) ready; #353 (A4)
  rebases over stage 4, ten graphics files shared; #354 (A3) needs a POSIX start that closes
  Workshop's descriptors (the guest door's socket would outlive Workshop in the app) and the truth
  that a POSIX start has no console (a first start decided from `run.sh`), then its rebase onto
  `main`. Loom, later: the bridge's sockets close on exec (private: a child holds them). Asked in
  A2, the founder (2026-10-22): the plan built from a flow's providers later; the export and the
  start decided with the alpha's package. The morning's lane
  ([continuation](../prompts/issue-lane-app-fixes-and-click.md), 2026-10-22): the ASan limit,
  A3's POSIX fixes, A4's rebase, and a view hearing its window's pointer. Reported
  ([report](../reportbacks/issue-lane-app-fixes-and-click-RB.md)) and reviewed by Vision
  (2026-10-22): #356 merged; #354 (A3, its POSIX start closing all but its three streams and saying
  it has no console), #353 (A4 rebased) and #358 (a view clicked into, fixes #357) green, each
  clean against `main` and after #359, but the three conflict among themselves (the population,
  the app's pages): #359 and #354 first, then #353 and #358 rebased in turn, #353's body losing
  "stage 4's". The build runner's child inherits the bridge's sockets too (private, with Loom's
  close-on-exec).
  #359 and #354 merged (`7d424790`, 2026-10-22). There #353 and #358 each conflict only in the
  population, and with each other in the app's pages: #353 rebased and #358 rebased onto its
  branch, chained one level, the lane's next continuation.
  For the package: the SDK install carries no OS window, so the release must ship SDL's window
  for this story; an app in the terminal window is unwitnessed. For A3: the build runner's
  sentences count two process starters, which the launcher makes three. Zengine's
  `docs/contributing/taking-an-issue.md` should name `tests/census_headers.hpp` among the files a
  change's rules force. For
  A1: Zengine's two claims of one process starter (`builder/run.hpp`, the build runner's
  manual) are stale since the Neovim editor's child (the research's doc gaps 2 and 3);
- the snake demo finalized; a way to the demos in place of a runner pane: Files at the demos, a
  right-click to run one (its shape open, 2026-10-21);
- the README's new preface, the founder's.

Other tools surveyed for layouts and small features, licenses checked
([handoff](handoffs/ide-survey.md), 2026-10-21): a command palette first.

The founder on the walk and the survey (2026-10-21):
- step 5 is an export to an app: its load plan built and opened by a new Loom host; the hard part
  is the window's side, Workshop's arranging done by something in the app;
- step 7: the app's Loom console is asked to connect, then to load a weave that speaks Workshop's
  debugging language, and the app's weaves are taken back into Workshop by a replacement across
  hosts, over the link;
- the palette on a double Shift, else Shift+Space; a hotbar of panes on a leader or a held
  modifier, usable in the Editor with the least conflict; a wire let go on empty space opening its
  search is high priority: the power a hand needs, appearing where it is;
- a floating pane is a whole workspace in a window of its own; the exported app is code of its
  own, not a Workshop pane, and a game edited in Workshop has its window cut off from it.

Cut from it: the C++ installer suite, theme presets, plain-language passes beyond what the story
touches, and fast forward's S2 and S4 to S6.

**The direction** (the founder, 2026-10-19, on Vision's state report): subtract before adding, one
owner at a time, and decisions before prompts.

1. Finish the Skin. Workshop's own area takes the whole pointer in a window and the window plans
   become the defaults (G1); then `surface/`, the Skins and Workshop's row projection go (G2).
   G1 is prompted ([prompt](../prompts/graphics-only-g1-window-pointer.md), 2026-10-19): a census
   of every pointer gesture against both windows and the routing first, then a stop.
   The founder took its routing (2026-10-19): D1 to D10 as recommended; D11 with Workshop declining
   `AreaHoldEnded` (G1 adds three kinds taken, one sent), and G2's fence set below Workshop's count
   at `7cc0ec14` (81 taken, 72 sent; lifted 2026-10-20 with every phase's, item 4), the bare
   pointer moments among what G2 drops. Built in one
   pull request ([continuation](../prompts/graphics-only-g1-window-pointer-build.md)); the
   defaults move after it merges. Opened as Zengine #333 (Workshop takes 84, sends 73; G2 would
   leave 78 and 70). The founder took the rename to #332's rule (`AreaButtonChanged`,
   `AreaPointerMoved`, `AreaWheelTurned`) and three loose changes into one push, before merge
   ([continuation](../prompts/graphics-only-g1-window-pointer-build-names.md), 2026-10-19).
   For G2: Workshop's `window_moment_` flag, which keeps its old relays off placed panes, goes
   with the Skin path. The defaults move next, with D11 reversed: Workshop takes `AreaHoldEnded`
   and `AreaPointerLeft`, which the window now tells it, and its own copy of the cover rule goes
   ([continuation](../prompts/graphics-only-g1-defaults.md), 2026-10-19).
   Merged as #338 (2026-10-20): Workshop takes 86 kinds and sends 73
   ([report](../reportbacks/graphics-only-g1-defaults-RB.md)). Its live witness found six window
   defects already on `main` that the switch made the default. The founder took Vision's
   recommendations (2026-10-20): defects 1-4 and 6 fixed before G2, a re-shown area by the
   window's word (`AreaRoom`, a new version), the two `SurfaceText` setups kept on the Skin's
   plan ([continuation](../prompts/graphics-only-g1-window-defects.md)); the status line and the
   Terminal's `SurfaceText` verb retire with the Skin in G2, which proposes the Terminal's
   ordinary verb. Opened as #339, green, reviewed by Vision (2026-10-20)
   ([report](../reportbacks/graphics-only-g1-window-defects-RB.md)): `AreaRoom` 3 says `empty`,
   `WindowOffered` 2 says `cell_px` (the OS window's unit is the pixel), text a cell a character
   in light; the setups on the Skin's plan are `presets` and `editor-materials` (the prompt's
   `commands` was wrong). For G2, Vision's recommendations: each owner paints its area's ground
   (`rows_drawing` fills its room), not a window per area; and Workshop's list of the offices that
   seat each pane in an area of its own (`pane_window_area`) goes, an area named by one rule or
   by its office. Corrected after the founder asked (2026-10-20): text in a window is measured in
   12-pixel cells, against BL-WORK-05 -- `WindowOffered` and `AreaRoom` carry no font measure,
   where `SurfaceExtent` and `PaneCanvasRoom` carry `text_advance_px` and `text_line_px` -- and
   #339's mark fix drew that grid honestly rather than fixing the measure (Vision had called it
   the right trade; it was not). `cell_px` is the whole-pixel work's own field and moved the OS
   window's layout to pixels. #339 merged; the founder took Vision's next G1 step before G2
   (2026-10-20): the OS window says its face's measure and offers its room in pixels, each
   owner places text by it, the terminal window keeps the cell, each owner paints its area's
   ground, and the SDL Skin's real face moves to the OS window if it serves it
   ([continuation](../prompts/graphics-only-g1-window-pixels.md)).
   Opened as #340, green, reviewed by Vision (2026-10-20)
   ([report](../reportbacks/graphics-only-g1-window-pixels-RB.md)): `WindowOffered` 3 offers the
   room in pixels and the face's measure, `AreaRoom` 4 and `PaintTask` 2 carry it, and the face
   (JetBrains Mono, 8 by 18) is copied to `graphics/window/fonts/`; found live, each pane's frame
   is an area of Workshop's at the pane's depth, and the OS window grows per axis. Two decisions
   asked; Vision: take both. For G2: frames named by the one area rule; Workshop's overlay
   labels placed by the face; a one-picture pane's second drawing, a row a cell, goes with the
   row projection; `tests/census_headers.hpp:242` still says `PaintTask v1`. Merged (2026-10-20).
   G2 is prompted ([prompt](../prompts/graphics-only-g2.md), 2026-10-20): a census of every use
   of `surface/`, of the Skins' seam and of the second picture each pane sends Workshop, and its
   routing -- what the agent desk, a guide mark, a frame and the managed opening read once that
   picture goes -- then a stop for the founder's word. Reported and reviewed by Vision
   (2026-10-20, [report](../reportbacks/graphics-only-g2-RB.md)): seven stages, smallest first;
   nine decisions asked, two of them private (an agent's hand in a window; a close is the
   window's). The prompt's seam range (14 to 33) was Vision's misreading: G2's open seams are
   14 to 51, all classified. The founder took all nine as recommended (2026-10-20), and every
   choice but one: `ZENGINE_SDL_SKIN` goes in stage 7, inverted (the founder): SDL is the
   default and the switch is the terminal-only build's, named for the medium, not a library
   (`ZENGINE_TUI_ONLY`, taken 2026-10-20); the old spelling refused at configure by name, never
   kept as a synonym. SDL in the OS window alone (the founder, 2026-10-20): stage 7 also retires
   `zengine-input-sdl`, whose last queue is the SDL Skin's, and loads `zengine-input` beside both
   windows; a weaver's plan row naming it is refused by name with the fix. And the launch tries
   the OS window and falls back to the terminal window, `--tui` choosing the terminal. A project's
   own plan copies the medium rows, so the founder took the window as a choice in the plan (OS
   window, else terminal), carried by the shipped default: G2's stage 8, after stage 7, a load
   plan format version. Stage 1 is prompted
   ([continuation](../prompts/graphics-only-g2-s1-stray-ends.md), 2026-10-20) and is Zengine #342
   (`572771bb`), reviewed (Vision, 2026-10-20, 7 of 8 checks): its run's 8 jobs green, ready to
   merge; the presets story through Info 2 recommended to stand, its authority refusal held by
   `tests/test_workshop_inventory_info.cpp`. With stage 2: the session's held rewrap `0b9d7485`,
   #342's run table, and the new case checking that no rule of the Terminal's names `Drawn`.
   #342 merged (`15afcb4e`). Stage 2, the shares to their owners, prompted
   ([continuation](../prompts/graphics-only-g2-s2-shares.md), 2026-10-20), is Zengine #344
   (`82114ac0`, [report](../reportbacks/graphics-only-g2-s2-shares-RB.md)), reviewed (Vision,
   2026-10-21, 10 of 10 checks): the mass edit regenerated byte for byte from `f53ab015`, its
   run's 8 jobs green (ASan 45:21 of 60, nearly cold), ready to merge with its seven choices.
   #344 merged (`3fa139a1`). Stage 3, the rigs on a window, prompted
   ([continuation](../prompts/graphics-only-g2-s3-rigs.md), 2026-10-21), with the kit's three
   doc gaps from stage 2's report and stage 2's self-comparing `static_assert`
   (`workshop/weave_handlers.cpp:242`), which Vision's review missed. Stage 3 is Zengine #345
   (`9a5159bd`, [report](../reportbacks/graphics-only-g2-s3-rigs-RB.md)), reviewed (Vision,
   2026-10-22, 12 of 12 checks): the desk read off the window's device, checked against
   `WindowShowAsked` every 32nd idle read; the terminal window composing on a grid (product, the
   same cells); two defects the rig found, each red before its fix; its run's 8 jobs green (MSVC,
   advisory, 43:57 of 60), ready to merge. Pressure it named: a waiting pane's body blank in a
   window, two windows showing one area (stage 6); a revived Workshop not started again under a
   window, `classic` showing no guide role in a terminal window, the caret drawn over its
   character (stage 7); the restore notice replaced at once by Inventory's startup note (no
   owner); the window's dirty cells an ordered set, 24% of the hottest case (stage 4).
   `GlyphGrid::rows_above` still defaults to `surface::kTuiCanvasTopRow`, the default behind the
   first defect (stage 4). Stage 4, the agent desk and the agent's hand in the window, prompted
   ([continuation](../prompts/graphics-only-g2-s4-desk-and-hand.md), 2026-10-22), chained on
   #345's branch, with #345's ends: the typed send's text checked again, that default, the dirty
   cells' cost. Stage 4 is Zengine #351 (`6d62b007`,
   [report](../reportbacks/graphics-only-g2-s4-desk-and-hand-RB.md)), reviewed by Vision
   (2026-10-22, the morning's four PRs, 23 of 23 checks): its run green, ASan 58:59 of 60 on a
   cold compile; #345's ends all taken; its body's "G2's fourth stage" taken out at the merge.
   Not as routed: an agent's press still moves the keys and the selection (BL-WORK-38's rule, for
   a weaver's host, waits for the agent desk); a wheel over a pane is swallowed while a value is
   carried (stage 6). CI's ASan job is at its 60 minutes whenever a widely included header
   changes: the founder raises it to 90 (2026-10-22, through the issue lane), and would like it
   back at 60 by the week's end, not a hard requirement: test time grows only as far as the suites
   need and stays as small as it can be -- another split of the Workshop panes suite the likely
   fix if it does not fall with the code's health, and fast forward's last stages if they come
   (BL-WORK-43). `main`'s push run after #350 and #351 took 39:16 in ASan, its cache warm; the 90
   goes through anyway (Zengine #356, fixes #355), its times tracked through the week; #356's own
   run took 61:52 in ASan, and #353's 58:20 under the old 60: the 90 was needed. #350 and #351
   merged as merge commits (`364ee623`); stage 5, the menu presenter in its own area, prompted
   ([continuation](../prompts/graphics-only-g2-s5-presenter.md), 2026-10-22). Stage 5 is Zengine
   #359 (`83280b71`, [report](../reportbacks/graphics-only-g2-s5-presenter-RB.md)), reviewed by
   Vision (2026-10-22): its run green, ASan 39:38; MenuShown 3 names the presenter's area and
   carries no lines; seams row 18 closed; no window, no pane menu until stage 7. Its seam: no shape
   says which drawing a press hit.
   #359 merged (`60eb5497`, a merge commit, its body clean). Stage 6, no second picture, prompted
   ([continuation](../prompts/graphics-only-g2-s6-no-second-picture.md), 2026-10-22), with the
   wheel swallowed during a carry, stage 3's waiting pane and two windows, the press seam hooked
   unless a case shows it, D12 (in no stage's row: here or stage 7) and the suites' time; one
   pull request, or two chained where the managed opening and the install stand apart.
2. Then the first real split, by job: the desk -- layouts, setups, and what each layout holds
   (settings, pins, locks, its theme baseline) -- becomes its own owner, out of Workshop's weave,
   in setup v6 as the settings research drew it.
   Researched first, read-only beside G1 ([prompt](../prompts/desk-split-research.md),
   2026-10-19); reported the same day ([report](../reportbacks/desk-split-research-RB.md):
   `zengine.layouts`, stages D1 to D3) and reviewed by Vision. The founder took its twelve
   decisions as recommended (2026-10-19), with four of Vision's changes:
   - the unlock (decision 9): none of it built in D1. WL-LOCK-02 says that on a development host
     a guest's hand is the weaver's, unlocking included; locks that bind such a guest are theme
     4's, the Terminal, the editor and the files together;
   - 3b's fold-in kept, its notice naming in full each entry it drops (one may be another
     session's);
   - rows 86-87's (b) (private) runs in the issue lane by a private prompt once G1's build
     merges; D1 then asks its gesture question in a shape of its own,
     `WeaversActRequested{gesture, office}`, answered `WeaversActAnswered{current}`;
   - D1 one phase, committed step by step, its report counting `LayoutEdit`'s operations and
     the lines beside the kinds.
   D1 is prompted once G1 and G2 merge, against that `main`.
   Layout choices beyond pixels (the founder, 2026-10-20): a share of the parent, a fit to what a
   pane holds, a fill, as the quarry's `CustomLayout` had, through a solver that turns them into
   the pixels each object needs. Researched read-only beside G1
   ([prompt](../prompts/layout-modes-research.md)); folded into D1's move where the design
   allows, not forced. Reported and reviewed by Vision (2026-10-20,
   [report](../reportbacks/layout-modes-research-RB.md)): the choices are words in today's
   `{mode, amount}` and `{mode, x, y}` -- sizes `share`, `fit`, `fill`; places the nine points of
   the frame -- no shape and no version (WL-SETUP-04), so nothing to fold; one solver, `ui/`
   grown to the pixel, called in `bounds_of`; the right column divides; Webster's rule after one
   step each. Follow: L1 (the solver, nothing drawn changing) in the issue lane beside D1 once G2
   merges, L2 (the words) after D1, L3 (the views) after G1's window-pixels step. The session
   stands at 64,197 of 65,536 decoded cells, so any per-row field (a minimum, a frame) overflows
   it. Twelve decisions asked of the founder. His notes (2026-10-20), sent back to the research
   ([continuation](../prompts/layout-modes-research-revised.md)): optional `x`, `y` and `amount`
   (Loom's optional fields), not zeros; `right-column` removed, its uses moved to the other
   words; a `fill` drags as a fill, its weight alone changing; `center`; and the cell limit a
   priority -- the session decoded a layout at a time in D1's v9, never Loom's limit raised.
   Fold or follow answered again, now that a format version is needed.
3. Settings stages 4 to 6 wait for that owner.
4. ~~Every phase's fence: Workshop's weave takes fewer kinds of message after it.~~ Off until
   Workshop is release-ready (the founder, 2026-10-19); the fences are revisited then. The
   counts above are a record, not a gate.
5. One phase, and at most one issue lane beside it (constitution section f). Vision checks every
   name a prompt gives against `main` before the prompt goes out. The lane opened 2026-10-19
   ([prompt](../prompts/issue-lane-first-three.md)): no Zengine issue was `ready`, so three
   bounded seams clear of G1 are filed and taken (#330 to #332, merged). Next in the lane once
   #333 merges: `workshop_panes` broken up, the longest entry and the sanitizer job's limit,
   researched read-only on #333's branch first
   ([prompt](../prompts/workshop-panes-split-research.md), 2026-10-19). The founder took its
   eight decisions as recommended: one program run as eight entries by subject, a whole-count
   check, each part's floor at its count, the COST rows from its own run. S1 is the lane's
   ([prompt](../prompts/issue-lane-panes-split.md)), taken as #335; S2, the kit's part
   selection, waits. Next in the lane after #335: CI's compiler caches kept across runner images,
   the cold Linux builds of a rollout ([prompt](../prompts/issue-lane-ci-cache-keys.md),
   2026-10-19). #335 merged (2026-10-20): with its measured COST rows the sanitizer job's verify
   took 676 s (1,209 before the split; 856 on `main`'s run after it). The cache fix is #336, taken
   as #337: green, each store named by its compiler's bytes, warm builds of 38 to 110 s, one
   across images ([report](../reportbacks/issue-lane-ci-cache-keys-RB.md)); merged before #338
   (2026-10-20). The lane's next issue is not chosen. A defect found reviewing a perspective is
   filed by a prompt (2026-10-20): three default keys never arrive from a POSIX terminal, and
   `posix_gap` does not say so ([prompt](../prompts/posix-ctrl-gap-issue.md)).
6. The decisions asked in the reports since 2026-10-15 are swept into one list: those the code has
   settled marked, the rest brought to the founder in small batches.
7. One list of the seams the reports keep deferring, each with one owner and closed in one phase.
   Items 6 and 7 are swept read-only beside G1 ([prompt](../prompts/reports-open-items.md),
   2026-10-19); reported the same day ([report](../reportbacks/reports-open-items-RB.md): 126
   decisions, 186 seams) and reviewed by Vision. G1's open rows (15-17, 20-21) come with G2's
   prompt, settings' (47, 48, 69-71) with stage 4's. The 28 seams with no owner get two:
   authority (theme 4) for the three private, the later splits for the rest.
8. Night Lab's other model drafts top-down material for these phases, never their prompts.
9. Then the founder's order: the UX batch, then the first complete maker story.

**The architecture's needs, as Vision measured them** (Zengine `aab5177`, 2026-10-14; updated
through `#323`/`#324`, 2026-10-19). At `aab5177`: one hub, Workshop's weave taking 68 kinds of
message and sending 62, `workshop/` 44k of Zengine's 112k product lines; repeated plumbing, 12 pane
weaves each writing their side of the pane protocol; two ways to draw, Workshop's screen and the
surface beside the graphics library; and a Timer that slept up to 10 ms at a time on the bus's one
thread in Workshop. Through Wave 17 (`#296`–`#324`): every weave a weaver or host meets carries and answers its
manual via `ManualFacet` (`#234`–`#249`, `#266`, `#268`, `#272`, `#292`, `#295`); every single- and multi-pane weave,
`PowersDoor`, `flow_host::Manager`, and `view::Manager` compose their protocol plumbing through `zengine/weave_facets.hpp`,
`workshop/pane_facets.hpp`, `workshop/pane_seat.hpp`, and `ZENGINE_VALUE_DOOR` (`#265`, `#269`, `#271`, `#278`, `#291`–`#295`),
closing P-WORK-72, P-WORK-73, and P-WORK-74; every pane declares what its presses cause (`#266`); the project's three
doors are unified in `zengine.project` (`#270`); the Terminal's host door and completion moved to `terminal/` and the
guest scope judge to `workshop/guest_judge.hpp` (`#275`, `#279`); Waves 1–5 (`#274`–`#288`) split every 2,000+ line file
across `workshop/`, `info/`, `graphics/`, `editor/`, `files/`, `builder/`, and `terminal/`; Waves 6–7 (`#290`–`#295`)
extracted shared control-strip / list-window facet drawing, multi-pane seats (`PaneCanvasSeat` + `MultiPaneFacet`),
action/menu facets (`PaneActionFacet`, `PaneMenuFacet`, `graphics::ActionFacet`), presenter seam helpers, and the shared
Editor office seam (`editor/office_seam.hpp`); Waves 8–13 (`#296`–`#313`) brought **every shipped pane, data-as-UI view,
Workshop's window arrangement and desk chrome/overlays, live terminal window extent/text input/resize, `window-load-plan.json`
with `zengine-input` session support and settled banner suppression, `zengine::graphics` SDK install, unified `WindowDrawing`,
and external-host unsettled-picture retry** onto `graphics/`; and Waves 14–17 (`#314`–`#324`) shipped **Settings Stages 2A–2D
& 3A (`WorkshopPrefs` v3, `OfficeSettings*` & `PaneSettingPin*` doors, 15 pane settings across 7 panes, 11 Workshop office settings
including per-pane `workshop.skin` with `"classic"`/`"block"`/`"day"`/`"night"` and `workshop.completion-order`, `component/tab_strip.hpp`,
and `settings/` theme files + composite DAG resolution + `zengine.settings` vocabulary), remappable keyboard focus
navigation (`focus.*`, WCAG 2.1.1/2.1.2), and `surface/` retirement Stages S1–S4A (`graphics/` severed from `surface/`,
`zengine-window-sdl`, full input/close parity, full medium + bus-door parity for clipboard, placement, pump, close, and
BMP/cells capture across both windows, window clipboard/placement/capture routing, and `sdl-window-load-plan.json`)**.
The spine that stood here (settings stages 3B to 6 and S4B, the desk's 3a and 3b, fast forward's
S2 and S4 to S6, the UX batch, the first maker story) gives way to the direction above
(2026-10-19). Where the desk's 3a and 3b (BL-WORK-38) and fast forward (BL-WORK-43) fall in it is
not yet decided.

## 1b. The roadmap's themes

From the founder's notes of 2026-10-14, with what is decided. Their UX items are drafts in
[ux-batch.md](ux-batch.md), filed together after the manuals and the split. Their principles: the
most important thing is the ability to intuit and learn; systems compose gracefully; what is good
for human makers is good for agents; source code stays a first-class way to create beside Flow,
neither needed to get value from the other. These are directions and review points, not a session or
pull request each; a useful slice lands when its evidence does.

1. **Documentation first** (the founder, 2026-10-14): docs stage C's manuals for every weave a
weaver meets, in the form the Builder's set; tutorials wait for the stories. Writing them maps
ownership (each piece of state's authoritative owner, writers, readers, lifetime and persistence,
kept apart from derived displays and caches) and sorts every message into request, performed action,
observation or outcome: the split's input ([prompt](../prompts/manuals-first.md)). **Done** as #234
to #249 (2026-10-15), with `ManualFacet` across single- and multi-pane offices (#266, #268, #292) and the
three host offices (`zengine.flow.host`, `zengine.view.host`, `zengine.builder.runner`) in #272 and #295
(2026-10-16 to 2026-10-17), plus the ASCII manual byte check in #251 (`0ea9441`): every weave a weaver meets
carries its manual, answered when asked (the menu presenters not yet: P-WORK-74). The maps
([ownership](../reportbacks/manuals-first/ownership.md),
[messages](../reportbacks/manuals-first/messages.md)) supplied the split's list and the reload-in-place
list (P-WORK-74, closed across Phases 1D, 1E, and 2B).

2. **One owner per job: the split.** The hub's responsibilities go to owners, guided by the manuals'
map, the census's ranked list (the terminal, the menu, Info's properties view, the guest scope
judge, the project's three doors) and the notes' candidate boundaries: input coordination, workspace
navigation, carry handling, subject and action descriptions, feature owners, presentation --
hypotheses to test, not six services. **Progress through Wave 12 (2026-10-18):** `zengine/weave_facets.hpp`,
`workshop/pane_facets.hpp`, and `workshop/pane_seat.hpp` (`#265`, `#269`, `#271`, `#278`, `#291`–`#295`) extracted
repeated pane/room/row/action/menu/seat/ask/manual plumbing; the project's
three doors joined into `zengine.project` (`#270`); the Terminal's host door, completer, and
transcript projection moved from `workshop/` into `terminal/door.hpp`, and `GuestDoor` into
`workshop/guest_judge.hpp` (`#275`, `#279`); `Info`'s property view moved to `info/property_view.hpp`
and dead `workshop/panes.cpp` was deleted (`#282`); Workshop's desk read moved to
`workshop/desk_read.hpp` and `workshop/weave_desk_read.cpp` (`#280`); Waves 1–5 broke up the
remaining 2,000+ line files across `info/`, `graphics/`, `introspection/`, `workshop/desktop-pane/`,
`editor/`, `files/`, `builder/`, `terminal/`, and `workshop/`; Waves 6–7 (`#290`–`#295`) unified the Editor
office seam (`editor/office_seam.hpp`), control strip & list window helpers, multi-pane seats, and presenter vocabulary;
and Waves 8–12 (`#296`–`#311`) brought every shipped pane weave, data-as-UI view, Workshop's own window arrangement,
desk chrome, overlays, live terminal window extent/text input/resize, `window-load-plan.json`, and `zengine::graphics` SDK
install onto `graphics/`.

3. **Describe once: actions, subjects, outcomes.** An owner describes an action's purpose, inputs,
availability, documentation and outcomes once, and menus, controls, Compose, the desk and automation
reuse it; mouse, keyboard and semantic invocation reach the same owner operation under their own
authority checks; a readable schema is not a writable one, and an offered action is not a granted
one. Outcomes are stable and attributable, with the subject's and the operation's identity, stale
and superseded work told apart, pending never taken for failed; their words come from localization
keys with typed arguments, which no consumer parses. **Progress (2026-10-18):** Phase 1B (`#266`)
and Phase 2B (`#271`) declared `v3::PaneActionRow` causes across every shipped pane (`Info`
`info.value.*`, `View Builder` `view.*`, and all remaining panes), so every pane's manual links each
press to what it sends; Phase 10C (`#293`) introduced `PaneActionFacet`, `PaneMenuFacet`, and
`graphics::ActionFacet` so pane weaves and graphics drawers handle actions through one `on_action(id, mail)`
contract; BL-WORK-37 Stages 2–7 (`#296`–`#311`) moved every shipped pane, data-as-UI view, and Workshop's window
arranger + desk chrome/overlays + live terminal window extent/text input/resize + `window-load-plan.json` onto `graphics/`.
**Next:** Land Wave 13 (`7D` & `7E` Stage 7 follow-up polish), then advance to BL-WORK-36 (Settings stages 2 and 3) and BL-WORK-38 (Desk 3a and 3b).

4. **Relationships and powers.** Explicit and inspectable: a window contains panes, a pane presents
components, a value has an owner, a participant has a lifecycle and granted powers, with visual
containment, data ownership, lifecycle and authority kept distinct. Today every loaded row but
Inventory is admitted `allow_any` (P-WORK-68); the agent-powers research is the start.
`SetupApplyRequested` judges no asker: any loaded weave, and a guest with the `demo` power, can put
a desk live (Vision, 2026-10-15); `WorkshopQuitRequested` judges its asker, a guest's quit on the
weaver's host refused. Not a security defect under today's trust, which admits loaded code
in-process; a gap this theme closes.

5. **Subject continuity.** A subject keeps its identity through navigation, inspection, composition,
editing and transfer, as a snapshot, a live reference, a draft with its source revision, or a saved
command; disappearance, replacement and a changed schema are said, and an old reference is never
silently redirected.

6. **Workspaces, perspectives, navigation.** A workspace arranges tools and material; a perspective
presents them for a task and may span workspaces; authority stays explicit. Moving between
workspaces, returning, and carrying across them (UX-08 to UX-11) wait for the workspace's owner.

7. **Two modes for agents** (with BL-WORK-38 and BL-LAB-01): human-interface, the visible output and
normal input of an authorized perspective; and semantic, granted messages, operations and
observations. A restricted run never falls back to hidden queries, and restriction is enforced at
the interfaces, not by hiding buttons. Open: what visible projection each restricted profile may
read.

8. **Graphics, components, and data as UI + presenter** (BL-WORK-37; the founder, 2026-10-14 and
solidified 2026-10-17): helpers written by hand first (`graphics/element_*.hpp` split into per-part
headers in `#276`; `gfx::Button` and `AskBook` proved in `examples/snake` in `#277`), a generator of
helper functions later, with the data conversion research (BL-WORK-41); whole controls, shapes,
lines and pixels; the View Builder's components are in the UX batch. **Solidified end-state (the
founder, 2026-10-17):** UI can be a relatively small JSON-like view file that hooks into its
surroundings through an owner who has paired that view with a presenter, using hierarchical names
(`path`s) and `action` ids to functionally link into the web of weaves — while keeping the manual,
hard-coded C++ `Sketch` path accessible and enjoyable to write as a first-class peer.

9. **Connected tools.** Loaded, Project and Compose researched as one journey, with examples done by
mouse alone, before deciding whether to combine them (`zengine.project` unified the project's three
doors in `#270`); Info's edit and save through owner-declared editing contracts (writable fields,
validation, revision and conflict checks, authority, outcomes), with BL-WORK-10.

10. **Configuration, persistence, personal work.** A source literal promoted to configuration in a
few actions, the configuration in the state schema with explicit upgrade paths (with BL-WORK-36);
each owner's persistence promises visible across navigation, shutdown, replacement and a crash,
authored work first (reload-in-place state preservation across the nine weaves from the manuals'
ownership map completed in `#268`, `#269`, and `#271`); personal changes kept apart from shared
contributions, their storage open (with #145); operators marked in code by a small code-tool action.

11. **Tools, demos, workers.** A reusable local worker environment (a cloned WSL or a kickstart
file, its image kept apart from identity and credentials; workers open pull requests, the founder
merges); tools and demos kept apart; the demo runner (UX-36); Python participants, a
documentation-drift scanner first (with #147), and the founder's candidate C++ ↔ Python live Snake
owner handoff demo (2026-10-16, with BL-WORK-40 and BL-WORK-37); the quarry out of Zengine (HK-01,
fileable now).

12. **Execution experiments, later.** Message cost measured first (redundant publications,
forwarding-only participants, serialization, fan-out, queueing, real latency); then a compiled
composition (direct endpoints, an event queue) with its equivalences defined first; speculative
threading with in-order commitment. A hash identifies approved code; it does not prove that
bypassing the message path keeps its meaning. Its far horizon (the founder, 2026-10-22): a
compile-down system, Loom and Zengine code compiled into a true standalone app with no Loom in
it: introspection, modularity and extensibility while developing, the overhead removed for a
release or a more proprietary form.

13. **The first complete story, last**: "A maker discovers a running participant, understands one
editable setting, changes it safely, preserves a useful reference or command, carries it into
another workspace, and uses it there," with the notes' questions and evidence: files and contracts
touched, steps, message chains, timings, failures and their recovery, and source-only, semantic and
interface evidence labelled apart.

## 2. Workshop and onboarding

### BL-WORK-01 — Workshop and onboarding grow together

**State:** GOAL-COUPLED  
**Owed:** Repeated maker friction must either improve the interaction or produce an available,
truthful explanation of the real concept. Keep the one tool-authoring path legible: a pane provider
is a weave communicating across the pane protocol. Files, Builder, Attention, Info, Terminal and
Editor have completed the selected extraction arc; the Goal Map names the remaining host-owned
surfaces (VD-19). Grow the human contributor front door from tested public explanations rather
than from private phase vocabulary.

**Wake:** every Workshop phase with repeated human-facing friction; mandatory before actively
inviting outside contributors.

**Evidence:** Workshop Goal Map, WG/DOC external-reader work, current public guides.

**Delivered foundation:** merged interaction authoring repairs the existing loaded-pane guide around
Tally, request handling and missing-reply diagnosis. Warm installed-package exercise is useful evidence,
not second-maintainer validation. The goal-coupled obligation remains open. The tower-defense example
(accepted Zengine #60) adds a public 0-to-game route whose every step is a documented ELH tool
and whose replay was proven from an empty directory; it is a maker's route, not onboarding proof.

### BL-WORK-02 — Keep the simple external pane useful as a learning artifact

**State:** ISSUE — [Zengine#124](https://github.com/Krealsion/Zengine/issues/124) holds it now (filed by deep review, 2026-10-09).

### BL-WORK-03 — Split the Info value view before it grows again

**State:** ISSUE — [Zengine#125](https://github.com/Krealsion/Zengine/issues/125) holds it now (filed by deep review, 2026-10-09).

### BL-WORK-04 — The Pane Creator retires into described views

**State:** CLOSED — merged as Zengine #91 (`5901b39`, 2026-10-05), from `prompts/whole-pixel-2.md`
and `prompts/whole-pixel-2-no-creator.md`. Nothing is kept for the Creator's files, flag or keys:
the founder never saved one  
**Owed:** The Pane Creator (WL-MAKER) makes a pane of static text regions that Workshop owns and
paints, edited in Info and saved as `workshop-pane.json`. The tally panel's show stage builds
described views beside it: each runs as its own participant, with fields, buttons and bindings,
and draws on its pane's canvas in whole pixels. Then the Pane Creator retires into them, so a
weaver has one way to make a pane from data and Workshop paints no authored pane of its own.

**Wake:** met: the graphical View Builder merged (Zengine #86, 2026-10-03). Its turn in the order
comes with BL-WORK-05.
**Source:** the founder's choice while the show stage's prompt was prepared
(`prompts/zengine-tally-show.md`); the research that missed it,
[the UI builder](../reportbacks/zengine-flow-powers/ui-builder.md).

### BL-WORK-05 — Workshop's unit becomes the whole pixel

**State:** CLOSED — merged in the founder's three stages (2026-10-04): 1, the unit and canvas
panes in pixels (`prompts/whole-pixel-1.md`), with an authored place measured from the room's
top-left (`prompts/whole-pixel-1-room.md`), as Zengine #90 (`2c06da5`, 2026-10-04); 2, what
Workshop still paints itself (`prompts/whole-pixel-2.md`), with BL-DEF-09, as #91 (`5901b39`,
2026-10-05); 3, arrangement snapping, and a pane the weaver launches always landing where they
can see it (`prompts/whole-pixel-3.md`, the founder, 2026-10-05), with BL-DEF-10 and its review's
fixes (`prompts/whole-pixel-3-fixes.md`), as #92 (`567f983`, 2026-10-05)  
**Owed:** Workshop measures in 48ths of a cell, a quarter pixel in the window, and lays out the
desk's fixed parts in cells before any font is measured. Reverse it: the whole pixel is the unit
and a cell is 12 of them, so a pixel is a twelfth of a cell, and nothing authors a fraction of a
pixel. The window's picture is complete in pixels; a terminal's is derived from it, floored to
cells, with text refitted to what the terminal measures.

With it goes what Workshop still paints itself: the old grey workspace behind the panes, laid out
in cells and belonging to no pane; Attention's compact indicator, the red box at the window's top
right, which moves into the Attention pane; and the Pane Creator's panes, which retire into
described views (BL-WORK-04). Arrangement mode snaps (P-WORK-10).

A canvas pane asks for its room in pixels, not in Workshop's text rows and columns: the
founder's choice (2026-10-03) of option (a) in the View Builder's size round
([its report](../reportbacks/view-builder-size-RB.md#decisions-asked)). Today a view offers its
size in 12-pixel canvas cells and Workshop reads them as its own text cells, so a 680 by 360
view got a pane about 456 pixels wide, cut on the right. Then views and the View Builder
measure in pixels end to end, nothing in a window forced onto cells: the window's picture is
the authority, and a terminal's is derived from it.

**Wake:** after BL-WORK-08.
**Source:** the founder, while the show stage's prompt was prepared
(`prompts/zengine-tally-show.md`), and again in the View Builder's size round (2026-10-03).

### BL-WORK-06 — The text panes draw on the canvas

**State:** CLOSED — merged in four stages (Vision, 2026-10-06), after it was DECIDED (the founder,
2026-10-02) and ORDERED fourth (2026-10-03), fifth since BL-WORK-24 moved before it (2026-10-05): 1,
the cell caret and the panes that list and show (`prompts/text-panes-canvas-1.md`), as Zengine #95
(`47f0de1`, 2026-10-06); 2, the medium's own ground for a moved pane (the founder, 2026-10-06), and
Files, the Builder, the Terminal and the Composer (`prompts/text-panes-canvas-2.md`), as #96
(`859f9e9`, 2026-10-07); 3, Info and Inventory with their views, and plain text in a terminal in the
terminal's own text colour (the founder, 2026-10-07; `prompts/text-panes-canvas-3.md`), as #97
(`826b05c`, 2026-10-07), with its review's fix (`prompts/text-panes-canvas-3-fixes.md`); 4, the
Editors, with the managed opening carrying a picture, and the held press's room #97 left keyed by
geometry alone (`prompts/text-panes-canvas-4.md`), with the hosted Windows jobs' fix and its
review's (`prompts/text-panes-canvas-4-fixes.md`, `prompts/text-panes-canvas-4-fixes-2.md`), as #98
(`b51c0f4`, 2026-10-07); and two cases that read the temporary directory's path, a quick repair
given in chat, as #99 (`bb0f851`, 2026-10-07)  
**Owed:** Every pane except Flow, the View Builder and described views writes rows and columns of
text through the prose door: Info, Inventory, Files, the Terminal, the Editors,
Builder, Powers and the rest. Each moves to the canvas, so every pane draws in pixels and a
terminal shows the fallback derived from that picture. Each pane it moves stays readable by
messages (BL-WORK-24): an agent reads its words on the canvas as it read its rows, by the names
its parts were given.

A caret in a cell medium is an inverted cell over its character (the founder, 2026-10-06, from
#93's follow-up report). A terminal now draws a caret by inserting a `_` glyph into the row
(`surface/region.hpp`), which stands every character after it a cell to the right and cuts a
full row's last character; #93 maps every measured column through it (`drawn_column`,
`shown_column`), and a press that moves a caret still moves text under a still hand, so a sweep
aimed by the picture before it ends a character early or late. Drawn over its character instead,
inserting nothing, a caret moves no text and the mapping goes. One convention for every cell
medium; a caret past a full row's end still needs a cell to stand on.

Stage 1 carried what #94 left (its reports and deep review, 2026-10-06): a part whose only
visible cell is its caret's at a terminal's right edge has no point, though a press there reaches
it (the deep review's P3 on #94's fixes, which the inverted cell answers); no page lists the names
each shipped pane gives its parts, or the places it leaves unnamed; and WL-HAND's register is at
its byte budget, so a law it takes needs the file split first.

**Wake:** met: #94 merged (2026-10-06); BL-WORK-36 follows it, then BL-WORK-09.
**Source:** as BL-WORK-05; the caret, the founder (2026-10-06).

### BL-WORK-36 — Settings: what a pane can set, kept with each layout

**State:** ORDERED — resting at stage 1: researched (2026-10-07); stage 1 merged as Zengine #101
(2026-10-09), Loom #31 beside it (`prompts/settings-stage-1.md`, 2026-10-08); selected by the founder
(2026-10-18) as the next phase after BL-WORK-37 Stage 7 (`7D` & `7E`); before BL-WORK-09  
**Owed:** Configuration for customization is one of Zen's pillars, and replaceable code alone does
not give it: some things a weaver wants to switch between without a code change or a reload (the
founder, 2026-10-07). A light mode is not special, and the magic numbers -- a ground, a text
colour -- belong in settings. Each pane may publish what can be set on it as a settings shape of
its own, with its defaults; the desk keeps a value per pane in each layout's setup row, beside its
place and size, and hands the pane the active layout's value whenever it is seated, the layout
switches or the value is edited, so a pane in two layouts keeps each layout's settings without
knowing which is active. An editor -- Info's field editing, or a settings pane on it -- reads and
writes them by message:

```text
PaneSettings          { provider, pane, value }  // value: the pane's own settings shape
PaneSettingsRequested { provider, pane }         // the desk answers with PaneSettings
```

Workshop stores and forwards a value and never reads inside it. Settings go in as the work meets
forks, so either path can be chosen. A pane's own settings may change its text size or show and
hide its parts; the skin's -- the palette, the window's ground, the font size -- belong to no pane.

The research settles: a settings shape's versions against values an older layout saved; where the
skin's settings live, likely for every desk at once; per-pane text size against the canvas's law
that a pane chooses no font; showing and hiding parts as one mechanism with BL-WORK-16's
accordions; the setup file's format past version 4.

Researched ([its report](../reportbacks/settings-research-RB.md), 2026-10-07): a pane declares rows
-- a key, a label, what the key takes and its default -- and the desk keeps the chosen values in
each layout's setup row (setup v5, session v8), hands a seated pane its row's values before any
room, and Info edits them as rows of the pane it inspects. Later stages add message doors, the
skin's own settings in a configuration file, and the per-pane text step. The founder took its
recommendations with four changes (2026-10-08): a value is typed -- a key and one optional field per
kind, exactly one present -- which Loom #31 made possible (a `ZEN_SHAPE` member of type
`std::optional<T>` is an optional field); the declaration stands alone on `PaneActions`' rules and
counts only while its declarer holds the office; the hand-off is gated on the holder accepting
`PaneSettings`, not on declared rows; and the shapes name the pane, never the provider. Stage 1
carries one setting end to end, the Terminal's legend edited in Info. The order after it, stage 2 or
the skin first, is the research's decision 9, still open.

A setting the founder wants (2026-10-08): the Terminal's completion offering a shape's required
fields first, then its optional ones, or in declaration order (P-LOOM-10). Workshop's terminal
participant builds the completion, not the pane, so the setting must reach it; that is its stage's
choice.

**The founder's Stage 2+ direction and decisions (2026-10-18):**
1. **Promote magic numbers and strings into settings while keeping the list useful:** Convert magic
   numbers and strings across panes into declared settings, organized by two mechanisms so a long
   settings list stays fast to use:
   - **Tags (`tags`):** Every declared setting carries one or more tags (e.g., `chrome`, `input`,
     `completion`, `limits`, `text`) in `v2::PaneSettingRow`.
   - **Hand-curated `pinned` list (`pinned = true` by default on the most useful 1–3 settings per
     pane):** A curated list at the top of the settings experience whose items can be **added
     (pinned), removed (unpinned), and reordered (moved up / moved down)** by the weaver.
2. **Compact tag-tab strip with horizontal `<` / `>` scrolling in `Info`:** In `Info`'s `SETTINGS`
   section, tags sort like compact tabs (`[pinned]`, `[all]`, followed by declared tags in
   alphabetical order, plus `[kept]` when undeclared stored keys exist), defaulting to `[pinned]`
   so only the active tab's settings rows are shown at a time. When the tag tabs exceed the row
   width, little `<` and `>` arrow indicators scroll horizontally through the tab strip.
3. **Consistent Workshop-wide pin order by default, configurable as a Workshop setting:** By
   default, a pane's custom pinned list (add, remove, reorder) is consistent across setups
   (Workshop-wide per `<office>/<pane>`, stored in Workshop's settings file and falling back to the
   pane's hand-curated `pinned = true` defaults), while whether pinned state is `workshop-wide` or
   `per-layout` is itself a Workshop setting (`workshop.pinned-scope`) so a weaver can switch it off
   the default.
4. **Setting Locks (`locked` user preferences):**
   - Individual settings can be **locked** so they cannot be changed (by manual edit, by applying a
     theme, or by a script/agent) until explicitly **unlocked**.
   - Locks protect a weaver's saved personal preferences (e.g., text step, high-contrast colors,
     navigation gestures, or accessibility settings) when applying themes, and can be managed across
     a single setup or across all setups at once.
5. **Themes, Composite Themes, and Explicit Event-Driven Application (replacing continuous load-order re-evaluation):**
   - **A Theme is a named, sparse group of settings:** It can apply to anything that accepts
     settings (`<office>/<pane>`, `workshop`, or wildcard/tag-matched targets across panes) and is
     saved from the Theme / Settings Manager.
   - **Partial and orthogonal by nature:** A theme does not need to specify every setting on a pane
     or desk. It can edit a single pane, every color-using pane it knows, functional/logic settings
     (e.g., completion order, internal pane sub-layouts, grid/snap behavior, navigation gestures),
     purely graphical settings (color, palette, decoration), or layout properties to the extent
     layouts are exposed as settings.
   - **Composite Themes (ordered dependencies + own customizations) & Explicit Application:**
     Instead of a runtime load order that re-evaluates on every tick or re-applies on boot (which
     would erase temporary settings from the last session), weavers can build **composite themes** —
     still just a Theme, carrying an ordered list of dependency themes (`includes`) plus the
     weaver's own customizations at the end — and **apply** them wholesale on demand.
   - **Triggered by the weaver or an authorized actor:** Themes and settings are applied only when
     requested by the weaver, or when a script, agent, or weave with the appropriate permission
     applies one (for example, a script that shifts themes throughout the day), writing the
     unlocked settings into the target setup(s) while leaving `locked` settings untouched and never
     restricting the weaver from applying their own tweaks afterward.
6. **Master Theme Files & Auto-Saving Loose Changes (`Option A` vs. `Option B` vs. Hybrid, researched in [prompt](../prompts/settings-themes-research.md), [report](../reportbacks/settings-themes-research-RB.md)):**
   - Two models for how a setup saves its settings and themes, resolved by the **Hybrid** (`storage.md`):
     - `SetupPane::settings` rows stay the one truth of what a pane is handed (`Option A`), so live tweaks ride the session on close and `s` on save without re-evaluating a theme stack on hand-off or boot, and without crossing Loom's 65,536-cell session decode ceiling (a maximal v8 session is already 64,116 cells; adding a field per stored setting overflows to 72,308, whereas the hybrid adds only 80 cells to reach 64,196).
     - Each layout (`WorkshopSetup` v6) keeps a **baseline theme link** (`LayoutTheme{name, fingerprint}`, `Option B`'s Master Theme as a relation), and **loose changes are derived on demand** by comparing the layout's rows against the resolved baseline and shown at the tail of the Master View (`LOOSE`), where weavers can **snapshot** a stable backup (`S`), **promote** loose changes into a reusable theme (`P`), **reset loose changes** to the baseline (`R`, preserving locked keys), or edit/save the master's `includes` (`W`).
7. **Two-Tier GUI-First Settings Experience on `graphics/` — Compact Pane Gear (`*`) Popover Overlay + Full-Screen Settings & Theme Studio with Live Pane Samples (the founder, 2026-10-18, overruling `manager.md`'s TUI-first ASCII table layout):**
   - **Tier 1 — Compact Pane Gear (`*`) Settings Popover Overlay (anchored to a pane's `*` header button):** Focused, lightweight popover card (`~440–480 px` wide) for configuring one pane in place without leaving the active workspace:
     - **Header & Scope Bar:** Shows `<Pane Name>` + `@<office>/<pane>`, `Rev #N`, handed status pill, and a compact scope toggle (`This Setup` vs `All Setups`) plus `Inspect` and `Studio ↗` buttons.
     - **Filter Strip & Scrolling Tag Tabs:** Quick filter input paired with compact horizontally scrolling `<` / `>` tag tabs (`Pinned`, `All`, declared tags in alphabetical order, and `Kept` when undeclared stored keys exist, plus a `Modified` filter pill).
     - **Pinned Section with Reorder & Unpin:** Hand-curated `pinned` rows at the top with `▲` / `▼` reorder arrows and a `★` pin toggle (`workshop-wide` by default, configurable via `workshop.pinned-scope`).
     - **Inline Typed Controls, Lock Scope Badge, & Provenance:** Each setting row shows its key, source badge (`Master`, `Loose`, `Default`, or `Locked`), summary, inline control (toggle switch for `flag`, `−`/`+` stepper + numeric box for bounded `number`, segmented choice pills or text box for `text`), a per-key reset (`↺`) button, and a lock (`🔒`/`🔓`) button with a `Layout Lock` vs `Workshop Lock` scope popover.
     - **Footer Actions:** Summary of modified/loose/locked counts with clean `Reset Loose` and `Open Theme Studio…` buttons.
   - **Tier 2 — Full-Screen Settings & Theme Studio (`zengine.settings`):**
     - **GUI-first priority & primary mouse navigation:** Built directly on `zengine::graphics` (`Sketch`, `Button`, `Checkbox`, `ScrollView`, bordered cards, colour swatches, and clickable pills) rather than flat 80-column ASCII text tables: click into tag tabs, sorting/grouping pills (`By Pane`, `By Tag`, `Shared Key`), setup targets, and visual theme cards.
     - **Bordered containers & clean `gfx::Button` labels:** Represent a Master Theme's **Included Themes**, **Theme-Owned Settings**, and **Loose Changes** in distinct bordered containers (`Sketch::rect` / `outline_rect` / `group`) so they separate at a glance. Use real `gfx::Button` controls (`Apply Theme`, `Save Master`, `Snapshot Backup`, `Promote Selected`, `Reset Loose`) with **no `(R)` / `(P)` / `(S)` hotkey suffixes** in the button text (`Hotkeys` already owns keybinding discovery, and hover tooltips can show shortcuts later).
     - **Live Interactive Pane Samples via Compile-Time Message Elimination (`SilentMail`):** Clicking a theme or adjusting a setting shows **live sample panes** (`Terminal`, `Editor`, `View/Flow`, mini desk) fed with sample input created by each pane's owner and instantiated with a compile-time `SilentMail` / `NullMail` policy that **compiles out all bus messages at zero runtime branch cost** (rather than checking a runtime debug/sample flag at every message point) while keeping local sample drawing and mouse interaction live inside the preview stage.
8. **High-value functional settings, TUI movement gestures, and Accessibility:**
   - 65 settings scraped across panes, Workshop, the medium (`zengine.skin` / `zengine.window.terminal`), and navigation (`scrape.md`).
   - Keyboard focus actions (`focus.next`/`previous`/`left`/`right`/`up`/`down`/`enter` and global `focus.leave` closing WCAG 2.1.1 G1 and 2.1.2 G2 in Wave 14B) plus a replaceable navigation presenter (`zengine-navigation`, Wave 18) offering **jump hints** (Avy/Vimium style over `control:<id>`) and **switch scanning** (1-switch auto, 2-switch step, inverse, shared with `BL-WORK-09`'s tutorial walk) and `motion.*` action bindings (`navigation.md`).

**Wake:** met: BL-WORK-06 closed with #98 and #99 (2026-10-07); Stage 2+ & Themes research completed
([prompt](../prompts/settings-themes-research.md), [report](../reportbacks/settings-themes-research-RB.md), 2026-10-18), reviewed by Vision and amended with the founder's GUI-first & compile-time live sample design (2026-10-18).
**Source:** the founder (2026-10-07), after #96's light terminal, with the two messages and the
setup file as the store his own; and (2026-10-18) for tags, pinned items, compact scrolling tag
tabs, Workshop-wide pin scope setting, setting locks, composite themes with explicit application,
Master Theme files & auto-saved loose changes, the GUI-first Settings / Theme Studio with bordered
cards, clean buttons, and compile-time `SilentMail` live pane samples, and TUI navigation /
accessibility settings.

### BL-WORK-38 — Agents and weavers on one desk

**State:** ORDERED — resting until the roadmap (the founder, 2026-10-14), the notice's aimed
picture (#213) and the Tutor (#215) merged (2026-10-12); in build before that: stages 0, 1 and 2
merged as #150, #151 and #158 (2026-10-09),
#151's three review fixes as #155, #157 and #156 in the issue lane; stages 3a and 3b wait for the
documentation overhaul's folder move and its stages 4a and 4b (BL-ADOPT-05), and an agent's
powers are researched ahead of them (2026-10-10, below); researched
([its report](../reportbacks/agent-desk-research-RB.md): stages 0 to 7, 24 decisions); decisions
7, 9, 11, 15 and 24, then 1, 2, 3, 5, 13, 14 and 19, and 4 and 18 in part, taken as recommended
(the founder, 2026-10-09)  
**Owed:** Agents and weavers do not work well together today, and Workshop is too technical for an
average user. One desk, two presentations: the weaver's GUI, made for people, and an agent's desk, a
text presentation made for agents.
- The agent's desk is the weaver's screen as text, a grid of characters the size of the monitor, so
  the agent sees the layout the weaver sees; a text area there holds far more text than the GUI can
  show.
- One capability, two hands: the agent's message activates the same control the weaver presses, and
  neither has a capability the other lacks.
- Documentation attached where it is used, for each pane, part and shape, and a guide to the running
  desk, an AGENTS.md by purpose and best practice.
- Regions and feeds: an agent takes one area, and follows an open pane's changes as they happen.
- Experiments stay experiments: an agent compiles and runs on its own host, apart from the main
  codebase until proven, pushed and merged; the weaver's host then pulls and upgrades in place, and
  an agent can wait on a merge.
- Then the GUI gets simpler, designed for people, an average user first.

It meets BL-WORK-09, BL-WORK-25, BL-WORK-26, BL-WORK-28, BL-WORK-29, BL-WORK-35 and BL-ADOPT-04, and
Goal 5 (Tutor, Builder, Steward).

The founder's decisions (2026-10-09), the ones stage 0 needs: a guests file names its version, and
each row the panes and actions its agent may use, nothing beyond (7); an agent's message moves
neither the weaver's keys nor the selection, and on the weaver's host a guest's typed text rests in
no pane (9); on the weaver's host the Terminal answers only the weaver (11); the weaver's host loads
only bytes built from checkouts the weaver lists (15); the guests file says whose host it is, and on
the weaver's every file write, the editor office and the Terminal answer only the weaver's hand
(24).

Stage 1's, taken as recommended the same day: the grid one character to each canvas pixel, read as
the drawn runs with each part's press point, a glance, and a rectangle written out where blanks
carry meaning (1); the grid follows the canvas, not the monitor (2); the reader on the agent's host
(3); `capture` widened to stage 1's reads, said as a widening, its second room and `read` power left
to stage 5a (4, in part); a covered pane's visible words (5); readings as files on the agent's host,
never inside a source checkout (14); a tool package of its own, `desk` (19); and stages 1 to 3b
ahead of BL-WORK-09 (18, in part). The other twelve wait for their stages, 4 and 18 in part.

The stages' own decisions (the founder, 2026-10-09): stage 0's 1, a guest's carried value rests in
no pane on a weaver's host (refused, as typed text is), and its 2 and 3 kept as they landed;
stage 1's 1, the weaver's keystrokes to an observer become a power of their own at stage 3a; its 2,
the founder's way: a stamp names a picture by a fingerprint Workshop takes of what the pane sent,
for every pane, so a pane does nothing for it and an unchanged picture keeps its stamp; its 3 kept.
Decision 13 (what a notice carries), as recommended. Owed and not yet placed: decision 1's dense
reading, a rectangle of the grid written row by row, which `desk/read` does not write (#151).

Stage 2's (the founder, 2026-10-09,
[its report](../reportbacks/agent-desk-2-RB.md#decisions-asked)): the notice's cost accepted as
measured, P-WORK-50 kept open, and a burst coalesced into one notice by a message Workshop sends
itself when a real desk shows the cost (1); a pane's holder leaving between deliveries is told at
Workshop's next look, until stage 6a, which builds the better solution: Loom tells Workshop when an
office's holder leaves (2, the founder's); a follower follows one version of a notice, since Loom's
`latest` holds by shape name (3). Stage 2 took the v2s `stages.md` names for stage 5a, so 5a's
become `PaneStamp` v3, `DeskRead` v3 and `PaneView` v6, its `DeskStamps` v2 nesting `PaneStamp` v3.

Stage 4b takes the Codex's form (the founder, 2026-10-09, from the "Perspectives" proposals): a
pane where a weaver reads what a weave accepts (`zen.DescribeAccepted`, live), each pane's and
shape's declared words (stage 4a) and the refusals (`Refused`), the weaver's face of the guide an
agent reads in `guide.md`. Never prose in `zen.SchemaDesc` (decision 12's mistake).

The founder's direction for an agent's host (2026-10-09), beyond the research:
- its writes kept inside its own working folder, and anything that must run outside it going through
  the pull-request channel;
- bounded probe doors: the weaver's host offers messages that run contained work against live data
  and send back the result, each a power the weaver grants, run under Loom's isolation;
- a guide power: an agent highlights a named part to walk the weaver through a process, changing
  nothing (BL-WORK-09's tutorial outline).

The founder's direction for agents' permissions (2026-10-10), researched before stage 3a
([prompt](../prompts/agent-powers-research.md)): permissions as gates, by how much each can
bypass; a Tutor's whole use case is reading the desk and highlighting its elements, the baseline;
pressing some buttons, scoped by pane, locked setup or button; an agent building code for one
issue that touches only certain files; anything more asked for through the weaver, set up
beforehand, or shared by a more trusted orchestrator from its own limited, higher power. With
Vision's amendment, accepted: no single ladder, a role (Tutor, Builder, Steward) is a named
bundle of separate powers, each enforced on its own.

Researched ([its report](../reportbacks/agent-powers-research-RB.md), 2026-10-10; reviewed by Vision
the same day, 26 decisions asked, answered in part below): a role is a bundle of separate powers --
Tutor, Builder, Player, Orchestrator (a row with `share`) and Steward -- and every scope the weaver
may widen live is a door, `<office>/<pane>[:<id>]` or `arrange:<id>`, held as Loom authority,
matched by segment and judged by its owner at the act; the three routes on Loom's Weaver, its
prompts numbered and decided by the weaver's local hand alone, the guests file the one place
anything persists, an orchestrator's share inside a ceiling the weaver wrote; every grant lasts its
session, never a time or once; an approval holds only against a contained agent, so a row that asks
or shares says `"contained": true`; an agent's code written in a view built from Loom's isolation
primitives, and a check at the pull request refusing a path outside its issue's `## Files` block.
Its stages: `door` (Loom, beside the overhaul), `tutor` (after docs B2 and `door`), #139, 3a, 3b,
`host` (before `ask`), `ask`, `check` beside, `probe` with the Steward's first consumer. The Tutor
walked on a weaver's desk against a prototype guide mark. With #181's switch to a manual answered on
ask, a guest asks a pane's office for its manual directly, needing no `capture` door since a manual
is public, and the document declarations leave its list of host keepings. Its view probe's canary
read the founder's SSH private key through `/mnt/c` into a log deleted within a minute (none of it
found since); rotating it is the founder's call.

The founder's answers (2026-10-10): the agent the desk supports is one completely contained command
structure, with access to great power when granted, and containing today's harness (Claude Code) is
a later problem; the Weaver's decisions name their prompt now, ahead of `door`
([prompt](../prompts/weaver-decisions.md), [report](../reportbacks/weaver-decisions-RB.md)), no
public issue, as Loom #49, reviewed ready to merge, its hosted run green on all ten jobs (Vision,
2026-10-11); its names count per Weaver, so a replacing Weaver's prompt 1 could take a decision sent
to the office for the old one, and a follow-up makes a name unique among the host's Weavers
([prompt](../prompts/weaver-prompt-names.md), [report](../reportbacks/weaver-prompt-names-RB.md)),
the WeaveId addressing #49 documents kept as the second guard: Loom #51, a name its Weaver's WeaveId
times 10^9 plus its count, reviewed (Vision, 2026-10-10) and merged by the founder (2026-10-11);
stage `door`'s prompt makes `AuthorityPrompt` v3 and `RequestAuthority` v2, and binds a decision
that crosses a link to the host's lifetime too, since a restarted host gives its WeaveIds, and so
its names, again; a Weaver reloaded in place by `swap_state` (its policy refuses only crash revival)
also counts again; the highlight researched to match a press, a message resolved to the control that
sends it on a view, and a message no control on the desk sends moving the weaver to a pane or setup
that can, or improving the tool where the control belongs
([prompt](../prompts/tutor-highlight-research.md)); an issue names its bounded areas in a `##
Folders` block, not files; and agents work under a GitHub machine account of their own,
`UnknownWorkers`, that comments, makes branches, pull requests and issues, and never merges. On a
personal account's repository a collaborator has one level, write, which merges and labels (Vision,
from GitHub's own pages), so Vision recommends no collaborator access: its branches in its fork, its
pull requests from there, `ready` the founder's alone to set, and a classic token with `public_repo`
for its agents, since a fine-grained token cannot contribute to a repository its user is no member
of. Vision may speak as the founder, with his login, once they agree, and says what went out in his
name: he is the final gate for everything, and wants it open (2026-10-10). Until a session of
Vision's reaches GitHub, its issues are written into `Zen/issues/` and filed by a Ceecee once
agreed; a security defect is never one of them. An issue carries a prompt's full information, read
cold, so that once it is `ready` other agents can take it under the founder's final approval, among
them a local frontier model a friend of the founder's runs (2026-10-10). Every other decision of the
powers research taken as recommended (the founder, 2026-10-11): stage `door`
([prompt](../prompts/agent-desk-door.md), [report](../reportbacks/agent-desk-door-RB.md)) is Loom
#52, reviewed (Vision, 2026-10-11): the door's grammar, containment by segment, the disjoint axis,
`RequestAuthority` v2 and `AuthorityPrompt` v3, a describe-only capability, as the research has
them; its first run ended `success` with its three Windows jobs, advisory, red, which the report did
not read; a continuation ([prompt](../prompts/agent-desk-door-windows.md),
[report](../reportbacks/agent-desk-door-windows-RB.md)) found both causes the change's, `doc_links`
reading block comments by a pattern CMake's regex engine recurses through past a Windows thread's
stack, and the host's largest unit past a COFF object's section ceiling, and repaired each: run
`38129706119` at `23f6ce3`, every job green, the advisory ones included, reviewed (Vision,
2026-10-11) and merged by the founder (2026-10-11). Stage `declare`
([prompt](../prompts/agent-desk-declare.md), [report](../reportbacks/agent-desk-declare-RB.md)) is
Zengine #186: each action row says what a press of it may cause, with the pane's mode, the row's
`enters` and the other modes' causes, kept true by the census (`tests/actions.txt`, 49 rows) and a
press witness, which found a cause the research missed (`authoring.commit` sends
`ProjectFrontierRequested`); reviewed (Vision, 2026-10-11), run `38127055466` 8 of 8 green, ready to
merge. Zengine's CI builds against Loom's `main` as it stands at run time, and neither run built the
two together, so Loom #52 merged first and #186's run ran again against it, 8 of 8 green, so #186
was ready to merge (Vision, 2026-10-11), and the founder merged it (2026-10-11); stage `tutor` is
next ([prompt](../prompts/agent-desk-tutor.md)), after the address law, #183, taken from the issue
lane first ([prompt](../prompts/address-law.md)). Its session stopped at the Folders (2026-10-12,
[report](../reportbacks/address-law-RB.md)): the outcome makes `agents/panes.md`'s count of the
Powers and Composer rows false; the founder amended #183 with that file, the sentence naming where
the rows are declared rather than counting them, and took the session's plan (Inventory's bar
unnamed while a name is edited, the View Builder's More as `control:choices`, the demo's id `reset`,
Flow's names kept with a keyless row each, its Hotkeys list 6 to about 39, the check in the readers)
([prompt](../prompts/address-law-amended.md)); `tutor` waits for it, and fast forward's S3 too,
since #183's folders hold the tools S3 rewrites. It stopped again (2026-10-12,
[report](../reportbacks/address-law-amended-RB.md)): `tests/test_workshop_panes_actions.cpp` pins
Powers at four rows; the founder amended #183 a second time with that file, its case naming the
actions rather than counting them, one shared header for the judge of `control:` parts, and the
address law a law of its own in `pane-parts.md` rather than a share of WL-HAND-06's bullet (rule 2);
an Inventory case's one unexplained red is to be explained first
([prompt](../prompts/address-law-amended-2.md)). Fast forward S1 is Zengine #203 and Loom #54
([report](../reportbacks/fast-forward-s1-s3-RB.md)), each run green on every job (8 and 10),
reviewed ready (Vision, 2026-10-12): the Timer and the serving host nap on a high-resolution
waitable timer on Windows, falling back to `Sleep`, their witnesses reading what the clock reads and
what a nap asked; Loom #54 merges first, then #203's run again against it, then #203. The kit's
second copies sit on C: beside their trees, the quiet window 10 s (Zen `f20dd0c9`,
[report](../reportbacks/executor-kit-speed-copies-RB.md)), reviewed (Vision, 2026-10-12). The
address law stopped a third time (2026-10-12, [report](../reportbacks/address-law-amended-2-RB.md)):
a law of its own, which Vision asked for, needs its record
`agents/decisions/a-pane-names-its-parts.md` to list it, Vision's miss; the founder amended #183 a
third time with that record's line, the session listing every file the change touches before it
starts ([prompt](../prompts/address-law-amended-3.md)). The Inventory red was a stale object: the
kit's ext4 copy kept a checkout's file time, so an edit made during a build looked older than its
object; the copy now stamps the time it writes (Zen `c9011952`). S1 merged: Loom #54, then #203
after its run again against it, 8 of 8 green (2026-10-12); `main`'s run for #202, the journey in the
pool, green. Overnight (the founder's choice, 2026-10-12), beside #183, three batches from the issue
lane, each issue its own pull request from `main` and a stop moving on to the next: Zengine #116,
#110, #109 and #105, documentation ([prompt](../prompts/overnight-docs-batch.md)); Loom #33, #32 and
#34 ([prompt](../prompts/overnight-loom-batch.md)); Zengine #191 and #192, proved by loaded repeats
([prompt](../prompts/overnight-load-flakes.md)); and #188 with #103 in the Builder suite
([prompt](../prompts/overnight-builder-tests.md)). Not tonight: #199 and #200 (every test file, one
build file), #194 (needs merges to witness), #106, #107, #112 and #115 (#183's files). #114, the
Info register's split, lost its premise to #201: `info-body.md` stands at 15,642 of the whole file's
24,576, so Vision proposes closing it. The address law is Zengine #207
([report](../reportbacks/address-law-amended-3-RB.md)), `3b8c778` on `7409847`, its run
`38212810792` 8 of 8 green, reviewed ready (Vision, 2026-10-12, 10 of 10 checks): WL-HAND-07, one
judge in `tests/control_parts.hpp` read on every `held_parts`, all 26 files inside the amended
Folders; it found `tools/fill_laws.sh` not idempotent on `main` (an issue to file). Overnight,
reviewed ready (Vision, 2026-10-12, 16 of 16 checks): #204, #205, #206 and #208 (#116, #110, #109,
#105; documentation), Loom #55, #56 and #57 (#33, #32, #34; #56 routes the one page a compiled case
reads to the official lane, kept), and #209 and #212 (#188, #103); #210 and #211 (#191, #192) await
their session's report. Merge order: the documentation, then #207, #209 and #212, then Loom's after
#57's run again against Zengine's `main`. The founder merged #207 (`285ace3`), the documentation,
#209 and #212 (2026-10-12; `main` `8e0e1bf`). `tutor` and S3 start together: S3 owns `DeskStamps`'
shape (v2, each pane's aimed picture number), its producer and readers, and merges first; `tutor`
scopes who hears it on top of v2 and does the rest meanwhile, since the two share the guests file,
the grant, the guest vocabulary, the desk reads and `tests/shapes.txt`
([tutor](../prompts/agent-desk-tutor.md), [S3](../prompts/fast-forward-s3.md)).
The load flakes are #210 and #211 ([report](../reportbacks/overnight-load-flakes-RB.md)), each red
on START under load and green after, its mutations caught, 8 of 8 loaded lanes and every hosted job
green, reviewed ready (Vision, 2026-10-12, 8 of 8 checks): the pilot's paid path is asserted, not
exercised, its expectation read in the Timer's own code (`apply_ensure`, `fire_due`). Merge order:
Loom #55, #56 and #57, then #210 and #211, `main`'s run after them the check of the two together;
then the apart lists go ([prompt](../prompts/timer-probes-in-pool.md)). S3 is #213
([report](../reportbacks/fast-forward-s3-RB.md)), 8 of 8 green, reviewed (Vision, 2026-10-12, 7 of 7
checks): `DeskStamps` v2's `aimed` is a list that must line up with `panes`, which Zengine's own
rule forbids (`tests/weavelib/operator_ask.hpp`), forced by Vision's fence ("no new shape beyond
`DeskStamps` v2"); the founder amended S3 (2026-10-12): each pane's entry carries its stamp and its
aimed number, one entry shape, `v2::PaneStamp` unchanged, F5 (a) dropped, the description's private
pointers gone ([prompt](../prompts/fast-forward-s3-amended.md)); `tutor`'s scoping builds on that.
The apart lists' follow-up is #214, and S3 amended is #213 (`DeskStamps` v2 `{desk, panes}` of
`v2::StampedPane{stamp, aimed}`), each 8 of 8 green and reviewed ready (Vision, 2026-10-12, 6 of 6
checks each). The stage `tutor` is #215 ([report](../reportbacks/agent-desk-tutor-RB.md)): the
guests file's version 3 (a role, `guide`, `keystrokes`, and `capture` and `guide` doors compiled to
Loom door rules Workshop asks at each read and mark), reading by pane, the weaver-only surfaces for
every guest, the guide mark `GuideRequested{pane, control, words}`, `desk/guide` and `desk/resolve`;
20 of 20 mutations, its run 38276039798 8 of 8 green; reviewed (Vision, 2026-10-12, 7 of 8 checks,
its tests unread); it conflicts with #213 in three files. The founder took its two recommendations
(2026-10-12): `DeskStamps` stays refused to a row that reads by pane, and the text checks' `/*`
crash goes to an issue. Merge order: #214, #213, then #215 rebased onto them
([prompt](../prompts/agent-desk-tutor-continued.md)).
The founder merged #214 and #213 (2026-10-12; `main` `a2f87c9`). #215 rebased onto them
([report](../reportbacks/agent-desk-tutor-continued-RB.md)), the three conflicts resolved as both
sides (the guest vocabulary declares 103), `DeskStamps` v2 refused to a row that reads by pane in
the observation case; its run 38287005825 at `4d5f0da` 8 of 8 green; reviewed ready (Vision,
2026-10-12, 7 of 7 checks). The text checks' `/*` crash is Zengine #216, `ready`, `defect`.
UnknownWorkers' `gh` login lives in
`GH_CONFIG_DIR=$HOME/.config/gh-unknownworkers` on the founder's machine (2026-10-10). An issue
needs no approval of its own: the fix's approval is the gate, and each issue says honestly how far
it was checked (the founder, 2026-10-10); so the check at the pull request bounds a change to its
issue's folders and asks nothing of who wrote the issue. Both repositories already teach the issue's
form (`docs/contributing/taking-an-issue.md`); their `ready` issues, checked before the folder move,
are refreshed on current main with their folders ([prompt](../prompts/ready-issues-refresh.md),
[report](../reportbacks/ready-issues-refresh-RB.md)): 16 of 16 still hold (Loom #33 in part), each
with a Folders block and a Checked against saying how far its check went, no private plan id left;
the form says so in Zengine #182 and Loom #50, documentation-only, reviewed (Vision) and merged by
the founder (2026-10-11); the address law is Zengine #183, filed under `UnknownWorkers`, `ready` and
`defect` set in the founder's name, taken once B2's pull request merges, since both change the
Builder's action census; Loom #41 predates the GCC 16 experiment and holds no Folders block, so the
founder took its `ready` off until his decision (2026-10-11). The check at the pull request reads an
issue's Folders block as it stood when `ready` was set, since the account that filed an issue can
edit it after (Vision).

The Tutor's highlight, researched ([its report](../reportbacks/tutor-highlight-research-RB.md),
2026-10-11; reviewed by Vision the same day, 12 decisions asked; the address law taken for the issue
lane now (decisions 1 and 11, the founder, 2026-10-11;
[continuation](../prompts/ready-issues-refresh-address-law.md)), the rest, 2 to 10 and 12, as
recommended (the founder, 2026-10-11), stage `declare` first
([prompt](../prompts/agent-desk-declare.md))): a press and a highlight name one address,
`<office>/<pane>:<id>`, drawn by the part `control:<id>`, so five panes' control parts are renamed
to their ids (the address law, Zengine #183 in the issue lane); what a press may cause is declared
on the action row (`causes`, with the pane's `mode`, the row's `enters` and the other modes' causes,
`elsewhere`), held where Workshop holds the rows and kept true by the census, a press witness and
the manual check on `Answers`; the agent resolves (`desk/resolve`), Workshop resolving nothing;
`GuideRequested { pane, control, words }` replaces the powers research's decision 4's address and
keeps its form; a weaver is moved by the messages that show panes, never through a weaver-only
surface; a case for a tool is filed under the agents' account after asking the weaver on their desk,
under the founder's issue rule of 2026-10-10 rather than the report's founder-only `ready`; a
described view joins the pane protocol; Loom adds nothing. Its stages: the address law; tutorial
mode after it and docs B2; `declare` (the causes) after B2; `door` beside; `tutor` after `declare`
and `door`; then #139 and 3a.

The walls, outside in (Vision, 2026-10-09): a separate OS user or a VM for the agent's host, the
only wall that holds against an agent that does not keep to its doors (decision 17); its own GitHub
identity without merge rights, and a protected default branch; its experiments as weaves under
Loom's isolation host (Linux: a private file view with only its working folder writable, no network
but a broker's, resource caps; abuse-tier); in time, an agent acting only through tools that run
contained, since Loom's tools are processes of the session's user today.

**Wake:** met (2026-10-08).
**Source:** the founder with 30k (2026-10-08), from 30k's proposal "The Autonomous Foundry & The
Living Schema" and Vision's review of it.

### BL-WORK-39 — Text is UTF-8 everywhere, drawn as the industry draws it

**State:** FILED — researched first; not yet ordered (the founder, 2026-10-08)  
**Owed:** Text on Zen's screens follows the industry standard: UTF-8 end to end, every character a
font holds drawn, the rest shown by a visible stand-in. Today:
- a canvas run takes one cell per byte and printable ASCII alone (`SurfaceLabel`,
  `canvas_content_problem`, WL-CANVAS-01), and panes spell outside text in ASCII
  (`pane_text::drawable`, `ascii_spelling`);
- the standard Editor refuses a document holding any byte beyond printable ASCII and tab, whole
  (`agents/workshop/editor.md`);
- Info and the Terminal take typed ASCII; the Files pane refused a name beyond it until #102's fixes
  (WL-FILES-10).

The research settles: what a cell holds (a character, not a byte); wide characters and combining
marks in a terminal's columns; fonts and their fallback in the window; where a press lands by
column; the Editor's byte law and documents beyond ASCII; typed text in Info and the Terminal; and
the agent's desk text (BL-WORK-38).

**Wake:** the founder orders it.
**Source:** the founder (2026-10-08), on #102's report: text moves to whatever the industry standard
is.

### BL-WORK-40 — The simplest snake, played by its own AI

**State:** FILED — the founder's idea (2026-10-09; expanded 2026-10-16 with a C++ ↔ Python owner handoff candidate); not yet ordered  
**Owed:**
- The snake demo as simple as it can be. `zengine-snake` (`snake/play.cpp`) keeps only its boot
  list; the demo's operator -- the skin swaps (classic, block, SDL), loading the score weave,
  growing the world, reload in place, new game and the list -- moves out of the host, to the
  external host's driver or into a weave of its own (in #277, `examples/snake` moved its new-game
  and operator buttons to `gfx::Button` and operator asks to `AskBook`).
- An AI plays snake through messages, with no agent in the loop; an unexpected occurrence calls the
  agent in to review, so the agent improves the AI. The tower-defense example's monitor already
  takes this route: its policy plays the game from the game's own typed events and says FINISHED,
  NEEDS ATTENTION or INCONCLUSIVE, with evidence (`examples/tower-defense/monitor/td_policy.py`,
  event-driven ELH observation, Loom #16 / Zengine #62).
- **Candidate expansion (the founder, 2026-10-16):** a live owner handoff of the running Snake game
  between C++ and Python (`C++ -> Python -> C++`), proving language-neutral office/state contracts
  over Loom shapes while the `graphics/` window keeps the retained `SnakeBoard` element intact across
  both runtime transitions (joining BL-WORK-37, BL-WORK-40, and BL-WORK-13 / #147).

**Wake:** the founder selects it.
**Source:** the founder (2026-10-09), after the tower-defense route: messages received and acted on
with no agent's intervention, the agent reviewing what was unexpected; and (2026-10-16) for the
C++ ↔ Python owner handoff.

### BL-WORK-41 — The Data Conversion Mapper: a Flow view that authors a migration

**State:** FILED — near roadmap; its order is the founder's to set (the founder, 2026-10-09)  
**Owed:** a perspective where a weaver or an agent sets two versions of a shape side by side (`v1`
and `v2` of a state, say), wires their fields, and gets the migration operator it authors. The
mechanism exists: a migration is an ordinary provider-contributed operator whose signature is the
edge it converts, named `zengine.migrate.<family>.v<from>-to-v<to>` (`operator/migration.hpp`), and
Flow composes and generates operators. A wanted chain stays authored, as a composite: no route
search. It pays off at every format change, as settings stage 1's setup and session versions did.

**Wake:** the founder orders it.
**Source:** the founder's idea, with the "Perspectives" proposals (2026-10-09).

### BL-WORK-42 — The Black Box Reader: refusals read whole

**State:** FILED — near roadmap; its order is the founder's to set (the founder, 2026-10-09)  
**Owed:** P-WORK-14's answer: a reader a maker can run over the journal (`--log <path>` keeps a
refusal whole, and nothing reads it but `loom::Logger::read`), then a place, a pane, to read a
chain of refusals in order. The founder agreed it is near roadmap; it is small enough to be an
issue once its first form is chosen.

**Wake:** the founder orders it.
**Source:** the "Perspectives" proposals (2026-10-09), meeting P-WORK-14.

### BL-WORK-43 — Fast forward: a walk as fast as its messages go, and the bus measured

**State:** ORDERED — researched ([prompt](../prompts/fast-forward-research.md),
[report](../reportbacks/fast-forward-research-RB.md), 2026-10-10; reviewed by Vision 2026-10-11; its
seven decisions taken as recommended, S1 and S3 queued after the Windows lanes phase (BL-WORK-44),
now prompted together, each its own pull request ([prompt](../prompts/fast-forward-s1-s3.md)), S1
trying Windows' high-resolution waitable timer before a raised resolution (Vision) (the founder,
2026-10-11)): a walk's time is the Windows tick, not the bus or the bridge -- the Timer reads
`GetTickCount64` and `loom-host --serve` naps through MinGW's `sleep_for`, each a 15.6 ms tick -- so
three probe levers took the terminal walks from 6.5 to 32-39 steps a second (50-53 in Release),
every step judging as before; a window walk's pictures are 92-97 % of it. The bus delivers 1.35
million messages a second in Release; a weave per body is 18x the math at 100,000 bodies, and a
bridge frame carries about 16,000 bodies of four scalars (`kMaxDecodedCells`). Its stages: S1 the
Timer's fine clock and nap, S2 the serving host waking on its sockets (Loom), S3 the hand on no
clock (`DeskStamps` carrying the aimed picture), S4 pictures skipped at speed and said, S5 the door
served on arrival if still beat-bound, S6 the virtual-clock Timer as a measurement's mode; its bus
measurement to a `bench/` folder of Loom's; the game's bodies arrays in a simulation weave, batched
at the bus's edges. Its incident: a cleanup's too-wide `taskkill` ended another session's test
binary at 23:41 UTC, inside runtime-gcc16's lane, whose `workshop_load` death in that run is likely
it (Vision). S1 merged as Zengine #203 and Loom #54 (2026-10-12); S3 is Zengine #213, amended so
each pane's entry carries its aimed number (the founder, 2026-10-12,
[prompt](../prompts/fast-forward-s3-amended.md)), merged as #213 (2026-10-12); S2 and S4 to S6
wait for the roadmap (the founder, 2026-10-14)  
**Owed:** A fast-forward mode for the demo runs, as in a game: a walk goes as fast as its actions
can go, where today it reaches four or five actions a second at most; faster runs let agents work
faster. Beside it, a speed test of the message bus: math like 3D collision, on a massive scale,
toward the founder's final test of Workshop, a small 3D third-person action game.

**Source:** the founder (2026-10-10).

### BL-WORK-44 — Faster builds: the quick wins

**State:** ORDERED, first beside the documentation (the founder, 2026-10-11) — reported
([prompt](../prompts/build-speed.md), [report](../reportbacks/build-speed-RB.md)) and reviewed
(Vision, 2026-10-10); from the fast-builds research
([report](../reportbacks/fast-builds-research-RB.md)) and the C: drive test
([report](../reportbacks/c-drive-builds-RB.md)): the Windows build trees on C:, the WSL lanes from
an ext4 source copy, and CI's Q1 to Q3 (Loom without its tests, a compiler cache written only by
`main`'s runs, parallel CTest on the Linux jobs), the research's decision 1 as recommended (the
founder, 2026-10-10). Zen itself stays on G:. CI's quick wins are Zengine #180, merged by the
founder (2026-10-11), its first run on `main` seeding the stores; by job median, before against warm
over distinct runs, Linux 1,847 to 457 s, ASan 2,692 to 798, MinGW-w64 2,464 to 822; a pull
request's run reads only what `main` saves, so the first warm one follows #180's merge. The Dev
Drive measured level with plain C:, so the founder chose C: and deleted D: (2026-10-10); the kit's
Windows trees are under `C:/Users/Joshua/zen-build/` and the WSL lanes run from an ext4 copy (Zen
`7ec2f1a6`). The parallel ASan lane met a race in `workshop_journey` I1, Workshop's guest door
serving before its plan is realized (P-WORK-62): the founder kept `-j4` on both Linux jobs and took
the race to an issue (#180's decision 1, 2026-10-11), Zengine #185, `ready`
([report](../reportbacks/guest-door-readiness-issue-RB.md)), a red with only that failure rerun once
and named until its fix merges. The MSVC job now bounds a run (the founder asked, 2026-10-11): on
#181's run it spent 1,080 s compiling and 1,034 s on a serial verify. The fast-builds research's
decision 10, open, kept it bare; a measured phase, on #180's branch once its session ends
([prompt](../prompts/windows-lanes.md)), the founder's choice (2026-10-11): the cache on pull
requests (embedded debug information and a launcher in CI's configure line, not Zengine's CMake),
one bare MSVC run on `main` nightly as the stranger's proof, and both Windows jobs' tests in
parallel where they do not clash. Zengine #187 ([report](../reportbacks/windows-lanes-RB.md)),
reviewed (Vision, 2026-10-11), not yet ready: by its report's medians MSVC 2,227 s before, 1,554
cold and 890 warm, MinGW-w64 856 to 464; `workshop_journey` runs alone on both Windows jobs, its
race met on MSVC too, and `timer` since #187's first run met it (P-BUILD-01); the run at `a86e349e`
ended green, 8 of 8, on its MSVC job's second attempt, the first cancelled at its limit on a slow
runner (P-BUILD-09), and the report records the end; its Counts and the pull request's Evidence miss
proof F's ASan red, so a continuation names it, adds the Linux jobs' list to #187 and files the
path-bound `builder` case as an issue ([prompt](../prompts/windows-lanes-run-end.md)). The founder's
decision 1 (2026-10-11): all four build jobs keep `workshop_journey` apart until #185's fix merges,
replacing the rerun-once rule, and a follow-up after the fix takes it out of all four. The
continuation did so: proof F's red is `audit_probes` probe D, a fixed 400 ms real-clock window under
ASan load (P-BUILD-13), not #185's race; the pull request's text is true; the `builder` case is
Zengine #188, `ready`; #187's run at `63edf86` 8 of 8 green, reviewed (Vision, 2026-10-11), merged
by the founder (2026-10-11), the proof branch deleted; its 17 caches, about 7.8 GB of the
repository's 10, remain until deleted or evicted. `audit_probes` kept apart on the Linux jobs too
until its repair (the founder, 2026-10-11), `timer` and probe D to the issue lane, and #185's
comment corrected to leave its fix inside its folders
([prompt](../prompts/windows-lanes-after-merge.md)). The cold builds after Loom #52 were Loom's
merge, not the stores (P-BUILD-14). After the merges, the `timer` and probe D issues are Zengine
#191 and #192, `ready`, and `audit_probes` apart is #193, whose run is the first to build `main`'s
merges together, since `main`'s own runs did not (P-BUILD-15): 8 of 8 green against Loom #53, MSVC
and `snake` included, reviewed (Vision, 2026-10-11), ready to merge alone, so that `main`'s run for
it saves every store against the new Loom, MSVC's first. The kit's own quick wins, Q4 to Q6, Q7's
issue and a slot given in turn, were prompted for a quiet window after docs B3
([prompt](../prompts/executor-kit-speed.md)), and the founder started the phase (2026-10-11),
`run-end.sh` added to it as a continuation ([prompt](../prompts/executor-kit-speed-run-end.md)); the
founder then tries the machine whole with several sessions, and what moves to an external host is
judged from the slot's waits (the founder, 2026-10-11): evidence-only lanes, never bytes a weaver's
Workshop loads (decision 7). The phase landed as Zen `ee2d32fb`
([report](../reportbacks/executor-kit-speed-RB.md)), reviewed (Vision, 2026-10-12, 8 of 8 checks, by
reading: no measurement rerun while two sessions held the slot): a second WSL tree 392.8 to 267.9 s
(243 of 303 hits), a Windows tree of one checkout 403.8 to 340.2 s, a test-only edit 239.9 to 179.0
s (`timer` 12.7 s), a same-bytes Loom reinstall 34.2 s to nothing, a Windows build's turn in the
order asked (waited 359.5 to 36.4 s); every lane whole under the settings; Zengine #199 (test
definitions carry absolute paths) and #200 (the load suite's reload copies), read cold, `ready`.
#200 quotes VM-LANE-11 as it stood before #198 narrowed it to what a tree builds. The founder took
both as recommended (2026-10-12): a phase's second copy cloned on Windows under the kit's root,
beside its trees, the primary and his checkouts unmoved, and the slot's quiet window at 10 s, landed
once nothing reads the kit, with a comment on #200
([prompt](../prompts/executor-kit-speed-copies.md)). The kit still taught the delivery from
before 2026-10-10 (`pass-tools/executor-kit/README.md:97-111`), so phases ran the full lanes before
the push: #340's local runs took 227 minutes, 64 of them in 19 loops of 62 entries each, each loop
measuring all the branch had changed (Vision, 2026-10-20). The founder's direction (2026-10-20): the
change's own suite while working; the local proof and the diff read before the push; the official
lane, the mutation matrices, the witnesses and any lane rule 6 asks for after it, while the hosted
run runs; the witness's Windows tree without the suites; prompted for once G2 stage 1's session
ends ([prompt](../prompts/kit-standard-delivery.md)). Vision set aside an issue to shorten
`neovim_journey`, every full lane's floor at 212 s: run beside the hosted run, the lane holds no
one up. The phase landed as Zen `a4c3df04`
([report](../reportbacks/kit-standard-delivery-RB.md)), reviewed and accepted (Vision, 2026-10-20,
6 of 7 checks, one in part): a test-only loop 68 to 77 s against #340's 246 to 252, the change's
own suite after a product edit 12.6 s, the SDL tree's first build 130 s against 468; `affected`'s
rules kept, since the journeys are reached through Workshop's own program, not the blanket rule.
What a build weighs, measured (Vision, 2026-10-20,
[handoff](handoffs/dll-size-and-compile-time.md)): 90 % of a weave DLL is debug information and
names, 74 % of the compile time is test objects. The founder's order (2026-10-20): the cheap cuts
before G2's stage 2 -- line tables on CI's GCC jobs, a cheaper facet merge, SDL measured before
anything more is cached for it ([prompt](../prompts/lighter-builds.md)); splitting
`tests/workshop_support.hpp`, the largest lever, after G2, which rewrites the rigs and deletes the
Skins and the seam that header carries. Then the founder's call (2026-10-21), measuring stopped:
CI's GCC jobs and the kit's GCC trees without debug information (`-g0`), the sanitizer builds with
line tables (`-g1`), a weaver's Debug build untouched
([continuation](../prompts/lighter-builds-g0.md)). Reported
([report](../reportbacks/lighter-builds-g0-RB.md)) and reviewed (Vision, 2026-10-21, 6 of 8
checks): Zengine #343 green in every job at `2b3cbf38`, ready to merge, `main`'s first run after it
cold in the GCC jobs; the kit's trees at `-g0`, the sanitizer's at `-g1`, `KIT_DEBUG=g` for a
debugger (Zen `9044b88e`). Measured on one runner per job, `-g1` against `-g` builds 7 to 12 %
faster with 16 to 33 % fewer object bytes; `-g0` unmeasured on the runners. The facet merge is not
where the time is (0.14 s counted once), so no pull request. SDL is about 2 % of a cold Linux job
and 5 % of a warm one: nothing cached. The MinGW-w64 assembler, about 40 s of a heavy object's
71 s, is sections and symbols, four for each of some 24,000 functions, not debug information.  
**Owed:** Every pull request waits on its hosted run since the local proof became the change's own
cases (constitution section c), so CI's length is the wait: #340's ran 52 minutes, its builds 18
to 35 minutes a job against 1 to 2 on a run whose cache hit, and its ASan job took 51:52 of a
60-minute limit; the Windows trees on C: were 2 to 17 times faster than on G: in the C: test.

**Source:** the founder (2026-10-10).

### BL-WORK-07 — The View Builder's polish

**State:** CLOSED — merged as Zengine #87 (`80c1e95`, 2026-10-03), from
`prompts/view-builder-polish.md` and `prompts/view-builder-size.md`  
**Owed:** A middle-button drag pans the design canvas, as it pans Flow's. A moved or resized
element snaps to a grid and to the edges of the other elements. Edge handles join the corner
handles, so one side can move alone.
The founder added the view's size to it (2026-10-03): a size the weaver sets by hand, which the
canvas draws the view in and the running view asks its pane for. The grid is off by default,
its size the weaver's to set (`prompts/view-builder-size.md`).

**Wake:** met: #86 merged (2026-10-03).
**Source:** the founder's notes, ordered with Vision (2026-10-03).

### BL-WORK-08 — Quick desk fixes

**State:** CLOSED — merged as Zengine #88 (`dd5ebf9`, 2026-10-04), from
`prompts/quick-desk-fixes.md`  
**Owed:**
- The window opens whole on the screen, centred, and stays on the screen while it resizes during
  load. Today it can open partly out of bounds.
- Layouts, the tab row, is on every desk by default, agent-run setups included. Today a demo
  setup can leave it out.
- Escape deselects, as a default every pane has: first what the pane has selected, then the pane
  itself, once the pane hands the Escape back unspent (`PaneEscapeUnspent`). Today a pane that
  never says so keeps every Escape.
- `external-host/demo.py`, the agents' demo launcher, says a start `failed` at the desk when the
  setup seats a described view, and its `stop` says `readiness deadline expired: None` when a
  pane refuses the quit.
- Inventory holds up to 36 portable views, not 12: single boxes of actions may be common enough
  to flood twelve (the founder, 2026-10-03). Workshop's own ceilings rise with it, to 96 (the
  founder, 2026-10-03): a session's catalog and one desk each hold at most 32 panes today, every
  pane counted (`kMaxPaneCatalogEntries`, `kMaxSetupPanes`), and the standard panes, Info's four
  views and eight made views already come to about 30.
- Inventory keeps up to 512 configured command hotkeys, not 16, and up to 512 can be on at once,
  each reaching its command (the founder, 2026-10-03). Nothing gave sixteen a reason. A bound on
  configured hotkeys stays because items in different views can share a key; hotkeys that are on
  never share one, so the keyboard itself bounds them, and they are the weaver's own choices.
  Three limits stop them first today: Desktop admits 24 switched-on shortcuts from one provider;
  Workshop takes 32 application rows, Desktop's own four included (`kMaxAppActionRows`, whose
  comment calls more "claiming the keyboard"); and Workshop delivers a shortcut only to an action
  its pane declared, while a pane declares at most 32 rows (`kMaxPaneActionRows`). The main
  Inventory pane declares a row for every configured hotkey beside 17 of its own, so a sixteenth
  hotkey already overflows it.

The file picker these notes also asked for is its own item now (BL-WORK-17, 2026-10-03).

**Wake:** met: #87 merged (2026-10-03).
**Source:** as BL-WORK-07; the two `demo.py` faults are from the View Builder's
reports (`reportbacks/view-builder-canvas-RB.md`, `view-builder-fixes-RB.md`), added with the
founder's OK (2026-10-03).

### BL-WORK-09 — What the canvas unlocks for every pane

**State:** ORDERED — fifth in the founder's order (2026-10-03; renumbered 2026-10-05), after BL-WORK-06
and the settings (BL-WORK-36, the founder, 2026-10-07)  
**Owed:** Once every pane draws on the canvas, every pane can have:
- A hover cue on whatever a press would activate, from `PaneCanvasHover`.
- A `?` at the pane's top right when the pane offers a summary or a tutorial. Workshop draws the
  mark; the pane supplies the guide.
- Tutorial mode: shifting outlines walk through the pane's own parts in turn, and the places that
  take a drop are outlined in another colour. It never reaches into another pane.

**Wake:** BL-WORK-36.
**Source:** as BL-WORK-07. It also serves Task 6 of `private/goals/stranger-legible.md`.

### BL-WORK-10 — Info rebuilt as a one-slot inspector

**State:** ORDERED — eighth in the founder's order (2026-10-03; renumbered 2026-10-05), after
BL-WORK-16 and BL-WORK-17  
**Owed:** The founder's picture of Info, seeded in `private/pressure.md` §7: a weave of many
panes, rebuilt with today's Info as a quarry, that takes anything dropped on it or picked in its
selection mode and edits it in fields with boxes. One piece serves it and BL-WORK-09: each pane's
parts and their boxes, read from the pane's press map. Selection mode is how Info, and later the
UI-editing overlay, reach those parts.

**Wake:** after BL-WORK-17.
**Source:** as BL-WORK-07; the seed in `private/pressure.md` §7.

### BL-WORK-11 — Images

**State:** ORDERED — ninth in the founder's order (2026-10-03; renumbered 2026-10-05)  
**Owed:** The canvas draws an image, and a view description holds an image element. A terminal
shows a fallback derived from the picture. An image is one kind BL-WORK-37's drawing door would
carry; its research decides whether Images waits for it (2026-10-07).

**Wake:** after BL-WORK-10; it needs the whole pixel (BL-WORK-05).
**Source:** as BL-WORK-07.

#### BL-WORK-37 — The skin's drawing door

**State:** ORDERED, STAGES 1–7 AND READABILITY PASS MERGED (`#218`, `#219`, `#296`–`#311`), STAGE 7 POLISH (`7D`, `7E`) PROMPTED
— [round 1](../prompts/graphics-weave-research.md),
[round 2](../prompts/graphics-weave-research-2.md),
[round 3](../prompts/graphics-weave-research-3.md),
[round 4](../prompts/graphics-weave-research-4.md),
[round 5](../prompts/graphics-weave-research-5.md); stage 1, the snake
([prompt](../prompts/graphics-stage-snake.md)), amended from rounds 4 and 5 (the founder,
2026-10-13; filed 2026-10-07); stage 2, one action path and `Attention` + `Connections` on `graphics/`
([prompt](../prompts/graphics-stage-2-panes-and-actions.md), merged as `#296` / `bf3981e`, 2026-10-17);
stage 3, three parallel lanes ([3A single panes](../prompts/graphics-stage-3a-single-panes.md) /
[report](../reportbacks/graphics-stage-3a-single-panes-RB.md) `#297` `7457af1`,
[3B multi-pane seats](../prompts/graphics-stage-3b-multi-panes.md) /
[report](../reportbacks/graphics-stage-3b-multi-panes-RB.md) `#298` `f75cc13`,
[3C data-as-UI presenter](../prompts/graphics-stage-3c-data-ui-presenter.md) /
[report](../reportbacks/graphics-stage-3c-data-ui-presenter-RB.md) `#299` `aad758c`, 2026-10-17);
stage 4, three parallel lanes ([4A canvas panes](../prompts/graphics-stage-4a-canvas-panes.md) /
[report](../reportbacks/graphics-stage-4a-canvas-panes-RB.md) `#302` `91b9b21`,
[4B editors](../prompts/graphics-stage-4b-editors.md) /
[report](../reportbacks/graphics-stage-4b-editors-RB.md) `#301` `99a08ea`,
[4C projection and stand-in unification](../prompts/graphics-stage-4c-projection-and-standin-unification.md) /
[report](../reportbacks/graphics-stage-4c-projection-and-standin-unification-RB.md) `#300` `e43c45d`, 2026-10-17);
stage 5, three parallel lanes ([5A Workshop arranger](../prompts/graphics-stage-5a-workshop-arranger.md) /
[report](../reportbacks/graphics-stage-5a-workshop-arranger-RB.md) `#304` `a9d5c99`,
[5B unified WindowDrawing and caret](../prompts/graphics-stage-5b-window-drawing-and-caret.md) /
[report](../reportbacks/graphics-stage-5b-window-drawing-and-caret-RB.md) `#303` `44a8bc2`,
[5C Hand unsettled retry and story_journey U2](../prompts/graphics-stage-5c-point-reader-unsettled-and-story-journey.md) /
[report](../reportbacks/graphics-stage-5c-point-reader-unsettled-and-story-journey-RB.md) `#305` `2ab3de0`, 2026-10-17);
stage 6, three parallel lanes ([6A window extent, text & overlays](../prompts/graphics-stage-6a-window-extent-text-and-overlays.md) /
[report](../reportbacks/graphics-stage-6a-window-extent-text-and-overlays-RB.md) `#308` `238bb70`,
[6B seat caret & View on WindowDrawing](../prompts/graphics-stage-6b-seat-caret-and-view-window-drawing.md) /
[report](../reportbacks/graphics-stage-6b-seat-caret-and-view-window-drawing-RB.md) `#307` `7b1ab14`,
[6C builder & monitor aimed retry](../prompts/graphics-stage-6c-builder-monitor-aimed.md) /
[report](../reportbacks/graphics-stage-6c-builder-monitor-aimed-RB.md) `#306` `1d11677`, 2026-10-18);
stage 7 wrap-up, three parallel lanes ([7A window load plan & SDK install](../prompts/graphics-stage-7a-window-load-plan-and-sdk-install.md) /
[report](../reportbacks/graphics-stage-7a-window-load-plan-and-sdk-install-RB.md) `#311` `5926167`,
[7B terminal resize re-offer](../prompts/graphics-stage-7b-window-terminal-resize.md) /
[report](../reportbacks/graphics-stage-7b-window-terminal-resize-RB.md) `#310` `5918a4b`,
[7C builder.choose, Monitor.rows & act.aimed](../prompts/graphics-stage-7c-builder-choose-monitor-rows-and-act-aimed.md) /
[report](../reportbacks/graphics-stage-7c-builder-choose-monitor-rows-and-act-aimed-RB.md) `#309` `7ed868c`, 2026-10-18);
stage 7 follow-up polish, two parallel lanes prompted ([7D settled banner & window plan input row](../prompts/graphics-stage-7d-settled-banner-and-window-plan.md),
[7E terminal input yield & graphics resize doc](../prompts/graphics-stage-7e-window-terminal-input-yield.md), 2026-10-18)  
**Owed:** A pane asks the skin to draw, and the skin keeps what it was asked:
`draw_rectangle name="mine" pos=(0, 0, 100, 50) color=RGB(60, 0, 160)` builds a draw function in
the skin, kept under the pane and its key and called every frame the skin draws until the pane
changes or removes it -- reference Zengine's `game_graphics`
(`Zengine/reference/src/zengine/graphics/`), whose draw list was cleared each frame, kept instead.
A pane draws from its own 0,0 as far as it likes, and the skin shows what falls in its area. Roles
stay a way to follow a theme; a pane may also give a colour itself, or take one from its settings
(BL-WORK-36). The kinds grow one at a time, each drawn as well as a skin can: borders, filled
rectangles, ovals, lines, polygons, images (BL-WORK-11), shaders on an area, and whole widgets --
a colour picker from a skin built on ImGui, its value coming back as a message. Each skin says
which kinds it draws, so a terminal can decline a shader and the pane choose another way: the skin
decides how, or whether, it draws what is asked.

The research settles: items sent together appearing together; an item's order, said as simply as
it can be -- reference Zengine's layers are not taken on, and a layer control is added one at a
time, only when pressure asks; a pane's budget; a skin replaced live keeping its items without
breaking the draw cadence; input to a skin's own widget, and its value back to the pane; and what
Workshop reads pictures for today -- agents reading words, parts and points (BL-WORK-24), and the
fence a press is judged against -- moving to the skin, which knows where each keyed item landed,
so a key may be the name an agent presses a part by. A move would then cost a pane nothing, and
one pane's change redraw one pane (P-WORK-50).

**Direction (the founder, 2026-10-12)**, after Vision measured why pane files grow (panes times
Workshop-wide features, each wired by hand in every pane; the Builder pane 56 KB on 2026-09-07, 151
KB on 2026-10-11): a graphics weave, a skin or theme manager, keeps what every participant has said
it draws -- what, where and how -- instead of the skin, and gives each task to a registered skin; a
pane may register its own skin, and another may be chosen at a whim; aspects of skins compose, as
themes. A skin draws UI as data onto a window the graphics weave manages and offers (a window weave
of its own once that process is codified), and the snake's skin swap runs through it. Panes stay
isolated from each other, yet dynamic and reactive enough to work together, with no large base
class: features like the manual, default keys and context-menu items are added on request, filling
small message schemas with what each needs, perhaps with a weave answering only messages whose
permissions it set up during that step.

Then (the founder, 2026-10-12, before the research is written): what to research first. Helper
functions after his old drawing library's pattern make the messages easy to write, for a human or an
LLM -- `drawRectangle("PlayerHitBox", x, y, h, w, Colors::Red);`, perhaps with overloads for layers
-- and the graphics system is the test for helper functions in general, later carrying rich text,
images and more. No mega file: a distributed system of components with simple outputs, graphically
Turing complete in a sense, and as close to ideal code to write as possible.

The stage `tutor` (#215) draws its guide mark in Workshop, in a surface role of its own, and leaves
a row that reads every pane all their pixels (WL-GUIDE-03); both are the graphics weave's to settle:
where a mark lives, and a picture withheld by region (Vision, 2026-10-12).

Researched once ([report](../reportbacks/graphics-weave-research-RB.md)): a graphics weave that
keeps named items and routes them, skins that paint and keep nothing, a window that stacks, three
kinds, the helpers measured with 42 fresh writers, the snake moved in scratch; 16 decisions,
reviewed (Vision, 2026-10-12). The founder did not take them (2026-10-12): `DrawnItem` is a glob of
different concepts. Components instead: a suite of minimalist GUI elements -- text, text boxes, SVG
icons, images, lists and so on -- all expressible through Workshop's own panes and views and in data
form, each with its own ways to be initialized (an SVG from a file or raw vector data, an image from
PNG bytes or a link), each a minimal, complete vertical slice that communicates by messages and acts
however is best; a text editor weave using Python syntax for edits on files it has permission for,
and helping with regex, as one to imagine. The minimal set is a lot: support one way, optimize it,
leave each expansion as a specific seam note (an issue), and get a complete set -- a full set of
graphical operators and a full suite of basic GUI elements from which everything else arises, then
optimize the basics. Update only what changed: the board is not sent every frame, since the graphics
weave already knows what and where it is. A simple, efficient snake game is the litmus test for a
solved design.

Then (the founder, 2026-10-12): build up, not down -- `DrawnItem`, or its successor, is the
primitive all things reduce to in the end, with diverse things living on top of it, so someone else
can later make a "RecyclerListView" that people use as easily as if Zen had built it. The default
operators on all sides hold what someone new to a language would expect without asking, like a
simplified calculator (a square root and logs; what is easily made on the spot may be left out);
whether a repeat or a grid earns a primitive, he is not sure. Round 2 prompted
([prompt](../prompts/graphics-weave-research-2.md)). The operator package's own default set is five
Int primitives today (`math.add`, `math.max`, `compare.less_int`, `logic.select_bool`,
`logic.select_int`): a calculator's set over Int and Float is bounded work, an issue to file
(Vision, 2026-10-12).

Researched again ([report](../reportbacks/graphics-weave-research-2-RB.md)): one primitive, a node
(path, operator, operands), with meaning in element records above it; seven operators every medium
draws; eleven elements as vertical slices, placed by the split rule; a stranger's recycler list
loaded and used as easily as ours; the snake's tick 619 bytes in 5 messages, beside today's 72 in 2
and round 1's 1,322 to 1,586 in 6; 13 decisions, reviewed (Vision, 2026-10-12). The founder took
its direction with a correction (2026-10-12): splitting one job across the keeper, a skin weave,
the window and the medium put a copy and a vocabulary at every hop and made the keeper the
bottleneck. Build the window system now; windows handle their own inputs; the graphics weave is
mostly a go-between; no one central code file. Vision's correction, taken: the graphics weave
introduces a pane to its window, and again when it moves, and stays off the hot path, keeping no
copy. Round 3 prompted: a window weave per OS window or terminal keeps the one retained copy, paints
with the skins it loads and routes its own presses and keys; the graphics weave is a directory; one
platform pump per process where the platform has one input queue (SDL). Round 2's decisions 2 (a
group is a layer; room, an integer layer) and 10 (the eleven seams filed as issues once 1 to 9 are
taken) wait for the founder. Whether Zen splits other jobs this way is BL-WORK-45.

Round 3 reported ([report](../reportbacks/graphics-weave-research-3-RB.md)) and reviewed (Vision,
2026-10-12, 11 of 12 checks): a window weave per OS window or terminal keeps the one retained copy,
paints with skins loaded as code (one C symbol on the provider seam's conventions), composes, writes
its device and judges presses; the directory introduces areas off the hot path; one pump a process.
A snake tick 202.9 bytes in 2 messages (round 2 619.1 in 5, today 72 in 2); two copies of a picture
against four; a fresh directory costs no picture byte; a pane moves between windows in 6 messages,
1,293 bytes. Not less code: the showing job 1,663 lines in round 2, 2,423 here, 268 of them painting
on demand and its index, forced by Vision's fence against a painted cache in the window, which
Vision withdraws. Built for presses and keys only: pointer motion, drags, wheel, hover, carry and
custody were neither built nor measured, and the census found them the reason Workshop keeps
arrangement beside composition (BL-WORK-45), so where arrangement lives is settled before Workshop's
panes move to windows; the snake's stage needs none of it. A skin as code loses only a skin out of
process: in process a skin weave's crash and stall were already shared, since dispatch is
single-threaded. Code shrinks where panes stop drawing by hand, through the elements and data-form
views, not by moving Workshop's window job into windows (Vision). Loom gap: a loaded weave cannot
read its own id, the Kernel setting only its adapter's (`src/kernel/kernel.cpp:1204`). Nine
decisions; the report's next is the first stage, the snake in a window doing the whole job, its
terminal built.

Then (the founder, 2026-10-12): why a snake tick costs 203 bytes on the bus in round 3 against 72
today, when sending less was the aim. Vision: today's 46-byte `SnakeVisual` is small because every
skin knows the snake; round 3 describes each change in full (name, operator as a word, operands
wrapped with their type), about 50 bytes for about 3 of fact; at the terminal round 3 is at the
minimum (32.5 bytes a tick against about 548 computed for today's classic skin). His principle:
input and visual output are two sides of one coin, each needing only minimal information, every
abstraction beyond it weighed on its own efficiency (ease of use, CPU, fewest calls), optimizing for
all. His idea: a game teaches its language up front and sends only data. Vision's correction, taken:
the translator pays only loaded into the window, as skins are -- inside the game the drawing still
crosses, and as a participant between both cross (round 2: +1 message, +204 bytes a tick) -- the
game choosing an element (the board a grid) and sending its changes (`UiGridSet`, 63 bytes a tick in
round 2), behaviour staying the owner's. Round 4 first, stage 1 waiting (the founder, 2026-10-12).

Round 4 reported ([report](../reportbacks/graphics-weave-research-4-RB.md)) and reviewed (Vision,
2026-10-12, 12 of 12 checks): the window presents elements from code it loads as it loads a skin
(`ElementPut` once, then `ElementChange{ref, kind, change}`, the change's shape implied), keeps
their state and its own painted cells; the snake's board as the game's own element (`SnakeStep{head,
freed, food, dead}`). A snake tick 67.0 bytes on the bus in 2 (today 72.0, round 3 196.4), 26 of
them the probe's clock, which stage 1 folds into the world (about 80 in 2 against today's 111 in 3,
summed from measured parts); the change 41, 30 of them Loom's envelope; the terminal 33.3 bytes a
tick against today's 548.0, measured. Kept: the element in the window, its short reference, an
operator implying its operands' shape, the painted cells; dropped: names said once, the operator as
a number, a palette index. Costs: the element seam carrying state in and out (336.0 bytes a tick,
1,151.4 for the generic grid), dearer first says and fresh windows, the window 1,660 lines, four
gaps found by reading; CPU not timed apart from the instruments. Eight decisions, recommended as
asked, the game's own board among them (the founder's idea); the founder ordered one more experiment
first (2026-10-12): the shape stressed until each workload breaks, up to an OS window drawn through
SDL's software and GPU renderers on the Windows tree, timed with the instruments off -- what Zengine
#120 (BL-ADOPT-03) waits for.

Round 5 reported ([report](../reportbacks/graphics-weave-research-5-RB.md)) and reviewed (Vision,
2026-10-13, 12 of 12 checks): round 4's shape grown until each workload broke, timed in optimised
builds with the probe's instruments compiled out, on the terminal (WSL) and on an OS window through
SDL3 on Windows. It broke first in the probe's own code -- the window's structures cost the area,
not the change (256 meters changing every frame 87.5 ms a frame, 4.75 remedied) -- and then in the
shape: each drawing shown as it came (256 areas 111.6 ms on the OS window, 5.4 shown once a frame on
a beat), an element's whole state through every call (one cell of a 100 x 40 grid 7.88 ms, 0.073
with the code keeping its state), a node a cell (a 100 x 40 screen 34 ms, 0.83 as one node), data
past Loom's 65,536 cells a value (paged instead), the OS window made again on a reload (56 ms, 3.1
handed over). Remedied, a 60 Hz frame holds about 768 elements changing every frame, 256 areas, a
400 x 160 screen as one node, a billion-row list paged; a change costs about 20 us, 13 of them the
element and skin seams. SDL's renderer never broke: six GPU renderers draw the same picture to the
bit, a lattice filling the window 1.16 to 1.44 ms a frame against 5.6 on the CPU, so SDL's GPU API
stays out. A key waits where the Timer naps (25.7 ms on a beat of one phase, 11.2 in two, 0.2 with
the nap woken by input; P-WORK-70). Where it loses: the snake's tick, 75 to 95 us against today's
32.7, under 0.1% of a core; a whole screen every frame is two to four times faster than today's.
Nine decisions, taken as recommended but the ninth: Zengine #120 stays parked until stage 1's window
exists, this round's harness and figures its baseline (the founder, 2026-10-13). Stage 1 amended
from rounds 4 and 5.

Stage 1 reported ([report](../reportbacks/graphics-stage-snake-RB.md)) as Zengine #218, four
commits, green on all eight hosted jobs at `d601d1f4`, 12 mutants caught, and reviewed (Vision,
2026-10-13, 10 of 10 checks): `graphics/` (the vocabulary, the canvas, the seven operators, the
terminal window in five files, 1,361 lines, the directory, the two seams, the classic and block
skins as painter libraries); the world the whole game, its board the game's own element, the
adapters gone; the Skins no longer know the snake. A tick 68.0 bytes on the bus (today 72.0), 27.5
to the terminal (567.0), 98.5 us (38.7). Readability, the founder's focus: the drawing reads as he
wanted, element code is a small pure struct, a skin is a look in 29 lines; but every drawer repeats
the room's handshake (the score weave 77 lines, about 3 of them drawing), the world's state keeps
where its board is shown, `show` must end every drawing handler, an element's changes are numbered
by their place in a tuple, about twenty new terms, and the snake example grew from about 690 lines
to 1,150. The report's five decisions taken (its fourth cites P-WORK-67 for per-row grants, which
are P-WORK-68). The founder merges #218 as it stands and orders one readability pass before stage 2
([prompt](../prompts/graphics-readability.md)): the handshake the library's, showing that cannot be
forgotten, a room naming the elements its window holds, a change type checked at build time; stage 2
takes the tick's time (the founder, 2026-10-13).

The readability pass reported ([report](../reportbacks/graphics-readability-RB.md)) as Zengine #219,
two commits, green on all eight hosted jobs at `027d6e5a`, 14 mutants caught, and reviewed (Vision,
2026-10-14, 13 checks run of 13, 12 passing; its builds, mutants and bench read from its evidence,
not rerun): `graphics/drawing.hpp`'s `DrawingWeave` owns the room's handshake and shows at the end
of every delivery (Loom's `after_delivery`), a drawer writing `picture` and an optional `on_room`;
the window sends the room, naming the elements it holds (`AreaRoom` 2), so the world's state keeps
no window; a change type outside its list does not compile. The score weave 77 lines to 49 (its
class 15, 4 of them drawing), the world 362 to 325, the operator 411 to 402, no `show()` left in
them; a tick 68.0 bytes on the bus and 27.52 to the terminal, as on `main`, 104.7 us against 99.4.
Its finding, by reading: growing the world, the heir's first tick sends a seeded game to the old 24
x 16 board in cells of the new 48-wide one, so the board likely blanks for a frame before the
inherited board lands, unwitnessed, the live walk never pressing `3`; filed and taken in the
ready-issues batch (merged as #233, `a48edc7`). Its two decisions as Vision put them: a room taken
on the window's word, a window office being a load plan's grant (asked again once strangers bring
windows); a refused presentation unmarking its element waits for the pane work. The founder merges
it as it stands (2026-10-14). Its two roadmap seams — P-WORK-72 (one end-of-delivery hook a weave)
and P-WORK-73 (a resize reaches no drawer) — were closed in Phase 1A (#265, `8b26fd7`, 2026-10-16);
Phase 1C (#267, `c2f2a5a`) added `wants_area_pointer` and pixel-relative area pointer events; Phase
4C (#276, `32f4e45`) split `graphics/elements.hpp` into per-part headers (`graphics/element_*.hpp`);
and Phase 5C (#277, `504ecf4`) moved `examples/snake`'s buttons to `gfx::Button` and operator asks
to `AskBook`.

**The window is graphics'** (the founder, 2026-10-14): storage and distribution belong to a graphics
weave, so drawing to a window needs a graphics weave and never a Workshop file. Workshop's
composition, arrangement and routing move there whole over stages 2 to 5, which the census's lesson
(a press crosses once) keeps in one window weave.

**Stage 2 and the solidified data-as-UI + presenter end-state** (the founder, 2026-10-17;
[prompt](../prompts/graphics-stage-2-panes-and-actions.md),
[report](../reportbacks/graphics-stage-2-panes-and-actions-RB.md)): Stage 2 (`#296`, merged as
`bf3981e`, 8 of 8 CI jobs green on run `39037359516`, 12/12 mutants caught, reviewed ready by
Vision 2026-10-17) introduces `PaneDrawingFacet` (`workshop/pane_facets.hpp`) and `drawn_rows`
(`workshop/pane_drawing.hpp`, reusing `graphics::term::spaces` and `Painter`) so a pane weave writes
one `picture(gfx::Sketch&)` and one `on_action(id, mail)` serving both `zengine.window.*` and
`zengine.workshop`, and rebuilds `Attention` (`attention/pane.cpp`, retiring its 48-line carried
`ListWindow` in favor of `component::cursor_window`) and `Connections`
(`external-host/connections-pane/pane.cpp`) on `graphics/`. Before starting Stage 2, the founder
shared the solidified long-term vision so Stage 2 introduces no roadblocks: UI can be a relatively
small JSON-like view file that hooks into its surroundings through an owner who has paired that view
with a presenter, using hierarchical names (`path`s) and `action` ids to functionally link into the
web of weaves, while keeping the manual C++ `Sketch` path accessible and enjoyable to use. Three
guardrails govern Stage 2 and subsequent stages: (1) no coordinate hit-testing in owners (interactive
items speak by `path` and `action` id via `ElementRecord`), (2) clean separation between owner domain
state / `on_action(id, mail)` and `picture(gfx::Sketch&)` (the exact seam a JSON-view presenter
fills), and (3) one drawing and action contract across standalone windows and Workshop panes.

**Stage 3 (Wave 8 — three parallel lanes, CLOSED 2026-10-17 — `#297` `7457af1`, `#298` `f75cc13`, `#299` `aad758c`):**
After `#296` merged as a tight 2-pane slice, the founder ordered scaling up Stage 3 across three
non-overlapping parallel lanes, and added the standing multi-lane rule that executors may step
outside their initial file list whenever needed provided they check with sibling lanes first and
record every out-of-scope file and why in their report-back:
1. **Lane 3A — Single-Pane Suite** ([prompt](../prompts/graphics-stage-3a-single-panes.md),
   [report](../reportbacks/graphics-stage-3a-single-panes-RB.md), PR `#297` merged as `7457af1`, 13 files,
   8 of 8 CI jobs green on run `39056554015`, 19/19 mutants caught, reviewed ready by Vision
   2026-10-17): upgrades `workshop/pane_drawing.hpp` (`rows_sketch`, emitting disjoint
   `parts/<row>.<run>` nodes in front of row text so overlapping parts resolve to `RowMap::at`'s
   winner rather than paint-order rank) and `PaneRowsFacet` (`workshop/pane_facets.hpp`, mapping a
   window's `ActionRequested` back to the pane's own
   `RowPress{.row, .column, .keys_went_here = false, .window = true}` so all five rows offices —
   `Terminal`, `Builder`, `Files`, `Composer`, plus `Demo` before moving — share one press path with
   zero per-pane action encoding tables), moves `demo::Control`
   (`external-host/demo-control/control.hpp`) to `PaneDrawingFacet`, and updates
   `external-host/docs/zengine.demo.md`, `composer/docs/zengine.composer.md`, and
   `workshop/docs/workshop-panes.md`.
2. **Lane 3B — Multi-Pane Seat Suite** ([prompt](../prompts/graphics-stage-3b-multi-panes.md),
   [report](../reportbacks/graphics-stage-3b-multi-panes-RB.md), PR `#298` merged as `f75cc13`, 14 files,
   8 of 8 CI jobs green on run `39059883066`, 16 mutants / 18 of 18 runs caught, reviewed ready by
   Vision 2026-10-17): upgrades `PaneCanvasSeat` and `MultiPaneFacet` (`workshop/pane_seat.hpp`) so
   every seat owns a `graphics::Canvas` at `<office>.<pane>` (`rows_drawing`, disjoint runs, bounded
   at `kMaxNodesPerArea` / `kMaxElementsPerArea`, whole resend once on a refused delta) and routes
   `AreaRoom`, `DrawnRefused`, and `ActionRequested` through `each_seat`, `on_window_room`, and
   `on_window_press`, bringing `Desktop` (`launcher`, `hotkeys`, `manual`), `Introspection`
   (`loaded`, `arrangement`, `powers`), `Info` (`info`..`info.4`), and `Inventory`
   (`inventory`..`inventory.N`) onto `graphics/` with zero file overlap with `#297`.
3. **Lane 3C — Data-as-UI Graphics & `view::Presenter`**
   ([prompt](../prompts/graphics-stage-3c-data-ui-presenter.md),
   [report](../reportbacks/graphics-stage-3c-data-ui-presenter-RB.md), PR `#299` merged as `aad758c`, 6
   files, 8 of 8 CI jobs green on run `39068582742`, 22/22 mutants caught across `m3` + `m4`,
   reviewed ready by Vision 2026-10-17): adds `view::sketch` (projecting the single `view::picture`
   via `rects_by` / `texts_by` so the one-renderer law in `agents/view.md` holds and Workshop's
   terminal room and a window room match rectangle-for-rectangle and text-for-text) and `graphics/`
   window support (`AreaRoom`, delta `Drawn`, two-step `DrawnRefused` handling, `ActionRequested`,
   and `window_farewell`) to `view::View` (`view/view.hpp`) and `view::Host` (`view/host.hpp`),
   links `zengine-graphics-vocabulary` in `view/CMakeLists.txt`, and introduces `view::Presenter`
   (`tell`, `set`, `on_action`, `sketch`, `act`, `refresh`, and `Host::pair(name, presenter)` that
   survives fresh re-registrations under the same view name).

**Stage 4 (Wave 9 — three parallel lanes, CLOSED 2026-10-17 — `#300` `e43c45d`, `#301` `99a08ea`, `#302` `91b9b21`, 36 files with zero overlap):**
Brings the last 4 shipped pane weaves in Zengine onto `graphics/` and cleans up the Stage 3 cross-lane seams:
1. **Lane 4A — Canvas-Picture Authoring Panes** ([prompt](../prompts/graphics-stage-4a-canvas-panes.md),
   [report](../reportbacks/graphics-stage-4a-canvas-panes-RB.md), PR `#302` merged as `91b9b21`, 14 files,
   26/26 mutants caught across `m1` + `m2`, reviewed ready by Vision 2026-10-17): introduces
   `workshop::canvas_sketch` (`workshop/pane_canvas_drawing.hpp`, 126 lines — projecting a
   `v4::PaneCanvasContent` into `picture/<n>` and `parts/<n>/<k>` groups so delta nodes stay in
   their layer and painted part groups receive `graphics::window::land` clicks) and brings
   `FlowPane` (`flow/flow-pane/pane.cpp`, `flow/flow-pane/view.hpp`, with `recovery_picture`
   fallback when a dense graph exceeds `kMaxNodesPerArea` / `kMaxElementsPerArea`) and
   `ViewBuilderPane` (`view/view-builder/pane.cpp`, unifying pointer and window presses in `choose`
   and drawing from a presentation copy so a window room never clamps Workshop's pan) onto
   `graphics/`.
2. **Lane 4B — Both Editors on `graphics/`** ([prompt](../prompts/graphics-stage-4b-editors.md),
   [report](../reportbacks/graphics-stage-4b-editors-RB.md), PR `#301` merged as `99a08ea`, 7 files, 8 of 8
   CI jobs green on run `39077688883`, 17/17 mutants caught across `m1` + `m2`, reviewed ready by
   Vision 2026-10-17): introduces `editor_office::EditorWindow` in `editor/office_seam.hpp` (drawing
   rows via `ws::rows_drawing` plus `mark` for accent selection runs and the `caret` vertical bar
   carrying the underlying part's action, with two-state refusal handling) and brings both
   `EditorPaneWeave` (`editor/editor-pane/pane.cpp`) and `NeovimEditorWeave`
   (`editor/neovim-editor/pane.cpp`) onto `graphics/`, respecting `ActivationCursor` so a sealed
   replacement candidate emits no `RoomAsked` or `Drawn` before admission and clearing `drag_` /
   `grab_` / `release_drag()` on discrete window presses.
3. **Lane 4C — Projection, Refusal, Stand-In Unification & `act.py` Retry**
   ([prompt](../prompts/graphics-stage-4c-projection-and-standin-unification.md),
   [report](../reportbacks/graphics-stage-4c-projection-and-standin-unification-RB.md), PR `#300` merged as
   `e43c45d`, 15 files, 8 of 8 CI jobs green on run `39075043364`, 7/7 mutant witness runs caught,
   reviewed ready by Vision 2026-10-17): moves the single templated `ws::rows_drawing<Part>` and
   `ws::WindowDrawing` (owning `graphics::Canvas`, `last_`, and the two-state `fresh_` /
   `drew_whole_` refusal rule where `drew_whole_` starts `true` so a refusal before any drawing sends
   nothing) into `workshop/pane_drawing.hpp` across `PaneCanvasSeat` (`workshop/pane_seat.hpp`, 500
   → 373 lines), `PaneRowsFacet`, and `PaneDrawingFacet` (`workshop/pane_facets.hpp`), deletes
   `tests/window_stand_in.hpp` in favor of `tests/pane_window.hpp`, and teaches `act.aimed`
   (`external-host/tools/workshop/act.py`) to wait through `"no settled picture"` bounded by the
   step's deadline.

**Stage 5 (Wave 10 — three parallel lanes, CLOSED 2026-10-17 — `#303` `44a8bc2`, `#304` `a9d5c99`, `#305` `2ab3de0`, 29 files with zero overlap):**
1. **Lane 5A — Workshop as `zengine.graphics` Arranger & Desk Chrome Drawer**
   ([prompt](../prompts/graphics-stage-5a-workshop-arranger.md),
   [report](../reportbacks/graphics-stage-5a-workshop-arranger-RB.md), PR `#304` merged as `a9d5c99`, 13 files,
   8 of 8 CI jobs green on run `39093569054`, 44/44 mutants caught across `m1`–`m3`,
   reviewed ready by Vision 2026-10-17): teaches Workshop (`WorkshopWeave` in `workshop/weave.hpp`,
   `workshop/weave_run.cpp`, `workshop/weave_handlers.cpp`, `workshop/weave_pointer.cpp`, `workshop/grant.cpp`,
   and `workshop_window_drawing` in `workshop/screen.hpp` / `workshop/screen_compose.cpp` / `workshop/screen_external.cpp`)
   to place open pane areas (`pane_window_area`) whose offices accept `AreaRoom` and `"zengine.workshop"` on
   `zengine.graphics` when mounted (producing zero `NoRoleHolder` refusals when `zengine.graphics` is absent)
   and to project the same planes `paint` composes (`Layouts` band, external pane borders and headers with
   `*`/`?` actions and waiting/refused/non-window fallback, arrangement rings, menus, and bottom band) onto
   `"zengine.workshop"` via `WindowDrawing` with a hash-rooted path so structural additions/removals never
   paint out of order.
2. **Lane 5B — Unified `WindowDrawing` & Caret/Selection in `rows_drawing`**
   ([prompt](../prompts/graphics-stage-5b-window-drawing-and-caret.md),
   [report](../reportbacks/graphics-stage-5b-window-drawing-and-caret-RB.md), PR `#303` merged as `44a8bc2`, 12 files,
   8 of 8 CI jobs green on run `39089254377`, 12 mutants / 16 of 16 witness runs caught, reviewed ready by
   Vision 2026-10-17): moves the caret bar (`"caret"`) and selection highlight runs (`"sel<r>.<run>"`) from
   `EditorWindow::mark` into `ws::rows_drawing` (`workshop/pane_drawing.hpp`, capped to drawn rows `max_rows`),
   passes `caret_` from `PaneRowsFacet::send` (`workshop/pane_facets.hpp`) so `Terminal` and `Composer` draw
   their caret and selection in a graphics window, adds `width()`, `height()`, `refused_whole()`, and the
   unchanged-sketch refusal guard (`graphics::difference`) to `ws::WindowDrawing`, and folds `EditorWindow`
   (`editor/office_seam.hpp`, 720 → 595 lines), `FlowPane` (`flow/flow-pane/pane.cpp`), and `ViewBuilderPane`
   (`view/view-builder/pane.cpp`) onto `ws::WindowDrawing`.
3. **Lane 5C — External-Host Point-Reader `"no settled picture"` Unification & `story_journey.py` U2 Startup Wait**
   ([prompt](../prompts/graphics-stage-5c-point-reader-unsettled-and-story-journey.md),
   [report](../reportbacks/graphics-stage-5c-point-reader-unsettled-and-story-journey-RB.md), PR `#305` merged as
   `2ab3de0`, 4 files, 8 of 8 CI jobs green on run `39092555815`, 12 `hand` + 4 `story_journey` mutants caught,
   reviewed ready by Vision 2026-10-17): introduces `Hand.aimed` and `no_settled_picture` (covering both canvas
   `"no settled picture"` and text `"no settled text picture"`) in `external-host/tools/workshop/hand.py` across
   `Hand.row`, `Hand.pointed`, `Hand.lattice_point`, and `act.aimed` (`external-host/tools/workshop/act.py`),
   pinned in `tests/session/workshop_tool_checks.py` (60/60), and updates `tests/session/story_journey.py` U2
   (`unresolved_runs`) to wait up to 10s for `01-held` to reach `running` at its first step.

**Stage 6 (Wave 11 — three parallel lanes, CLOSED 2026-10-18 — `#306` `1d11677`, `#307` `7b1ab14`, `#308` `238bb70`, 29 files with zero overlap):**
1. **Lane 6A — Live Window Extent, `TextEntered`, Staging & Desk Overlays**
   ([prompt](../prompts/graphics-stage-6a-window-extent-text-and-overlays.md),
   [report](../reportbacks/graphics-stage-6a-window-extent-text-and-overlays-RB.md), PR `#308` merged as `238bb70`, 20 files,
   8 of 8 CI jobs green on run `39103907554`, 24/24 mutants caught across `m1` + `m2`, reviewed ready by Vision 2026-10-18):
   stages `zengine-graphics`, `zengine-window-terminal`, `zengine-paint-classic`, and `zengine-paint-block` in
   `workshop/CMakeLists.txt` and `cmake/ZengineInstall.cmake` (witnessed in `tests/package/CMakeLists.txt`); emits
   `TextEntered` from `WindowBase` (`graphics/window/window.hpp`), forwards `TextEntered` via `to_keys` to areas with
   `keys == true`, and publishes `WindowOffered` as `office()`; teaches `WorkshopWeave` (`workshop/weave_handlers.cpp`)
   to accept `WindowOffered` for session startup and cell-grid resize when no skin is mounted, keeps `keys = true` on
   `kWorkshopProvider` (`keys = false` on pane areas), and projects `[value]` drag pills and guest `guide_layer` marks
   in `workshop_window_drawing` (`workshop/screen_compose.cpp`) with `kWorkshopProvider` raised in front while an overlay stands.
2. **Lane 6B — Multi-Pane Seat Caret & `view::View` on `WindowDrawing`**
   ([prompt](../prompts/graphics-stage-6b-seat-caret-and-view-window-drawing.md),
   [report](../reportbacks/graphics-stage-6b-seat-caret-and-view-window-drawing-RB.md), PR `#307` merged as `7b1ab14`, 6 files,
   8 of 8 CI jobs green on run `39102354851`, 13/13 mutants caught, reviewed ready by Vision 2026-10-18):
   teaches `PaneCanvasSeat` (`workshop/pane_seat.hpp`) to retain `said_caret_` in `say` and pass it to `ws::rows_drawing`
   in `redraw` so multi-pane seats draw their caret and selection in a graphics window; teaches `view::sketch` (`view/view.hpp`)
   to draw the `"caret"` line node for a focused number field; and folds `view::View` onto `ws::WindowDrawing`.
3. **Lane 6C — `builder.py` & `monitor.py` Aimed Unsettled-Picture Retry**
   ([prompt](../prompts/graphics-stage-6c-builder-monitor-aimed.md),
   [report](../reportbacks/graphics-stage-6c-builder-monitor-aimed-RB.md), PR `#306` merged as `1d11677`, 3 files,
   8 of 8 CI jobs green on run `39100980822`, 19/19 mutants caught, reviewed ready by Vision 2026-10-18):
   routes `builder.calm`, `builder.keys_into` (`external-host/tools/workshop/builder.py`), and `Monitor.press_at`
   (`external-host/tools/workshop/monitor.py`) through `Hand.aimed` so `"no settled picture"` and `"no settled text picture"`
   are waited through alongside `"picture moved"`.

**Stage 7 Wrap-Up (Wave 12 — three parallel lanes, CLOSED 2026-10-18 — `#309` `7ed868c`, `#310` `5918a4b`, `#311` `5926167`, 23 files with zero overlap):**
1. **Lane 7A — Shipped `workshop/window-load-plan.json` & `zengine::graphics` Public SDK Install Surface**
   ([prompt](../prompts/graphics-stage-7a-window-load-plan-and-sdk-install.md),
   [report](../reportbacks/graphics-stage-7a-window-load-plan-and-sdk-install-RB.md), PR `#311` merged as `5926167`, 16 files,
   8 of 8 CI jobs green on run `39126892001`, 7/7 mutants + 1 install mutant caught, reviewed ready by Vision 2026-10-18):
   authors and stages `workshop/window-load-plan.json` (`zengine-graphics` + `zengine-window-terminal` in rows 2 and 3,
   `kWindowLoadPlanName` in `workshop/load_persist.hpp`, `workshop/CMakeLists.txt`, `workshop/workshop.cpp`,
   `workshop/README.md`, `workshop/docs/load-plans.md`, `workshop/docs/load-plan.md`, and `PlanRig` proof in
   `tests/test_workshop_load.cpp`), and exports `zengine::graphics` (`zengine-graphics-vocabulary` + the 20 public
   `graphics/` and `graphics/elements/` headers) in `graphics/CMakeLists.txt`, `cmake/ZengineInstall.cmake`,
   `agents/packaging.md`, `tests/package/CMakeLists.txt`, and `tests/package/public_surface.cpp`.
2. **Lane 7B — Live Terminal Resize Detection & `WindowOffered` Re-Publication in `zengine.window.terminal`**
   ([prompt](../prompts/graphics-stage-7b-window-terminal-resize.md),
   [report](../reportbacks/graphics-stage-7b-window-terminal-resize-RB.md), PR `#310` merged as `5918a4b`, 3 files,
   8 of 8 CI jobs green on run `39121549940`, 9/9 mutants caught, reviewed ready by Vision 2026-10-18):
   teaches `WindowT::on_pump` (`graphics/window/window.hpp` and `graphics/docs/zengine.window.terminal.md`) to measure
   `terminal_.size()` on each `zengine.window.pump` beat and, when `(cols, rows)` changes, mark the resized cell grid
   dirty and re-publish `WindowOffered` with the new `cols` and `rows` under the same `epoch`, proven in `tests/test_graphics.cpp`.
3. **Lane 7C — Settled-Picture Discipline in `builder.choose` and `Monitor.rows`, and Deduplicating `act.aimed` onto `hand.aimed`**
   ([prompt](../prompts/graphics-stage-7c-builder-choose-monitor-rows-and-act-aimed.md),
   [report](../reportbacks/graphics-stage-7c-builder-choose-monitor-rows-and-act-aimed-RB.md), PR `#309` merged as `7ed868c`, 4 files,
   8 of 8 CI jobs green on run `39122773961`, 28/28 mutants caught across `m1`–`m3`, reviewed ready by Vision 2026-10-18):
   routes `builder.choose` (`external-host/tools/workshop/builder.py`) through `pressing(ctx, hand)`, teaches
   `Monitor.rows` / `_Asker` (`external-host/tools/workshop/monitor.py`) to wait through `takes_no_press` and
   `no_settled_picture` via `DeskStamps` notices (both with an open `Hand` and as a watching-only monitor), and
   deduplicates `act.aimed` (`external-host/tools/workshop/act.py`) onto `hand.aimed`, proven in
   `tests/session/workshop_tool_checks.py`.

**Stage 7 Follow-Up Polish (Wave 13 — two parallel lanes, PROMPTED 2026-10-18 — 14 files with zero overlap):**
1. **Lane 7D — Settled `stdout` Banner Suppression Over Terminal Media & `zengine-input` in `window-load-plan.json`**
   ([prompt](../prompts/graphics-stage-7d-settled-banner-and-window-plan.md)):
   adds `load::medium_holds_terminal` (`workshop/load_execute.hpp` and `workshop/workshop.cpp`) so Workshop does not print
   its settled arrangement banner over a measured terminal held by `zengine.window.terminal` or a terminal `zengine.skin`,
   adds `zengine-input` (`zengine.input`) to `workshop/window-load-plan.json` so guest input sessions work under the window
   plan, and closes the doc gaps in `workshop/docs/load-plans.md`, `workshop/docs/load-plan.md`,
   `workshop/docs/getting-started.md`, and `cheat_sheet.md`, proven in `tests/test_workshop_load.cpp`.
2. **Lane 7E — Process-Scoped Terminal Input Claim for `zengine-window-terminal` & Graphics Resize Doc**
   ([prompt](../prompts/graphics-stage-7e-window-terminal-input-yield.md)):
   adds a PID-stamped, refcounted process claim (`claim_window_terminal_input`, `release_window_terminal_input`,
   `window_holds_terminal_input`, `terminal_reader_may_use_terminal` in `input/terminal_reader.hpp` and `ProcessTerminal`
   in `graphics/window/window.cpp`) so `zengine-input` yields `stdin` when `zengine-window-terminal` holds the process's
   terminal while still serving guest input sessions (`InputSessionRequested`, `InjectInput`, `PointerMotionRequested`,
   `InputSessionClosed`), updates `input/docs/zengine.input.md` and `graphics/docs/zengine.window.terminal.md`, and fixes
   the `WindowOffered` resize doc gap in `graphics/docs/zengine.graphics.md`, proven in `tests/test_input.cpp`.

**Wake:** Stages 1–7 are merged (`#218`, `#219`, `#296`–`#311`); Stage 7 follow-up polish (`7D` & `7E`, Wave 13) is prompted.
Zengine #146 (several Workshop windows, BL-WORK-12) builds on its window weave later.
**Source:** the founder (2026-10-07), after #96, from reference Zengine's `game_graphics` and a
draw list the skin keeps.

### BL-WORK-45 — Forced participants: a census against the split rule

**State:** REPORTED, REVIEWED, AND EXECUTING IN THE SPLIT ARC — [prompt](../prompts/participant-census.md),
[report](../reportbacks/participant-census-RB.md); its decisions the founder's (2026-10-12);
extractions merged in #232, #270, #275, #278, #279, and #282 (2026-10-15 to 2026-10-16)  
**Owed:** The founder's question (2026-10-12), once the graphics design's third round gave the
window the whole job: are there more places where Zen forces a participant where something
functionally self-contained would complete the purpose? Less a GUI question than one for an
experiment, perhaps a few. His split rule is the measure (Zengine's `AGENTS.md`: split a pane or
tool until a piece is too small to be useful alone; that piece becomes an operator other weaves
compose), tested both ways: participants that should be a library or an operator inside what they
serve, and C++ inside a host or a pane that would be useful alone, Workshop first. Vision's first
criterion, for the census to test rather than follow: a participant earns its place when it is
useful alone -- more than one partner speaks to it, it is swapped or reloaded alone for a reason,
it holds a permission its partner should not, or it must be isolated -- and is forced when it is a
pipe, a mirror, or one half of a chatty pair. In process a permission is message authority only
(P-WORK-67). Where to look first (Vision, 2026-10-12): the snake's controls and clock, each one
partner in and one out, translating, yet the seam an AI pilot (BL-WORK-40) or a replay would take;
the menu presenter, one partner, with a second presenter beside it (`examples/numbered-presenter`);
and the other way, Workshop. A probe re-cuts one forced participant, measured beside today's.

Reported and reviewed (Vision, 2026-10-12, 10 of 12 checks): the bus tap over Zengine's whole CTest
population (2.2 M deliveries, 60 of 60 entries) and the live Workshop; 48 rows, 28 earn, 7 mixed, 9
forced, 1 a missing door. The criterion sharpened: a use exercised, not claimed; permission only
where enforced, since every loaded row but Inventory is admitted `allow_any` (P-WORK-68); a pipe
judged by deleting it. The only pipes are the snake's three adapters: folded into the world, 3.27 to
2.14 messages a tick, the same game, the pilot, replay, faster clock and reload surviving. The
mirrors (Attention, Connections, Info's properties view, Introspection) become data-form views once
BL-WORK-37's elements land (in the meantime, #269, #271, and #278 moved Attention, Connections, and
Introspection's seats onto `PaneRowsFacet` / `introspection/seats.hpp`, and #282 extracted Info's
property view to `info/property_view.hpp` and retired the duplicate list); the menu presenter takes
the whole menu once the window shape is set. The terminal was the strongest case, Workshop relaying
the session through a pointer at 4.81 messages an act: Vision's native terminal door holding the
session, completer, and transcript landed in #275 (`8189c0c`) and #279 (`34c6dfd`, `terminal/door.hpp`),
alongside `GuestDoor` (`workshop/guest_judge.hpp`) and the unified project office `zengine.project`
(#270, `8d5c5d0`). The desktop's "inspect in Info" row defect (#217) merged as #232 (`98fd5c3`).

**Wake:** the snake's fold, its criterion record and snake-score's label landed in BL-WORK-37's
stage 1 (#218); the terminal door, guest judge, project office, and mirror/Info cleanups landed in
#270, #275, #278, #279, and #282; the menu presenter and full data-form views follow BL-WORK-37's
window stages.
**Source:** the founder (2026-10-12), after BL-WORK-37's round 2 review.

### BL-WORK-46 — Every pane a free picture, text a helper inside it

**State:** DECIDED AND ORDERED -- step 1 in G2's follow-up
([prompt](../prompts/graphics-only-g2-s6b-press-and-notice.md); Vision's fold, 2026-10-23, the
same press path); step 2 the issue lane's, once the package's share is in (the founder,
2026-10-23)  
**Owed:** The founder (2026-10-23), reading #380's rows: "ONLY full freedom, and then you have
helper methods for placing text." The window takes any drawing from any pane; `PaneRowsFacet` is
the limit, and most panes sit on it because rows are the paved path: before stage 6 every pane
said rows to Workshop, the three shipped pane examples draw rows (tower defense its board as
characters), and so do the palette and the quick setup. A button where the weaver puts it, a
rainbow underline: possible on `PaneDrawingFacet` today, never on the rows facet. Two steps, the
founder's (2026-10-23):
1. `PaneDrawingFacet` reads a press against each named part's pixel box, as the View does
   (`view::Picture::hit`), where today it reads the text cells of the picture last sent
   (`drawn_rows`): a `graphics::Button` is pressed over its whole face, where it is drawn. Small.
2. The row tools -- control strips, list windows, the caret and selection, what each row means,
   a press read back to a row -- become helpers any picture calls; one shipped example is drawn
   freely as the reference, so the next pane copies freedom; panes move one at a time, and
   `PaneRowsFacet` retires with the last. No hook on the rows facet: it would grow what this
   retires.
- **Not scheduled, the founder's direction:** each window presents what a pane draws in its own
  way. WL-GEO-07 (one quantization law) narrows to where panes sit, which its decision's reasons
  are about (`agents/decisions/the-whole-pixel.md`: two authorities for one desk, a visit
  authoring); an agent reads names, boxes and values (`PanePart`), never cells. No cell a pixel
  (the founder, 2026-10-23).

**Wake:** the issue lane's package share (N1 to N4, N6) merged, and #380.
**Source:** the founder and Vision, 2026-10-23.

### BL-WORK-12 — Multiple windows

**State:** ISSUE — [Zengine#146](https://github.com/Krealsion/Zengine/issues/146) holds it now (filed by deep review, 2026-10-09).

### BL-WORK-13 — Python scripts as participants

**State:** ISSUE — [Zengine#147](https://github.com/Krealsion/Zengine/issues/147) holds it now (filed by deep review, 2026-10-09); paired with the C++ ↔ Python live Snake owner handoff demo (`C++ -> Python -> C++`, the founder, 2026-10-16; see also [BL-WORK-40](#bl-work-40--the-simplest-snake-played-by-its-own-ai) and [BL-WORK-37](#bl-work-37--the-graphics-library-elements-a-window-keeps)).

### BL-WORK-14 — A pane's minimum size

**State:** ISSUE — [Zengine#126](https://github.com/Krealsion/Zengine/issues/126) holds it now (filed by deep review, 2026-10-09).

### BL-WORK-15 — The View Builder zooms

**State:** ISSUE — [Zengine#127](https://github.com/Krealsion/Zengine/issues/127) holds it now (filed by deep review, 2026-10-09).

### BL-WORK-34 — Text that steps down to fit its room

**State:** ISSUE — [Zengine#143](https://github.com/Krealsion/Zengine/issues/143) holds it now (filed by deep review, 2026-10-09).

### BL-WORK-16 — Accordions and anchors, researched first

**State:** ORDERED — sixth in the founder's order (2026-10-03; renumbered 2026-10-05), after the text
panes reach the canvas  
**Owed:** A research phase, then the work it supports. The weaver shows and hides the parts of a
pane with an accordion, and hides the pane itself the same way, and a pane's place can be
anchored to another pane or to any edge, such as its parent's right side, so dependent placement
follows when something opens, closes or moves. Some of this exists or was planned: the goal
map's first target for a library of GUI transformations is an accordion attachable to a pane that
preserves anchor paths ([the goal map](goals/workshop.md#further-shell-extraction-reusable-effects-and-playful-consumers));
arrangement keeps each resize's opposite edge anchored and a default place reactive (Zengine
`agents/workshop/arrangement.md`, WL-ARR-05 and WL-ARR-06, and
`agents/decisions/anchors-and-axes.md`); the Compose motion phase (#48) left the accordion layout
story for later (its plan, removed 2026-10-03, is in Git at `aa2fb18`); and relative placement
waits with P-WORK-10.
The research reads these and the code as it stands before anything is built. Files' path line
and its marks, the quick places, are first consumers (BL-WORK-17); the founder sees Info's
nested values as another (BL-WORK-10).

**Wake:** after BL-WORK-06 and BL-WORK-09.
**Source:** the founder (2026-10-03).

### BL-WORK-17 — Files answers a request for a path

**State:** ORDERED — seventh in the founder's order (2026-10-03; renumbered 2026-10-05), after
BL-WORK-16  
**Owed:** A file picker that is Workshop's own work, not the operating system's dialog. A pane
asks for a path, to open or to save, with the kinds it takes and a suggested name; Files answers
later with the path the weaver chose, or says the choice was cancelled, and only the asker gets
the answer. A request brings Files up with the keys if it is hidden, saying who asks and why;
Escape cancels. In Files: a line to type a path into, absolute or from where the weaver is
looking; the marks, which already survive restarts, as quick places in an accordion
(BL-WORK-16); filters by kind; and a name line for saving. The View Builder's file box,
Inventory's toolboxes, the Builder's recipe catalog and the editors' save-as take their paths
through it. Open questions: a request whose asker goes away, two at once, the keys while
choosing, overwriting on save, and whether Files may make a folder (its guide says it creates
nothing).

**Wake:** after BL-WORK-16, with Files on the canvas (BL-WORK-06), so its picture is built once.
**Source:** the founder's notes, split from BL-WORK-08 with the founder's OK (2026-10-03).

### BL-WORK-18 — Inventory finds an entry without walking folders

**State:** ISSUE — [Zengine#128](https://github.com/Krealsion/Zengine/issues/128) holds it now (filed by deep review, 2026-10-09).

### BL-WORK-19 — Inventory views retire

**State:** ISSUE — [Zengine#129](https://github.com/Krealsion/Zengine/issues/129) holds it now (filed by deep review, 2026-10-09).

### BL-WORK-20 — Hotkey contexts beyond on and off

**State:** ISSUE — [Zengine#130](https://github.com/Krealsion/Zengine/issues/130) holds it now (filed by deep review, 2026-10-09).

### BL-WORK-21 — Inventory's smaller extras

**State:** ISSUE — [Zengine#131](https://github.com/Krealsion/Zengine/issues/131), [Zengine#132](https://github.com/Krealsion/Zengine/issues/132), [Zengine#133](https://github.com/Krealsion/Zengine/issues/133), [Zengine#134](https://github.com/Krealsion/Zengine/issues/134), [Zengine#135](https://github.com/Krealsion/Zengine/issues/135) hold it now (filed by deep review, 2026-10-09).

### BL-WORK-22 — Run a stored command without giving it a hotkey

**State:** ISSUE — [Zengine#136](https://github.com/Krealsion/Zengine/issues/136) holds it now (filed by deep review, 2026-10-09).

### BL-WORK-23 — Terminal command scripts

**State:** ISSUE — [Zengine#137](https://github.com/Krealsion/Zengine/issues/137) holds it now (filed by deep review, 2026-10-09).
**Broadened** (the founder, 2026-10-20): Zenscript comes back as a language of Loom messages --
run under the authority it was given, refused where that fails, ending in an answer either way;
a pane as UI data whose events reach handlers; helpers for agents, run with parameters; native
operators as its escape, made when a pattern repeats. No C++ inside a script for now; `maker/`
its runtime, a small interpreter filling out a definition's fields from readable text (maker's
authoring was set aside for a grammar written in C++). A side-experiment research
([prompt](../prompts/zenscript-research.md)), to start once the layout research reports; it
lifts #137's fence against a broad shell language.

### BL-WORK-24 — Agents read the desk by messages

**State:** CLOSED — merged in two stages (Vision, 2026-10-05): 1, what Workshop owns and holds,
by message (`prompts/desk-by-messages-1.md`, with its review's fixes in
`prompts/desk-by-messages-1-fixes.md`), as Zengine #93 (`2305850`, 2026-10-06); 2, each pane
names its own parts, and the walk presses them by name (`prompts/desk-by-messages-2.md`), with
two deep-review findings on #93 and #93's doc gaps (the founder, 2026-10-06), and its review's
fixes (`prompts/desk-by-messages-2-fixes.md`), as #94 (`7b73239`, 2026-10-06). Stage 1 also carries what #92's reviews asked for (the founder,
2026-10-05): two checks in the constitution's attack pass, a census of shapes, a message timeline
in the test rig, a rule for records' headers, #92's doc gaps, a shorter off-screen sentence, the
Linux job's limit and the kit's exact replacements  
**Owed:** An agent gets all it needs from the message system. Each pane's controls, rows and
elements answer to stable IDs, with their places and sizes in pixels as numbers, so an agent
checks a size by the number returned instead of counting pixels in a screenshot, and picks a
menu row by its ID instead of by where it falls. Tests prove each number matches what is really
drawn. Screenshots stay evidence of presentation and are needed less: they are costly to move,
and a long story's record can outrun the retained history. Which pane holds the keys is one
such number: Workshop's band says it ("typing goes to ..."), but no pane view does, so a setup's
walk can check a selection by its rows and a put-down only by its picture (#89's report).
A canvas pane answers too: its words, controls and elements, as a text pane's rows do. Today the
inspection door describes text panes only, so #91's witnesses drove the View Builder by pixels
read off pictures (its report's second recommendation); BL-WORK-06 then keeps every pane it moves
readable. The walk tool's ways of reaching a row and a point go with it (`workshop/act`,
`external-host/tools/workshop/act.py`): `select` reads a two-column cursor marker that Info's
one-column property rows defeat, and `x,yc` counts a terminal console's cells, two rows above its
canvas (#91's report, recommendations 3 and 4).

**Wake:** met: #92 merged (2026-10-05).
**Source:** the founder (2026-10-03), joining two pressures from the finished drafts: menu rows
reached by position, and the cost of evidence (`reportbacks/zengine-comfortable-demo-setups-RB.md`,
`zengine-inventory-command-presets-RB.md`).

### BL-WORK-25 — Agents act by intent

**State:** ONGOING — beside BL-WORK-24 (the founder, 2026-10-03)  
**Owed:** An agent states an intent in one dense message that carries the whole idea, and Zen
translates it into what it means in the live code, instead of many small commands that each
restate the same context. Every intent made solid adds to it. Editing through Flow comes first:
GUI, keyboard and messages share one semantic edit model, but authoring Flow from the Terminal or
an ELH is not usable end to end yet (`drafts/flow-ux-research.md` §7;
`reportbacks/zengine-flow-ux-research/agent-interface.md`).

**Wake:** with BL-WORK-24; it continues after.
**Source:** the founder (2026-10-03), widening the finished drafts' item on agents editing Flow.

### BL-WORK-26 — Load metadata, researched

**State:** ORDERED — tenth in the founder's order (2026-10-03), at the end of the current arc  
**Owed:** Research, then the smallest useful answer: what a weave was loaded from, by whom and
when, with other useful context, discoverable through its contract. Keep apart what the author
declares (purpose, documents, source and build locators, tags), what the host observes (the path
asked for and the one opened, content and build identity, incarnation, when loading or activation
happened), who asked and who approved, and which clock a time comes from. Each fact names its
owner, retention and reader. An actor the host cannot establish stays unknown, and no one load's
time or actor enters a schema's identity. Metadata grants nothing. An unfamiliar reader proves
the answer in an info box.

**Wake:** after BL-WORK-24.
**Source:** selected by the founder earlier and never run. The goal map keeps its summary
([the maker-story section](goals/workshop.md#complete-maker-stories-and-reusable-information));
the full questions are in the removed maker-story arc (in Git at `aa2fb18`,
`drafts/maker-story-development.md`).

### BL-WORK-27 — A dead weave's last state, inspectable

**State:** ORDERED — eleventh in the founder's order (2026-10-03), at the end of the current arc  
**Owed:** When a weave can no longer answer, the owner that still holds its last state offers it
for inspection, typed. An isolation host keeps a child's admitted snapshots and their schemas,
which outlive the child but not the host; native `last_known_good` is not a running journal. A
saved value, a retained recovery snapshot, a current reply and a published observation each say
which they are, and the schemas to read a value stay after its supplier is gone. Looking or
copying neither restores nor runs it; recovery is its own explicit operation.

**Wake:** after BL-WORK-26.
**Source:** as BL-WORK-26 (the arc's section on recovery material).

### BL-WORK-28 — Parallel work publishes without trampling (ELH Experiment 3)

**State:** ISSUE — [Zengine#138](https://github.com/Krealsion/Zengine/issues/138) holds it now (filed by deep review, 2026-10-09).

### BL-WORK-29 — Stronger input control for agents

**State:** ISSUE — [Zengine#139](https://github.com/Krealsion/Zengine/issues/139) holds it now (filed by deep review, 2026-10-09).

### BL-WORK-30 — Flow opens a native operator's source

**State:** ISSUE — [Zengine#140](https://github.com/Krealsion/Zengine/issues/140) holds it now (filed by deep review, 2026-10-09).

### BL-WORK-31 — A recycling list for views

**State:** ISSUE — [Zengine#141](https://github.com/Krealsion/Zengine/issues/141) holds it now (filed by deep review, 2026-10-09).

### BL-WORK-32 — Flow's UX milestones

**State:** ISSUE — [Zengine#142](https://github.com/Krealsion/Zengine/issues/142) holds it now (filed by deep review, 2026-10-09).

### BL-WORK-35 — An app of its own, edited live from Workshop

**State:** ISSUE — [Zengine#149](https://github.com/Krealsion/Zengine/issues/149) holds it now (filed by deep review, 2026-10-09).

### BL-WORK-33 — Undo and time travel

**State:** ISSUE — [Zengine#148](https://github.com/Krealsion/Zengine/issues/148) holds it now (filed by deep review, 2026-10-09).

## 3. Bounded defects and quick repairs

### BL-VERIFY-01 — Reconcile Builder field clicks locally

**State:** ISSUE — [Zengine#123](https://github.com/Krealsion/Zengine/issues/123) holds it now (filed by deep review, 2026-10-09).

### BL-DEF-06 — Zengine cleanup notes the `ui/` pass left

**State:** ISSUE — [Zengine#121](https://github.com/Krealsion/Zengine/issues/121), [Zengine#122](https://github.com/Krealsion/Zengine/issues/122) hold it now (filed by deep review, 2026-10-09).

### BL-DEF-09 — Three deep-review findings, for stage 2

**State:** CLOSED — merged with stage 2 as Zengine #91 (`5901b39`, 2026-10-05)  
**Owed:**
- **An old canvas picture refused for a sliver** (#90). A rect of an earlier
  `PaneCanvasContent` (version 2, sub-units) narrower than a pixel can floor to zero width, and
  `canvas_content_problem` then refuses the whole picture; the same sliver three sub-units over
  floors to one pixel and passes, and #89 accepted both. Judge an old picture by its own rules,
  then drop what floors to nothing, as #89's window painted it
  (`workshop/pane_canvas_vocabulary.hpp`, `canvas_content_of_legacy`). In the tree only a test's
  provider still speaks version 2.
- **Fallback text drawn off the grid its presses use** (#90). Where a pane's body holds no row of
  the window's face, the window draws its text in 12-pixel bitmap cells from the body's own pixel
  origin, but presses (`prose_column_of_pixel`) read the canvas's cell grid, and the inspection
  door aims (`cell_center`, `workshop/weave_inspection.cpp`) at the drawn glyphs. A body 6 pixels
  past a grid line, the norm for a pane placed on whole cells since the window's room top is 42,
  sends a press on the right half of each glyph to the next column, and `PaneViewRequested`
  refuses the pane. Drawing, pressing and aiming take one origin (WL-GEO-01); aiming from the
  grid alone leaves the press wrong. A terminal is unaffected; BL-WORK-34 would retire the
  fallback.
- **A setup's start depends on its panes' order** (#88). `seat_desk`
  (`external-host/tools/workshop/demo_setup.py`) stops filtering at the first pane the setup
  builds, so an unoffered optional pane after it stays on the temporary desk, and the start fails
  before Builder runs; the reverse order starts. What the temporary desk leaves off must leave
  the final desk too, or the start fails after building instead. Latent for every shipped
  setup: only the tower defense example builds a pane, and nothing after it on that desk can be
  missing.

**Wake:** stage 2's prompt.
**Source:** the deep reviews of #90 and #88 (2026-10-04), each reproduced by Vision (`f3bde59`,
`61c28e8`).

### BL-DEF-10 — Two findings for stage 3

**State:** CLOSED — merged with stage 3 as Zengine #92 (`567f983`, 2026-10-05)  
**Owed:**
- **The View Builder's launch record survives a view file that is missing for a while** (the deep
  review of #91 at `78928fb`). Saved and run, the view's file moved away, Workshop relaunched: the
  builder cannot open it, and the next `remember` (a reload of the builder, or merely `describe`)
  writes the record over with no file and not running, so the file's return no longer brings the
  view back at a launch (`view-builder/pane.cpp`, `on(ProjectRoot)` taking `remembered_` from the
  record, then `resume`). The record keeps the saved file and whether it ran until the view opens
  again or the weaver names another.
- **The hotkeys guide's keymap example is a file Workshop refuses** (#91's follow-up, its doc gap).
  `docs/workshop/hotkeys.md` writes `{"zen":"1",...,"value":{...}}`; Loom's text codec reads
  `"fields"`, with the envelope's numbers as numbers, so the example copied is refused (`keymap
  refused -- default bindings stand`). The example says what Workshop reads.

**Wake:** stage 3's prompt.
**Source:** the founder's deep review of #91 (2026-10-05) and
`reportbacks/whole-pixel-2-no-creator-RB.md` (Doc gaps).

## 4. Adoption and release

### BL-ADOPT-01 — Human contributor front door

**State:** GOAL-COUPLED  
**Owed:** Turn the truthful but thin contributor entry into a practical human route: persistent
installed Loom/Zengine prefixes, IDE discovery (`CMAKE_PREFIX_PATH`/package dirs), canonical lanes,
repository ownership, and links to the product concepts Workshop has proven. Reuse public guides;
do not make humans read the executor constitution.

**Wake:** before actively soliciting outside contributors or claiming second-maintainer onboarding.

**Delivered foundation:** Loom #14 / Zengine #53 supply an exercised loaded-pane authoring
route and explicit diagnostic commands. Persistent setup, IDE discovery and independent human
onboarding remain broader work; this bounded repair does not close the item.

### BL-ADOPT-02 — Release identity and compatibility promise

**State:** ISSUE — [Zengine#119](https://github.com/Krealsion/Zengine/issues/119) holds it now (filed by deep review, 2026-10-09).

### BL-ADOPT-03 — Performance evidence before performance claims

**State:** ISSUE — [Zengine#120](https://github.com/Krealsion/Zengine/issues/120) holds it now (filed by deep review, 2026-10-09).
Its wake has come: BL-WORK-37's window weave against today's drawing path. It stays parked until
stage 1's window exists, BL-WORK-37 round 5's stress host, tables and canary its measurement and
their figures its baseline (the founder, 2026-10-13).

### BL-ADOPT-04 — GitHub from Workshop

**State:** ISSUE — [Zengine#145](https://github.com/Krealsion/Zengine/issues/145) holds it now (filed by deep review, 2026-10-09).

### BL-ADOPT-05 — The documentation overhaul: a man page on each weave, a tutorial for each step

**State:** ORDERED — resting at B3, B2 (#184) and B3 (#198) merged (2026-10-11); C is the
roadmap's first step, documentation first (the founder, 2026-10-14), its manuals the ownership
map (Vision); D after the release. Before that: first beside the build-speed changes (the
founder, 2026-10-11) — researched
([its report](../reportbacks/docs-overhaul-research-RB.md)); its ten decisions taken as recommended
but F2: no forwarding headers, since the move precedes the first release (the founder, 2026-10-10).
Stage A, the move, merged as Zengine #179 with Loom #47 (2026-10-10). B1, the Builder's manuals
([prompt](../prompts/docs-overhaul-b1.md), [report](../reportbacks/docs-overhaul-b1-RB.md)), is
Zengine #181, merged as `f55a82a` (2026-10-11), its two commits reviewed (Vision), each one's hosted
run green on all eight jobs (the second's, on `3592c04`, 51 minutes): a weave carries its manual
compiled in (`MANUAL`, `cmake/ZengineManual.cmake`), a pane declares it beside its offer and
Workshop holds it while the sender holds the office, dropping it at a re-offer, and the Builder
office answers `ShapeDocumentRequested` from its page; the `manual` check, the action census
`tests/actions.txt` and the key markers; the Builder's two manuals and its first tutorial; its ten
choices accepted, then 2 and 3 reversed: the founder chose a pane's manual answered on ask instead
of held by Workshop, in #181 before it merges (2026-10-10;
[prompt](../prompts/docs-overhaul-b1-ask.md)): the research's decision 12 held it, on the settings
declaration's pattern, so the `?` could redraw from words in hand, which an answer kept while the
`?` is open gives as well; the held copy, its drop at a re-offer and its lines in WL-DESK-06 went (a
law of verdicts, the placement the B1 prompt carried from the research: Vision's miss), in #181's
second commit ([prompt](../prompts/docs-overhaul-b1-ask.md),
[report](../reportbacks/docs-overhaul-b1-ask-RB.md)): `PaneDocumentRequested` asked of the pane's
office directly and answered to the asker alone, the whole page or one section; a manual is public,
the repository's own page, so reading one needs no scope. B2
([prompt](../prompts/docs-overhaul-b2.md), [report](../reportbacks/docs-overhaul-b2-RB.md)) is
Zengine #184, one commit, its hosted run green on all eight jobs, reviewed ready to merge (Vision,
2026-10-11): a `?` and a gear (`=`) on a pane whose holder answers its manual, the desktop's Manual
pane showing it with the keys in force (`Ctrl+f`, above every mode), and the two spellings in the
preferences file (v2); its pictures' roots under `C:/Zen-pictures`, though the Builder's header
still shows the build tree's `C:\Users\Joshua\zen-build\...`; B3 after it
([prompt](../prompts/docs-overhaul-b3.md)), stacked on #185's repair since it met that race on
Windows ([continuation](../prompts/docs-overhaul-b3-after-185.md)); its `?` and settings need
nothing new; its tutorial mode follows the highlight research
([report](../reportbacks/tutor-highlight-research-RB.md)): after the address law and B2, it reads a
control part's section by its id with no ask, and asks the pane (`PanePartDocumentRequested`) only
for a subject part's `Shows` key; the `?`, tutorial mode, the census and the Tutor's highlight read
the one action row. Into B2: a setting each for how the band and the Hotkeys view spell a key,
chosen apart, the defaults as now (the band short, `B`, `^p`, `enter`; the Hotkeys view full,
`shift+b`, `ctrl+p`, `return`), reached by a gear beside the `?` (the founder, 2026-10-10), the `?`
spelling as the Hotkeys view does (Vision); the `?` finding a section's keys from data the splitter
writes, never a C++ reading of the page. Into B3: the tutorial's pictures taken from a root under
`C:/Zen-pictures`, with the tree the Builder names under it too, so no path of this machine shows,
as every tutorial's and demo's pictures are from now on (the founder, 2026-10-10: first `D:/Zen`,
then this once D: went; they show `G:/programming/cpp/Zen/scratch/` today), and the Pane Manager put
away before the last. B3 is Zengine #198 ([report](../reportbacks/docs-overhaul-b3-RB.md)), two
commits on `9e289e2`, its hosted run `38180509676` green on all eight jobs, reviewed ready to merge
(Vision, 2026-10-11, 12 of 12 checks): `tutorial_walks`, in the session gate on every OS, installs
the build into a prefix of its own, starts each `<feature>/docs/tutorials/<name>/` from the copy the
install gathered into the tool package's `setups/`, and replays its `tutorial` walk; its six
pictures show only `C:/Zen-pictures` and the standard CMake path. Its witness of the build tree
re-reads `build/workshop`, where other session entries run their Workshops, none building there, so
a later entry that builds there turns it red under the wrong name. Its gaps join C's: a start that
fails after `demo.json` exists leaves Workshop and the host running, which
`workshop/docs/demo-setups.md` does not say; the text check that every `## Step N` shows
`images/step-N.png` is unbuilt; the entry grows by a start and a first build per tutorial (13-45 s
each). Into C: an office offering several panes (the desk, Introspection, Info,
Inventory) under one page, which `pane_document`'s one pane does not yet fit; the key markers
checked on every page under a `docs/` (`workshop/docs/load-plans.md` names the Builder's `o`, `f`,
`b` and `c` bare, `builder/docs/recipes.md` Files' `u` and `a`); one walker of a pane's modes for
the census; the report's manual scaffold; nothing in a running Workshop is granted
`ShapeDocumentRequested` yet, so its first asker brings the grant; a page near `kMaxManualBytes`
makes a declaration past the history recorder's 64 KiB payload ceiling. Into D:
`cmake/ZengineManual.cmake` needs policy CMP0054 NEW, which a stranger's old
`cmake_minimum_required` would not give. Then B2, the `?`, with B3, its tutorial replayed; C's manuals landed as #234 to #249
(2026-10-15), with the manual ASCII check in #251 (`0ea9441`), `ManualFacet` across single- and
multi-pane offices in #266 (`54d8cc0`) and #268 (`60a41e5`), and the three host offices
(`zengine.flow.host`, `zengine.view.host`, `zengine.builder.runner`) in #272 (`b26630b`, 2026-10-16);
C's remaining tutorials wait for the complete stories; D after the release. BL-WORK-38's stages 3a
and 3b follow B2. The research's findings are verified and filed in deep review's place
([report](../reportbacks/overhaul-findings-RB.md)): Zengine #162-#168, six taken and merged as
#169-#174 (2026-10-10). #164, the Builder pane's build-and-load notice: the founder chose reading
(b), with the build send keeping its ticket (2026-10-10); taken with the follower's lost realization
(#176) as #177 and #178, merged before the move (2026-10-10)
([report](../reportbacks/realization-notice-RB.md)). Stage C's inputs from them: the told history in
`agents/` that [the F6 record](../reportbacks/overhaul-findings/verify/F6-realization-history.md)
lists; `docs/workshop/limitations.md`'s unload sentences and package count beside
`docs/getting-started.md`'s target list; and the `builder` tool's module note and its
`loom-tool.json` description, which list `unknown recipe` among a taken ask's endings; and the
move's own doc gaps ([its report](../reportbacks/docs-overhaul-a-RB.md#doc-gaps))  
**Owed:** Documentation a layman reads well, almost a full tutorial for each step (the founder).
- Docs are attached to the specific weave and organized by command, and the `man` page equivalent
  is the primary reference, whether the weave links its Markdown file or a new macro carries it.
  Stage 4a's declaration and its Markdown beside the source are the seam
  ([documentation.md](../reportbacks/agent-desk-research/documentation.md#authored-where-the-code-is));
  the `?` (stage 4b) and the agent's guide read the same words.
- Folders become part of the intuitive navigation: a feature's folder holds its docs and its
  parts. The founder's sketch, which he says may not catch them all:

  ```
  Zengine
    builder
      docs
      builder-pane
    flow
      docs
      flow-host
      flow-pane
    inventory
      docs
      inventory-pane
    editor
      docs
      editor-pane
      neovim
        neovim-pane
  ```
- The tutorials make one flow, read beside each other. A new pane is not a stranger's first
  experience: the first tutorials start from a release extracted into an empty folder, with nothing
  else installed, and the first is a Terminal hello world (the founder, 2026-10-10, finding the
  Builder's tutorial pretty good). The release they start from is BL-ADOPT-06.
- The agent guide's doc gaps are its examples of errors to make impossible
  ([the report](../reportbacks/agent-guide-RB.md#doc-gaps)): a wrong target name, stale counts,
  missing routing rows, and three routing tables that already disagree with the registers.

It meets Tasks 1 and 7 of [the stranger-legible goal](goals/stranger-legible.md), which the
rewrite places; BL-WORK-38's stages 4a and 4b; BL-WORK-09; and the fast-builds research, since a
feature's folder is the natural unit of a pane built alone.

**Source:** the founder (2026-10-09), reviewing the agent guide.

### BL-ADOPT-06 — A release ready to run, for Windows and Linux

**State:** ORDERED — cut to the alpha's nightly package (N0 to N10, the founder taking its six
decisions and overturning decision 8 below, 2026-10-23). Before that: R0 to R5 not started and
their 10-22 date dropped, the
founder closing what is open first (2026-10-14). Before that: researched
([its report](../reportbacks/release-research-RB.md), 2026-10-10):
one package per platform made by the repositories' own install and judged clean, a C seam so a pane
author's compiler is theirs, and stages R0 to R5 with Loom's L1 and the Builder's R1b, 10-11 to
10-22, the build slot their constraint. The founder agreed with its direction and put it beside the
architecture work, taken in the issue lane as the machine allows (2026-10-10), its fifteen decisions
as Vision put them: as recommended, but the pane's runtime rule in Loom's weave build contract, and
0.1 a preview with Task 1's cold walk on a dry run. L1 ([prompt](../prompts/release-l1.md),
[report](../reportbacks/release-l1-RB.md)): Loom #46 (no bytecode) and #48 (a weave opens from any
folder, a refusal names what is missing, every Loom program in the UTF-8 code page) merged
(2026-10-10); #41, a weave carrying its runtime, held for the founder: on MinGW-w64 a runtime
instance per weave runs out of TLS indexes after about 1,088 loads (P-LOOM-11), so decision 2 is
open again. The GCC 16 experiment ([report](../reportbacks/runtime-gcc16-RB.md), reviewed by Vision
2026-10-10): native TLS does not end the leak, which is winpthreads' index (a guarded static,
`std::call_once`, `std::thread`), and a Loom stand-in that returns a weave's indexes and its
exception pool at unload makes Zengine's MinGW-w64 lane pass against #41 on GCC 16, 55 of 55, where
#41 alone fails; the founder took the stand-in for #41's MinGW-w64 half (2026-10-11), with the
reload witness in Loom's lanes and P-LOOM-12 closed beside it
([prompt](../prompts/weave-runtime-windows.md)); reported
([report](../reportbacks/weave-runtime-windows-RB.md)) as Loom #53, reviewed (Vision, 2026-10-11):
run `38133001920` every job green; the stand-in returns every TLS and FLS index and the pool at
unload (1,200 loads clean, under 2.5 KB left a load), the contract accepts MinGW-w64 GCC from 12.2
and Clang from 18.1 and refuses older in words, and no exception crosses a host door. Under the MSVC
ABI a weave's C stdio is its own, so Zengine's `snake` reads nothing from a skin loaded before its
catcher; the founder kept it so, a host redirecting the Windows handle before a weave loads
(decision 1 (a), 2026-10-11, kept so it holds alike across platforms for now, compiler updates
perhaps allowing a better option later): `snake`'s fix in Zengine merges first, then #53, then the
Zengine documents #53 makes false ([continuation](../prompts/weave-runtime-windows-msvc-stdio.md),
[report](../reportbacks/weave-runtime-windows-msvc-stdio-RB.md)): KERN-05 says it, the reload weave
writes through `std::cout` and stays clean, #41's done-when amended, Zengine #189 (`snake`'s
catchers made before the load, a hush leaving no weave a closed handle) and #190 (the documents),
every run green, reviewed (Vision, 2026-10-11), and merged by the founder in that order, #189, #53,
#190, closing #41 (2026-10-11) (P-LOOM-14)  
**Owed:** A full release for Windows and Linux, ready to run: extracted into a folder, Workshop
starts with nothing else installed, and the first tutorials begin there (BL-ADOPT-05). A tutorial's
replay on the extracted package can witness the package itself.

It meets [Zengine#119](https://github.com/Krealsion/Zengine/issues/119) (the release's identity and
compatibility promise) and BL-ADOPT-01 (the contributor front door).

**Source:** the founder (2026-10-10), on the overhaul research's first gap.

## 5. Architectural debt that waits for pressure

### BL-ARCH-01 — Cross-layer public include debt

**State:** ISSUE — [Loom#36](https://github.com/Krealsion/Loom/issues/36) holds it now (filed by deep review, 2026-10-09).

### BL-ARCH-02 — Current-law carrying cost must remain bounded

**State:** WATCH / SUBTRACTIVE DUTY  
**Owed:** Keep mandatory and routed current law organized by subject and rewritten in place. If a
routed file becomes a phase-indexed chronicle or repeated concepts require phase archaeology,
consolidate it without deleting the enforceable law or proof history.

**Wake:** a cold reader cannot find the owner without phase names, or a routed current-law file's
growth materially slows every task touching that surface.

Woken (2026-10-11): #185's guest-door law needed about 1 KB in `agents/workshop/guests.md`, 98 bytes
from its 16,384 budget. Twelve registers stand within 5% of the budget, four under 100 bytes from it
(`geometry`, `project`, `code`, `files`), and the WL router `agents/workshop.md` has 53 bytes left
of its 8,192, so a new register cannot be routed either; five more stand between 85 and 95%. Across
the 53 WL registers PROVEN BY is 49% of the bytes, the laws themselves (LAW, MEANS, DOES NOT MEAN)
37%, and the check already verifies every citation mechanically. Vision's proposal: peel the proofs
out of the registers, rather than split registers one by one, each split adding a router row
(Vision, 2026-10-11). The founder chose (2026-10-11): the budget raised by about half, the added
bytes an appendix of the proofs, their lists compressed, searching and linking a later pass; after
#185 and docs B3 merge, before the address law and `tutor` touch registers
([prompt](../prompts/law-register-appendix.md)). #185's repair, Zengine #197, merged with
`guests.md` trimmed to exactly its budget (2026-10-11); the appendix waits on B3 (#198). The
appendix is Zengine #201 ([report](../reportbacks/law-register-appendix-RB.md)), one commit on
`10241b3`, its run `38184693918` green (docs only, the five build jobs skipped), reviewed (Vision,
2026-10-11, 12 of 12 checks): all 68 registers, WL, MW and VM, laws first and proofs under
`### <id>` in an appendix at the end (`## Proven by`, `## Seen`), laws 16 KB, the appendix 8 KB,
every router 12 KB, the proofs' syntax compressed by 6%; Vision's own comparison found every LAW,
MEANS, DOES NOT MEAN and WHY line unchanged but the two restored guest lines, and every proof's
3,006 identifiers and 1,420 cases under the same files; nine mutations, eight red, the ninth (a case
cited under the wrong file) green as it was before. Found: the 8 KB appendix binds first -- `code`,
`geometry`, `guests` and `opening` stand at 92 to 94% of it while their laws parts are half empty,
so each takes about one more law, not half again; the founder chose the laws' 16 KB kept and the
whole file capped at 24 KB in place of the appendix's 8 KB (2026-10-11;
[prompt](../prompts/law-register-appendix-whole-file.md)). The pull request's text names Zen's tool
path and commit. The report's two questions: the file legend (about 20 KB) left for the
search-and-link pass, and one router budget, which `workshop/AGENTS.md` also needed (44 bytes from
the old 8 KB), both as it leaned, not overruled (the founder, 2026-10-11). A case is resolved
against every test file, not the file cited before it (as before #201): binding it is the next
pass's. The cap is #201's second commit, `7c8e6ee`
([report](../reportbacks/law-register-appendix-whole-file-RB.md)), its run `38186766249` green (docs
only), reviewed (Vision, 2026-10-12, 10 of 10 checks): `ZEN_LAW_FILE_BYTES` 24,576 in place of the
appendix's own cap, the self-test red a byte past each cap and green at both, an appendix grown to
9.6 KB under the file cap green and a file at 25.2 KB red, the description free of Zen; one page
left stating the old budgets, `agents/verification.md`'s `law_register` bullet (a router 8,192 since
the first commit, missed by both reviews), its fix a continuation
([prompt](../prompts/law-register-appendix-page.md)). The page fixed in `b90b37d` (run `38189723777`
green), each budget under its value marker, `code_values` red on a stale one (Vision, 2026-10-12):
#201 ready, but it and #202 both rewrite VM-LANE-11 and conflict in either order, so #202 merges
first and #201 is rebased by regenerating its registers from the new `main`
([prompt](../prompts/law-register-appendix-rebase.md)), a docs-only run. #202 merged as `fb6d231`
(2026-10-12); #201 rebased as `d78a2a6` on it, its registers regenerated from that `main` and proven
again, VM-LANE-11 with #202's BECAUSE, run `38194233891` green, Vision's comparison against
`fb6d231` the same as before ([report](../reportbacks/law-register-appendix-rebase-RB.md)): ready to
merge (Vision, 2026-10-12).

## 5a. Night Lab

### BL-LAB-01 — Night Lab, era 2: agents make panes and setups for both hands

**State:** HELD, TOP-DOWN (the founder, 2026-10-15) — the thread that ran the merge train holds it,
while a new Vision writes Path 1's prompts ([the
handoff](handoffs/night-lab-scaffolding-handoff.md)): the lab drafts, ahead of Phases 2 and 3, the
panes and setups on the target, how a gesture or a request travels, and what each screen shows a
person and offers an agent, in [`rebuild-scaffold/`](../rebuild-scaffold/README.md) until the wall
is built; no pull request of its own while Path 1 cuts the spine; its findings go through the
founder to Vision. A1, the panes, drafted (2026-10-15). The wall built and checked (2026-10-16): its
own distribution, `Zen-Night-Lab`, with no Windows drive, program or PATH, no GPU, no root for its
agent, WSLg off for every distribution, and a token reaching only `zen-night-lab`; 23 checks passed,
the shared network the one limit ([machine facts](machine_facts.md)). Before that: ORDERED, ITS
THREAD GONE — the lab's own thread went, with deep review, before any of era 2 reached the lab's
repository (its last commit 2026-08-07): "we are going to need to take hold of Night lab if we want
to use it" (the founder, 2026-10-14). Vision proposes holding it: era 2's question becomes the
roadmap's story, done by an agent through a person's eyes and hands on installed packages inside the
wall; readied in the gaps, the wall first, then the standing prompt; runs on his word once the
story's first slice exists; the wall was never built, nothing of it having left a trace in Zen (the
founder, 2026-10-14). Before that: after the agent's desk (BL-WORK-38) and the documentation
rewrite; its own thread prepared ([the handoff](handoffs/night-lab-handoff.md)) (the founder,
2026-10-09)  
**Owed:** the lab's new question, "Can agents create new panes and setups that are efficient for
both them and the human user?" An agent on its own host drives a Workshop through the agent's desk,
and each pane or setup it makes is judged by what it costs an agent and what it costs a person.
- The wall, agreed: a dedicated WSL distribution, fresh, with drive automount, Windows interop and
  the Windows `PATH` off; the executor inside it; Loom and Zengine pinned per run from GitHub and
  recorded in `substrate.lock`; a GitHub token that reaches only `zen-night-lab`; its own Workshop a
  development host.
- Findings: raw in each run's folder of the lab repository; the best explained in its
  `experiments/` folder, with what was left unfinished and suggestions for the next experiment;
  security findings never in the public repository; a promoted finding becomes an issue or a plan.
- The era before it (`current/`, ZNL-R to ZNL-06, Loom only) ran dry: its last four runs opened no
  new friction entry.
- Seeds from the "Perspectives" proposals (the founder, 2026-10-09): prototypes of the Codex and
  the Data Conversion Mapper as panes and setups an agent makes; the Proving Grounds once the
  desk's stage 7 lands (a crash is caught only out of process, under Loom's isolation host or a
  session run); the Autopsy Table and the Conductor as lab ideas only. The Cartographer waits on a
  Loom decision: Loom enumerates no participants, and `zen.QueryRole` cannot tell an unheld role
  from one held where the kernel cannot see, so a map of the bus would invent facts.

**Source:** the founder (2026-10-09).

## 5b. The local lane

### BL-LANE-01 — Open-weight models on a friend's cards, and our agents on them

**State:** SHELVED — the founder is weighing where the agents run, on our side or on the friend's
machine beside the models (2026-10-10). Researched
([its report](../reportbacks/local-lane-research-RB.md), its decisions in
`local-lane/decisions.md`); L3 would become the Pi coding agent, the harness the
friend runs, its switch written ([prompt](../prompts/local-lane-2.md)) and run (2026-10-10, Zen
`31120f9`, a kit-wide build slot among its changes; unreviewed while shelved); the other nine,
and L7's room, await his word. The fast-builds research counts a kit-wide build lock beside stage
7d's slot a mistake (its decision 6), which L7's room would need to answer. The friend offers his
machine as a build machine (2026-10-10), which the founder sees as easier now than the whole
pipeline for fixing issues  
**Owed:** bounded work keeps moving beside the architecture work, now and past the founder's window
(2026-10-26): three stations on the friend's AMD host (MiniMax-M2.5 for code; Qwen3.8-27B for docs,
triage and review; Qwen3.5-9B for condensing), our agents in a wall on the founder's machine, a
courier and a gate between them and GitHub, and a trial of three `local-ok` issues and one guide
test.

**Source:** the founder (2026-10-09 and 2026-10-10).

## 6. Explicitly not backlog

The following remain trigger-governed horizons or pressure, not owed cleanup:

- tabs, Vim emulation inside the built-in Editor, syntax highlighting, a VFS, file watcher, or Flow
  editor (a differently-shaped Editor arriving as a pane weave is P-WORK-07's case, not this);
- arbitrary pane drawing, same-PaneRef multiplicity, or plugin discovery;
- live artifact replacement before a concrete owner/continuity case;
- general obligations, group/consensus, metadata, or persistence frameworks;
- multithreaded dispatch;
- Windows native containment or escape-tier security;
- production Bridge hardening before hosted/remote use;
- a replacement SDL executor for Loom's portable pixel layout brain.
