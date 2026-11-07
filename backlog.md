# Zen backlog

**What it holds:** the work Zen has decided it owes and has not finished, in the order it runs.  
**Updated:** 2026-10-27, rewritten short. The old file is kept whole as
[history/closed_work.md](history/closed_work.md): every closed arc, and the full story of each
item below up to that day.  
**Beside it:** [pressure.md](pressure.md), pressure that may become work;
[ideas-2026-10-27.md](ideas-2026-10-27.md) and [ux-batch.md](ux-batch.md), asks not yet filed.

## How this file works

- An item is here only once Zen has decided the work is owed. Possibilities, seams and pressure
  stay in pressure.md until then. Nothing here is authorized work until a prompt says so.
- Each item says what it is, where it stands, what starts it, and where its prompt, report or
  issue is. No history: a round's story is its report, and a closed item's goes to
  closed_work.md.
- Bounded work goes to a GitHub issue, filed by Vision's prompt under `UnknownWorkers` with the
  labels set in the founder's name; a filed item keeps one line in section 6. A security defect
  is never a public issue: it goes into a draft private security advisory.
- An issue's pull request merges first, and an open phase branch rebases onto it.
- A prompt not yet run waits in `prompts/unrun/` (constitution section d).
- Issue and pull request numbers written before 2026-11-01 are the `-history` repositories'; an
  open issue was carried to a new number ([map](relicense/issues-map.tsv)).

## 1. Now: the wave

Four lanes run at once on three build slots: two work slots at 8 jobs, one final slot at 4
(constitution section f). WSL has 48 GB.

- **Report-backs land in `Zen/unreviewed/`** (the founder, 2026-11-06): uncommitted until Vision
  reviews them, then moved into `reportbacks/` and committed (constitution section d, amended).
  The status overlay rewritten as a board -- the lanes one row a session, the reports to review
  and prompts unrun, the pull requests and CI, the build slots -- its cleaner retired, the kit
  taught the landing ([prompt](../prompts/unrun/status-board.md), warm). The clock, view-cost and
  build-memory rounds reported under the old rule, committed in `reportbacks/`; reviewed
  2026-11-06. The build warning: #114 ([report](../reportbacks/ci-sanitizer-build-memory-RB.md)),
  ready. The clock's next round ([report](../reportbacks/clock-reactor-research-RB.md)): one wait
  on every source takes an idle Workshop from 300 turns a second to 1; asked: the order, the wait
  set as a claim, Loom's round now, the 16 ms beat, the rest's cap, and where the one wait lives
  (Vision's lean: in Loom, beside `LineInput` and `BridgeServer`). The view cost
  ([report](../reportbacks/view-cost-research-RB.md)): Inventory re-declares every view at each
  change, Workshop repaints per declaration and solves the desk per pane; R1 (Inventory declares
  only changes) now; asked: R7's shape (Vision's lean: Loom's after-turn hook) and R8.
- **The kit's phase is one shared file** (`Zen/primary/PHASE`): another lane's `kit.sh phase`
  re-pointed two rounds' helpers mid-session (2026-11-06); both pinned `ZEN_PHASE` by hand. A
  wrong phase makes another's folders read as the session's own to `kit.sh end --clear`.

- **Relicense to AGPL-3.0-only** (the founder, 2026-11-01), before anything else. Done but its
  loose ends: both histories rewritten so no commit says MPL (plain AGPL until a creations
  exception is drafted, no README note), pushed to the new public repositories and green;
  settings, labels and the 103 open issues carried
  ([report](../reportbacks/relicense-agpl-history-RB.md), reviewed 2026-11-01 and 2026-11-02).
  No copy of the old history is left on the machine but the bundles; the six repositories that
  stay carry a pre-push guard; private vulnerability reporting on; `zen-night-lab` and
  `zen-arena` private; #100 merged and the package on (the founder, 2026-11-02). The loose ends
  done (reviewed 2026-11-03): of the carried work 99 dropped and #487's branch kept, the View
  Builder's quarry ([sheet](drafts/loose-changes-2026-11-02.md)); the toolchains in
  `zen-build/toolchains/`; the kit's left-behind check. What it found, cleared, `parked` and
  `later` retired ([report](../reportbacks/left-behind-cleared-RB.md), reviewed 2026-11-03):
  nothing left behind. `v0.2.0` is tagged (`84446fb5`): the MCP server's 0.1.2 package swapped
  for it next. Pushed branches never merged stay in `-history`, carried on request. Still owed:
  the creations exception, drafted with counsel. Asked, not decided: a CLA before outside
  contributions; the trademark.
- **Main lane: Flow made over**, pushed as #559 at the founder's word (2026-10-29,
  [report](../reportbacks/flow-live-requests-RB.md)): batches A to E live in his Workshop, the
  Windows build mended after the first hosted run, three guide pictures taken from recipes (the
  older ones wait on #521). Reviewed 2026-10-29: green at `8ffdacfb`, every job, after the
  sanitizer and MSVC runs found a case reading a copy freed before the read; merges clean onto
  `main`. Flow's next round (the founder, 2026-10-29, after #559): the three old dialogs (Add a
  trigger, Add an emit, Add field) in request 8's words, and a kept field and a trigger's message
  field of one name refused at the edit, which the maker's admission refuses at Run. Later, with
  accordions (BL-WORK-16): the docks narrowed to tags that open on hover with their names and
  connectors.
- **Issue lane**: the UX batch done ([report](../reportbacks/issue-lane-ux-batch-RB.md)): 65
  issues in Zengine (#492 to #566) and Loom #73 (section 6), its eight pull requests merged, the
  weekly mutants run 341 of 341 caught and #476 closed. Then the ELH audit's findings
  ([report](../reportbacks/issue-lane-elh-audit-RB.md), reviewed 2026-10-29): #570, `repo` alone
  in `accounts-machine` so approving `workshop-machine` grants no push, and Loom #77, a spelling
  `loom-session` cannot type refused by the input's name, both green; 21 issues (#569, #571 to
  #589, Loom #76). Then the founder's decisions and the agent tools
  ([report](../reportbacks/issue-lane-decisions-agent-tools-RB.md), reviewed 2026-10-30): eleven
  decisions written on their issues, Loom #73 retraced; #590 the desk tools (#571, #573, #582),
  #591 the input owner's busy words (#579), #592 the workshop tools (#574 to #578, #581, #585,
  #586, #589), each green; #584 and #587 left open with a question each (section 5).
- **Kit lane: the picture tool**, done ([report](../reportbacks/kit-pictures-RB.md)): a picture
  taken from its recipe, an audit of all 128, 26 recipes; twelve retaken in #558, merged. An
  audit of `main` at `14669927` (the accordion lane's, 2026-10-29) finds three already out of
  date: `hotkeys-keymap-folder-window.png` (Start here, after #563), and the Files manual and the
  Pane Manager's row menu the kit round left; the Hotkeys and palette counts do not move with
  #568. After #559, an audit again. The manuals' recipe shows its own hand (Info inspecting the
  Manual's geometry, Notices listing the commits that placed it); a cleaner composition for a
  later kit round. The next two ran and were reviewed (2026-11-04):
  [background launches](../reportbacks/kit-background-launches-RB.md), the kit in Zen
  (`08e23581`) and Zengine #103 (the OS window put behind every window on Windows; green on every
  job, merges clean with #101 and #104, any time): an agent's Workshop opens without the
  foreground and covers nothing, `winhand.ps1` and `conshot.ps1` take the foreground only under
  `KIT_FOREGROUND=1` or `-Foreground`, `front.ps1` brings one forward, and the left-behind check
  counts a report from its first commit. [Private words](../reportbacks/kit-public-words-RB.md)
  (`891cf87a`): `public-words.py` marks a text before it is posted, never refusing. Asked, with
  Vision's leans: the flag named for what it now means (`ZENGINE_SDL_BACKGROUND`, in #103 before
  it merges); next kit round, `behind.ps1` as a guard in the launchers and a `pr-say.sh` route
  that runs the words check on a pull request's text. The windows branch of #103 is compiled by
  no hosted job; the night's Windows package build is its first.
- **Accordion lane: stage 2**, as #568 ([report](../reportbacks/accordion-stage-2-RB.md)): the
  group borrows its owner's list and keeps no copy, so a pane's state is the truth; Info's values
  a tree (WL-INFO-16), with Right, Left and Shift+Left. Rebased onto `main` at `c46f3098` and
  green (its last section, reviewed 2026-10-29): the floors measured (component 59, info 185), an
  open walking a list in any order, witnessed under libstdc++'s debug mode, Info's manual picture
  retaken; merge-ready. Three decisions (section 5).
- **WASM lane: stages 2 and 3** ([report](../reportbacks/wasm-tier-s2-s3-RB.md)): S2 merged as
  Loom #74, `Kernel::containment(name)`, D7's statement in `capabilities.md` as recorded. S3 as
  Loom #75, rebased onto it and green, tests only: the door cases run on boxed twins built from
  the same fixtures (24), and the five bounds met; merged. S4, a Zengine pane boxed in Workshop,
  reported and reviewed 2026-10-30 ([report](../reportbacks/wasm-tier-s4-RB.md)): Loom #78 green,
  12 of 12, merges first; Zengine #594 green but its boxed job, refused at configure until #78 is
  in. #78 merged (`619d102f`); #594's rerun green on every job, the boxed one included, its body
  put right; reviewed 2026-10-30; merged (`8559e428`). S4b, the Builder's second target: the
  founder took it into the Builder (2026-10-30), a recipe making its pane native, boxed or both
  through Workshop ([prompt](../prompts/wasm-tier-s4b-builder.md), warm): reported 2026-10-30
  ([report](../reportbacks/wasm-tier-s4b-RB.md)), its review next.
- **Docs lane: Loom's README as the front door.** The journey page (#79, +1044 lines) closed by the
  founder (2026-10-30): docs get smaller and clearer, never longer. First the eight Loom entries of
  the docs-against-code list in one small pull request, Loom #80, merged (`a2fe7e2`), so the
  rewrite reads no contradiction. Then `Mail::reply` falling back to the stamped sender when no
  reply address was given, ordinary grant-checked speech still (the founder, 2026-10-30;
  [prompt](../prompts/mail-reply-fallback.md)): Loom #81, reported green at `1429803c`, its
  review next. Then Loom's README rewritten
  below the preface: a punchy, honest summary; the ideas, ordered for a reader, each section able to
  stand alone as bullets; install, build, the console, a first weave, loading code, sending a
  message; deep-dive links (loading code, a message's path, the console's commands) folded from
  today's guides. Every command and code block run by a test, each a small main-only program; a cold
  reader following it on a clean machine is the gate, the founder's read last. Vision drafts the
  outline (summary, ideas as takeaways, sections) for his markup before the prompt. After it: the
  self-test cross-referenced, Zengine's README the same way (its entries of the list fixed first),
  then readers outside the project seeding an FAQ of plain questions with direct answers a layman
  can follow.
- **The review waves** (2026-10-29). The first: #485, #491, #489, #486, #484, #490 and #488
  merged, #487 closed. The second, reviewed the same day: #553, #555, #561, #557, #563, #567,
  #550, #565, #558 and Loom #74 merged. The third, reviewed that evening, all green and each
  clean on `main` and with the others: #570, #568 and #559, then Loom #75 and #77 back to back.
- **UI census**, reported ([report](../reportbacks/ui-census-RB.md), `08693d45`) and reviewed
  (2026-10-29): an element set of nine and an order; its nine decisions with the founder
  (section 5).
- **Closed this week**, each in its report: the desk's round 2 (#467, #469, #470, #472); the
  repository's mutants and their follow-up (#471, #473, #475); the View Builder lane (#484, #489,
  #490, #491; #487 not merged, the builder made over after Flow); the text lane (#485, #488);
  accordion stage 1 (#486); the kit's compile gate (12 GB a work slot, each tree its own peaks).

## 2. Next, in order

1. **Flow made over** (BL-WORK-32), its prompt written (2026-10-28, section 1). The clickable
   [mockup](https://claude.ai/artifact/JxK1MLFeeSmQh2GgD3v4jY): When, Do and Then kept as colour
   with more room to Do; the rule read as a sentence; a Next line in place of Run's refusals; a
   nine-stop tour. The founder's calls (2026-10-27): a press may change several things, and
   several messages may change one field; each node listens only to its own message and
   condition, so pressing `+` computes no divide; a gear for settings. Quicksort needs a branch
   form (only the chosen side computed) and list operators. Start here's moves for steps 2 and 3
   wait on it. Zengine #142 holds the older milestone question.
2. **The element set, its text pieces first** (prompted 2026-10-30,
   [prompt](../prompts/element-set-text.md), warm) (the founder, 2026-10-29: "High quality
   components means higher quality composites"), a stage worth the time. The census's set
   (section 3), its drawn faces lifted from Flow's pen once his round ends. First the text: one
   core (the text, places in it, the selection, the word rules, the window over it, the copy);
   the text area over it, read only; the text box over it, adding the caret and the editing, at
   first with every behaviour its 25 users have today, then the whole box pressed and the caret
   blinking. The box seen as a box (the founder, 2026-10-29): a 1 px border in a light grey role
   a theme maps; Loaded's search is the first that needs it. Before the View Builder's makeover,
   which builds on it. The text stage reported 2026-10-30
   ([report](../reportbacks/element-set-text-RB.md)): Zengine #593, green on every job at
   `492e96c9`. The founder (2026-10-30): `[text___]` in cells; every text box always seen as a
   box, empty included; Loaded's search shown from the start; `component/` knowing no medium.
   The faces round (`bd184417`) green on every job, reviewed 2026-10-30, merge-ready:
   `component/` measured in characters, each look a face in `graphics/elements/`, a row carrying
   its box. The founder (2026-10-30): the Terminal's own line plain in cells (`> ls -l`), its
   outline kept in a window. #593 merged (`13cc5674`, squashed); the Terminal's line came as
   #595, one commit on `main` ([prompt](../prompts/element-set-text-terminal-line.md)), its report
   due.
3. **The View Builder made over** (the founder, 2026-10-29), after Flow, as Flow was: the design
   as a whole, not the lane's three notes one by one. What it carries: the kinds a row each below
   Grid (his note of 2026-10-27); the width that responds, which he liked (#487, never merged,
   its branch the makeover's quarry: the kit primary's `carried/batch/lane-view-builder`);
   Discard asking a second press, as New and Open do; the census's element set as its kinds; and
   after it, Workshop's two pictures of the builder taken again (`quit-box.png`,
   `pane-manager-new-view-builder.png`), and its `<action> complete` (WL-NOTE-06), a leftover the
   issue lane left to it. Then a pass over the smaller panes on the new pieces (the founder,
   2026-10-29), in a few phases side by side. The three picture panes' boxes (view host, View
   Builder, Flow) go onto `text_box_face` with this makeover and Flow's next round, not alone
   (the founder, 2026-10-30). The Builder earns a makeover of its own after this one (the
   founder, 2026-10-30).
4. **The operator suite** (BL-WORK-48), which Flow's calculator runs on. Today: five Int
   primitives (`operator/primitives.hpp`). To add:
   - Math: subtract, multiply, divide and remainder (both refusing 0), negate, abs, min; square
     root and logs, which want Float beside Int;
   - comparators: equal, not equal, less or equal, greater, greater or equal;
   - Logic: and, or, not;
   - later: Lists, with the quicksort; Text after.
5. **The UX batch**, filed by the issue lane (above), then **the first complete maker story**
   (theme 13, section 7).

## 3. Decided, not yet ordered

Each starts on the founder's word; "wake" is what must be true first.

- **The visual foundation** (the founder, 2026-10-31,
  [answers](drafts/decision-wave-graphical-answers.txt)), before the makeovers, built for the ideal
  future: the earned rule retired the same day.
  - Colours, a new system: the painter knows no colours, each draw carries its own; a pane colours
    by an exact value, a name from a shared pool named by use (background, text...), or a slot it
    exposes to themes; themes are JSON, loaded without compiling, setting any exposed slot, each
    theme saying whether a slot nothing exposes is skipped or refuses it whole; the same pool holds
    fonts and text sizes. Census 9's emphasis colours fold into it. Names reached as C++ names,
    generated as the quarry's Config Generator did: a name per pool entry and per exposed slot,
    a typo a compile error, the window turning the name into a colour when it paints (the
    founder, 2026-11-02).
  - Looks: Vision's model (when, what, how; operators a closed set the window knows, a weave's own
    only boxed and later), several at once on one node, an operator taking a value struct (a fade's
    end colour). The window-looks record rewritten so: (b) to (d) yes, (e) the act tool holding
    steady for its run. Looks of one trigger on one property chain in the order added (the
    founder, 2026-11-02); of two triggers, the one fired last wins while it holds.
  - Text: weight, size and every character past ASCII drawn in the window; `?` only where a
    terminal can't show one.
  - The element set: button (once `control`), field, list, collapsible, text area, hint
    (2026-11-02; `collapsible` the founder's, 2026-11-03: one fold, a group of them an
    accordion, so the code's `Accordion` and `IndependentAccordions` are renamed to match).
    Search is the list's filter: filters and a sort chained in order, by the list's type and
    parameters. A choice is no element but a rule (the founder, 2026-11-03): a group over
    elements that have an on state, wherever they sit (three radio buttons, each over a form of
    its own), saying how many may be on. A form greyed out until its box is checked, a field
    required or checked, are rules of the same family, his linked-field logic: designed as one
    when the element set reaches forms. Tabs are toggle buttons under a one-of rule, `tab_strip`
    their strip's layout. Groups are a pane's layers, painted
    and hit in tree order; a move puts a node before or after a sibling, a raise flag lifts one
    until lowered without touching the order, never across groups (Vision's call, the founder
    deferring). The old drawn classes retired as faces supersede them, Image and Grid kept
    until superseded; a menu row's key and submenu mark as fields;
    every key a hint names read from the keymap; Info's list rule with the list piece; Workshop's
    panes on a shared piece wherever one fits.
  - Keys: a pane hears a key first, what it doesn't consume going up to Workshop, and a pane may
    opt out of Workshop's defaults; a pane owns its own key (from outside it opens or selects the
    pane, inside it closes it); one action shape carrying its source (a click and its place, a key,
    an agent's). Keymap ids scoped by their owner (2026-11-02). Every pressable thing an action
    and one way in, a button its own declaration, a press declaring what it does (a message, the
    message a draft holds, or the pane's own code), a hotkey only a keymap binding: Vision's
    ideal, taken (the founder, 2026-11-03). A command tile's press runs it. Jump hints with a
    mode each, press and focus first, a hint's letter triggering its action. One way out is
    always Workshop's: a pane may take any key, and a press reaches only the area under it, so
    the setups bar stays one.
  - Docks cover the room, and only authored anchors move panes; a dock keeps a strip its edge's
    whole length, open or shut. Fold and dock are typed fields of a setup's pane row (setup v7,
    session v13; the founder, 2026-11-02).
  - Settings: the double-click speed is input's; themes merge and reset (the research's two);
    locked settings a final layer; a failed key skipped or the theme refused, the theme saying
    which, a wrong type always loud; a reset whole, or applied on top; several keys an action.
  Answered 2026-11-02 and 2026-11-03 ([clarify](drafts/decision-wave-clarify-1.md),
  [clarify 2](drafts/decision-wave-clarify-2.md)). Workshop in its own repository: the right end
  state (Vision's read, taken): the boundary proven in one repository first, a stranger lane,
  then the move, after the visual foundation's first stages; the distance measured
  ([report](../reportbacks/workshop-as-a-stranger-research-RB.md): 111 reverse include lines,
  the seam Zengine's, 23 closings). Designed whole (2026-11-03,
  [design](../reportbacks/visual-foundation-research/design.md),
  [stages](../reportbacks/visual-foundation-research/stages.md),
  [report](../reportbacks/visual-foundation-research-RB.md)): eleven stages in Zengine, V1 the
  pool and palettes first. Both reviewed 2026-11-03, their thirteen calls with the founder
  ([review](drafts/research-review-2026-11-03.md)). The visual foundation's six settled the same
  day, the design amended so (the founder, 2026-11-03), V1 prompted
  ([prompt](../prompts/unrun/visual-foundation-v1.md), warm) and V8 beside it in a second lane
  ([prompt](../prompts/unrun/visual-foundation-v8.md), warm):
  - **Pictures**: one may change where the change is the point, named with its reason, before
    and after, for his review; byte for byte only for V2's sweep. Every picture added or retaken
    comes from a recipe the kit's picture tool replays. Excised rather than carried: which of the
    four looks ship as themes is proposed with pictures for him to pick; no widening of old
    shapes for strangers (`v0.2.0` is pre-1.0), a bridge for our own drawers ending in V2; the
    conversions of saved setups and sessions kept.
  - **V1**: `Paint` named `Color`, and `color` in every new name. Generated names give
    autocomplete, and a name nobody declared does not build; any name is fine. The generator a
    CMake script, installed, the floor 3.22, a version a lane runs. The skin seam retired, the
    painter one library behind one interface in the window. A colour's terminal word (`cells`)
    optional: without it, the nearest colour the terminal shows; its own ground never matched.
  - **V2**: Flow's 31 hues collapsed to as few slots as is reasonable (about six by Vision's
    count), the rest pool names.
  - **V3**: monospaced first; the platform's fonts, then an embedded last resort that draws the
    character; cases and pictures on the embedded faces; a fallback glyph in its own cells.
    Proportional text a stage of this arc, after V3 and before V9, a pane writing one layout for
    both media.
  - **V4**: a theme's entries for a pane the load plan names wait for it; `refuse` judged when
    the theme is applied, a miss found later skipped and said.
  - **V5**: the beat an office-wide setting, changed through the settings door; a look computed
    from the time since it began, so it lasts its length at any rate. `back` named
    `reverse_on_end`; `repeats` a count, forever a named largest value, not 0. A look never moves
    a hit: the hit drawn at its largest extent, a leaving node taking no press.
  - **V6**: the press lambda stays in its pane, only its message's shape declared; a hotkey asks
    an action by its id, and that action's own press form runs.
  - **V7**: one way-out chord, Ctrl+Q by default, moved only by the weaver; the band shows it
    while a pane holds the keys, and a notice says once where it went if the legend is hidden.
    Inputs, batched ones too, resolved one at a time against the state the last one left, the
    chord never waiting; how keys are routed is Ceecee's.
  - **V8**: shut on the title bar once it is a `Collapsible`, the arrow at the bar's start (the
    left of a horizontal bar, the top of a vertical one); meanwhile on today's title row, no
    second bar; a shut pane keeps its title row with titles hidden.
  - **V9 to V11**: each element stage reviewed for feel, its faces in both media and a pane's
    code using them, before it merges.
  - **Built**: V1 as Zengine #101 and V8 as #102, each green on every required job, reviewed
    2026-11-03 ([V1](../reportbacks/visual-foundation-v1-RB.md),
    [V8](../reportbacks/visual-foundation-v8-RB.md)). #101 merges first, then #102 rebased
    (`tests/shapes.txt`, adjacent lines; [prompt](../prompts/unrun/visual-foundation-v8-rebase.md),
    hot). Their texts stay as posted: an edit keeps the old words in GitHub's history.
    Asked, with Vision's leans: the looks (night and day ship, block a tests' fixture, classic
    another word for night; the pool's `own` kept for text and grounds alone, so a terminal shows
    the other colours by nearest ink; into V2); the snake's `1 skin` (kept); the advisory MSVC
    job's hour, settled (the founder, 2026-11-04): ninety minutes before #101 merges, since a job
    stopped at its limit saves no cache and cancels the run, and the night packages only a passed
    one, green all the same; the night made to say so: #104
    ([report](../reportbacks/ci-msvc-hour-RB.md), reviewed 2026-11-04, green on every job), then
    #101 rebased onto `main` and run again
    ([prompt](../prompts/unrun/visual-foundation-v1-rebase.md), hot), then #102's rebase.
    #104 merged (2026-11-04). A reviewer of the founder's read the open work (2026-11-04): #66
    closed by #101 and the word `skin` named as known debt in #101's record, both in its rebase;
    v0.2.0's notes ("replaces the package before it") untrue for the first release alone, fixed on
    the release, and `main's tip` kept out of a pull request's Package run: #105
    ([report](../reportbacks/ci-release-notes-RB.md), reviewed 2026-11-04, merged; the notes
    edited). Its cost, the reviewer's: the judge runs in no pull request, so one that breaks it
    passes; the judge exercised on fixed cases in every pull request that changes it
    ([prompt](../prompts/unrun/ci-tip-judge-cases.md), warm): #106
    ([report](../reportbacks/ci-tip-judge-cases-RB.md), reviewed 2026-11-05, ready), eight
    cases, one judge; its first live witness the first night after it merges. #100's stale-green
    night already answered by #104's tip job; the shapes conflict and #102's role-picked colours
    (V2's sweep) as known. The peek (waived until
    the title bar's composite); the fifteen held pictures (one recipes pass after V3); one word for
    theme, palette and skin where a weaver sees it (theme, renamed with V4; block's summary
    still says "classic's light").
    #102 rebased onto `main` (2026-11-04): its sanitizer job stopped three times mid-verify by a
    runner shutdown (exit 143), under its 90-minute limit. The job sits at its runner's memory:
    `main` peaks at 15.1 of 16 GB at four jobs, #102 155 MB above it
    ([report](../reportbacks/visual-foundation-v8-rebase-RB.md)); its fix (the founder,
    2026-11-04): each entry measured, the heaviest apart, three at a time only if none stand out,
    the peak said and warned past 12 GB
    ([prompt](../prompts/unrun/ci-sanitizer-memory.md), warm): #107
    ([report](../reportbacks/ci-sanitizer-memory-RB.md), reviewed 2026-11-04, merged 2026-11-05,
    `main` green with it), the two
    largest panes suites apart, 6.4 GB on the runner; then #102 rebased
    ([prompt](../prompts/unrun/visual-foundation-v8-rebase-2.md), hot;
    [report](../reportbacks/visual-foundation-v8-rebase-2-RB.md), reviewed 2026-11-05, ready: green,
    its sanitizer job at 88 of its 90 minutes after a rerun for a full disk). The looks
    (the founder, 2026-11-04): night and day ship, and block as the terminal look, the one theme
    that changes how a terminal draws (the tests and the snake keep it; a layer over night or day
    with V4's `merge`); classic another name for night; `own` for text and grounds alone. V2
    prompted ([prompt](../prompts/unrun/visual-foundation-v2.md), warm): #108
    ([report](../reportbacks/visual-foundation-v2-RB.md), reviewed 2026-11-05), its content ready;
    it follows #102, by its applier from the new start, once the lane's scaling lands
    ([prompt](../prompts/unrun/ci-sanitizer-scale-research.md), warm): its sanitizer job passed its
    90 minutes, the runners' doubling, not V2's. The founder's calls on it (2026-11-05): `own`
    named `terminal default`; a pane's ordinary border grey in a terminal; Flow's columns on a
    second background (`background_alt`, the DO column's old `#20252d`); a terminal matched to
    what it can show later, with the terminal research: V2 continued once #102 merges
    ([prompt](../prompts/unrun/visual-foundation-v2-continued.md), hot). The snake's pictures
    taken in play by a pilot, the first participant an agent runs to play a program for it,
    playing against the world's own beat and never stepping it, a pause the world honours
    for a picture ([prompt](../prompts/unrun/snake-pilot.md), warm), after the research.
    V2 continued: #108 ([report](../reportbacks/visual-foundation-v2-continued-RB.md), reviewed
    2026-11-05, ready: green on every job, its sanitizer job 74 of its 90 minutes); three block
    pictures in a terminal stale for want of recipes, for the held pictures' pass. The pilot:
    #109 ([report](../reportbacks/snake-pilot-RB.md), reviewed 2026-11-05, ready after #108),
    its place by an exercised replacement (WL-PART-01, asked); onto `main` once #108 merges,
    with the snake's pictures in play ([prompt](../prompts/unrun/snake-pilot-continued.md), hot).
    #108 merged (2026-11-06). The sanitizer job at scale: #110
    ([report](../reportbacks/ci-sanitizer-scale-RB.md), reviewed 2026-11-06, ready, clean onto
    `main`), in before the pilot's continuation; asked: Inventory's view cost (P-WORK-81) and a
    warning for the builds' memory (P-BUILD-21). The clock's first steps: #111 and #112, their
    report not yet in, #111's run going; both merge clean onto `main` with #110, and #111 meets
    the pilot in the snake's CMake list and the population.
    #110 merged (2026-11-06). The pilot continued: #109
    ([report](../reportbacks/snake-pilot-continued-RB.md), reviewed 2026-11-06, ready on today's
    `main`): the snake's two pictures in play, steady; its test names and rig still say classic
    (V4's word pass). The clock's first steps: #111 and #112
    ([report](../reportbacks/time-first-steps-RB.md), reviewed 2026-11-06), their content ready,
    their runs on `9bc2f646`: onto `main` after #109, with the facet's claim trap fixed
    ([prompt](../prompts/unrun/time-first-steps-continued.md), hot). Asked: whether the reactor
    or frame clock (the idle wakes, about 220 a second) is the next round. Not measured: a key in
    a Neovim pane; the switch asked from the Terminal answered and left the standard Editor.
    #109 merged (2026-11-06). The founder took Vision's three leans (2026-11-06): the clock's next
    round, a reactor or a frame clock, researched first
    ([prompt](../prompts/unrun/clock-reactor-research.md), warm); the view cost researched as the
    product's, the case unchanged ([prompt](../prompts/unrun/view-cost-research.md), warm); and the
    sanitizer builds warned past 14 GB, in a lane beside them
    ([prompt](../prompts/unrun/ci-sanitizer-build-memory.md), warm). The clock round's
    continuation reported: #111 and #112 onto `main`, the facet's claim trap in #113
    ([report](../reportbacks/time-first-steps-continued-RB.md), reviewed 2026-11-06, all three
    ready, one tree in any order); the Timer's own claim hook unneeded once #113 is in, one line.

- **State or checkpoint: a research pass** (the founder, 2026-10-29). The Hotkeys pane's open
  sections (`DesktopState::hotkeys_open`, #486) are a checkpoint: the truth is the accordion
  group in the pane's view, copied into the state after each act and read back only when the
  weave activates, so an edit to the field would show nothing and the next act would overwrite
  it. The pass: every weave's state, each field the truth or a copy; each copy made the truth, or
  named for what it is (his `HotkeysStateBackup`). First the eleven states that are `ZEN_EXPOSE`d
  (two in the snake example), where a poke's write is acknowledged; `IntrospectionState` already
  says the rule: "a copy here would be the answer that goes stale". The Hotkeys pane's own fix,
  accepted (the founder, 2026-10-29): its open sections kept in its state as the truth. Beyond the
  pass (the founder, 2026-10-29): components mark the fields they would keep (a text box's words,
  never a hover), and a pane given leave keeps its view's marked fields, by a message set apart
  from snapshot and restore, so no pane keeps a second copy of what it shows. Research at that
  stage; the element set's values (the census) are where the marks would live.
- **What terminals can show: a research phase** (the founder, 2026-10-29, in place of an issue).
  The terminal medium asks a colour of each role (`sgr_for_role`,
  `graphics/window/terminal_io.hpp`) and turns on VT processing in a Windows console, yet the
  accordion's console pictures showed every role in one grey. What each terminal shows, and why
  that console showed none; the medium draws what it honestly can, and no two media promise one
  picture.
- **A message picked by name, declared whole** (near roadmap; the founder, 2026-10-29). Flow's
  New message declares a view's message by name with no fields, and listening for a message is of
  use only with its fields: knowing something happened without its data is hearing an action and
  not being able to answer it. Needs an owner that answers a message's shape by its name.

- **A pane's own top right** (desk round 2's parked item): close and move, a gear, a box around
  each icon, the arrange markers on boxes of their own, "remove from the setup"; about 116 page
  pictures retaken with it. Wake: the kit's picture tool, now built (#558, 2026-10-29). With the
  accordion's desk stages (the founder, 2026-10-28): the title bar is the pane's own accordion
  header, its words and buttons there, a double click shutting or opening the pane; a dock's tag
  is the same bar drawn small, a vertical one its icons stacked and its name a letter a row.
- **One element set for the panes and the View Builder** (Vision's proposal, 2026-10-28, from
  the old `zen-ui-vocabulary.md`, the rebuild scaffold's element census and the code): each
  element a value in `component/` and a face drawn from it, drawn by the panes and offered to
  makers as the View Builder's kinds. The census reported and was reviewed (section 1,
  [report](../reportbacks/ui-census-RB.md)); its nine decisions, the scaffold's call 6 among
  them, wait on the founder (section 5). The text area, from the founder's note (2026-10-29): in
  cells, markers for what is above and below; in a window, free scrolling with a bar of 4 to 8
  pixels on the right; wrapping by width; its text selected and copied. Vision's reading: the
  value keeps the scroll and the selection as places in the text, never rows or pixels, so a
  rewrap keeps both; free scrolling needs the window to cut a line of text by its pixels (today a
  group's clip drops a line whose top is outside it and lets the last spill); the bar's room kept
  whether or not the text overflows, so nothing reflows when it appears, and pressed in a wider
  band than it is drawn; a copy is the text as written, without the wrap's breaks or indents; in a
  terminal the selection is drawn by the pane, since Workshop holds the terminal's mouse. The
  founder's calls (2026-10-29): the bar drawn 8 px wide, 12 px while the pointer rests on it (the
  widening's animation later), its room and its press 16 px, to adjust once used; the markers
  `... 3 more below` and `3 more above...`; the text box built on the text area, with its own
  caret, the whole box pressable (today only its text is) and the caret blinking.
- **The window-run element retired** (the founder, 2026-10-29): `ElementPut`, `ElementChange`,
  the element seam (`graphics/element_abi.h`, `element_export.hpp`, `ZENGINE_EXPORT_ELEMENT`), the
  window's element code and its four shapes, so no window keeps an element's state; the snake's
  board drawn by its world as a picture. About 22 files; two installed headers go, a change to
  the package. Filed as #546 (2026-10-29); `limitations.md`'s line on `graphics/elements/` (#565)
  goes with it.
- **What a window may carry: looks that change with time or the pointer** (the founder,
  2026-10-29, from the blinking caret). A pane's drawing names a behaviour from a closed set the
  window knows (a caret's blink, a part lit while the pointer rests on it, a pressed look while
  held, a change eased from one drawing to the next, perhaps a scroll inside rows drawn past the
  edges), and the window runs it with no message; what the pane must know to answer (a
  selection, a fold, what a press means, where a scroll settled) stays the pane's. The test: if
  the window forgot it now, nothing but a frame of looks is lost. No pane's code in the window,
  which keeps it apart from the retired element seam. Pictures and cases need a steady mode
  (no blink, a change shown at its end). A research, the element set stage's first step. The
  founder (2026-10-29): each animation says its own length, since one may loop for good; and an
  agent's press skips animations: the act tool's own press carries the skip, never a key a
  weaver uses, such as Shift, which will extend a selection (agreed, 2026-10-29).
- **A pane's bar tinted while it holds news the weaver has not seen** (the founder, 2026-10-28),
  shut, covered or only unfocused; the pane's own word says what is news, and looking clears it.
  To weigh against Attention's conditions before a second channel is made.
- **Settings, stages 4 to 6** (BL-WORK-36; stages 1 to 3B merged, #101 and #314 to #326). Stage
  4 is the settings weave applying themes, once its research is read again against the desk's
  owner; it takes the open report rows 47, 48 and 69 to 71. First check whether stage 3B's
  stopgap (locks, pins and baseline in Workshop's settings file) moved with the desk split. The
  design is the founder's eight decisions of 2026-10-18. Wake: met.
- **Every pane a free picture** (BL-WORK-46; steps 1 and 2 merged, #387 and #394). Next: the
  thirteen panes still on rows move one at a time, `PaneRowsFacet` retiring with the last.
- **Control schemes** (BL-WORK-47; the POSIX slice merged, #402). Next: a loader that stacks
  schemes as themes stack, and a chooser in Workshop, the first-run screen's first.
- **Layout modes L3, the views** (L1 #413 and L2 #421 merged). A share's inverse and an anchor's
  offset sit in `workshop/setup.hpp` for it. Wake: met (#340).
- **The story's step 7**: Workshop reconnects to an exported app and takes its weaves back (C1,
  L2 and C2 of the [research](../reportbacks/app-export-research-RB.md)); it needs prompts, not
  research. With it, Loom's small follow-ups: an installed `AuthorityDesk` seat, `authority
  trust` naming a host's baseline, and the bridge's sockets closed on exec (private). Wake: after
  the release.
- **The editor-switch weave** (WL-SWITCH-07): a small weave holding the four switch asks the
  Terminal holds, its remembered choices in the session's header. Wake: met (D1, #415).
- **Places kept across runs**: a pane closed in one run comes back where it was in the next.
  About a day: the session's and the setup file's next versions.
- **Agents and weavers on one desk** (BL-WORK-38). Left: #139, stages 3a and 3b, `host`, `ask`,
  `check` and `probe`, then 4a to 7; the dense reading (a grid rectangle row by row) not yet
  placed. Until the agent desk, an agent's press still moves the keys and the selection.
- **Untrusted code, the WASM tier** (S1 to S4 merged: Loom #72, #74, #75, #78; Zengine #594).
  Left: S4b, the Builder's second target (section 1), then S5, its doors (a clock, standard
  output as messages, a module cache), designed whole. D7's statement is in Loom's
  `capabilities.md` as the research wrote it (#74). An agent without a shell waits on this and on
  tools by reach.
- **The MCP adapter's live check** through the app, and the weaver case on package 0.1.3. Wake: a
  lane left empty.
- **The ELH audit's findings** (a cold agent for the founder, 2026-10-29,
  [report](../reportbacks/elh-audit-report.md)), checked by Vision against the code: the
  `workshop-machine` package's `repo` tool gives git push and pull requests to any session that
  approves Workshop's machine tools; act passing a press its owner refused; `open` leaving a pane
  being placed; Loom's `loom-session` reading an unknown bool spelling as false (`cli.py:247`);
  `inspect-capture`'s test inputs on an agent's tool; scenario scripts a quarter of the catalog;
  no quickstart, and no tool asking for a pane's document. Its claim that Inventory, Info, Demo
  and Compose declare no causes does not hold (30, 7, 2 and 1 rows); resolve answering a missing
  shape as a real one does. Wake: the issue lane's round after its UX batch
  ([prompt](../prompts/unrun/issue-lane-elh-audit.md), warm, 2026-10-29).
- **The Perspectives Lab's pages** rebaselined after D1, before any becomes a prompt. Wake: met.
- **Faster builds** (BL-WORK-44; #343 merged): split `tests/workshop_support.hpp`, the largest
  lever (2026-10-27: 36 of the 45 compiles over 2 GB include it, 43 % of a cold build's compiling);
  the sanitizer job back to 60 minutes if the code's health allows (90 now, #356; #419 profiles its
  longest entries); the old CI caches evicted.
- **Fast forward** (BL-WORK-43; S1 and S3 merged): S2 and S4 to S6.
- **The release for Windows and Linux** (BL-ADOPT-06). The nightly package is live (`v0.1.0` on
  2026-10-24, 0.1.3 since, its tally story walked each night). Left: the rest of the release,
  the first tutorials starting from the extracted folder.
- **Loom's own release** (BL-ADOPT-07, [prompt](../prompts/loom-release-research.md)): researched
  once Zengine's nightly has published a few clean nights.
- **The documentation overhaul's rest** (BL-ADOPT-05): stage C's tutorials wait for the complete
  stories; stage D comes after the release.
- **The founder's order of 2026-10-03**, after the settings:
  1. what the canvas unlocks (BL-WORK-09): a hover cue, and a tutorial mode walking a pane's
     parts;
  2. accordions and anchors, researched first (BL-WORK-16; anchors to edges and shares landed in
     L1 and L2, the research's prompt written 2026-10-28, section 1);
  3. Files answering a request for a path (BL-WORK-17);
  4. Info as a one-slot inspector (BL-WORK-10);
  5. images (BL-WORK-11);
  6. load metadata, researched first (BL-WORK-26);
  7. a dead weave's last state, inspectable (BL-WORK-27).

  Agents acting by intent (BL-WORK-25) runs beside them.
- **On the founder's word alone**: text in UTF-8 everywhere, researched first (BL-WORK-39); the
  simplest snake played by its own AI, with a C++ to Python owner handoff (BL-WORK-40); the Data
  Conversion Mapper (BL-WORK-41); the Black Box Reader (BL-WORK-42); the demos' last step, a
  right-click that runs one.
- **Maybe later**: a second package set named with `_python`, carrying a Python for those
  without one; the setup words a row lower, with Workshop's own title bar.

## 4. Standing duties and watches

- **Workshop and onboarding grow together** (BL-WORK-01): repeated friction gets a better
  interaction or a true explanation; mandatory before inviting outside contributors.
- **A front door for human contributors** (BL-ADOPT-01): installed prefixes, IDE discovery, the
  lanes; before soliciting contributors.
- **Current law stays cheap to carry** (BL-ARCH-02; #201 merged): the next pass binds each case
  to its cited test file, then the search-and-link pass.
- **The drawing door grows to its full set** (BL-WORK-37; stages 1 to 7 merged): ovals,
  polygons, images, shaders and whole widgets, built for the design rather than as consumers ask
  (the founder, 2026-10-31).
- **The census's remainder** (BL-WORK-45): the mirrors (Attention, Connections, Info's
  properties, Introspection) become data-form views.
- **Night Lab, era 2** (BL-LAB-01): held, top-down; its findings go through the founder to Vision.
- **The local lane** (BL-LANE-01): shelved while the founder weighs where the agents run.

## 5. Waiting on the founder

- Workshop's seven calls, W-1 to W-7 ([review](drafts/research-review-2026-11-03.md),
  2026-11-03), each with Vision's lean; the first closings' prompt waits on W-1, W-2 and W-7.
  The visual foundation's six settled the same day (section 3).
- An adversarial read of Loom, Zengine and Workshop (the founder's Grinch agent, 2026-11-05,
  revised with Vision's corrections): gates inside the visual foundation's rest -- the clock
  (A2) before V5, the interaction contract (A4: gesture streams, a focus chain, dispositions,
  key routing from declarations against the settled pane-first) before V6 and V7, door-level
  authored migration edges (A1) and roles on every element before V9 to V11; async causality
  host-only with an own-origin form for recipients (A5). Cheap now: handler times measured,
  Neovim's reads off the dispatch thread (`call_now` blocks it up to 2 s, 10 s to adopt or
  start), the nap between turns rather than inside the Timer's handler: taken (the founder,
  2026-11-05; [prompt](../prompts/unrun/time-first-steps.md), warm), input's wire unchanged.
- The composer's bare values and optional fields (Loom #31's report, 2026-10-08, not asked since):
  a bare value fills the first field in declaration order, optional or not, so `7` for
  `{limit?: Int, n: Int}` fills `limit` and leaves `n` open, and the reply does not say where `7`
  went. Vision's lean: a bare value fills the first required field, an optional one is filled by
  name, and the reply says where each value went.
- `authority pending`: a grammar change, only if he wants one.
- The Demo pane's development recipe: Vision's lean is none.
- Show me opening over Start here, covering its words: Vision's read is to leave it.
- The graphics research's round 2, decisions 2 (a group is a layer: how it lands, in
  [clarify](drafts/decision-wave-clarify-1.md)) and 10 (its eleven seams filed as issues).
- Where the desk's 3a and 3b (BL-WORK-38) and fast forward (BL-WORK-43) fall in the direction.
- The open decisions in one wave (the founder, 2026-10-30), not small batches: every decision
  asked since 2026-10-15 swept against `main` (Zengine `13cc5674`, Loom `a2fe7e2`), with this
  section's, on one [sheet](https://claude.ai/artifact/XQRS3aJeBCbcR9KGDZ4no2) (2026-10-30): 64
  to answer in 12 groups, colours first; 15 small calls Vision takes unless he says otherwise;
  15 not wise to answer yet, each with its reason, at its group's end. His answers save to the
  sheet; Vision reads them back and folds them in here. The sweep's record:
  [drafts/decision-wave-2026-10-30.md](drafts/decision-wave-2026-10-30.md). The items below that
  the sheet carries are answered there. Its first half answered (2026-10-31) in a file of his own,
  kept [verbatim](drafts/decision-wave-graphical-answers.txt) and recorded in section 3; his open
  calls from it, with Vision's answers, in [clarify](drafts/decision-wave-clarify-1.md).
- Where the local lane's agents run (BL-LANE-01).
- The accordion research's eight decisions: Vision takes seven of its recommendations (docks
  taking room, the two row words, the bar's length one setting, the piece in `component/`, Info a
  tree after the first stage, Files' places with the Hotkeys pane first, a pane shut where it
  stands). The founder's shape (2026-10-28): one accordion (a section) apart from its groups, each
  group a small component over it: independent, exclusive, and a pair ("two-sided": two, one always
  open, their space constant); a pane on the desk one accordion, its neighbours following by
  anchors between panes. Settled the same day: an exclusive group may be all shut; a pair is a
  set-size frame of its own, placed like a pane, its first header always at the top and the second
  under it while the first is shut, at the foot while it is open, so it needs no anchors and may
  itself be a section of an outer accordion; docks (the bars) before anchors between panes, a
  vertical bar spelling each tag one letter a row. The founder (2026-10-31): docks cover the
  room, only authored anchors moving panes, and a dock keeps a strip its edge's whole length; the
  row words asked again ([clarify](drafts/decision-wave-clarify-1.md)).
- The census's nine decisions ([report](../reportbacks/ui-census-RB.md)): Vision takes the
  recommendations of 1 to 8, with the hint fed by one facet that hears the keymap, the View
  Builder's parts moved into its makeover; for 9, the drawn faces lifted from Flow's pen once his
  round ends, its emphasis faces as roles a theme maps, not Flow's own colours (2026-10-29). The
  founder (2026-10-29): the window-run element retired whole (section 3); then "I love what we
  have so far", read by Vision as yes to these leans, to confirm. The founder (2026-10-31): 3, 4,
  6 and 7 yes, Image and Grid kept until superseded; 9 folded into the colour system (section 3);
  1 and 5 asked again ([clarify](drafts/decision-wave-clarify-1.md)); 8 with the View Builder.

- #568's first decision ([report](../reportbacks/accordion-stage-2-RB.md)): no door edits
  `DesktopState` or `InfoPaneState` from outside today (Loom's poke writes scalars, its reset
  wants every field exposed), Vision's lean the intended reach for now, the door a later Loom
  stage (on the sheet). Its other two settled as #568 merged.
- The issues' decisions (the founder, 2026-10-29), to be written on each issue and labelled
  `ready` by the next issue lane: #492 every launch key, `Ctrl+p` among them, selects its surface
  when it is open and not selected and closes it when selected; #493 a press outside ends the
  arranging, a one-pane arranging too; #526 the shipped catalog carries every pane's recipe, the
  Demo pane's none; #533 the 34 `using namespace` lines first, the issue kept open to audit the
  530 aliases later; #535 the maintainer's copy of `quarry/` kept in a Zen folder; #572
  `desk/resolve` walks the paths each owner declares a message leads to, hop by hop, branching
  where an owner declares several, stopping at a loop or a bound, and its answer carries no rule
  for filing an issue (the guide does); #580 a refusal said whole as a notice, beside #548; #583
  `zengine.demo` answers a setup's guidance by message, each pane's office its purpose; #588 the
  one-story tools and the demo service in a demos package, the test-only inputs in their own,
  `lane` and `source` where they are; #543 a pane may change its own settings while it runs,
  limits like `keep` among them, Info's rows over another pane's with a settings pane later;
  Loom #73 retraced first (Loom already scopes a grant to a run, to a Weaver's session and for
  good with `authority revoke`; the console grants only for good), session a new grant's
  default, a grant for one run a later scalpel. With their stages: #494, #495, #503, #518, #519,
  #522 to #525, #534. Written on each issue (2026-10-30).
- The decisions round's questions, answered (the founder, 2026-10-30), for the next issue lane to
  write on their issues: #584 an entry's value decoded by Inventory and answered by message; Loom
  #73 `authority allow` lasts the session by default and `authority trust` stays as it is ("trust
  is earned, allowance is a leash to test it on"). #587, a walk carrying a value from an earlier
  step: yes, its whole scope talked through with the founder first.
- Flow's decisions ([report](../reportbacks/flow-live-requests-RB.md)): 3, a view's message
  declared whole, is section 3's near-roadmap item; 5 was agreed (section 1).

## 6. Filed as issues

GitHub holds these; each issue is written as a small prompt any lane can take. Zengine unless
marked.

- **The UX batch** (2026-10-29, [report](../reportbacks/issue-lane-ux-batch-RB.md), whose table
  maps each draft to its issue): #492 to #566 and Loom #73; 39 `ready`, 16 `needs-decision`, 11
  waiting on a lane, another issue or a reproduction.
- **The ELH audit's findings** (2026-10-29, [report](../reportbacks/issue-lane-elh-audit-RB.md)):
  #569 (taken by #570), #571 to #589 and Loom #76 (taken by #77); grouped by tool, 17 `ready`.
- **Needs a decision:** #117 a UTF-8 path cut at a clipped boundary; #118 a required Windows
  lane under non-ASCII folders; Loom #35 a path-encoding contract for `loom-host` sessions on
  Windows.
- **Ready:** #419 profile the Info and Project entries that dominate the sanitizer's verify.
- **Parked:**
  - #119 a release identity and compatibility promise (BL-ADOPT-02);
  - #120 the workload behind the first performance promise (BL-ADOPT-03);
  - #121 the unused authored UI API, and #122 `frame_in` with resolution (BL-DEF-06);
  - #123 the Builder's field-click evidence (BL-VERIFY-01);
  - #124 the simple external pane as a learning example (BL-WORK-02);
  - #126 pane controls reachable when the room is small (BL-WORK-14);
  - #127 the View Builder zooms (BL-WORK-15);
  - #128 to #135 Inventory: an entry found without walking folders, unused views retired, the
    next hotkey context, a folder deleted with its contents, Back and Forward, several entries
    at once, locked entries kept in place, tags (BL-WORK-18 to BL-WORK-21);
  - #136 a saved command run without a hotkey (BL-WORK-22);
  - #137 Terminal command scripts (BL-WORK-23), with Zenscript's research beside it;
  - #138 parallel work detects publication conflicts (BL-WORK-28);
  - #139 a held agent gesture cancelled (BL-WORK-29, a stage of BL-WORK-38);
  - #140 a native operator's source opened from Flow (BL-WORK-30);
  - #141 row views reused in a long list (BL-WORK-31);
  - #142 Flow's next milestone (BL-WORK-32; the makeover is section 2);
  - #143 canvas text fit with a size floor (BL-WORK-34);
  - #144 maker participants' addressed requests and conditional speech (P-WORK-36);
  - Loom #36 cross-layer public include debt (BL-ARCH-01), and Loom #37 a shape's name owned
    explicitly where vocabularies must coexist (P-LOOM-08).
- **Later:** #145 GitHub from Workshop (BL-ADOPT-04); #146 several Workshop windows
  (BL-WORK-12); #147 Python scripts as participants (BL-WORK-13, paired with the snake's handoff);
  #148 undo through the owners (BL-WORK-33); #149 an app of its own, edited live (BL-WORK-35).

## 7. Directions that govern

- **Never avoid a version bump** (the founder, 2026-11-02): a shape or a file format moves to a
  new version whenever it changes; the migration path is worth the exercise.
- **The goal** (the founder, 2026-10-14): Zen legible, and good to use as a human weaver:
  documentation, then the split, then the UX batch, then complete stories on a well-formed
  architecture.
- **The direction** (2026-10-19): subtract before adding, one owner at a time, decisions before
  prompts. Phase fences are off until Workshop is release-ready.
- **The founder's order**: the UX batch, then the first complete maker story.
- **The principles**: the ability to intuit and learn comes first; systems compose gracefully;
  what is good for human makers is good for agents; source code stays a first-class way to make,
  beside Flow.
- **The roadmap's themes** (each in full in closed_work.md, section 1b):
  1. documentation first: done, its tutorials waiting for the stories;
  2. one owner per job: the later splits take the ownerless seams;
  3. actions, subjects and outcomes described once;
  4. relationships and powers: every loaded row but Inventory is admitted `allow_any`, and
     `SetupApplyRequested` judges no asker;
  5. a subject keeps its identity;
  6. workspaces, perspectives and navigation (UX-08 to UX-11), waiting for the workspace's owner;
  7. two modes for agents; open: what each restricted profile may read;
  8. graphics, components, and data as UI with a presenter;
  9. connected tools: Loaded, Project and Compose researched as one journey;
  10. configuration and personal work, kept apart from shared contributions;
  11. tools, demos and workers: the quarry out of Zengine is fileable now;
  12. execution experiments, later, message cost measured first;
  13. the first complete story, last.
- **Cut from the alpha**: the C++ installer suite, theme presets, plain-language passes beyond
  what the story touches, fast forward's S2 and S4 to S6.
- **Design calls that still govern**:
  - POSIX keys are a compatibility layer patching the defaults, each weave declaring its own;
  - a press is refused only where a new element stands under the hand;
  - a pane too small to be useful is the weaver's choice until it cannot be found or recovered;
  - Notices says only what helps the weaver understand what just happened;
  - a placing ends only at a key or a press;
  - a page's old pictures wait until the page next changes;
  - a floating pane is a whole workspace in a window of its own, and an exported app is code of
    its own;
  - work is done by mouse where it can be, its keys the ideal ones (the Perspectives Lab's rule);
  - a terminal is never made to show every element a window shows: a border, a bar or a look is
    the window's, and the cells' own layout decides how an element reads there (2026-10-30);
  - `component/` knows no medium: a piece is measured there in characters, and its looks, the
    window's and the terminal's, are faces side by side (2026-10-30).

## 8. Loose ends for the next issue sweep

GitHub labels (the founder, 2026-11-03): `parked` goes with no replacement, and `later` with it,
both vague and restrictive; `needs-decision` stays, the honest kind of not ready. Their issues
keep their other labels; better-named labels may come. Prompted in `left-behind-cleared`.

Loom's threading line (the founder, 2026-11-02): `docs/laws/messaging-laws.md` says multi-threaded
dispatch is not built, and nothing may assume it never will, not "a non-feature until a consumer
forces it". The same stance stands twice more: MSG-09 ("neither is planned") and
`docs/reference/known-seams.md` ("Maybe or never").

Filed by the UX batch (2026-10-29, section 6): the guest `ask` row (#536), `fill_laws.sh`
(#537), the `Surface*` shapes (#538), `apply`'s scan (#539), the desk split's cases (#540) and
its close sentence (#541), `three-places.md` (#542), Notices' `keep` (#543), the held drag
(#544), the fixture split (#545), the window-run element (#546), a window's release and text
(#547), a refusal `act` cannot hear (#548), the palette's start line (#549). Taken by its pull
requests: the census's doc gaps (#565), the corpus page (#555). Found settled on `main`: the
census header's `PaintTask`, the notices headers (#430), the build runner's starters, G2's SDK
install, the restore notice (Notices keeps every notice; reasoned).

- Comments and pages still name `judge_content` and `canvas_content_problem`, which exist in
  neither repository, and say one byte a canvas cannot draw refuses a pane's whole picture:
  `builder/builder-pane/pane.cpp`, `introspection/loaded.hpp`, `files/files.cpp` (twice),
  `workshop/pane_text.hpp`'s header, `agents/panes.md`, `agents/decisions/
  a-build-keeps-its-own-words.md`, two cases' comments. #553 mended `drawable`'s alone.
- In the pages' pictures the terminal's Pane Manager covers Info's first column, and the
  smallest window's Notices covers Info (the kit's audit).
- A suite's floor is the fewest cases any configuration compiles (`input`: 62 on Linux, 59 on
  Windows, #591's first run red): `docs/contributing/taking-an-issue.md` says "the measured count"
  without saying on which.
- A loaded weave cannot read its own id (Loom; no owner).
- The desk split's `-s` aborts in nine more assertions, fixed at each case's next change.
- An issue to shorten `neovim_journey`, set aside.
- Doc gaps not located on `main` from these words (2026-10-29): `AGENTS.md`'s floor wording (now
  the sum over four); doctest's `--duration` on WSL's stepped clock.
- The kit: the mutation script could count each mutant's text before building; a probe helper,
  asked twice.
- A rows pane draws its caret whether or not it holds the keys, so with every box shown two
  carets stand at once (Loaded's empty box beside the Terminal's line, #593's picture).
- `story_journey`'s U7, a 0.5 s wait in the tower-defense story driver, ran out on a slow
  MinGW-w64 run (#594's first attempt at `8f40dbf`); green on the rerun.
- Docs against code, from the founder's self-test (2026-10-30): 26 places where a page or a
  comment says one thing and the code another, each with its lines, in
  [drafts/docs-vs-code-2026-10-30.md](drafts/docs-vs-code-2026-10-30.md). The weightiest:
  `messaging.md` calls `Mail::reply` a send back to the sender when it goes only to `reply_to`,
  so README's first snippet replies to no one; the poke pages call reading opt-in when every
  field reads by default; Loom's sessions guide says a package's `asks` where the code reads them
  per tool; the demo setups' page leaves out the two `-machine` packages every setup approves;
  four Zengine pages call the Input weave the sole producer of input, which the SDL window is not.

## 9. Not backlog

These stay trigger-governed horizons or pressure, not owed work:

- inside the built-in Editor: tabs, Vim emulation, syntax highlighting, a VFS, a file watcher, a
  Flow editor (a differently shaped editor arrives as a pane weave instead, P-WORK-07);
- one pane shown several times, and plugin discovery (a pane's free drawing is BL-WORK-46's);
- live artifact replacement before a concrete owner and continuity case;
- general obligation, consensus, metadata or persistence frameworks;
- multithreaded dispatch;
- Windows native containment, or escape-tier security;
- production hardening of the bridge before hosted or remote use;
- a replacement SDL executor for Loom's portable pixel layout.
