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

**Bounded work moves to GitHub issues** (the founder, 2026-10-09). Defects, review leftovers, doc
fixes, and parked or later ideas are filed as issues on the public repositories, each written as a
small prompt with its fences, so any executor can take one, ship it as its own pull request and
merge it when it is ready. An issue's pull request merges first, and an open phase branch rebases
onto it. A security defect is never a public issue: it goes into a draft private security advisory.
Deep review files them, from [the handoff](handoffs/issues-handoff.md), and files its own findings
outside the pull request under review the same way. A filed item leaves this file for its issue
link. The ordered arcs, research items and direction stay here and move by phases.

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

**State:** ORDERED — in build: researched (2026-10-07); stage 1 written on Loom #31
(`prompts/settings-stage-1.md`, 2026-10-08); before BL-WORK-09  
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

**Wake:** met: BL-WORK-06 closed with #98 and #99 (2026-10-07).
**Source:** the founder (2026-10-07), after #96's light terminal, with the two messages and the
setup file as the store his own.

### BL-WORK-38 — Agents and weavers on one desk

**State:** ORDERED — in build: stages 0, 1 and 2 merged as #150, #151 and #158 (2026-10-09),
#151's three review fixes as #155, #157 and #156 in the issue lane; stages 3a and 3b wait for the
documentation overhaul's folder move and its stages 4a and 4b (BL-ADOPT-05); researched
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

**State:** FILED — the founder's idea (2026-10-09); not yet ordered  
**Owed:**
- The snake demo as simple as it can be. `zengine-snake` (`snake/play.cpp`) keeps only its boot
  list; the demo's operator -- the skin swaps (classic, block, SDL), loading the score weave,
  growing the world, reload in place, new game and the list -- moves out of the host, to the
  external host's driver or into a weave of its own.
- An AI plays snake through messages, with no agent in the loop; an unexpected occurrence calls the
  agent in to review, so the agent improves the AI. The tower-defense example's monitor already
  takes this route: its policy plays the game from the game's own typed events and says FINISHED,
  NEEDS ATTENTION or INCONCLUSIVE, with evidence (`examples/tower-defense/monitor/td_policy.py`,
  event-driven ELH observation, Loom #16 / Zengine #62).

**Wake:** the founder selects it.
**Source:** the founder (2026-10-09), after the tower-defense route: messages received and acted on
with no agent's intervention, the agent reviewing what was unexpected.

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

### BL-WORK-37 — The skin's drawing door

**State:** FILED — researched first; not yet ordered (the founder, 2026-10-07)  
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

**Wake:** the founder orders it.
**Source:** the founder (2026-10-07), after #96, from reference Zengine's `game_graphics` and a
draw list the skin keeps.

### BL-WORK-12 — Multiple windows

**State:** ISSUE — [Zengine#146](https://github.com/Krealsion/Zengine/issues/146) holds it now (filed by deep review, 2026-10-09).

### BL-WORK-13 — Python scripts as participants

**State:** ISSUE — [Zengine#147](https://github.com/Krealsion/Zengine/issues/147) holds it now (filed by deep review, 2026-10-09).

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

### BL-ADOPT-04 — GitHub from Workshop

**State:** ISSUE — [Zengine#145](https://github.com/Krealsion/Zengine/issues/145) holds it now (filed by deep review, 2026-10-09).

### BL-ADOPT-05 — The documentation overhaul: a man page on each weave, a tutorial for each step

**State:** ORDERED — researched ([its report](../reportbacks/docs-overhaul-research-RB.md)); its ten
decisions taken as recommended but F2: no forwarding headers, since the move precedes the first
release (the founder, 2026-10-10). Stage A, the move, opens 2026-10-12
([prompt](../prompts/docs-overhaul-a.md)); then B1, the Builder's manuals; B2, the `?`, with B3,
its tutorial replayed; C, feature by feature in the issue lane to 2026-10-22; D after the release.
BL-WORK-38's stages 3a and 3b follow B2. The research's findings are verified and filed in deep
review's place ([prompt](../prompts/overhaul-findings.md))  
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

**State:** ORDERED — researched first, beside the documentation overhaul's stage B, since it
touches packaging and CI rather than the features, to land before the freeze (2026-10-23)
([prompt](../prompts/release-research.md)) (the founder, 2026-10-10)  
**Owed:** A full release for Windows and Linux, ready to run: extracted into a folder, Workshop
starts with nothing else installed, and the first tutorials begin there (BL-ADOPT-05). A
tutorial's replay on the extracted package can witness the package itself.

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

## 5a. Night Lab

### BL-LAB-01 — Night Lab, era 2: agents make panes and setups for both hands

**State:** ORDERED — after the agent's desk (BL-WORK-38) and the documentation rewrite; its own
thread prepares now ([the handoff](handoffs/night-lab-handoff.md)) (the founder, 2026-10-09)  
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
friend runs, its switch written and parked ([prompt](../prompts/local-lane-2.md)); the other nine,
and L7's room, await his word. The fast-builds research counts a kit-wide build lock beside stage
7d's slot a mistake (its decision 6), which L7's room would need to answer  
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
