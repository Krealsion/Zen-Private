# The UX batch: issue drafts

**Status:** DRAFTS -- filed together after the manuals and the split (the founder, 2026-10-14)  
**Source:** the founder's notes of 2026-10-14 ("Zen: pause and rethink", with his raw notes).
Some of the raw notes are out of date, so every draft is rechecked on `main` when it is filed.  
**Plans:** `backlog.md` section 1b

Each draft becomes one Zengine issue in the form `docs/contributing/taking-an-issue.md` teaches: its
Folders and Checked against are added when it is filed, against the code as the split leaves it;
`enhancement`, or `defect` where the recheck reproduces a fault. A draft that an existing issue
already holds becomes a comment on that issue instead. Nothing here names a private page.

The batch's own rules, from the notes: mouse and keyboard reach the same thing; state is never shown
by colour alone; an offered action is not permission to take it; one coherent component beats two.

## 1. The window's furniture and polish

### UX-01 -- A manual opens in a smaller window over its subject
- Wanted: the manual opens over the pane it describes, not across the desk, with some padding
  around it (16 to 32 pixels to explore).
- Done when: opening a pane's manual shows it over that pane, and the pane's edges stay visible.
- Fences: the manual's words and how they reach the window are unchanged.

### UX-02 -- The key that opens a surface closes it
- Wanted: where it is unambiguous, the key that opened a surface closes it: the manual's key opens
  the manual and the same key closes it.
- Done when: each toggling surface closes on its own key, and its manual says so.
- Fences: a key already bound to something else in that surface keeps its meaning.

### UX-03 -- Clicking outside an arrangement ends it
- Wanted: a click outside the pane being arranged ends arrangement mode.
- Done when: the click ends it, and a gesture held at that moment ends in a said way (dropped or
  cancelled), never left half-held.

### UX-04 -- A hidden pane comes back where it was
- Wanted: a pane hidden and shown again returns to its place and size.
- Done when: a setting, on by default, keeps a hidden pane's placement; off, it opens as today.

### UX-05 -- Menus show their shortcuts, and mouse and keyboard reach the same things
- Done when: every menu row shows the weaver's current key for it, and every action a menu offers
  has a keyboard path, and the reverse.

### UX-06 -- The weaver arranges the whole window
- Wanted: the top and bottom regions are the weaver's to arrange too: the hotkey helper can move,
  stand vertically, or go; no element keeps a forced position, even the ones thought necessary.
- Done when: each piece of the window's furniture can be moved or removed and comes back as left.

### UX-07 -- Notices that come and go, and can be found again
- Wanted: notices as an overlay, a popup, or a brief line in the middle of the screen that fades,
  instead of a fixed bar; one missed can be read again.
- Done when: a notice can be shown each of those ways by setting, and a list of recent notices keeps
  each one with the subject it was about.

## 2. Moving between workspaces (needs the workspace's owner, from the split)

### UX-08 -- An obvious way between workspaces, and back
- Done when: a weaver can see the workspaces, move to one, and return to where they were, by mouse
  and by key.

### UX-09 -- The subject you were on survives the move
- Done when: the subject active before a move is still the active subject after moving back, with
  its context (selection, scroll, draft).

### UX-10 -- Carrying something into another workspace in one motion
- Wanted: material carried to another workspace without dropping it and picking it up again.
- Done when: a carry crosses workspaces and lands; a carry whose target goes away, or that is
  cancelled, ends in a said way.

### UX-11 -- Gestures to navigate, explored
- Wanted: try a middle-button drag to move around, and a secondary button pressed during a primary
  drag to move between spaces.
- Done when: each gesture tried is kept or dropped with its reason, and each kept one has a visible
  alternative.

## 3. The View Builder's components

### UX-12 -- A basic set of components, each behaving as people expect
- Wanted: text box, radio button, dropdown, label, table and icon, each with its expected behaviour:
  focus, keyboard use, editing with commit and cancel, disabled, validation, text that can be
  translated, and inspection by an agent.
- Done when: each component is in the View Builder with that behaviour witnessed.
- Fences: one coherent component beats two; a component that both shows and takes input is fine.

### UX-13 -- A component's events are triggers
- Done when: a maker can wire a component's meaningful event (an edit finished, a radio button
  changed) to an action without code.

### UX-14 -- Notes on an element
- Done when: an element can carry metadata, shown as a tooltip, in its context menu, and opened in
  Info.

### UX-15 -- Open views as tabs, unsaved ones marked
- Done when: open views show as named tabs above the canvas, an unsaved one marked `*` (an orange
  border may add to it, never replace it).

### UX-16 -- Closing a view with unsaved work asks
- Done when: the tab's close control asks save, discard or cancel when the view has unsaved work,
  and closes at once when it has none.

