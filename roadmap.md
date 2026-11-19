# Zen roadmap

**What it is:** the order Zen follows: the long road, and the directions it takes now, each with
why it matters and its goals in order. It changes only when the direction or the order does.  
**Beside it:** [README.md](README.md), the map and the rules; [current_state.md](current_state.md),
where Zen is now and what runs; [goals/](goals/), a checklist a goal;
[backlog.md](backlog.md), work decided and not pursued.  
**Updated:** 2026-11-18, the state split out into its own file.

## The long road

Its stages, in order: a credible substrate; a Workshop makers enjoy; projects anyone can build; a
Zen strangers can read; hosted weaves; trust across many authors; and at its end Zen teaching,
building and stewarding beside the people in it. Where each stands: Workshop is the current one;
a Zen strangers can read is underway through the standing duties below; hosted weaves are not
selected (they get a goal of their own before any hosting work); trust across many authors is a
required long path, unbuilt; Tutor, Builder and Steward are a horizon, three roles kept distinct.

## The near road

The founder's direction of 2026-11-08: finish what is already decided, through Workshop's move to
its own repository, stopping only for detours that are plainly right, with concerns marked for
the end. Three directions joined it since: Loom's gaps closed so that Zengine's files shrink
rather than grow around them (2026-11-10); drawing that fits a real-time frame and reads
naturally to the person writing it (2026-11-14); and readability as a pillar beside modularity,
in the code and in the docs (2026-11-15). The release comes after them.

## The goals

Each direction, with why it matters, and its goals in order; each goal is a checklist in
[goals/](goals/), and what runs now is in [current_state.md](current_state.md).

Now:

1. **The ways of working.** The plan and both constitutions were rebuilt in three days; a reader
   with no memory checks them before Ceecee's memory is rebuilt around them. And the law an agent
   carries, over half a megabyte, is cut to what a stranger could break.
   [instruction-audit](goals/instruction-audit.md), [audit-recheck](goals/audit-recheck.md),
   [law-cut](goals/law-cut.md).
2. **The machine.** Every lane waits on it.
   [machine-restore](goals/machine-restore.md).
3. **Drawing for real-time games.** A game is the hardest everyday test of a drawing design; the
   founder wants drawing that fits a 16 ms frame and reads naturally to the person writing it.
   [tile-defense](goals/tile-defense.md), [drawing-order-names](goals/drawing-order-names.md),
   [drawing-speed](goals/drawing-speed.md), [game-time](goals/game-time.md),
   [ports](goals/ports.md).
4. **Security** (private). A defect outranks features. [queue-budget](goals/queue-budget.md);
   the session key and the schema id finished 2026-11-10 (history).
5. **Loom's foundation.** Close the gaps Zengine builds around, so its files shrink and no
   god-file grows back. [data-plane](goals/data-plane.md), [takeover](goals/takeover.md),
   [one-host](goals/one-host.md), [schema-evolution](goals/schema-evolution.md),
   [unions-rest](goals/unions-rest.md), [calls-in-zengine](goals/calls-in-zengine.md).

Next:

6. **Untrusted code.** One home for it that holds on every platform; recovered 2026-11-15, after
   it fell off the plan. [wasm-box](goals/wasm-box.md),
   [sandbox-retired](goals/sandbox-retired.md).
7. **The Workshop split.** The founder's baseline runs through it.
   [pane-contract](goals/pane-contract.md), [owned-names](goals/owned-names.md) (decided
   2026-11-09, never built), [workshop-move](goals/workshop-move.md).
8. **The visual foundation.** "High quality components means higher quality composites" (the
   founder, 2026-10-29). [looks-in-time](goals/looks-in-time.md),
   [keys-and-presses](goals/keys-and-presses.md), [element-set](goals/element-set.md),
   [view-cost](goals/view-cost.md).
9. **The makeovers.** The panes rebuilt on the new pieces, Flow's way: the design taken whole.
   [flow-next](goals/flow-next.md), [view-builder-makeover](goals/view-builder-makeover.md),
   [operator-suite](goals/operator-suite.md).
10. **Readability.** Code pleasant to write, docs plain first.
   [language-pass](goals/language-pass.md), [front-doors](goals/front-doors.md).
11. **The release.** Zen in people's hands, after Workshop's move. [release](goals/release.md).

## Standing duties

- **Reviews and filing** (Vision): every report in `unreviewed/` reviewed and filed, and the plan
  changed as [README.md](README.md) orders it.
- **A Zen strangers can read** (the founder, 2026-09-25): a plain first-read path; no private
  information in documents or comments.
- **The drawing door's full set** (BL-WORK-37): ovals, polygons, images, shaders and whole
  widgets, built for the design rather than as consumers ask.
- **Grow with use**: Workshop and onboarding together (BL-WORK-01); a front door for contributors
  before asking for any (BL-ADOPT-01); current law cheap to carry (BL-ARCH-02).

## Marked for the end

The concerns the baseline set aside, readdressed when the Workshop split is done:

- `PaneRefusalRequested` (#126) lets any seated pane have Workshop say a sentence as its own
  refusal notice; the notice should say whose refusal it is.
- The issue lane posts none of the comments `taking-an-issue.md` asks for.
- The security pair's one-way doors and its structure.
- #18's quoted red cannot come from its final case; #136's catalog counts four text documents
  where there are five.
- Office to role's leftovers: the code's multi-word names (a census of identifiers first) and the
  13 console pictures; once both are in, the kit's version-1 grants of `Run` and `RunList` go.

## Horizons, and what stays out

A horizon defines a completeness test; it never authorizes a demo-driven build.

- **Horizons**: live debugging; a scalable kernel; replaceable weaves; modders are players; a
  semantic computing environment where declaration, presentation, runtime, source and failure
  are navigable views of meaningful things; one-shot authority, which Loom has not earned;
  Zenscript's return; scouting threads that prepare answers for the main thread to check and
  apply; a compile-down to a standalone app with no Loom in it; a small 3D third-person action
  game with procedural animation as Workshop's final test.
- **Stays out** (not owed work): tabs, Vim emulation, syntax highlighting, a VFS, a file watcher
  or a Flow editor inside the built-in Editor (a differently shaped editor arrives as a pane
  weave); one pane shown several times, and plugin discovery; live artifact replacement before a
  concrete owner and continuity case; general obligation, consensus, metadata or persistence
  frameworks; multithreaded dispatch (not built, and nothing may assume it never will); Windows
  native containment (the box runs everywhere instead); production hardening of the bridge
  before hosted or remote use; a replacement SDL executor for Loom's portable pixel layout.
