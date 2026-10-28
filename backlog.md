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

## 1. Now: the wave

Four lanes run at once on three build slots: two work slots at 8 jobs, one final slot at 4
(constitution section f). WSL has 48 GB.

- **Main lane: the desk, round 2**, merged ([report](../reportbacks/desk-round-2-RB.md)): #467 the
  review's three fixes, #469 Start here's step 4 and the way in (the dependencies page), #470 the
  Pane Manager by name, #472 the quit box (2026-10-28); `main` green after them and #471, every job
  of each merge's run. Not built: the Hotkeys pane in accordions, no room; a pane's own top right
  waits for the picture tool (section 3). Next, Flow made over
  ([report](../reportbacks/flow-made-over-RB.md), `d2a315de` on `flow/made-over`, not pushed):
  close to the mockup; the founder works on it live, reloading Flow in place (2026-10-28), from
  fourteen requests in four batches ([requests](../prompts/unrun/flow-live-requests.md), hot):
  his notes (autocomplete, moving When and Then, deselecting, double clicks, one typed constant
  box) and Vision's. Later, with accordions (BL-WORK-16):
  the docks narrowed to tags that open on hover with their names and connectors.
- **Issue lane: the repository's own mutants**, merged (#471, fixing #468). Its follow-up, reviewed
  ([report](../reportbacks/issue-lane-mutants-follow-up-RB.md)): #473 the corpus level with `main`,
  then #475 the 30 survivors settled (13 by stronger cases, 9 corrected, 8 dropped with their
  reasons), both green; to merge in that order. Filed: #474 (a stale comment in the Inventory
  pane); the weekly run's own issue #476, closed once a run after the merges is green. Next, the UX
  batch filed from [ux-batch.md](ux-batch.md) and the ideas, leaving out what the desk's round 2
  took, with its housekeeping: #474, the four second guards, the weekly run once more and #476
  closed, the corpus page's two gaps. Two leftovers for it: the View Builder still says `<action>
  complete` (WL-NOTE-06), and the quick setup in a package names pages the package does not carry.
  With the batch it files the split of `tests/workshop_support.hpp` as an issue (BL-WORK-44; the
  founder, 2026-10-28).
- **View Builder lane** (not started, [prompt](../prompts/unrun/lane-view-builder.md)): a Discard
  button; the kinds below Grid; widening grows the canvas alone; then Project scrolls, Loaded
  searches, Compose shows a message's fields.
- **Accordion lane**, researched ([report](../reportbacks/accordion-research-RB.md), reviewed):
  one idea at both levels. In a pane, a shared piece in `component/`, a part's fold the pane's
  setting and a content fold its state; on the desk, a pane shut to its title and docks on an
  edge, as `workshop.fold` and `workshop.dock` in the pane's row. First stage: Files' places with
  the Hotkeys pane; then Info's tree, the desk in three stages, Flow's tags. Eight decisions
  (section 5).
- **Text lane** (not started, [prompt](../prompts/unrun/lane-text-input.md)): the Terminal's Enter
  and Shift+Enter; Files' paths centre-truncated; the Editor's right-press menu.
- **The kit's compile gate** ([report](../reportbacks/kit-build-memory-RB.md)): a work slot's
  compiles held to a budget, so all three slots run at once (22.8 GB of 47 at 10 GB). Next, the
  founder's calls of 2026-10-28 ([prompt](../prompts/kit-gate-budget.md), running): 12 GB
  a work slot, and the official and sanitizer trees each learning their own peaks. Then the
  picture tool (the founder, 2026-10-28): a page's pictures retaken from a recorded walk, each
  with its recipe beside it (`witness.sh picture`, desk round 2's recommendation).

## 2. Next, in order

1. **Flow made over** (BL-WORK-32), its prompt written (2026-10-28, section 1). The clickable
   [mockup](https://claude.ai/artifact/JxK1MLFeeSmQh2GgD3v4jY): When, Do and Then kept as colour
   with more room to Do; the rule read as a sentence; a Next line in place of Run's refusals; a
   nine-stop tour. The founder's calls (2026-10-27): a press may change several things, and
   several messages may change one field; each node listens only to its own message and
   condition, so pressing `+` computes no divide; a gear for settings. Quicksort needs a branch
   form (only the chosen side computed) and list operators. Start here's moves for steps 2 and 3
   wait on it. Zengine #142 holds the older milestone question.
2. **The operator suite** (BL-WORK-48), which Flow's calculator runs on. Today: five Int
   primitives (`operator/primitives.hpp`). To add:
   - Math: subtract, multiply, divide and remainder (both refusing 0), negate, abs, min; square
     root and logs, which want Float beside Int;
   - comparators: equal, not equal, less or equal, greater, greater or equal;
   - Logic: and, or, not;
   - later: Lists, with the quicksort; Text after.
3. **The UX batch**, filed by the issue lane (above), then **the first complete maker story**
   (theme 13, section 7).

## 3. Decided, not yet ordered

Each starts on the founder's word; "wake" is what must be true first.

- **A pane's own top right** (desk round 2's parked item): close and move, a gear, a box around
  each icon, the arrange markers on boxes of their own, "remove from the setup"; about 116 page
  pictures retaken with it. Wake: the kit's picture tool (the founder, 2026-10-28).
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
- **Untrusted code, the WASM tier** (stage 1 merged, Loom #72). Left: S2 to S5 (a box's own
  doors, its lines on standard error, `containment_note` on boxes) and ASan beside Wasmtime. An
  agent without a shell waits on this and on tools by reach.
- **The MCP adapter's live check** through the app, and the weaver case on package 0.1.3. Wake: a
  lane left empty.
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
- **The drawing door grows one kind at a time** (BL-WORK-37; stages 1 to 7 merged): ovals,
  polygons, images, shaders and whole widgets, as consumers ask.
- **The census's remainder** (BL-WORK-45): the mirrors (Attention, Connections, Info's
  properties, Introspection) become data-form views.
- **Night Lab, era 2** (BL-LAB-01): held, top-down; its findings go through the founder to Vision.
- **The local lane** (BL-LANE-01): shelved while the founder weighs where the agents run.

## 5. Waiting on the founder

- `v0.1.0`'s fixed colours: take them, or send them to the settings phase.
- `authority pending`: a grammar change, only if he wants one.
- The Demo pane's development recipe: Vision's lean is none.
- Show me opening over Start here, covering its words: Vision's read is to leave it.
- The graphics research's round 2, decisions 2 (a group is a layer) and 10 (its eleven seams
  filed as issues).
- Where the desk's 3a and 3b (BL-WORK-38) and fast forward (BL-WORK-43) fall in the direction.
- The reports' 126 open decisions, to bring in small batches
  ([report](../reportbacks/reports-open-items-RB.md)); none brought yet.
- Whether to rotate the SSH key a test canary read in BL-WORK-38's stage 1.
- Where the local lane's agents run (BL-LANE-01).
- The accordion research's eight decisions: Vision takes seven of its recommendations (docks
  taking room, the two row words, the bar's length one setting, the piece in `component/`, Info a
  tree after the first stage, Files' places with the Hotkeys pane first, a pane shut where it
  stands); "two-sided" is the founder's to say: several panes in one dock, or a bar between two.
- The four second guards no case can tell from the first (#475's choice 6: `drawable` in the
  Hotkeys file row and in Attention, Files' emit list, the Terminal's wait for its row): Vision's
  lean is to keep them, each saying the host behaviour it guards against.
- #474's labels: Vision's lean is `docs` and `ready`.

## 6. Filed as issues

GitHub holds these; each issue is written as a small prompt any lane can take. Zengine unless
marked.

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
  - work is done by mouse where it can be, its keys the ideal ones (the Perspectives Lab's rule).

## 8. Loose ends for the next issue sweep

- A guest row with `"admit": "ask"` parks its connection for good (`GuestDoor::decide` has no
  caller): a defect to file.
- `tools/fill_laws.sh` is not idempotent on `main`: an issue to file.
- Eight graphics shapes are still named `Surface*`.
- A window's release and text are refused on the bus by owners that take neither (an app's
  views, the snake).
- A refusal an owner says in its answer carries no press, so `act` cannot hear it.
- A loaded weave cannot read its own id (Loom; no owner).
- The manuals' pictures show the old desk; in the pages' pictures the terminal's Pane Manager
  covers Info's first column, and the smallest window's Notices covers Info.
- The palette's start line is cut at its right edge.
- `apply` finds each said record by a scan (bounded at 1,024).
- `main`'s hosted entries ran longer at `1c470497` than #419 recorded, untraced: readers still
  solve the whole desk for one pane (with #419).
- The desk split's leftovers: an `-s` abort in nine more assertions, fixed at each case's next
  change; a reload not witnessed live; the held-row gate cased for 2 of 8 panes; a toggle judging
  a stale copy while a close is in flight, not cased; a close's sentence with two composers;
  `agents/decisions/three-places.md` still names `close_pane`.
- Notices: the record's two headers route their law to `attention.md`; whether a pane edits
  `keep`.
- The restore notice is replaced at once by Inventory's startup note (no owner).
- `tests/census_headers.hpp:242` still says `PaintTask v1`.
- The app export's doc gaps: the build runner counts two process starters (the launcher makes
  three); `docs/contributing/taking-an-issue.md` should name `tests/census_headers.hpp`;
  `builder/run.hpp`'s claim of one starter is stale.
- Whether G2's stage 8 settled the SDK install carrying no OS window.
- An issue to shorten `neovim_journey`, set aside.
- Doc gaps: `AGENTS.md`'s floor wording (now the sum over four); doctest's `--duration` on WSL's
  stepped clock.
- The kit: the mutation script could count each mutant's text before building; a probe helper,
  asked twice.
- The corpus's front page (`tests/mutants/README.md`): a hunk's context lines name the function
  its entry names (two survivors were anchored in the wrong one), and how to probe a survivor.
- A held drag in the desk's arrangement says `moved <pane>: ...` at each motion, against
  WL-NOTE-06 (desk round 2, picture 08): a defect to file.

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
