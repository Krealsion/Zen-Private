# The loose changes: what the clean-up carried, and what to keep

**What this is:** every piece of work the relicense clean-up found that `main` lacked, now on the
new history: 100 pieces. Yours sit in `Zen/Loom` and `Zen/Zengine`; the rest are `carried/*`
branches in the kit's primary (`Zen/primary/`). Also the three pull requests `-history` holds closed
without a merge. Vision read each against `main` on 2026-11-02: its commits, its pull request, and
how much of it `main` already holds. Pull request numbers are the `-history` repositories'.

**Vision's lean:** keep 1, let the other 99 go. Nearly all are earlier states of work that merged
later in a better form.

**How to answer:** a "Your call:" line under each group. To keep a single piece from a group you let
go, name it there. Ceecee then deletes what goes, in one short round. A piece only this machine held
is then gone for good; anything once pushed stays in `-history`.

## 1. Keep (1)

- `carried/batch/lane-view-builder` (primary, 3 commits, 2026-10-28): #487, closed without a merge.
  The View Builder keeps one layout at every width, Add's kinds a row each beneath Grid, its pages
  taken again. The makeover carries both; this is its start.

Your call:

## 2. Landed in main, in a later form (59)

- `carried/156` (primary, 2 commits, 2026-10-09): The glance keeps every word at its own cell, a
  word on a frame's edge wr... -- landed.
- `carried/accordion/stage-2` (primary, 6 commits, 2026-10-29): A pane's open sections are read from
  its state and written there: the in... -- landed as #568.
- `carried/backup/pre-rebase-fixes-2` (primary, 14 commits, 2026-10-08): Every Zengine program on
  Windows runs in the UTF-8 code page, its tests ... -- landed.
- `carried/backup/pre-rebuild-1` (primary, 5 commits, 2026-10-08): Every Zengine program on Windows
  runs in the UTF-8 code page, its tests ... -- landed. Its one commit main lacks is a 5-file
  wording change about UTF-8 paths in the records.
- `carried/backup/pre-rebuild-2` (primary, 5 commits, 2026-10-08): Every Zengine program on Windows
  runs in the UTF-8 code page, its tests ... -- landed.
- `carried/batch/lane-text-input` (primary, 2 commits, 2026-10-28): The Editor's right press opens
  its own menu -- undo, redo, cut, copy, pa... -- landed.
- `carried/batch/lane-text-input-2` (primary, 3 commits, 2026-10-28): The Editor's right press opens
  its own menu -- undo, redo, cut, copy, pa... -- landed.
- `carried/docs/law-register-appendix` (primary, 3 commits, 2026-10-11): The law registers' proofs
  stand in an appendix with a budget of its own,... -- landed as #201.
- `carried/docs/tutorial-walks` (primary, 1 commit, 2026-10-11): Every tutorial is replayed from an
  installed prefix: tutorial_walks, and... -- landed.
- `carried/editor/right-press-menu` (primary, 4 commits, 2026-10-28): The Editor's right press opens
  its own menu -- undo, redo, cut, copy, pa... -- landed as #488.
- `carried/editor/right-press-menu-c8542310` (primary, 2 commits, 2026-10-28): The Editor's right
  press opens its own menu -- undo, redo, cut, copy, pa... -- landed as #488.
