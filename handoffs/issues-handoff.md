# Handoff to deep review: Zen's bounded work moves to GitHub issues

From the founder (Krealsion), 2026-10-09. Written by Vision. Given beside it: `backlog.md` and
`pressure.md`, the founder's private plans, which hold most of the items named below.

## Why

Zen now moves in two lanes:

- **Phases**: the large architectural arcs, prompted, built, reported and reviewed one stage at a
  time, as today. They stay in the private plans.
- **Issues**: bounded work, on GitHub, so it leaves everyone's context until it is taken. Any
  executor takes one issue, ships it as its own pull request (`Fixes #n`), and it merges when its
  hosted run is green and it is reviewed.

An issue's pull request merges first. An open phase branch rebases onto it. So an issue is written
small enough to merge ahead of any phase.

## What to file now

Check each item against current `main` before filing it: Zengine `cd444d3` (#102 merged), Loom
`b664311`. Drop one already fixed, and say so in your list.

**1. Bounded fixes**, labelled by kind, and `ready` once you have verified them:

Zengine:
- Two panes claim front order 3: `toolbox_fixture`'s view row claims rank 3 on the `values` desk,
  already full at ranks 0 to 3 since every shipped desk gained Layouts, so Workshop's reader refuses
  it (`two panes claim front order 3`). (`defect`)
- `docs/workshop/images/editor-materials-restored.png` shows a path on the founder's machine in its
  Editor and Files rows. Crop or capture it again. Do not repeat the path in the issue. (`docs`)
- `agents/workshop/press-chain.md` cites a case under `tests/test_workshop_screen.cpp` that lives
  in `tests/test_workshop_panes_window.cpp`. (`docs`)
- `docs/workshop/panes.md` says hidden titles last "for the current run", but
  `workshop/prefs_persist.hpp` saves them. (`docs`)
- On Windows before Python 3.15, `tests/session/demo_recipes.py` and
  `tests/session/workshop_journey.py` read a child program's output in the ANSI code page, so
  beneath a `%TEMP%` named beyond ASCII their path checks fail. (`test`)
- `docs/contributing/build-and-test.md`'s installed-package witness steps leave out runs the
  witness makes: `witness-pane-menu`, `witness-pane-settings`, the message drafts and the Flow
  programs. (`docs`)
- Which tools build in a folder named beyond ASCII is written nowhere: Ninja does, MinGW Makefiles
  and MSYS2's ccache do not, and the Loom prefix must sit in a folder `ld` can spell. Owner:
  `docs/contributing/supported-toolchains.md`. (`docs`)
- The legacy import reads a file of at most 1 MiB, below a legal session (`kMaxSessionBytes`,
  2,654,208 bytes). Owner: `user_paths.hpp`. (`defect`)
- Info's register is at 16,280 of 16,384 bytes (`editor.md` 15,957, `opening.md` 15,657): split it
  before its next change. (`docs`)
- From the plans: P-BUILD-05, P-BUILD-06, P-BUILD-07, P-WORK-17, P-WORK-21 and BL-DEF-06.

Loom:
- Loom does not install `kMaxDecodedCells`, so a consumer names the decode budget in prose and
  proves it by a round trip. (`defect`)
- From the plans: P-LOOM-06. (`docs`)

**2. Needs a decision**, labelled `needs-decision`, never `ready`:

- A path cut inside a letter. The notice row (`detail::fit`, a byte cut by law WL-TEXT-05) and
  `fit_path` (the `setup:` slot and the project line) can cut a letter beyond ASCII in half. The
  canvas carrying it fails, and the screen keeps its last picture until the text changes. Options:
  the cut steps back to a whole letter; the rows are spelled to ASCII before the cut, as a pane's
  rows are; or it waits for text beyond ASCII to be drawn properly. (Zengine)
- A required CI build in a folder named beyond ASCII. It waits on the item above and the next one.
  (Zengine)
- `loom-host` carries no UTF-8 code page on Windows: `loom-host --serve` on a folder beneath a name
  beyond ASCII ends at `Illegal byte sequence`. Zengine's programs take theirs from
  `cmake/ZengineCodePage.cmake`. (Loom)

**3. Parked and later ideas**, labelled `parked` or `later`, never `ready`: each in plain words,
with the scope the founder decided and its wake condition.

- `parked`: BL-WORK-02, 03, 14, 15, 18, 19, 20, 21, 22, 23, 28, 29, 30, 31, 32 and 34; BL-VERIFY-01;
  BL-ADOPT-02 and 03; BL-ARCH-01; P-WORK-36. In Loom: P-LOOM-08.
- `later`: BL-WORK-12, 13, 33 and 35; BL-ADOPT-04.

**Not filed**: they stay in the private plans and move by phases. The ordered arcs (BL-WORK-36,
38, 09, 16, 17, 10, 11, 26 and 27), the research items (BL-WORK-37 and 39), BL-WORK-01, 25,
BL-ADOPT-01, BL-ARCH-02, every `WATCH` note in `pressure.md`, and the rest of its items (arcs,
seeds, partly delivered).

## The form of an issue

An issue is a small prompt. Whoever takes it acts on it alone.

- **Title**: the outcome, in one line.
- **What is wrong** (or wanted), plainly.
- **Done when**: the outcome, and a test that fails before the change and passes after it.
- **Fences**, binding:
  - Loom, not host code: a change that adds C++ inside a host where a weave or an operator could do
    the work is the wrong change.
  - Nothing changes beyond the outcome.
  - No AI attribution in commits or pull request text. The repository's attribution check refuses
    it.
- **Checked against**: the `main` commit you verified it on.
- **Plan ID**, last line, when it has one (`Plan ID: P-BUILD-05`), so the plans can point at the
  issue.

Labels: one kind (`defect`, `docs`, `test`, `ci`) and one state (`ready`, `needs-decision`,
`parked`, `later`). Create any that are missing. Executors take only `ready` issues.

## Both repositories are public

- No path on the founder's machine, no private file names (`Zen/...`, report names), no people's
  or AI sessions' names, no AI attribution, and nothing from the private plans beyond the work
  itself.
- **A security defect is never a public issue.** Anything that lets someone do what they should not
  goes into a draft private security advisory instead: the repository's Security tab, Advisories,
  New draft security advisory. If you cannot create one, list it for the founder.

## From now on

A finding of yours outside the pull request under review becomes an issue in this form, or an
advisory. A finding in the pull request under review comes back to the founder as today.

## When you are done

Send the founder one list: each issue filed (number, title, labels), each advisory drafted, and each
item not filed and why.
