# Handoff: Phase 1 — Composable Weave Facets and One Action Path

From the founder (Krealsion), 2026-10-15. Written by Vision for mid-vision and the Phase 1
execution sessions, assuming Phase 0 (the Round 2 merge train of `#220` to `#249`: ready issues and
the 33 weave manuals) has landed cleanly on `main`.

## Why Phase 1 Comes First

Phase 0 (`manuals-first`, `#234` to `#249`, with the participant census in `BL-WORK-45`) gave us the
empirical map of Zengine's coupling:
- `Zen/reportbacks/manuals-first/ownership.md`: 179 cross-weave entanglement points in 69 ranks, 9
  weaves keeping reload-volatile state in C++ members, and 4 states duplicated across two weaves.
- `Zen/reportbacks/manuals-first/messages.md`: 306 message shapes, 166 with names that do not state
  whether they request, report a deed, observe or answer; 9 messages handled by every pane and 21 by
  half or more.
- `Zen/reportbacks/participant-census-RB.md`: `WorkshopWeave` at 44k LoC (68 accepted / 62 emitted
  shapes, 17 `HostContext` closures, and 4.81 messages/act relaying `TerminalSession`).

Our efficiency rule for the roadmap is strict: **never migrate a bloated pane or split a tangled hub
until the target seam makes the resulting code smaller.**

Right now, two architectural seams must be settled *before* we split `WorkshopWeave` (Phase 2) or
move Workshop's 12 panes onto `graphics/` windows (`BL-WORK-37` Stage 2, Phase 3):

1. **Composable Weave Facets & Multi-Hook `after_delivery` (`P-WORK-72` & `P-WORK-73`)**:
   In `#219` (`graphics/drawing.hpp`), `DrawingWeave` wrapped `loom::WeaveBase` by inheritance and
   claimed Loom's single `after_delivery(loom::Mail&)` hook. That works for a standalone drawer like
   `snake/score.cpp`, but collides with any weave that already defines `after_delivery`
   (`WorkshopWeave`, `EditorPaneWeave`, `NeovimEditorWeave` — `P-WORK-72`), and `Canvas::room`
   ignores terminal/window resizes when the window and incarnation have not changed (`P-WORK-73`).
   More broadly, panes participate in multiple mini-protocols at once (drawing, manuals, actions,
   settings). Implementing them as stacked base classes creates a fragile template tower; implementing
   them by hand in every pane is why `builder-pane/pane.cpp` grew from 56 KB to 151 KB.
2. **Describe Once & One Action Path (`backlog.md` §1b, Theme 3)**:
   Today a click on a drawn control in `graphics/` reaches its owner as `ActionIssued` from the
   window (`graphics/vocabulary.hpp`), while a key reaches a pane through Workshop's keymap as
   `PaneActionRequested`. Meanwhile, only the Builder pane and the desk declare what a press causes
   (`v3::PaneActionRow`), so the other panes' manuals cannot link a press to what it sends. Under
   the founder's naming rule (2026-10-15: a request ends `Requested`, an answer `Answered` or
   `Refused`, a deed in the past tense, an observation as a noun), those two action paths become one
   request path before Graphics Stage 2 puts a Workshop pane on a `graphics/` window.

---

## Baseline (Assuming Phase 0 Complete)

- **Zengine `main`**: `#219` (`aab5177`), the ready-issues batch (`#220` to `#233`), and the manuals
  batch (`#234` to `#249`) all merged and green on `main`, with population floors updated from the
  round-two merge train.
- **Loom `origin/main`**: `3afe9e3` or later.
- Verify `git status` and `git log -n 5` on `main` before branching.

---

## Stage 1A: Composable Weave Facets, Multi-Hook `after_delivery`, and Room Resize (`P-WORK-72`, `P-WORK-73`)

### Outcome

1. **Composable Facets (`With<Facets...>`)**:
   A weave can attach zero or more independent protocol facets as value members (no deep inheritance
   chain), where each facet encapsulates one mini-protocol:
   - Its `Accept<...>` and `Emit<...>` lists are automatically unioned into the weave's
     `accepted_schemas()` and `emitted_schemas()` at mount time so Loom's gate (`GATE-01..04`) and
     `zen.DescribeAccepted` see the exact, truthful schema set.
   - Inbound deliveries matching a facet's `Accept` list route to that facet's handler (`facet.on`),
     while the weave's own `Accept` list routes to `Self::on` as today.
2. **Deterministic Multi-Hook `after_delivery` Chain (`P-WORK-72`)**:
   At the end of every mutating delivery (and mutating poke), the weave's own
   `self->after_delivery(mail)` (if defined) runs **first**, followed by each attached facet's
   `facet.after_delivery(*self, mail)` in declaration order. A weave that updates its state or
   canvas inside its own `after_delivery` has its canvas flushed by `DrawingFacet` in the same turn
   with zero hook collision.
3. **Room Resize Reaches the Drawer (`P-WORK-73`)**:
   `Canvas::room` (and `DrawingFacet` / `DrawingWeave`) detects when an `AreaRoom`'s `w` or `h`
   changes even when `window` and `epoch` are unchanged, updates the room dimensions, and triggers
   the drawer's `picture` / resize redraw.
