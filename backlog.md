# Zen Standing Backlog

**Status:** PRIVATE LIVE AUTHORITY  
**Refreshed:** 2026-10-03\
**Role:** work Zen knowingly owes but is deliberately not doing now  
**Pressure:** `private/pressure.md`

An item here is not authorized work and does not imply urgency. Closed items have been removed from
the live file; their evidence remains in reports and Git history.

## 1. Rules

An item belongs here only when Zen has decided work is owed. A possibility, known seam, or observed
pressure stays outside until that decision exists. Every item names its wake condition and source.

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

**State:** PARKED / PRESERVATION  
**Owed:** Do not let the small Hello/provider witness become incomprehensible or disappear before an
ordinary maker can inspect how a pane arrives. If Workshop gains a real project-template or
installed-pane story, convert the witness into a dissectible example rather than inventing a second
tutorial implementation.

**Wake:** installed external-pane distribution, project templates, or a Workshop-native “open this
tool's source” path.

**Boundary:** this does not itself authorize a plugin SDK or an installation system.

### BL-WORK-03 — Split the Info value view before it grows again

**State:** PARKED / MAINTAINABILITY  
**Owed:** `info-pane/value_view.hpp` is one class of about 1,340 lines holding the draft, the
owner-operation record and its adoption rules, the watch custody, sampling, field pickup, and the
picture with its controls. The corrections kept it whole because a split was not needed to make the
repairs clear. Extract the picture/controls composition and the watch custody (`Watch`, `ending_`,
start, stop, cycle and the lease answers) into their own image-local headers, keeping every record
per view and the one act entry point. Behaviour and law stay as they are.

**Wake:** the next change that adds an operation, a pending-request kind or a control to that file,
or the file passing 1,500 lines.

**Source:** [corrections report](../reportbacks/zengine-independent-info-workbench-corrections-RB.md).

### BL-WORK-04 — The Pane Creator retires into described views

**State:** DECIDED (the founder, 2026-10-02); ORDERED third, with BL-WORK-05 (2026-10-03)  
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

**State:** DECIDED (the founder, 2026-10-02); ORDERED third (2026-10-03)  
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

**State:** DECIDED (the founder, 2026-10-02); ORDERED fourth (2026-10-03)  
**Owed:** Every pane except Flow, the View Builder and described views writes rows and columns of
text through the prose door: Info, Inventory, Files, the Terminal, the Editors,
Builder, Powers and the rest. Each moves to the canvas, so every pane draws in pixels and a
terminal shows the fallback derived from that picture.

**Wake:** after BL-WORK-05; BL-WORK-09 follows it.
**Source:** as BL-WORK-05.

### BL-WORK-07 — The View Builder's polish

**State:** CLOSED with Zengine #87 (accepted 2026-10-03; the founder merges on green CI), from
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

**State:** ORDERED — second in the founder's order (2026-10-03)  
**Owed:**
- The window opens whole on the screen, centred, and stays on the screen while it resizes during
  load. Today it can open partly out of bounds.
- Layouts, the tab row, is on every desk by default, agent-run setups included. Today a demo
  setup can leave it out.
- Escape deselects, as a default every pane has: first what the pane has selected, then the pane
  itself, once the pane hands the Escape back unspent (`PaneEscapeUnspent`). Today a pane that
  never says so keeps every Escape.
- A file picker for import and export paths: a request for a path that any pane can make, and
  Files answers.
- `external-host/demo.py`, the agents' demo launcher, says a start `failed` at the desk when the
  setup seats a described view, and its `stop` says `readiness deadline expired: None` when a
  pane refuses the quit.

**Wake:** after BL-WORK-07.
**Source:** as BL-WORK-07; the two `demo.py` faults are from the View Builder's
reports (`reportbacks/view-builder-canvas-RB.md`, `view-builder-fixes-RB.md`), added with the
founder's OK (2026-10-03).

### BL-WORK-09 — What the canvas unlocks for every pane

**State:** ORDERED — fourth in the founder's order (2026-10-03), after BL-WORK-06  
**Owed:** Once every pane draws on the canvas, every pane can have:
- A hover cue on whatever a press would activate, from `PaneCanvasHover`.
- A `?` at the pane's top right when the pane offers a summary or a tutorial. Workshop draws the
  mark; the pane supplies the guide.