- `carried/fix216` (primary, 1 commit, 2026-10-14): The two text checks read a /* in a C++ line
  comment or string literal as... -- landed.
- `carried/flow/wire-drop` (primary, 2 commits, 2026-10-22): Flow drags a wire from either end, and
  let go on empty room it asks what... -- landed as #362.
- `carried/flow/wire-drop-625ba999` (primary, 3 commits, 2026-10-22): Flow drags a wire from either
  end, and let go on empty room it asks what... -- landed as #362.
- `carried/graphics/g2-no-second-picture` (primary, 1 commit, 2026-10-23): A pane draws only in its
  own area of the window -- landed as #380.
- `carried/graphics/window-shaped` (primary, 3 commits, 2026-10-22): An app's window takes its name
  and its size from the office that arrange... -- landed as #353.
- `carried/graphics/window-shaped-8370c984` (primary, 3 commits, 2026-10-22): An app's window takes
  its name and its size from the office that arrange... -- landed as #353.
- `carried/graphics/window-shaped-96ffb21d` (primary, 2 commits, 2026-10-22): An app's window takes
  its name and its size from the office that arrange... -- landed as #353.
- `carried/head-0623f609` (primary, 1 commit, 2026-10-22): The editor a weaver switched to is the
  editor the next start opens -- landed.
- `carried/head-29d0f333` (primary, 1 commit, 2026-10-10): Every part moves into its feature's
  folder and every page into the folde... -- landed.
- `carried/head-29ebdba8` (primary, 2 commits, 2026-10-22): A command palette lists every action and
  pane by name, and Workshop runs... -- landed.
- `carried/head-63b1e543` (primary, 1 commit, 2026-10-14): A test compile reaches its checkout and
  build tree by name, so a compile... -- landed as #230.
- `carried/head-76b11947` (primary, 2 commits, 2026-10-15): Compose moves, includes and goes back by
  the action rows it declares, so... -- landed as #232.
- `carried/layout/words-on-the-desk` (primary, 4 commits, 2026-10-25): The desk takes ui's words:
  share, fit and fill, and the room's points -- landed as #421. Its one commit main lacks is a
  2-line fixup!.
- `carried/layouts/desk-own-owner` (primary, 5 commits, 2026-10-24): Layouts: the store as a value,
  Workshop asking it for every change -- landed as #415.
- `carried/manuals/desk-doors` (primary, 1 commit, 2026-10-15): The opening office, the realization
  owner and the menu presenter each ca... -- landed.
- `carried/manuals/desk-workshop` (primary, 1 commit, 2026-10-14): Workshop's office carries its
  manual: the pane protocol, shape by shape -- landed.
- `carried/manuals/info` (primary, 1 commit, 2026-10-15): Info carries its manual and answers it for
  each of its panes -- landed.
- `carried/manuals/introspection` (primary, 1 commit, 2026-10-15): Loaded, Project and Powers, and
  the three doors they ask, carry their ma... -- landed.
- `carried/manuals/inventory` (primary, 1 commit, 2026-10-15): Inventory carries its manuals, the
  office's and the pane's, and answers ... -- landed.
- `carried/palette/other-entries` (primary, 1 commit, 2026-10-26): The palette lists layouts,
  manuals, setups and apps, each run by the pat... -- landed as #444.
- `carried/rehearsal` (primary, 11 commits, 2026-10-15): Compose carries its manual and answers it,
  as a pane and for the shapes ... -- landed.
- `carried/snake/grow-keeps-the-board` (primary, 1 commit, 2026-10-15): A grown snake world leaves
  the window its old board until the inheritanc... -- landed as #233.
- `carried/terminal/enter-takes-a-moved-row` (primary, 4 commits, 2026-10-28): The Editor's right
  press opens its own menu -- undo, redo, cut, copy, pa... -- landed.
- `carried/tests/tree-paths` (primary, 1 commit, 2026-10-15): A test compile reaches its checkout
  and build tree by name, so a compile... -- landed as #230.
- `carried/view/window-pointer` (primary, 2 commits, 2026-10-22): A view hears its window's pointer,
  so an app's fields are clicked into -- landed as #358.
- `carried/workshop/agent-desk-2` (primary, 1 commit, 2026-10-09): The desk says when it moved, a
  stamp names each picture by what it shows... -- landed as #158.
- `carried/workshop/desk-read-bytes` (primary, 1 commit, 2026-10-09): A pane's page and the desk
  read stay inside one reply's bytes as well as... -- landed as #157.
- `carried/workshop/editor-remembered` (primary, 1 commit, 2026-10-22): The editor a weaver switched
  to is the editor the next start opens -- landed as #371.
- `carried/workshop/legacy-import-bound` (primary, 1 commit, 2026-10-14): The legacy import reads up
  to the durable file's own read ceiling, so a ... -- landed as #225.
- `carried/workshop/log-selection-owner` (primary, 1 commit, 2026-10-14): Workshop's durable log
  selection is one named value the host builds its ... -- landed as #226.
- `carried/workshop/log-selection-owner-d06f6c25` (primary, 1 commit, 2026-10-14): Workshop's
  durable log selection is one named value the host builds its ... -- landed as #226.
- `carried/workshop/palette` (primary, 1 commit, 2026-10-22): A command palette lists every action
  and pane by name, and Workshop runs... -- landed as #368.
- `carried/workshop/pane-row-gaps` (primary, 1 commit, 2026-10-14): A pane row the terminal cannot
  produce is admitted as it stands and its ... -- landed as #227.
- `carried/workshop/restore-said-once` (primary, 1 commit, 2026-10-26): The restore's sentence is
  said once, in the unit the first window names,... -- landed as #441.
- `carried/kernel/box-doors` (primary, Loom, 2 commits, 2026-10-29): Every door through a real
  module: the door cases run on boxed twins, and... -- landed as Loom #75.
- `docs/vision-consolidation-20260910` (your Zengine, 2 commits, 2026-09-10): Route extracted pane
  work to its behavior and protocol owners -- landed.
- `reflog/1ebc9a1225` (your Zengine, 1 commit, 2026-09-30): A documentation lane for a change that
  touches no compiled line -- an earlier state of a commit you amended; it landed.
- `reflog/2d9b0cbab5` (your Zengine, 1 commit, 2026-09-06): Workshop: a realize refusal has a place
  it can be read whole -- an earlier state of a commit you amended; it landed.
- `reflog/453e4f2cb6` (your Zengine, 5 commits, 2026-10-07): an earlier state of commits you
  amended; 4 of its 5 landed, and the fifth adds one line to an ignore file.
- `reflog/6ca9b557b7` (your Zengine, 1 commit, 2026-09-07): A pane's notice stands until the maker's
  next act, and has a row to stan... -- an earlier state of a commit you amended; it landed.
- `reflog/969c19a6d6` (your Zengine, 1 commit, 2026-09-06): Workshop: a realize refusal has a place
  it can be read whole -- an earlier state of a commit you amended; it landed.
- `reflog/9ca2c55abd` (your Zengine, 1 commit, 2026-08-26): Make TextBox feel like a text box:
  selection, clipboard, history, one ke... -- an earlier state of a commit you amended; it landed.
- `workshop/comment-compression` (your Zengine, 3 commits, 2026-09-24): Compress Workshop's comments
  into their owners, and keep them there -- landed as #61.
- `reflog/181b7707e5` (your Loom, 1 commit, 2026-08-08): Make the component depth cap the first
  bound, not the C++ stack -- an earlier state of a commit you amended; it landed.
- `reflog/5b0a993a13` (your Loom, 1 commit, 2026-09-30): code_values holds the values the code owns
  -- an earlier state of a commit you amended; it landed.
- `reflog/cb65dd2714` (your Loom, 1 commit, 2026-09-30): code_values holds the values the code owns
  -- an earlier state of a commit you amended; it landed.
- `reflog/d58639a3ea` (your Loom, 1 commit, 2026-09-30): A documentation lane for a change that
  touches no compiled line -- an earlier state of a commit you amended; it landed.
- `weave/carry-runtime-on-windows` (your Loom, 1 commit, 2026-10-10): A weave built through the
  contract carries its own C++ runtime on Window... -- landed as Loom #53.

Your call:

## 3. Stopped, then done another way (15)

- `carried/desk/glance-boundary-row` (primary, 1 commit, 2026-10-09): a WIP of #156's glance, which
  landed.
- `carried/flow/made-over` (primary, 27 commits, 2026-10-29): Flow's makeover before #559 squashed
  it. Main holds it, and Flow's next round on top.
- `carried/flow/made-over-7b82fde6` (primary, 7 commits, 2026-10-28): an earlier state of the same
  makeover (2026-10-28).
- `carried/head-19c63b74` (primary, 2 commits, 2026-10-27): the mutants corpus while it was built;
  the corpus landed that day and was settled the next.
- `carried/pr333` (primary, 3 commits, 2026-10-19): #333's routing plus a laws commit; 77 of its 127
  added lines are in main, the rest moved on.
- `carried/wip-mutants-1793158047` (primary, 16 commits, 2026-10-27): the same corpus WIP, 16
  commits; main's corpus has 48 pages to its 43.
- `carried/exp/editor-managed-open-corrections` (primary, Loom, 3 commits, 2026-09-12): your Codex
  session's managed-open experiment (2026-09-11/12). Loom's joint operations and the editor's
  custody landed another way.
- `audit/panel-sheet` (your Zengine, 3 commits, 2026-09-29): the panel audit's local proof, never
  for push; the audit's renames merged.
- `reflog/52c7884db3` (your Zengine, 1 commit, 2026-09-08): Info's retirement from the host,
  unfinished (2026-09-08); Info became a weave later.
- `reflog/c9382f614e` (your Zengine, 2 commits, 2026-09-29): the maker-to-weaver rename's hand pass
  in progress; the rename merged.
- `stash@{0}` (your Zengine, 1 commit, 2026-08-15): your stash, on a commit of 2026-08-14: DIST-0,
  Windows bundles linking the C++ runtime statically. The package workflow ships Workshop another
  way.
- `reflog/8b163f853a` (your Loom, 29 commits, 2026-09-27): the Loom comment arc before it was
  squashed, as you wanted (2026-09-27).
- `reflog/906a772c9b` (your Loom, 30 commits, 2026-09-28): the same arc, a later state.
- `reflog/9e981ded10` (your Loom, 30 commits, 2026-09-27): the same arc.
- `reflog/c45ede5570` (your Loom, 38 commits, 2026-09-27): the same arc, 38 commits.

Your call:

## 4. Proofs, probes and scratch, never meant to merge (25)

- `carried/head-40a38d2e` (primary, 1 commit, 2026-09-15): a mutation matrix's scratch tree
  (2026-09-15).
- `carried/proof/ci-windows-lanes-cache` (primary, 2 commits, 2026-10-11): a CI cache proof, never
  meant to merge.
- `carried/proof/ci-windows-lanes-cache-fcbc1053` (primary, 1 commit, 2026-10-11): the same proof.
- `carried/proof/line-tables-ab` (primary, 1 commit, 2026-10-20): a build measurement (-g against
  -g1), its numbers in its report.
- `carried/proof/line-tables-g` (primary, 1 commit, 2026-10-20): the same measurement.
- `carried/proof/line-tables-g1` (primary, 1 commit, 2026-10-20): the same measurement.
- `carried/proof/sdl-share` (primary, 1 commit, 2026-10-20): SDL's share of the Linux jobs,
  measured; its numbers in its report.
- `carried/uncommitted/Zen-primary-set-aside-before-relicense-zengine` (primary, 1 commit,
  2026-11-01): the Develop Workshop run configuration, 2 lines.
- `carried/uncommitted/d2-src-zengine` (primary, 1 commit, 2026-11-01): test edits in desk split
  D2's WSL copy; D2 merged.
- `carried/uncommitted/desk-split-d2-start-zengine` (primary, 1 commit, 2026-11-01): the same edits,
  D2's START copy.
- `carried/uncommitted/desk-split-d3-start-zengine` (primary, 1 commit, 2026-11-01): test edits in
  desk split D3's START copy; D3 merged.
- `carried/uncommitted/issue-lane-after-the-alpha-pics` (primary, 1 commit, 2026-11-01): four
  pictures from the alpha's picture lane, two never committed; retaken since.
- `carried/uncommitted/lane-src-zengine` (primary, 1 commit, 2026-11-01): edits left in the
  keyboard-focus lane's copy; its phase is done.
- `carried/uncommitted/red-src-zengine` (primary, 1 commit, 2026-11-01): a red test written to show
  a guest-door defect; its phase is done.
- `carried/uncommitted/start-src-zengine` (primary, 1 commit, 2026-11-01): the same edits, its WSL
  copy.
- `carried/uncommitted/start-src-zengine-fcb0fc0d` (primary, 1 commit, 2026-11-01): the same edits
  again.
- `carried/uncommitted/trees-red-zengine` (primary, 1 commit, 2026-11-01): the same red test.
- `carried/uncommitted/wse-devroot-Zengine` (primary, 1 commit, 2026-11-01): a one-line mutation
  left in a mutation tree.
- `carried/uncommitted/zen-build-wdl-src` (primary, 1 commit, 2026-11-01): a three-line mutation,
  the same kind.
- `carried/uncommitted/COLD-1-negative-loom-mutation` (primary, Loom, 1 commit, 2026-11-01): a
  deliberate one-line mutation of a cold-start check.
- `carried/uncommitted/joshua-cold1-loom-probe` (primary, Loom, 1 commit, 2026-11-01): a cold-start
  probe's test tweak.
- `carried/uncommitted/joshua-cold1-loom-w` (primary, Loom, 1 commit, 2026-11-01): a cold-start
  probe's CMake toggle.
- `carried/uncommitted/participant-census-trees-loom` (primary, Loom, 1 commit, 2026-11-01): 70
  lines of counting added to the switchboard for the participant census research.
- `proof/ci-quick-wins-cache` (your Zengine, 1 commit, 2026-10-10): a CI cache proof, never meant to
  merge.
- `reflog/caea32fb6b` (your Loom, 5 commits, 2026-08-05): three TEMPORARY probe commits (R2F-Fa)
  beside the reloadable-weave contract, which landed.

Your call:

## 5. In `-history` only, closed without a merge (3)

- Loom #79 `docs/message-journey`: the message's-journey page, which you set aside (2026-10-30).
- Zengine #195 and #196 `fix-utf8-decoding-in-tests`: issue 112's UTF-8 decoding in the Python
  session tests, closed; issue 112 is closed too.
- #487 is section 1's piece. The other pushed branches the copies held (49 tips) are states of pull
  requests that merged.

Your call:
