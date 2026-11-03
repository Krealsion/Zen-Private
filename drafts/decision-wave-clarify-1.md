# Decision wave, first half: what you asked, answered (2026-10-31)

Your answers are kept beside this, verbatim: `decision-wave-graphical-answers.txt`. Everything
you settled is in the backlog (section 3, "The visual foundation", and section 5). Below: only
what you asked about, each ending in a line for your call.

## 0. The earned rule

Gone from Zen's own documents (committed):

- `zen-orientation.md`, section 5: "Build from consumers" is now "Build for the future Zen is
  taking"; "Appreciate seams without building them" is now "Name the seams" (built when the plan
  reaches them, not when their absence hurts); section 4's "a real consumer pulls" now reads "the     ### "not when their absence hurts" -> "or when their absence would weaken the next works goals" better clarity I think
  design calls for"; a weaver's identity is "still to be designed", no longer "earned by pressure".
- `executor-constitution.md`, section a: "Do not build speculative frameworks..." now reads:
  build for the future the direction sets, whole and with care; what no plan or direction names
  is still a guess; the vision never waives a required check.
- `giant-shoulders.md`: Knuth's note says "measure before optimizing".
- The backlog: the drawing door and the WASM tier's S5 no longer wait "as consumers ask".

Gone from the repositories once a prompt runs (path in chat): Zengine's record "A component is
earned" and the laws citing it, the "grounded in real consumers, not speculative abstractions"
line in both AGENTS.md, a record declining "a widget framework" because "two consumers earned
one packer", and "not earned yet" in the best-practices page.

Three I left alone, because each may not be the rule you mean:

1. **WL-PART-01, "a participant earns its place."** It decides when a piece is its own weave
   rather than part of another: two partners or more, a replacement actually used, an authority
   it enforces, or state the weaver changes. It's about how finely to split, not about waiting:
   it folded the snake's controls and clock into the world (3.27 messages a tick became 2.14).
   Keep it as it is? Your call: Agreed
2. **Loom: "multi-threaded dispatch is an explicit non-feature until a consumer forces it."**
   That's the waiting rule's wording on a real choice, the single-threaded bus. Your principles
   also say no design should rule out threading later. Reword to "not built; nothing may assume
   it never will", or keep? Your call: Agreed
3. **`private/pressure.md`.** Every seam there carries a "wake" condition: the waiting rule's
   machinery. Proposal: keep the file as the list of seams and what each enables, drop "wake"
   as a gate, and let the direction order them. Your call: Agreed

Leans on the sheet's second half that the direction changes, so you don't answer the old ones:

- zenscript-research:10: design the list and text operators as one set, not one at a time.
- sweep:111: build Loom's customization point and retire Zengine's value-door macro now.
- graphics-weave-research-2:10: file the seams and plan them into the visual foundation.
- wamr-probe-research:D1-room: close it; one runtime.

## 1. Colours: my reading of your design

Confirm or correct:

- The painter knows no colours: every draw carries its colour.
- A pane colours a thing with an exact value, a name from the shared pool (named by use:
  background, text, accent...), or a slot of its own that it exposes to themes. A colour it
  doesn't expose is its own and no theme touches it.
- A theme is a JSON file loaded at run time. It sets pool names and exposed slots, whether or
  not an older theme knew them. A theme naming a slot nothing exposes follows its own setting:
  skip it and say so, or refuse the whole theme. Every entry is resolved before anything applies.
- The same pool holds fonts and text sizes.
- My lean on one detail: a name becomes a colour in the window, at paint time, so switching
  theme repaints without asking any pane. The other way, each pane resolving its own, makes a
  theme switch a message to every pane. The theme itself can be a Loom sense (a latest claim
  anyone may read), as you floated.
- One theme file for colours, fonts and settings (stage 4's themes), all under the merge rules
  you set in settings 2 to 5?

Your call: This sounds correct. I only would like helper functions generated (like I have done in the past) to get around with requiring element names to be referenced by string though. As is, if you add a `BLUE` color, I feel like our only current path is something like `zengine::graphics::themes::colors::get_color("BLUE")`. I'd like to avoid that and have something more like `zengine::graphics::themes::colors::BLUE`, so that an IDE auto-complete can resolve names, rather than needing the JSON file open to find the names. The Config Generator in the quarry is the shape of what I want.

## 2. Window looks and the element set

**Element set text 1, one detail.** Recorded: several looks at once on one node, each on its
own property; an operator takes a value struct (the colour a fade ends at) besides the
element's own values. Open: two looks on the *same* property at once (hover brightens, hold
reddens). Lean: the later trigger wins while it holds, and the other resumes after. Or leave it
to the stage. Your call: I'd say those seem to be conflicting at first, where both change color, but perhaps that is actually useful. We can have them form chains if they are the same trigger and effect, like a button that goes from white to yellow, to orange, to red for a heating up effect. So they would happen in order of being added.

