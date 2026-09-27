# Stranger-Legible Zen Goal Map

**Status:** PRIVATE LIVE GOAL AUTHORITY  
**Refreshed:** 2026-09-26\
**Strategic authority:** `private/zen-strategic-map.md`, Goal 2  
**Role:** Goal 2's selected tasks: what a stranger must be able to read, and how it stays true

This map is forward-looking. Reports and Git retain phase history.

## 1. The goal

A stranger opens a public Zen repository (Loom or Zengine) and can read it. The stranger has
ordinary programming knowledge and nothing else: not the maintainers' vocabulary, process,
history, machines or private files.

The founder's words (2026-09-25): the repository must become, and stay, plainly readable by a
stranger on its first-read user path, using no privileged knowledge; everything must apply to
the user's available knowledge alone. No private information belongs in documents or comments.
History belongs in the documents kept for it and in Git's version history, not in endless
comment bloat.

## 2. Tasks

### Task 1 — A plain first-read path

**State:** SELECTED 2026-09-25; no phase yet  
**Owed:** Each public repository names its first-read path: the pages and files a new user
reads, in order, starting at the README. Every step on it uses only what the reader knows at
that point: ordinary programming knowledge and what earlier steps said. A term is explained
before it is used; nothing leans on the maintainers' vocabulary, process or history.  
**Done when:** a cold reader who knows nothing of Zen walks each path end to end and meets no
term before its explanation and no step that needs knowledge the path did not give.  
**Kept true by:** judging every change to a page on the path against the path, and a new cold
walk at thresholds: before outside contributors are invited (BL-ADOPT-01), at a first release
identity (BL-ADOPT-02), and after a large change to the path.  
**Position (2026-09-25):** neither repository names its path. Zengine's README explains a weave
in its first paragraph and sends library users and makers through separate doors. Loom's README
uses "weave", "content-id" and "grants" before explaining them, and states the kernel's C ABI as
v6 where the code is at v9.  
**Relation:** the public external-reader rule (`docs/contributing/repository-conventions.md`)
already keeps maintainer knowledge out of public documents; this task adds the reader's own
order of learning. BL-ADOPT-01's contributor front door builds on this path.

### Task 2 — No private information; history in its place

**State:** SELECTED 2026-09-25. Zengine's comments meet it (the comment arc, through #67), and
#68 retired the phase codes from its case names, their citations, its messages and its documents
(merged 2026-09-26). Loom's comments are next (BL-ARCH-03).  
**Owed:** No current-facing document or comment in either repository carries private
information: a development-phase name or private id used as explanation; a reference to the
private repository, the reports, the workspace or a maintainer's machine; or the development
process's own roles. History lives in Git's version history and in the documents designated as
history (each repository's `docs/history/`), never in comments or in current-facing text.  
**Done when:** both repositories hold this on their official lanes, so a regression is red:
`source_comments` does for Zengine's comments, `doc_links` for paths outside a repository, and
with #68 `law_register` for a plan code in a case name or a phase id in a current-facing
Markdown file.  
**Position (2026-09-26, Zengine main at #68's merge):** no case name carries a plan code, a law
id a case name opens with is declared, and no current-facing Markdown file names a phase id.
#69 (`prompts/zengine-phase-code-repairs.md`, merged 2026-09-26) closed what #68's
review found: every case a document cites resolves, no case name opens with a bare letter or
number, "this phase" is gone (MW-DEF-07 reworded with the founder's approval), and every law id a
C/C++ comment names is declared. `law_register` holds all but "this phase", which is words.

What remains:
- "Phase" as the development process's clock stands in about 45 places, most in the method
  registers and decision records ("a phase that adds cases raises the floor"); several point at
  "the phase records, kept outside this repository", and one law does (VM-WIT-24).
- The finished mass-edit tools under `tools/` quote codes in strings and comments; no check
  reads `tools/`.
- History put in words ("the new rows", "re-homed") passes any id check (Task 3).

Loom, measured 2026-09-27 at `0839bfc` with Zengine's grammar: 168 phase or private ids in 27
current-facing Markdown files, 224 in comments, and 364 of 1,316 case names carrying a plan code;
several documents describe the maintainers' workspace and process. Loom's phase takes all of it
(`prompts/loom-comments-and-documents.md`).

### Task 3 — An audit of executor habits and process

**State:** CANDIDATE, soon. The founder, 2026-09-25: an audit pass on overall executor habits
and process "may be in order soon".  
**Why it touches this goal:** much of what Tasks 1 and 2 remove was written by habit: phase ids
cited as explanation, a paragraph per phase appended to `tests/test_population.txt` (157 KB of
comments over 54 entries), essays atop headers. If the habits stay, keeping these tasks true
means cleaning up forever.  
**Scope:** the founder's to set when it is selected; this map records only its link to Goal 2.

### Task 4 — The weaver rename and a panel audit

**State:** SELECTED 2026-09-26, last in the order below; no prompt yet  
**Owed:**
- `maker` becomes `weaver` wherever it names the person; `maker` keeps one meaning, the maker
  library (`maker/`, `zengine::maker`, the MW registers under `agents/maker/`). The founder
  expects mostly comments and prose: where code names the person, it names that same entity.
  Zengine is built on Loom and inherits its terminology. A true conflict is brought up, not
  resolved in passing.
- The `panel` references are audited for fit. `pane` stays the public word: the founder dropped
  `pane` to `panel` on 2026-09-26, since 86 schema names and the published pane protocol would
  have moved with it. Internals still say `panel` (`PanelKind`, `panels.selected`,
  `panel::kLayouts`); each use that no longer names what it means is reported with a proposed
  name.
- The five installed `maker/` headers whose openings run 18 to 36 lines (`weave`, `succession`,
  `definition`, `write`, `vocabulary`) are read for restatement against their reference pages
  while the rename rewrites them (BL-ARCH-04; the founder, 2026-09-27).

**Scale (2026-09-26, current-facing text and identifiers):** Zengine says `maker(s)` 3,670 times
in 441 files and `panel(s)` 2,748 times, with 544 identifiers built on `panel`; Loom says
`maker(s)` 94 times in 43 files and `panel(s)` 8 times.  
**Loom's Weaver, as the founder states it (2026-09-26):** the person's representation inside a
system, an authority key (`zen/weaver/weaver.hpp`, `docs/reference/weaver.md`). A host holds one
weaver, for the person who started or owns it, to give programs authority; other weavers can be
reached by message. Calling the person `weaver` names that same entity, so the rename inherits
Loom's meaning.

**Relation:** one noun per concept is part of reading plainly (Task 1).

## 3. Order

The founder's order (2026-09-26):

1. Phase codes retired from Zengine (Task 2): `prompts/zengine-phase-code-retirement.md`, merged
   as #68, then its repairs: `prompts/zengine-phase-code-repairs.md`, merged as #69. Before
   step 2, off this goal: `prompts/zengine-witness-restoration.md` gives the four law clauses
   #69's trace found unwitnessed a case each again, merged as #70.
2. `ui/`'s two installed headers read as public documentation (`private/backlog.md`,
   BL-ARCH-04): `prompts/zengine-ui-headers.md`, #71.
3. Loom's comment phase, with its documents (`private/backlog.md`, BL-ARCH-03):
   `prompts/loom-comments-and-documents.md`, in seven stages.
4. The weaver rename and the panel audit (Task 4).

Task 1's first-read path and Task 3's audit are not yet placed.
