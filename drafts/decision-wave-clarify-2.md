# Decision wave, first half: your answers, read back (2026-11-02)

Your answers stay in `decision-wave-clarify-1.md` (committed). This file: what they settle, my
answer where you asked or left it to me, and the few calls still open, each with a line for you.

## Settled, and recorded in the backlog

- **The earned rule's last three.** WL-PART-01 stays as it is. Loom's threading line becomes "not
  built; nothing may assume it never will" (a small Loom docs change, for the next issue round).
  `pressure.md` no longer waits on wakes: its rules say so now, and PARKED is retired. Your
  wording for seams is in `zen-orientation.md`: built when the plan reaches them, or when their
  absence would weaken the next work's goals.
- **Colours** as I read them, with names you reach by autocomplete (below).
- **`control` becomes `button`.**
- **Search becomes the list's filter**: filters and a sort, chained in order, chosen by the
  list's type and parameters.
- **Census 5 and 6** as read: the submenu mark a field of the row, the cursor its own mark.
- **Keymap ids scoped by their owner**, with the key-routing change.
- **The old keymap's collision note**: not now.
- **Fold and dock**: two typed fields of a setup's pane row, setup v7 and session v13. And your
  rule beside it: never avoid a version bump; the migration path is worth the exercise.
- **The dock** for its first build: a strip the whole length of its edge, as read.
- **"Sends the message this draft holds"**: yes, one round with 4's form.

## My answers where you asked or left it to me

### Colours by name, as your Config Generator did

The quarry's generator (`quarry/src/zengine/config_code_gen.cpp`) wrote a C++ name for every
entry of the JSON: a typo is a compile error, while the value stays a lookup at run time. The
same for colours, with one turn: the generated thing is a *name*, not a value. A sketch:

```cpp
namespace zengine::graphics::themes::colors {
    inline constexpr ColorName accent{"accent"};   // generated from the pool's names
}
// a draw carries colors::accent; the window turns it into a colour when it paints
```

So autocomplete finds every name, a typo doesn't build, and a theme switch still repaints
without asking any pane. A pane's exposed slots generate the same way under its own namespace
(`flow::colors::wire`); fonts and sizes too.

### Two looks on one property

Your rule: looks with the same trigger on the same property chain, in the order they were added
(white, yellow, orange, red as it heats). For different triggers on one property (hover
brightens, hold reddens), unless you say otherwise: the one that fired last wins while it holds,
and the other resumes after.

### A choice of options: tabs, radio buttons

Interface design calls this a choice: a set of options, and a rule for how many may be chosen.
One element, `choice`:

- `one`: tabs, radio buttons, a segmented bar, a dropdown;
- `many`: a set of checkboxes, toggle buttons.

How it looks is its face: the same choice can be tabs across the top of a pane or radio buttons
in a form, and `tab_strip`'s fitting into a width becomes the tab face's own arithmetic. Name it
`choice` (short, what a weaver would say) or your `option_list`.

Your call:

### Section: a section of what?

Of a pane. A section is a titled block that folds: its header always shows, its body opens and
shuts. It is the accordion's piece. Your accordions are groups of sections (independent, one at
a time, the pair), and a dock folds the same way. So the set is: button, field, list, choice,
section, text area, hint.

### Groups as layers: my call, since you left it to me

- Groups are the layers. A group paints its children in order; hits read the same order,
  topmost first. No z number anywhere.
- A lasting change of order is a move: "put X before (or after) Y" among its siblings. One small
  message; nothing is resent.
- A temporary raise is a flag, not a move: "raise X" paints and hits X above its siblings until
  "lower X". The order itself never changes, so lowering always puts things back exactly, however
  many neighbours were raised and lowered in between. Your edge case cannot happen.
- Never across groups.
- How the window keeps the order (your linked list, or anything that makes a move cheap) is the
  window's own, Ceecee's call when it is built.

### Every press reachable (4): the ideal

Today a pane declares its actions by hand, a row each (id, label, default key, what a press may
send), in `PaneActions` (`workshop/pane_vocabulary.hpp`). A presenter's button that runs its own
code is not in that list, so the keymap, the manuals, the press witness and agents cannot see it.

The ideal:

- **Every pressable thing is an action, with one way in.** A click, a key, a jump hint and an
  agent all press the same action. Hotkeys are not a second system: a hotkey is the keymap
  binding a key to an action's id.
- **A button is its own declaration.** A pane builds its buttons, and Workshop reads the actions
  off them; no list to keep by hand.
- **What a press does is part of the button**: send a message (your one-line lambda: the shape
  comes from what it returns, so the declaration writes itself), send the message a draft holds
  (5), or run the pane's own code. Nothing pressable goes undeclared.
- **Inventory then needs nothing special.** A command tile is a button whose press sends the
  message it holds; its hotkey is a keymap binding to the tile's action; a view's hotkeys on or
  off is the keymap's scope.

Inventory's page describes a press on a tile as selecting it, and a command as running by its
hotkey. Lean: a press on a command tile runs it, as any button does; the right press keeps its
menu, and dragging still moves it.

Your call:

### Jump hints and keyboard modes (6)

Your answer stops mid-sentence ("...the simple letter button that corresponds with that item's
hint,"). How Vimium does it, as a start: one key shows hints that press, another hints that only
move the keys there, another hints that open a thing's menu. Lean: the same hints with a mode
each, press and focus first.

Your call (and the rest of the sentence):

### Escape paths (1)

Your answer stops at "taking over the whole screen, input and". My reading so far: a pane that
needs one escape may take it (a terminal wants Ctrl+Q), but never all of them; whatever a pane
takes, one way out stays Workshop's (a chord, the mouse, the palette). Right?

Your call (and the rest of the sentence):

### The `parked` label

On GitHub, `parked` reads "Deferred until its stated wake condition", the machinery you just
retired. Lean: its issues take `later`, and `parked` goes (Ceecee, next round).

Your call:

### Workshop in its own repository: my read

- **It's the right end state.** Zengine becomes the packages any host can load (the panes, the
  element set, graphics, input, the operators), and Workshop one host made from them, as Zengine
  is one consumer of Loom.
- **What it buys:**
  - host code can't hide among the packages: "write Loom, not host code" becomes a boundary the
    build enforces;
  - a stranger who wants the packages doesn't wade through the app;
  - each repository releases on its own clock;
  - the creations exception, once drafted, can sit on the packages people build with, while
    Workshop stays plain AGPL.
- **What it costs:** a change across the seam becomes two pull requests in order, CI and the
  issue lane run in two places, and versions must line up.
- **How, without a big bang:** prove the boundary inside one repository first, as Zengine proved
  Loom's. Workshop builds only against an installed Zengine, and a CI lane says so. When that
  lane is green, moving the folder is mechanical.
- **When:** after the visual foundation's first stages, which reshape both sides. Before then, a
  short research round could measure the distance: every place Workshop reaches into a package's
  insides. Want it queued?

Your call:
