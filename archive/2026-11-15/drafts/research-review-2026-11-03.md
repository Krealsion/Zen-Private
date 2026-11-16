# Research review: the visual foundation, and Workshop as a stranger (2026-11-03)

Vision's review of the two research rounds, with the left-behind round beside them. Answer inline
after each "Your call:", as in the clarify files; a bare "yes" takes the lean.

- The visual foundation: [report](../../reportbacks/visual-foundation-research-RB.md),
  [design](../../reportbacks/visual-foundation-research/design.md),
  [stages](../../reportbacks/visual-foundation-research/stages.md).
- Workshop as a stranger: [report](../../reportbacks/workshop-as-a-stranger-research-RB.md),
  [distance](../../reportbacks/workshop-as-a-stranger-research/distance.md).

## 0. The short of it

- **Left behind: clean.** 1,036 leftovers removed, each named; GCC 16 and the lane-tests homed;
  `parked` and `later` deleted (32 issues lost one); the primary on `main`. What the kit listed
  at its end was the two researches' own, and each cleared its own.
- **Both researches: identity clean, fences held.** Every commit Krealsion with no trailers, each
  prompt moved alone, nothing built or pushed, Zengine and Loom the same at start and end
  (`84446fb5`, `98ea61c`). Every claim I checked in source held (section 4).
- **The visual foundation is sound as a whole.** Five calls. I add a sixth (keys), and fences
  for four of its stages.
- **Workshop as a stranger is well measured.** Seven calls. My main change is the order: the move
  after V7, not V5.
- **Thirteen calls in all**: V-1 to V-6, then W-1 to W-7. The six V calls settled in chat the
  same day (section 2.4, and the backlog's section 3); W-1 to W-7 stay open.

## 1. New words

- **Pool**: the shared names, by use, a pane colours and sizes by (`background`, `text`,
  `accent`; sizes `body`, `heading`).
- **Slot**: a name a pane exposes for themes to set, with its default (`flow::colors::wire`).
- **Palette**: a theme resolved for the window (its colours, fonts, sizes and each office's
  slots) at a revision. A theme switch is a new revision.
- **Theme reader**: the `zengine-settings` weave, the one place a theme file is read.
- **Face**: stateless drawing code for an element's value (`button_face` over a `Button`).
- **Look**: a record beside a drawn node: when it plays (hovered, held...), what it changes
  (colour, scale...), and how (duration, curve).
- **Steady**: the window showing every look at its end while someone holds it so (a picture, a
  case, the act tool's run).
- **Widening**: reading an old version of a shape as the new one, so older senders still work.
- **The skin seam**: today's library door through which a window loads a painter with its colour
  table (classic, block, day, night).
- **Reach**: a place one side's build uses the other's insides. Forward is Workshop into
  Zengine; reverse is Zengine's panes into Workshop.
- **The contract**: the 23 headers Zengine's panes include from Workshop, which any host would
  offer its panes.
- **Closing**: one change that removes a reach.
- **Stranger lane**: a CI arm that builds Workshop from an installed Zengine alone.
- **Text check**: a script of seconds: no file outside Workshop's folders includes a Workshop
  header the package does not install, and no target outside them links one of Workshop's.

## 2. The visual foundation

### 2.1 The architecture as a whole

One frame, end to end:

1. **A pane draws** faces over values. Every colour it names is an exact value, a pool name or a
   slot; the names are C++ names generated from JSON, so a typo does not compile.
2. **The window keeps the drawing** and turns each name into a colour when it paints, from the
   palette its area wears. The painter is handed exact colours and knows none.
3. **A theme is JSON** the theme reader reads at run time, judges by your rules (merge or reset,
   locks last, skip or refuse as the theme says, a wrong type always refused) and offers as a
   palette. Every window repaints; no pane is asked.
4. **Looks play in the window** on its 10 ms beat, with no message: several at once, chained by
   trigger as you ruled. Groups are layers: a move between siblings, a raise until lowered.
5. **Every character is drawn**: the text core counts 0, 1 or 2 columns a character; the window
   sets bold and named sizes; a terminal shows what its encoding carries, `?` past it.
6. **One way in**: every pressable thing is a button that declares itself (id, label, default
   key, what its press does), and one shape, `ActionAsked`, says how it was asked: a press with
   its place and clicks, a key, a hint, an agent. A key goes to the pane holding the keys first.
7. **Folds and docks** are typed fields of a setup's row (setup 7, session 13).

A pane's drawing and one of its buttons (design section 4):

```cpp
sk.fill_rect("card", b.x, b.y, b.w, b.h, colors::surface);       // a pool name, by use
sk.line("card/wire", b.x, b.bottom(), to.x, to.y, mine::wire);    // Flow's own slot
// sk.fill_rect("x", 0, 0, 1, 1, colors::acent);                  // does not compile
sk.look("bar", "widen", look::hovered().scale(1500, 1000, anchor::kRight).over(120).back());

inline const ws::Button open{"files.open", "Open", ws::key::kReturn,
    press::sends([](const Files& f) { return OpenSourceRequested{f.chosen_path()}; })};
```

A theme, `<config>/themes/night.json` (`cells` is what a terminal shows where it cannot show the
colour):

```json
{ "format": "zengine-theme", "format_version": 2, "name": "night", "on_failure": "skip",
  "colors": [ { "name": "accent", "color": "#ebcb8b", "cells": "yellow" } ],
  "slots": [ { "office": "zengine.flow",
               "colors": [ { "name": "wire", "color": "#88c0d0", "cells": "cyan" } ] } ] }
```

The eleven stages, all in Zengine, Loom in none:

- **V1** the pool and palettes; a painter with no colours; the four skins become four themes,
  every terminal golden and window picture the same byte for byte.
- **V2** every drawer by name, the roles gone: a mass edit of 82 files by sheet and applier.
- **V3** every character, bold and sizes; columns by character.
- **V4** themes read at run time: settings stage 4 with the colours in it.
- **V5** looks and layers; steady.
- **V6** presses, one way in: buttons that declare themselves.
- **V7** keys, the pane first; keymap ids by owner; the way out.
- **V8** folds and docks on the desk.
- **V9 to V11** the element set: button, field, hint and the menu row; the list with its
  filters and sort; collapsible and tabs, the old classes and the window-run element retired.

Order: V1; then V2, V4 and V8 beside each other; V3, V5 and V6 after V2; V7 after V6; V9 after
V3, V5 and V6; V10 and V11 after V9.

### 2.2 Mistakes to avoid

What I found that the design does not yet guard against:

1. **A key answered late lands in the wrong pane.** In the design a pane is handed each key and
   says by message the ones it did not spend (`KeyUnspent`); Workshop acts after. Messages take
   time: press a Workshop key that moves the keys to another pane, then `a`, and `a` reaches the
   old pane before Workshop has moved them.
   The house met exactly this with Escape (`agents/decisions/escape-is-back.md`: "Matching
   current state does not identify the event being answered") and fixed it: each answer echoes
   its key's correlation, honoured only while that key is the latest gesture (WL-ARR-15). The
   design retires `PaneEscapeUnspent` for `KeyUnspent` and carries neither rule, and with
   Workshop no longer seeing the key first, it has nothing to judge "latest" by. Call V-6.
2. **A theme refused after it was applied.** Under V-3's lean a waiting slot entry is judged when
   its pane declares, perhaps an hour later, and a theme that says `refuse` cannot be refused
   then without undoing it. Fence: `refuse` is judged when the theme is applied; a miss found
   at a later declaration is skipped and said, whatever the theme says.
3. **A look that widens what it cannot hit.** "A look never moves a hit" is right, but a bar
   widened from 8 px to 12 px on hover still takes presses only on its 8. Fence for V5: the
   drawer gives the hit its largest extent and the look paints within it. A node playing its
   `leaving` look takes no press, and its path is free at once.
4. **Pictures that change with the machine's fonts.** Platform fonts differ by machine. Fences
   for V3: cases and pictures draw with the embedded faces only; a fallback glyph sits in its
   cells, never placed by its own advance (the grid wins, or a line drifts); the platform is
   asked per missing character and the answer kept, never a font folder scanned at start.
5. **A CMake floor no lane runs.** Zengine promises 3.16, and nothing runs 3.16: every hosted
   job uses the runner's CMake (`ci.yml` only prints `cmake --version`), the WSL lane 3.22.1.
   Whatever V-5 picks, one lane should run it.

### 2.3 Room for divergence

Not leans; places the design can bend later without undoing anything:

- **The way-out chord as a prefix.** The chord could later hand the next key to Workshop
  (`ctrl+q`, then any Workshop key), so a keyboard weaver in Neovim reaches the whole keymap in
  two keys. V-2's chord is the first half of it.
- **V2 need not gate V3, V5 and V6.** A mass edit by applier re-runs on any base (Zengine's rule
  o), so those three could start right after V1, with V2 regenerated onto what has merged: one
  L stage off the longest path, more rebasing for V2. I'd keep the research's order unless the
  lanes run short of work.
- **The painter one library inside the window**, behind one interface: if a GPU painter ever
  comes, the seam returns as packaging, not as a redesign (with V-1).

Small things for the stage prompts, no call needed:

- An id scoped by its owner need not repeat it: `zengine.files/open`, not `files.open` under
  `zengine.files` (the samples mix the two).
- One spelling for what a weaver types: `colors` in theme files and generated names, as you
  spelled it, and the reader refuses an unknown key by name, so `colours` is an error, not a
  silence.
- The pool's ground named `window` reads oddly beside the window ("the window paints window");
  `ground` reads clearer. Your veto.
- The design's pages cite the CMake floor as "call 6"; it is call 5, V-5 here.

### 2.4 The calls

**V-1. The skin seam.** Today a window paints through a skin: a small library holding a painter
and a colour table (classic, block, day, night). With the colours out of the painter, a skin has
nothing left to choose.

- **Retire it** (the research's lean): the window paints with its own painter, and another way
  of painting is another window weave, already replaceable. One ABI less to keep, and one
  crossing less a change (6.5 us when measured).
- **Keep it, colour-free**, so a stranger can ship a painter (rounded corners, a GPU path)
  without writing a whole window.

Lean: retire, the painter kept one library behind one interface inside the window (2.3).

Your call: (in chat, 2026-11-03) Agreed.

**V-2. The way out with no pointer.** You decided the way out is a press on the setups bar, and
your assumption holds: the window gives a press only to the area under it (`agents/graphics.md`,
"Each owner hears the pointer in its own area"). But a terminal that ignores the ask for mouse
reports, and a weaver on the keyboard alone, have no press to make: a pane taking every key
traps them.

- **One chord stays Workshop's** (the research's lean): `ctrl+q` by default, movable by the
  weaver, so Neovim or the Terminal can have `ctrl+q` once the way out moves. The setups bar
  stays the second way.
- **The press alone**, as decided: a keyboard-only weaver can be trapped.
- **A fixed chord** no one can move: no pane can ever have it.

Lean: one chord, movable. It is the keyboard-only support you asked for, and "one escape path is
all we need" still holds for each hand: one for the mouse, one for the keys.

Your call: (in chat, 2026-11-03) One chord, Ctrl+Q by default, and the weaver can find where it
moved: the band shows it while a pane holds the keys, a notice once if the legend is hidden.

**V-3. A theme's slots for a pane not loaded yet.** A pane says which slots it exposes only while
it runs, so a theme applied before Flow loads finds Flow's slots exposed by nothing.

- **Wait for a named office** (the research's lean): an office the load plan names keeps its
  entries waiting until it declares; "nothing exposes" is an office no plan names, or a slot its
  declaration lacks.
- **Judge only what is loaded**, as written: a theme applied early loses or refuses Flow's
  colours.
- **Every slot entry waits** until something declares it: a misspelt office is never caught.

Lean: wait for a named office, with 2.2's fence: `refuse` is judged when the theme is applied,
and a miss found at a later declaration is skipped and said.

Your call: (in chat, 2026-11-03) As leaned.

**V-4. Faces.** Every pane lays text out by characters of one width, so a proportional face would
put every line in the wrong place. And JetBrains Mono, today's one face, holds Latin, Greek and
Cyrillic, not the scripts past them.

- **The pool's fonts**: monospaced only (the research's lean), a proportional one waiting for a
  door that measures a run of text for its owner; or any face now, that door built first.
- **What JetBrains Mono lacks**: the platform's own fonts, with a small embedded face as the last
  resort (the research's lean); or one wide-coverage face embedded, tens of MB; or a box where no
  face has the character.

Lean: both of the research's, with 2.2's fences, and a last resort that draws the character
itself (a bitmap face such as GNU Unifont), not a sign for its script.

Your call: (in chat, 2026-11-03) As leaned, monospaced first, and proportional text supported in
this arc: a stage of its own after V3 and before V9.

**V-5. Zengine's CMake floor.** The generated names come from a CMake script installed with the
package, so a stranger's pane generates its slots as Zengine's do. CMake reads JSON from 3.19;
Zengine promises 3.16.

- **Raise the floor to 3.19** (the research's lean).
- **3.19 only where names are generated**, refused by name below it.
- **A small C++ generator** instead, built before everything else (a cross build builds it for
  its host too).

Lean: raise it, to 3.22 rather than 3.19: Ubuntu 22.04's, and what our WSL lane runs, so the
promise is one a lane keeps (2.2).

Your call: (in chat, 2026-11-03) CMake as the generator, the reason sound; the floor at 3.22.

**V-6. Keys answered late** (mine, from 2.2). A key that moves the keys elsewhere is answered by
message, and a key typed right after it can reach the old place first. The race holds whichever
way keys are routed, so the mechanism alone does not close it.

Your call: (in chat, 2026-11-03) Inputs, batched ones too, are resolved one at a time, each
against the state the last one left. Vision's addition, taken: the way-out chord never waits in
that line. How keys are routed is Ceecee's.

## 3. Workshop as a stranger

### 3.1 The architecture as a whole

- **Workshop is no stranger yet, and the larger distance runs the other way.** Workshop reaches
  past the installed package in 39 include lines, 12 link edges and 84 more CMake lines.
  Zengine's own panes include Workshop's uninstalled headers in 111 lines from 15 folders (I
  recounted: 111), and 14 of their targets link Workshop's private vocabulary.
- **The seam is Zengine's.** What the panes include is the contract any host offers its panes:
  13 seam vocabularies, the pane machinery, three utilities, the key spelling and the load plan.
  Installed by Zengine, these 23 headers take the reverse count from 111 to 8.
- **The line.** Workshop takes `workshop/` less the contract, the Builder, `external-host/` and
  the launcher, about 52,000 lines. Zengine keeps every library, every other pane, the menu
  presenter and the app host, and gains the contract. After the closings, 5 forward and 4
  reverse include lines remain, each with its closing.
- **23 closings**: 6 small, 14 medium, 3 large. None changes a shape; 8 change a law's text, 7 of
  them the packaging law's "deliberately out".
- **What no line shrinks**: tests (16 programs straddle), law (121 proofs cite package files) and
  documents (566 links cross). Mechanical, and most of the move's work.
- **The proof is a pair**: the stranger lane sees the forward reaches, the text check the
  reverse ones.

The end state, each arrow "depends on", nothing pointing back:

```text
Workshop (the host, the Builder, the launcher, the external host)
   |
   v
Zengine (the libraries, every other pane, the menu presenter, the app host, the contract)
   |
   v
Loom
```

### 3.2 Mistakes to avoid

1. **Moving after V5 splits V6 and V7 across two repositories.** They reshape the seam itself:
   `ActionAsked`, `PaneActions` 5, `KeyUnspent`, `PaneKey` and `PaneEscapeUnspent` retired, the
   keymap 3. Done in one repository, each lands whole, not as two changes kept in step.
2. **The same move made twice.** V4 moves the theme reader off Workshop's headers
   (`settings/theme_persist.hpp:11-14`: the gesture spelling, the safe write, `Written`, a
   setting's kinds), and closings 13 and 14 move the same pieces (the safe write and `Written`
   to the contract's side, the key spelling to `input/`). V7's key matching belongs beside that
   spelling. Each moves once.
3. **A boundary held only at the end.** The in-tree include root lets any target include any
   header, so every stage before the move can add a reverse reach unseen. The text check from
   now, not at the move.
4. **A law's reason gone stale.** The packaging law keeps the Flow host's runtime out as
   "Workshop session policy", but Zengine's own app host mounts it too (`app/host.hpp:400`).

### 3.3 Room for divergence

- **A sibling Zengine tree** inside Workshop's build, as `ZEN_LOOM_DEV` gives Zengine Loom's, can
  sit beside W-4's named trees later, as a convenience for working on both at once.
- **Zengine's examples installed** (W-5's other side) would prove in a real host the examples a
  stranger copies; the cost is examples in the package.

### 3.4 The calls

**W-1. The seam is Zengine's.** The contract's 23 headers and the three asks' words
(`builder/vocabulary.hpp`, `builder/recipe.hpp`, `launcher/vocabulary.hpp`) join the pane
protocol in Zengine's package, reversing the packaging law's "Workshop being Workshop"
(`agents/packaging.md:104-107`). The other way, the panes going with Workshop, leaves Zengine
without its panes.

Lean (the research's, and mine): yes. It is how Zengine stands to Loom: the words in the lower
package, each side's code with its owner.

Your call:

**W-2. The open sides.** With Workshop: the Builder (its own page: "The Builder is part of
Workshop"), `external-host/` ("Workshop from another host") and the launcher (it starts
Workshop's demos). With Zengine: the app host (an app with no Workshop) and the menu presenter
(already built from installed headers alone).

Lean: as the research draws them.

Your call:

**W-3. The Flow host's runtime** (`flow/flow-host/runtime.hpp`): exported whole, or its Workshop
policy moved to Workshop and the rest exported. The research gives no lean.

Lean: exported whole. Both hosts mount it (`workshop/workshop.cpp:1233`, `app/host.hpp:400`), so
its policy is the Flow host's, not Workshop's; the law's reason is corrected with the export. A
split waits for a second policy.

Your call:

**W-4. Workshop editing itself across two repositories.** WL-CODE-06 and WL-CODE-07 bind the
development catalog and its runtime to one tree.

- **Named trees** (the research's lean): Zengine's configure writes its own tree's catalog, the
  weaver names that tree to Workshop, and the runtime binds two trees.
- **A sibling Zengine tree** built inside Workshop's, as `ZEN_LOOM_DEV` does for Loom: one
  configure, the law nearly unchanged.

Lean: named trees. A maker editing their own pane in their own repository needs exactly this, so
it serves the first maker story too; the sibling tree can come later (3.3).

Your call:

**W-5. The pane examples Workshop's suites load** (`tally-pane`, `guard-pane`,
`numbered-presenter`): Workshop's own fixtures, or Zengine's examples installed for it to load.

Lean: fixtures. A suite owns what it loads, the package carries no examples, and Zengine's
examples stay free to change as teaching.

Your call:

**W-6. The stranger lane's pair**: Zengine built without Workshop's folders, or the text check.

Lean: both, the text check first (seconds, in the documentation lane), as the research says;
and the text check lands now, with the first closings, so every visual stage is held to the
line (3.2).

Your call:

**W-7. The order.** The research's: closings 1 to 5, 7 to 12 and 16 now; 13 and 14 after the
visual design; 18 to 20 after 13; 6 and 15 on their calls; 17 and 21 to 23 at the move, which
comes after V1 to V5.

Lean: the research's, with three changes:

- the move after V7, not V5 (3.2, first);
- each shared piece moved once: V4 moves the theme reader's (part of closing 13, all of 14), and
  V7's key matching sits beside them in `input/` (3.2, second);
- the text check with the first closings (W-6).

Your call:

## 4. What I checked

- **Identity**: every commit of both rounds Krealsion as author and committer, with no trailer
  or AI mention (Zen `892fd3e2`, `878a9b33`, `36e2b02f`, `047ffe91`, `81ed4d7e`; private
  `770ebe3`).
- **Fences**: research only; nothing built or pushed; each read its own clone at `origin/main`,
  the same at start and end; your checkouts untouched.
- **The visual foundation's, in source at `84446fb5`**: the eight roles and `Paint{role, rgb}`;
  the Looks in the light painter and its role lookup; the skin seam's export macros; the 10 ms
  beat; one column a byte (`component/text.hpp`); `kDoubleClickMs` at 400; `focus.leave` on
  `^q`, global; the floor at 3.16 and the launcher's 3.19 guard; no weave holding the settings
  office; one face at 13 points, glyphs `!` to `~` only; the law keeping injected keys out; the
  law's "docking absent and refused".
- **Workshop's, the same**: the 111 reverse include lines, recounted with the 24 installed
  headers left out; the source root as the pane protocol's include path; `zengine_manual` at
  `workshop/CMakeLists.txt:25` and `builder/CMakeLists.txt:18`; the packaging law's exclusion and
  its doc gaps (the `surface` target no CMake file makes, two headers the tree lacks, "Ten of
  the fifteen" over 13).
- **Not checked**: the costs and sizes (by reading, as both say), and anything only a build
  shows.
- **Memory**: my prompts' Memory line was read two ways, as the store (the visual round added a
  route) and as the backlog (Workshop's round routed its line). Both harmless; the backlog is
  routed now, and my Memory lines will name the store from here.

## 5. After your answers

- **Prompts**: V1 (warm), waiting on V-1 and V-5; the first closings with the text check (warm),
  waiting on W-1, W-2 and W-7. They can run side by side, meeting only in the build files (the
  install file, Workshop's staging list): a small rebase.
- **The kit, one fix owed**: its left-behind check calls a report written once the file exists,
  committed or not, so a session that has written its report but not committed it could have its
  clones marked to go under it (the visual round's first recommendation). Into the next kit
  round.
- **`v0.2.0` is tagged** (`84446fb5`), so the MCP server's package swap is due.
- **The 32 issues** that lost `parked` or `later` carry no state label now: a triage when you
  want it, with the new labels you mentioned.