4. **Shipped Facets in Stage 1A**:
   - `graphics::DrawingFacet` (replacing or underlying `DrawingWeave` so `snake/world.cpp`,
     `snake/score.cpp`, and `snake/play.cpp` use it cleanly).
   - `manual::ManualFacet` (answering `PaneDocumentRequested` / `ShapeDocumentRequested` from the
     weave's compiled-in `kManual` without per-weave handler boilerplate).

### Deliver (Stage 1A)

1. One pull request in Zengine (or paired with a small Loom header PR only if `loom::WeaveBase`
   itself is extended; prefer keeping Zengine-specific facet sugar in Zengine if `WeaveBase` needs no
   change).
2. Rewritten consumers: `snake`'s drawers (`world.cpp`, `score.cpp`, `play.cpp`) and at least two
   manual-answering weaves migrated onto `ManualFacet` to prove line-count reduction.
3. Witnesses, each red without the change:
   - A weave defining its own `after_delivery(loom::Mail&)` alongside `DrawingFacet` and
     `ManualFacet` runs both hooks in order (`self` first, then `DrawingFacet`), flushing changes
     made inside `self->after_delivery` (`P-WORK-72`).
   - An `AreaRoom` with the same `window` and `epoch` but changed `w` or `h` updates `Canvas` dimensions
     and redraws (`P-WORK-73`).
   - `zen.DescribeAccepted` on a facet-equipped weave reports the exact union of the weave's and
     its facets' accepted schemas.
   - Every witness from `#218` and `#219` stays green, and Snake's bus bytes/tick (`68.0`) and
     terminal bytes/tick (`27.52`) do not regress.
4. Hosted run green on all 8 jobs, and `Zen/reportbacks/phase-1a-facets-RB.md`.

---

## Stage 1B: Describe Once & One Action Path (`backlog.md` §1b, Theme 3)

### Outcome

1. **One Action Request Path**:
   Unify `graphics::ActionIssued` and Workshop's action invocation under the founder's naming rule
   (`*Requested` for requests, `*Answered` or `*Refused` for answers, past-tense verb for deeds,
   noun for observations). A click on an element with an action in a `graphics/` window and a key or
   semantic invocation reach the owner through one action request shape.
2. **Direct Window Key Routing**:
   In `graphics/`, when an area holds `keys = true`, the window routes key events straight to the
   area's owner with no Workshop keymap relay in the middle.
3. **Complete Cause Declarations Across Panes**:
   Extend `v3::PaneActionRow` cause declarations (`causes`, with the pane's `mode`, the row's
   `enters`, and `elsewhere`) to the remaining Workshop panes that currently omit them (every pane
   beyond the Builder pane and Desktop, as mapped in `manuals-first-RB.md`), verified by
   `tests/actions.txt`, the press witness, and the `manual` check so every pane's manual links a
   press to what it sends.
4. **Composable `ActionFacet`**:
   Package action declaration and request dispatch into a facet on Stage 1A's mechanism so a pane
   declares its action table once and does not hand-roll action-announcement and dispatch plumbing.

### Deliver (Stage 1B)

1. One pull request on top of Stage 1A.
2. Updated `tests/actions.txt` census, press witnesses, and pane manuals where newly declared
   `causes` link presses to their emitted shapes.
3. Witnesses, each red without the change:
   - Clicking an action-bearing element in a `graphics/` window and invoking the action semantically
     deliver the same `*Requested` shape to the area's owner.
   - Every shipped Workshop pane's action rows declare their `causes`, verified by the press witness
     and `manual` check.
4. Hosted run green on all 8 jobs, and `Zen/reportbacks/phase-1b-actions-RB.md`.

---

## Fences & What Not To Do (Both Stages)

- **Code and complexity must shrink or hold flat**: report the net line change in every touched
  consumer weave. If a facet makes a consumer longer or harder to read, stop and surface why.
- **No wholesale wire rename**: apply the message naming rule (`*Requested`, `*Answered`/`*Refused`,
  past-tense deed, noun observation) strictly to every new or unified shape in Phase 1; leave
  untouched legacy shapes for the phase that extracts their owner (`backlog.md` §1b.3).
- **Do not move Workshop's panes onto `graphics/` windows in Phase 1**: that is Graphics Stage 2
  (after Phase 2 extracts the Terminal door and completes the window/arrangement seam).
- **Nothing of ours that a stranger's weave could not use the same way**: facets and action
  contracts must use public Loom/Zengine headers only.
- **Standalone public pull requests**: no `Zen/` paths, report names, plan IDs, or AI attribution in
  commits or pull request descriptions.
- **Work in clones of your own**: leave the primaries and the founder's checkouts untouched and
  unfetched; one full build at a time (constitution section f); do not merge.

---

## Workflow Across Vision, Path 1 (Primary Dev), and Path 2 (Night Lab)

1. **Path 1 (Primary Dev Executor, driven by Vision)**:
   - Once the Round 2 merge train (`#220` to `#249`) is merged and `main` is green, run Stage 1A
     from `Zen/prompts/phase-1a-facets.md` (warm or cold).
   - Bring `Zen/reportbacks/phase-1a-facets-RB.md` and the PR back to Vision for review before
     merging, then launch Stage 1B.
2. **Path 2 (Zen Night Lab, held by the repurposed merge-train thread)**:
   - Runs concurrently from `Zen/private/handoffs/night-lab-scaffolding-handoff.md`, producing the
     pane/setup scaffolding, interaction choreography, and pairing-intent UI drafts in
     `Zen/rebuild-scaffold/` ahead of Phase 2 and Phase 3.
3. **What Follows Phase 1 (Phase 2 Preview)**:
   With composable facets and the unified action path in place, Phase 2 begins the hub split
   (`backlog.md` §1b, Theme 2): extracting the native Terminal door first (ending Workshop's
   4.81 messages/act relay), fixing the 9 reload-in-place state leaks (`ownership.md`), and moving
   the window/arrangement job whole into `graphics/`.