**UI census 1, what the three are:**

- **control** is the button: a label, whether it's available now, and its action id.
  ("control" because it's the value, drawn however the medium likes; `graphics::Button` was the
  old drawn class.) Rename it `button`? Yes. Button is a more discoverable and intuitive name
- **search** isn't a new widget: it's a text box wired to a list's filter, plus the "N more
  match" count. Four panes each wrote their own (Flow, Powers, Loaded, the palette).
  Proposal: make it the list's filter, not an element. I like the design as I understand it. A list allows filter operators based on its type and parameters. This bring up things like sorting as well. Thinking similar to the animation chaining, we could even let filter chain to filter multiple things, and sort, however they choose. 
- **tabs** are buttons where exactly one is chosen, fitted into a width with an overflow.
  Proposal: a strip of controls in "one of" mode; `tab_strip` is that fitting arithmetic. Understood, this makes sense, and is worthwhile, but we can probably expand the scope somehow. Things like a set of three radio buttons where only one can be selected would be a use case, but `tab_strip` doesn't really fit that naming. Something like `option_list` makes more sense where each element has a selected and unselected state or function, but not 100% would love UI design input.

That leaves the set as: control, field (the checkbox is a Bool field), list (with its filter,
cursor, markers and columns), section, text area, hint. Your call: The notes above describe those elements. I will say, I kind of glossed over Section? A section of what?

**UI census 5.** You read it right. The window shows `?` today only because its face holds
ASCII glyphs (`graphics/light_paint.hpp:476`). With your yes on Flow made over 4, the window
draws every character; `?` stays only where a terminal can't show one. What's left of census 5
is one spelling for each mark: the list cursor, the "N more" marker, the active tab. Nothing
more to answer.