- Tutorial mode: shifting outlines walk through the pane's own parts in turn, and the places that
  take a drop are outlined in another colour. It never reaches into another pane.

**Wake:** BL-WORK-06.
**Source:** as BL-WORK-07. It also serves Task 6 of `private/goals/stranger-legible.md`.

### BL-WORK-10 — Info rebuilt as a one-slot inspector

**State:** ORDERED — fifth in the founder's order (2026-10-03)  
**Owed:** The founder's picture of Info, seeded in `private/pressure.md` §7: a weave of many
panes, rebuilt with today's Info as a quarry, that takes anything dropped on it or picked in its
selection mode and edits it in fields with boxes. One piece serves it and BL-WORK-09: each pane's
parts and their boxes, read from the pane's press map. Selection mode is how Info, and later the
UI-editing overlay, reach those parts.

**Wake:** after BL-WORK-09.
**Source:** as BL-WORK-07; the seed in `private/pressure.md` §7.

### BL-WORK-11 — Images

**State:** ORDERED — sixth in the founder's order (2026-10-03)  
**Owed:** The canvas draws an image, and a view description holds an image element. A terminal
shows a fallback derived from the picture.

**Wake:** after BL-WORK-10; it needs the whole pixel (BL-WORK-05).
**Source:** as BL-WORK-07.

### BL-WORK-12 — Multiple windows

**State:** LATER — after its own research (the founder, 2026-10-03)  
**Owed:** Workshop opens more than one window. A pane drags from one window into another, and
each window has its own tab row.

**Wake:** the founder selects it, after BL-WORK-11.
**Source:** as BL-WORK-07; `Zengine/reference/todo.txt` asks for it too ("Allow for multi-window").

### BL-WORK-13 — Python scripts as participants

**State:** LATER — after its own research (the founder, 2026-10-03)  
**Owed:** A demo script written in Python runs as a participant in the session: it speaks Zen
shapes on the bus under its own grants, through Loom's ABI (`docs/reference/dynamic-abi.md` in
Loom). Today the demo tools are Python workers of Loom's run manager, and they drive Workshop
from outside, across the admitted link (`external-host/demo.py`).

**Wake:** the founder selects it.
**Source:** as BL-WORK-07.

### BL-WORK-14 — A pane's minimum size

**State:** PARKED / DECIDED (the founder, 2026-10-03)  
**Owed:** Find a good minimum size for a pane to display: the least room in which it shows every
control it offers, and what it does when given less. A pane says only its initial comfort today
(`v2::PaneOffered`, rows and columns), never its least. First met in the View Builder: with the
five-element tally panel in an 800×400 canvas, a shape of three fields dropped on Total asks which
field to show, but the list's reserved rows push the choice and its More below the room, so none
can be chosen. With one row left under the question, More has no row of its own.

**Wake:** the founder selects it.
**Source:** the deep review of #86 (2026-10-03), parked by the founder.

### BL-WORK-15 — The View Builder zooms

**State:** PARKED / DECIDED (the founder, 2026-10-03)  
**Owed:** Zoom on the design canvas, working with the pan and the view's size, so a weaver places
an element to the pixel by hand. A canvas draws text only at its room's one measured size
(`PaneCanvasText` holds no size), so the builder alone could scale the boxes but not the words,
and the canvas would stop showing the view as it runs. Workshop's canvas first learns to draw a
picture at a scale; a terminal does not zoom.

**Wake:** after BL-WORK-05, when the founder selects it.
**Source:** the founder, while the View Builder's polish ran (2026-10-03).

## 3. Bounded defects and quick repairs

### BL-VERIFY-01 — Reconcile Builder field clicks locally

**State:** PARKED / LOCAL FOLLOW-UP; explicitly not a blocker to merging Zengine PR #43.
**Owed:** Resolve the retained Builder role-field evidence: the terminal capture shows
`abcdKef...` while its report claimed `abcKdef...`; the native capture shows `Kabcdef...`
after Home, which cannot distinguish a missed click from a caret-placement defect. Retain the
actual coordinate space, x/y, expected insertion point and before/after value on a local rerun.
Repair product behavior only if the diagnosis establishes a defect.

The native `witness/gui/host/step.ps1` must retain its sent command and fail on an unsettled or
failed probe, missing fresh capture, child failure or mismatched expectation. Exercise a negative
control through that driver. The existing Files checks and maker journey remain usable; no full
workflow replay or new input architecture is owed here.