### UX-17 -- A blinking caret in text boxes
- Done when: a text box with the keyboard shows a blinking caret, and whether its setting is
  Workshop's, the view's, or inherited with an override is decided and said.

## 4. Loaded

### UX-18 -- Search what is loaded
- Done when: Loaded filters its rows by a typed search over participants and what they offer.

### UX-19 -- Loaded's context menu: inspect, reload, remove
- Done when: a loaded participant's context menu offers Inspect, Reload and Remove where supported
  and allowed, each saying exactly what it does.
- Fences: removing a running participant never deletes its artifact or its source.

### UX-20 -- From a participant to its source, recipe, owner and messages
- Done when: a loaded participant links to its source, its recipe, its owner and the messages it
  declares, when they are known; unknown stays shown as unknown.

## 5. Compose

### UX-21 -- Composing shows the manual
- Done when: choosing a command in Compose shows its section of the feature's manual.

### UX-22 -- Compose's catalog, organized
- Done when: Compose's catalog can be grouped and filtered by tags.

### UX-23 -- A readable schema beside the command
- Done when: each command shows a readable preview of its schema after its name and version.

## 6. Info

### UX-24 -- Nested schemas, opened and closed
- Done when: each nested level expands and collapses, and one action returns to the top.

### UX-25 -- Edit by name, and a schema's definition on hover
- Done when: a value's context menu offers `Edit <SchemaName>`, and hovering a schema's name shows
  its definition.

### UX-26 -- Follow a value to its owner
- Done when: from a value, Info follows its owner up to the weave: who started it, what it sends and
  what it hears, when known and allowed.

### UX-27 -- Drag and drop messages and values
- Done when: a message or value dragged from Info lands where a drop accepts it.

### UX-28 -- Save, Reload, and the state of what you are editing
- Wanted: Save and Reload, and a visible state: saved to Inventory, the same as the owner's, changed
  here, changed at the owner, owner gone, the owner's schema changed. Several can hold at once.
- Done when: each state shows with its label or icon (the notes' colours may add to them: blue,
  green, yellow, orange, red), and unsaved changes are never lost silently.
- Fences: saving goes through the owner's editing contract, never by writing its state from
  outside (the plans' editing-through-owners item).

## 7. Inventory

### UX-29 -- A game's inventory: a grid of slots
- Done when: Inventory shows rows, columns and single slots with thin borders and compact text, the
  grid growing with the room it has, not with what is stored.

### UX-30 -- Sort and filter by type
- Done when: a row of type icons, or a dropdown, sorts and filters the entries.
- Related: #134 (locked entries keep their place when sorting).

### UX-31 -- An item's full schema, on hover and on Inspect
- Done when: hovering an item shows its full schema in an Info-style tooltip, and Inspect opens it
  in a reserved Info view that leaves any open draft alone.
- Related: #128 to #135, Inventory's parked issues.

## 8. Project, the Editor and the Builder

### UX-32 -- Project scrolls
- Today: reported not scrolling. Recheck first: a `defect` if it reproduces.

### UX-33 -- Project's context menu, and how it meets Loaded
- Done when: Project's rows have context actions, and moving between authored material and the
  participant running from it is one action each way.
- Related: the research on Loaded, Project and Compose as one journey (plans, section 1b).

### UX-34 -- The Editor's context menu
- Done when: the Editor's context menu offers close file, save, undo and redo, each with its key
  shown, and unsaved work is handled on close, on replacement and on navigation.

### UX-35 -- The Builder, made over
- Wanted: the current step and what matters in it clear at a glance; only that step's information
  and controls, diagnostics still one action away; Realize as a button, by mouse and by key.
- Fences: the Builder reuses the shared components and outcomes; no vocabulary of its own.

## 9. Tools and demos

### UX-36 -- The demo runner
- Done when: a weaver can reset to the default opening or to an empty state (what a reset touches,
  and what happens to their work, said), list the demos installed or supplied, edit one, see what
  it needs, and replay it at a chosen speed, each step waiting on its outcome, not a delay.
- Fences: demos reuse the tools; tools and demos live apart.

### UX-37 -- Where time and messages go, shown in Workshop
- Done when: Workshop shows message traffic, expensive operations and waiting for a chosen
  workflow, the measures picked from real workflows.

## 10. Fileable now

### HK-01 -- The quarry leaves Zengine
- Wanted: `quarry/`, the earlier engine kept as reading material, leaves the repository; its
  material is kept elsewhere, and nothing is discarded.
- Done when: the folder and its 18 mentions are gone (the root README, AGENTS.md, LICENSING.md,
  THIRD_PARTY_NOTICES.md, the checks' exclusions and two shape tests among them), and the two fonts
  whose terms are unverified leave with it.
- Fences: history is not rewritten; before the removal, the maintainer's copy is made.