**UI census 6.** Mostly right. Today a row's key and its submenu mark live inside the label: a
tab character before the key and " >" after the label (`workshop/pane_menu.hpp`, `Offer::row`
and `Offer::submenu`), split back out by `menu_row_words`. A label with its own tab or " >"
breaks it: your injection case. Fields fix that, and each presenter draws them its own way.
One correction: that arrow doesn't point at the row; it says "this row opens another menu".
The pointer at the chosen row is the list cursor (census 5). So the submenu mark becomes a field
(drawn as an arrow at the row's end for now), and the cursor stays its own mark. Your call: Agreed.

**Graphics research round 2, decision 2: how groups as layers lands.**

- Today a pane's drawing is a tree of named nodes. Paint order is tree order: a group paints its
  children in order, a new node goes after its siblings, and a node put again keeps its place.
  Hits read the same order, topmost first.
- So a pane makes layers with groups, put in order: `board/`, `pieces/`, `overlay/`.
- The weak spot is raising one card above its siblings. Putting it again keeps its place, so
  today you remove it and put it again, resending its whole subtree.
- Done poorly: a global z number on any node (a child paints above things outside its group,
  escapes its group's clip, and hits stop matching paint); or re-sorting every frame.
- Done well, either:
  - (a) a move: a drawing can say "put X before or after Y" among its siblings. Nothing is
    resent, and the tree stays the one order; or
  - (b) a layer number scoped to siblings: siblings sort by layer, then by when they were put;
    putting a node again with a new layer raises it, subtree and all. Never across groups.
- Lean: groups as layers, plus (a). One order, stated by the tree; raising is one small message.

Your call: I may not have followed that perfectly, so let me try to put it together. Groups are essentially layout trees, and a node can be updated in place easily. Changing it's visible "Z-level" however, due to it being based purely on order in the group, cannot be easily represented as a change of value as if there *were* a layer system. It's not ideal to put the Z-Level into every component, as that is just more data, and more complications for the window to resolve. Sorting it before-hand in which case it's just extra data to order it like they were packets, and sorting it every frame out of place to draw is exceptionally worse. My preference if I were programming it would be to do what you are saying with (a), except with a Linked List, as then we would not run into reordering problems like with a std::vector, especially if the groups are large or numerous. The moving then becomes easy, but we are still missing good helpers for moving and resetting it in the case of an element only being brought forward temporarily, and not clashing in edge cases where you are continuously repositioning elements that are next to eachother and ensuring the order at the end after every move is undone is the same as at the start. Given all of this info, I will defer to what you think would be best given the goals and code.

## 3. The window, keys and presses

**1, your key model, my reading.** A pane hears a key first; what it doesn't consume goes up to
Workshop; a pane can opt out of Workshop's defaults. One fence I'd add: one or two chords always
go to Workshop first (leave pane, the palette), so no pane, an untrusted one least of all, can
trap you. Today's `supersedes` (a pane's row standing in for one of Workshop's while the pane
has the keys) is the start of this. Your call: I think you're right that we need protections, but there are always legitimate use cases for overriding a single escape path. The only real way to trap someone is by taking over the whole screen, input and 

**4.** It's the first meaning. "Reachable by a key" means the keymap *may* bind a key to it if a
weaver wants one; nothing forces a hotkey. Why only buttons that send a message: each action
declares what its press may send (`ActionCause{shape, version, subject}`), and the keymap, the
manuals and the press witness all read that declaration. A presenter's button that runs its own
code sends no message, so it has nothing to declare, and all three can't see it; neither can an
agent asking by id. The fix is a cause form that says "this press runs the pane's own code".
Your agent tool (ask for an action, let the tool work out a press or a key) is agents acting by
intent (BL-WORK-25), and it needs every action declared, which this gives. Your call: Agreed, we should be able to reach those buttons. The question is how. Will it be a feature panes need to declare manually, or can we make this a feature of all pressable thing that happens automatically? Will these be unified in hotkeys, or separate? How will Inventory "buttons" work, as they have hotkeys (and does clicking those slots trigger a press currently)? Looking for what the ideal is here.

**5.** Each button declares the message its press may send, so a manual can say "Send sends a
ComposeX" and the press witness can check it. Compose's Send and Inventory's command rows send
whatever message you built, so they can't name one shape and declare nothing. The question:
should there be a form meaning "sends the message this draft holds"? Lean: yes, in one round
with 4's form. Your call: Yes, that makes perfect sense to me. This is exactly what we would want for inventory slots. This may also be a pathway for us to add a sort of "callback lambda" form of setting the type (sends a message), and the message itself, defined and filled out in one line. That is mostly a coding preference of mine though, so don't let it weaken the overall idea if it has that risk.

**6.** Jump hints: press a key, every pressable thing shows a short label (as Vimium does), and
you type a label to act. Switch scanning: an accessibility mode where a highlight steps through
things on its own and one switch picks. The question: when either lands on something, does it
press it, press and activate it, or only move the keys there? Lean (the research's): a named
control runs its action; anything else is a press that only focuses a pane that wasn't active;
a whole pane gets focus. Your call: This seems like a really good direction for keyboard only users. Definitely want to suppor them, especially as a vim user myself. I think we should check the scope of this section against that desired goal. For instance, we should be able to click on buttons, which I think is the "named control" you said, but I almost think we should have multiple modes for the keyboard input to be able to represent different desired actions. For instance, clicking a button in a pane you have selected could be as easy as toggling on the hints, and clicking the simple letter button that corsponds with that items hint, 

**7.** Your answer reads as the rule for a pane's own key: from outside, it opens or selects the
pane; inside, the same key closes it (#492's rule, yes). The question itself was smaller: when an
old keymap file bound Ctrl+Q to something else, it now gets a collision at load. Should that
message also say "Ctrl+Q is leave pane now"? Lean unchanged: yes, one line. Your call: Oh, unnecessary at the moment, but good instinct for future update backwards-compatibility.

**8.** How it plays out: today the keymap file names actions by bare ids, one namespace shared
by Workshop and every pane, so Flow's `run` and an old retired Workshop `run` are the same
string. Under your 1 and 7, where a pane owns its keys, a row names its owner (Flow's `run`, or
Workshop's), so a retired Workshop id can't land on a pane's. Lean: scope keymap ids by owner,
as part of the key-routing change; then no special list and no renaming Flow's ids. Your call: Agreed.

## 4. Layout and docks

**2, the specifics.** A setup keeps one row a pane: `SetupPane{ref, place, width, height, front,
settings}` (`workshop/setup.hpp`). Where the pane is (place, size, in front) is typed fields;
`settings` is a list of key and value pairs, where Workshop keeps one word of its own,
`workshop.skin`. The question: fold (open, shut, hidden) and dock (an edge), as two more typed
fields beside place (a new setup file version, 7, and session version, 13), or as two words in
`settings` (no version; an older build refuses them by name)? The research chose words to avoid
a version. Under the new direction my lean flips to typed fields: they say where the pane is,
like place and front, and aren't settings of the pane. Your call: Yes, two new fields. We should never avoid version bumps. I encourage them, in fact, especially as we have a useful migration pattern that can always use extra stress testing.

**3, my reading of your dock.** A dock reserves a strip the whole length of its edge, always:
the room is narrower by the strip whether the dock is open or shut, like a scrollbar's gutter.
An arrow sits centred on the strip, pointing in when shut and out when open. The docked pane
opens over the room and covers what's there. So the bar's length is the whole edge, with no
setting. Your call: For an intitial implementation, yes this is my thought. As for what the future holds, I do see possible future settings, but they would be built on some of the other, more foundational features, like the animations and maybe later future components that can nest them in interesting ways.

## 5. Settings and themes

**1.** Agreed: the double-click speed is input's setting, not Workshop's. On moving Workshop to
its own repository, with Zengine kept as an inert set of default packages: want my read? Your
call: Sure, I would love your read.
