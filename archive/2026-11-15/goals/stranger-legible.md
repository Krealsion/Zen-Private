# Stranger-Legible Zen Goal Map

**Status:** PRIVATE LIVE GOAL AUTHORITY  
**Refreshed:** 2026-10-03\
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
uses "weave", "content-id" and "grants" before explaining them (its C ABI version, once v6 where
the code was at v9, is a checked value since Loom #30). Zengine's maker register and a decision
record say "re-floored" without defining it (#81's report, 2026-09-30).  
**Relation:** the public external-reader rule (`docs/contributing/repository-conventions.md`)
already keeps maintainer knowledge out of public documents; this task adds the reader's own
order of learning. BL-ADOPT-01's contributor front door builds on this path.

### Task 2 — No private information; history in its place

**State:** SELECTED 2026-09-25. Zengine's comments meet it (the comment arc, through #67), and
#68 retired the phase codes from its case names, their citations, its messages and its documents
(merged 2026-09-26). Loom's comments and documents followed, as #17 to #23.  
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
- The process as a clock: both repositories' checks refuse its common forms (Zengine #78, Loom
  #29), and Zengine #81 rewords the 19 it found in other words; review catches any further ones.
- History put in words: the checks refuse its narrow told forms ("used to be", "**Retired
  with**"); the rest is review's. Zengine's `docs/reference/workshop-panes.md` § The pane system
  still argues with what retired (the built-in Builder and Info, the terminal overlay, the `p`
  picker, the object canvas), and tells history in three more sentences ("originally", "until it
  became a pane", a change note).

Loom, measured 2026-09-27 at `0839bfc` with Zengine's grammar: 168 phase or private ids in 27
current-facing Markdown files, 224 in comments, and 364 of 1,316 case names carrying a plan code;
several documents describe the maintainers' workspace and process. Loom's phase takes all of it
(`prompts/loom-comments-and-documents.md`).

### Task 3 — An audit of executor habits and process

**State:** DONE 2026-09-30, as executor optimization. The audit
(`prompts/executor-optimization.md`) was answered and applied, with values that move with the
code and a documentation-only lane, as Loom #29 and #30 and Zengine #78 and #79, and closed by its
clean-up, Zengine #80 (`prompts/executor-optimization-cleanup.md`); all merged 2026-09-30.  
**Why it touches this goal:** much of what Tasks 1 and 2 remove was written by habit: phase ids
cited as explanation, a paragraph per phase appended to `tests/test_population.txt` (157 KB
before the comment arc, 6 KB now), essays atop headers. If the habits stay, keeping these tasks
true means cleaning up forever.  
**Scope (the founder, 2026-09-29):** both habits, what the executor writes into the
repositories, and process, how a phase runs from the prompt to the merge.

### Task 4 — The weaver rename and a panel audit

**State:** DONE 2026-09-29. The person is a weaver in both repositories (Loom #27, Zengine #75,
`prompts/weaver-rename.md`). Workshop's internals say `pane` where they said `panel` (Zengine #77,
`prompts/panel-audit.md` and its continuation): `panel` named nothing `pane` does not, and it is
left only as plain English and in retired spellings a case forbids. `pane` stays the public word.  
**Loom's Weaver, as the founder states it (2026-09-26):** the person's representation inside a
system, an authority key (`zen/weaver/weaver.hpp`, `docs/reference/weaver.md`). A host holds one
weaver, for the person who started or owns it, to give programs authority; other weavers can be
reached by message. Calling the person `weaver` names that same entity, so the rename inherits
Loom's meaning. The person and `loom::Weaver` share the word, as a user and a `User` record do;
only a sentence about authority or trust says which it means (the founder, 2026-09-29).

**Relation:** one noun per concept is part of reading plainly (Task 1).

### Task 5 — One word for a pane on or off the desk

**State:** OPEN — before a release (the founder, 2026-10-01).
Zengine #83 names the act: a weaver hides a pane ("hide pane", "hide X") and shows it ("show X").
The state still says `closed` and `open`: the pane-state classifier's word, the Pane Manager's
`[open]` mark, Info's subject rows ("closed -- show it from the Pane Manager"), Attention's
conditions, law WL-PANE and the setup guides. The state takes the act's word, so a reader meets
one word for one thing. Action and shape ids stay, as `manage.remove` did.
**Evidence:** [the words report](../../../../reportbacks/pane-menu-words-RB.md#pressure-exposed).

### Task 6 — The tool explains its own words

**State:** OPEN — before a release (the founder, 2026-10-02).
A developer tool can teach the jargon it uses. Wherever Workshop shows a term or a thing (a fold,
a form, an accumulator, an office, a grant), a short description is one gesture away, where it
appears, so a weaver learns the word from the tool rather than from a search engine. The fold
(Zengine #84) raised it: its name is the functional-programming term, and today its description
is reached only through discovery.
**Relation:** Task 1 (a plain first-read path) and Task 4 (one noun per concept). A pane's `?`
guide and its tutorial mode serve it (`private/backlog.md`, BL-WORK-09).

### Task 7 — A change path, for whoever makes or reviews a change

**State:** OPEN — for the documentation rewrite the founder wants (2026-10-05); not placed  
**Owed:** Beside the stranger's first read (Task 1), a path for a change: for each kind of change
(a new pane, a new message, a shape change, a law), the smallest set of pages and files enough to
make or review it. Its centre is one page of the patterns a change meets -- ask and answer, trial
then commit, belt and take-back, guards against a stale answer, kept-until, judging after the
write -- each with a short example and the timeline of its messages. The laws stay the reference
behind it, not the way in.  
**Source:** the founder's deep reviewer on reviewing Loom code (2026-10-05): Loom gives a review
strong tools, and the cost is reconstructing a conversation across files and finding the smallest
sufficient reading path; compact examples, reusable request-and-recovery patterns and readable
message timelines would make a correct operation cheaper to recognize.  
**Relation:** Task 1; BL-ARCH-02 (current law stays bounded); BL-WORK-24's message timelines, which
can illustrate the patterns.

## 3. Order

The founder's order (2026-09-26):

1. Phase codes retired from Zengine (Task 2): `prompts/zengine-phase-code-retirement.md`, merged
   as #68, then its repairs: `prompts/zengine-phase-code-repairs.md`, merged as #69. Before
   step 2, off this goal: `prompts/zengine-witness-restoration.md` gives the four law clauses
   #69's trace found unwitnessed a case each again, merged as #70.
2. `ui/`'s two installed headers read as public documentation: `prompts/zengine-ui-headers.md`,
   #71.
3. Loom's comment phase, with its documents: `prompts/loom-comments-and-documents.md`, in seven
   stages, merged as #17 to #23.
4. The weaver rename and the panel audit (Task 4): the rename is `prompts/weaver-rename.md`,
   merged as Loom #27 and Zengine #75; the panel audit is `prompts/panel-audit.md`, applied as
   Zengine #77. Before it, off this goal, `prompts/tool-audit.md` took finished passes' tools out
   of both repositories, merged as Loom #28 and Zengine #76.
5. The executor audit (Task 3): `prompts/executor-optimization.md`, applied by its continuation
   and closed by its clean-up (Zengine #80).
6. Zengine's last process words (Task 2), the documentation lane's first live run:
   `prompts/zengine-process-words.md`.

Task 1's first-read path and Task 7's change path are not yet placed; they meet in the
documentation rewrite the founder wants, whose direction he gave on 2026-10-09: a man page on each
weave, a tutorial for each step, and folders by feature
([BL-ADOPT-05](../history/closed_work.md#bl-adopt-05--the-documentation-overhaul-a-man-page-on-each-weave-a-tutorial-for-each-step)).
Tasks 5 and 6 land before a release.