**Wake:** the next local Builder role-field check or reuse of this native witness driver.

**Source:** founder's 2026-09-21 decision to merge with local evidence follow-up;
[verification review](../reportbacks/zengine-files-builder-mouse-verification-review/review.md).

### BL-DEF-06 — Zengine cleanup notes the `ui/` pass left

**State:** NARROWED on delivery 2026-09-28 by `prompts/backlog-must-have-repairs.md` (Zengine PR
#73, merged), which stated the first three notes' current facts; the two below wait
for their wake  
**Owed:**
- `zengine::ui`'s authored half (`Element`, `resolve`, `hit` and the rest) has had no consumer
  outside its own tests since the object canvas retired (`6c5754a`). It stays public API and is
  revisited at the first release identity (BL-ADOPT-02): retired then if nothing uses it.
- `ui::frame_in` and `ui::resolve` can disagree on a repeated identity; #71 documents it. A fix
  changes `Scene`'s shape, so it waits for a first consumer.

**Wake:** the `ui` question at BL-ADOPT-02; a first consumer of `Scene` for `frame_in`.
**Source:** `reportbacks/zengine-ui-headers-RB.md` (Decisions asked) and the review of #71.

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

**State:** PARKED  
**Owed:** Establish dependable tags/release identity and a public stability/deprecation posture
before external consumers are asked to depend on a named Zen release rather than pinned `main`
identities.

**Wake:** first public release/support promise or multiple external consumers exposed to churn.

### BL-ADOPT-03 — Performance evidence before performance claims

**State:** PARKED  
**Owed:** Do not manufacture a benchmark suite for maturity theater, but do not make throughput or
latency claims without claim-specific measurements.

**Wake:** first material performance promise, observed bottleneck, or adoption decision that
depends on performance.

**Measured foundation:** accepted interaction authoring measures local implementation and shared-fixture
header invalidation on one Windows/MinGW Debug configuration. Native grant edits now have a compiled
owner; the large shared fixture remains a measured pressure, not a claimed general speedup.
The phase evidence owns exact counts/times and the limits of mtime-only probes.

### BL-ADOPT-04 — GitHub from Workshop

**State:** LATER — after its own research (the founder, 2026-10-03)  
**Owed:** Sign in to GitHub from Workshop by GitHub's device sign-in, with the token kept in the
operating system's credential store and never in a Zen file. Upload a weave into a directory of
its own; mark a directory on the computer as linked to a GitHub repository; pull with one click.
What a pull brings loads only under explicit authority (P-WORK-18), and this meets product
distribution (P-ADOPT-01).

**Wake:** the founder selects it.
**Source:** the founder's notes, ordered with Vision (2026-10-03).

## 5. Architectural debt that waits for pressure

### BL-ARCH-01 — Cross-layer public include debt

**State:** PARKED (reassessed 2026-09-12 at the ABI v8 landing; not made material)  
**Owed:** A few portable/public surfaces depend on headers whose current contents happen to remain
platform-neutral. Repair ownership only when a package/platform break or public-header evolution
makes the debt material.

**Measured disposition (loom-joint-publication-landing):** the touched public boundary was traced
header by header. Every new type lives in the layer that owns its concept -- the operation and
its authority beside the Sense types in `switchboard/sense.hpp`, the hook's answer beside the weave
contract, the notices beside `DispatchRefused` in `weave/`, the two statuses and slots in the C
`abi.h` -- and every new include points downward or sideways (switchboard → core; weave → switchboard;
kernel → switchboard, as before). The three-way answer has one truth on each side of the C seam,
joined by two mapping functions (`do_claim_published` library-side, `HostAdapter::claim_published`
host-side), and the package witness and the MinGW/MSVC lanes passed on the installed headers. No
upward include, no platform-conditional content entered a portable header; the debt is unchanged
and left parked with this argument in the report.

**Wake:** relevant package failure, platform break, or touched ownership boundary.

### BL-ARCH-02 — Current-law carrying cost must remain bounded

**State:** WATCH / SUBTRACTIVE DUTY  
**Owed:** Keep mandatory and routed current law organized by subject and rewritten in place. If a
routed file becomes a phase-indexed chronicle or repeated concepts require phase archaeology,
consolidate it without deleting the enforceable law or proof history.

**Wake:** a cold reader cannot find the owner without phase names, or a routed current-law file's
growth materially slows every task touching that surface.

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
