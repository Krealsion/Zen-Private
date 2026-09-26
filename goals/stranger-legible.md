# Stranger-Legible Zen Goal Map

**Status:** PRIVATE LIVE GOAL AUTHORITY  
**Refreshed:** 2026-09-25\
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

**State:** SELECTED 2026-09-25; underway for Zengine's comments through the comment arc
(BL-ARCH-03)  
**Owed:** No current-facing document or comment in either repository carries private
information: a development-phase name or private id used as explanation; a reference to the
private repository, the reports, the workspace or a maintainer's machine; or the development
process's own roles. History lives in Git's version history and in the documents designated as
history (each repository's `docs/history/`), never in comments or in current-facing text.  
**Done when:** both repositories hold this on their official lanes, so a regression is red, as
`source_comments` already makes it for Zengine's comments and `doc_links` for paths outside a
repository.  
**Position (2026-09-25, counted with the source-comment check's id rule, public law families
excluded):** Zengine's current-facing Markdown carries 952 phase-shaped ids, 912 of them under
`agents/` and 34 in `docs/reference/`. Loom's carries 183, most in `docs/reference/` (75) and
its top-level `docs/` pages (42). Zengine's `workshop/` and package comments are held by the
check; its tests phase is prepared (`prompts/zengine-test-comment-compression.md`); Loom's
comments come last in the arc.

### Task 3 — An audit of executor habits and process

**State:** CANDIDATE, soon. The founder, 2026-09-25: an audit pass on overall executor habits
and process "may be in order soon".  
**Why it touches this goal:** much of what Tasks 1 and 2 remove was written by habit: phase ids
cited as explanation, a paragraph per phase appended to `tests/test_population.txt` (157 KB of
comments over 54 entries), essays atop headers. If the habits stay, keeping these tasks true
means cleaning up forever.  
**Scope:** the founder's to set when it is selected; this map records only its link to Goal 2.

## 3. Order

Only the comment arc is running. The founder selects the next prompt for each task.
