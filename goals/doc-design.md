# The documentation's design

A goal of *readability* on the [roadmap](../roadmap.md); how this file works:
[README](README.md).

Done when (the founder, 2026-11-19):

- [x] the design settled with the founder: its principles, its readers and their questions, one
  owner for each answer, the comment and page rules, the required path
  (`Zen/documentation-design.md`, the fourth pass, 2026-11-19)
- [x] researched, read-only (2026-11-19, `reportbacks/doc-design-research-RB.md`): each reader's
  questions traced to where their answers live today, what is said more than once, what is loaded
  unasked, and the executor constitution sorted into public, generic and private
- [x] tried: one folder rewritten to the design on a scratch branch, and a cold reader's task on it
  compared with the same task on today's text (2026-11-19, `reportbacks/doc-design-trial-RB.md`)
- [x] distilled: the design published in each repository's contributor pages, the guide all new
  text is written with (2026-11-20: Loom's `docs/contributing/documentation-design.md`, linked
  from both guides)
- [ ] the rewrite planned in three passes, a slice at a time, each slice measured by kind against
  its start; smaller encouraged, never forced (the founder, 2026-11-19)

Tasks:

- [x] the third pass, looked at by the founder and taken to the trial (2026-11-19)
- [x] the trial (stage 3), `prompts/doc-design-trial.md`, run and reviewed 2026-11-19
- [x] the cold reader's setup archived for later exceptions, out of `Zen/.claude/agents/`:
  `pass-tools/cold-reader/` (2026-11-19)
- [x] the fourth pass: what the trial taught, with the founder's answers (2026-11-19)
- [x] stage 4's prompt, written 2026-11-19: `prompts/unrun/doc-design-publish.md`, cold, for the
  laptop, after #178 merges. Loom's pull request (the design as a contributor page, its
  standards, the start file, the recommended setup, the six-line limit paused, the census on code
  lines) merges first; then Zengine's (the guide, the start file, the glossary, the checks in two
  kinds, `folder_map` and `law_register` holding both shapes) with `timer/` converted from the
  trial's record
- [x] stage 4 run (`prompts/doc-design-publish.md`) and reviewed 2026-11-20: Loom #39 and
  Zengine #181, green; the founder's calls as Ceecee chose (a census row keeps its class below
  the threshold; the second pass's marks in `Zen/pass-tools/`)
- [x] the review's fixes, `prompts/doc-design-publish-fixes.md`, run and reviewed 2026-11-20:
  "More lanes" into `build-and-test.md`; the recommended setup only for choosing a setup, its
  practices stated in Loom's guide and listed in best practices; small faults. Filed with stage 4
  (`reportbacks/doc-design-publish-RB.md`)
- [x] the founder merges Loom #39 (`beb74e2`), then Zengine #181 (`75987b6`), 2026-11-20
- [x] `Zen/documentation-design.md` trimmed to what is private (the dated decisions, the
  baseline, the stages and passes), linking Loom's page (2026-11-20)
- [ ] the first pass's folders in an order, from stage 4's report

Open, each with Vision's lean:

1. The first pass's second folder: one heavy with the agent layer, part of `workshop/` for
   example, where the duplication is. Lean: yes, decided from stage 4's measures.

Decided (the founder, 2026-11-19), on the research's thirteen decisions:

- As Vision leaned: 1 (the shrink is counted over the pages), 2 (a rule about one declaration in
  its comment; a rule across files a numbered law on a public page; the proof lists a manifest;
  the methods reference), 3 (one front page a folder), 4 (`AGENTS.md` a short start file, tested
  in the trial), 5 (Loom owns the shared half), 6 (a label may stay a noun phrase; what explains,
  warns or forbids is a sentence), 8 (the standards and checks change at publication), 11 (the
  recommended setup in Loom's contributor pages, naming kinds of machine), 12 (`timer/` for the
  trial), 13 (the design binds what the program says, test names, and lightly commits and
  issues).
- 7: the design teaches its comment rule with a worked example, good and bad comments and why:
  one built for it, or the hardest and most comment-worthy real passage with its comments as they
  stand, why they are so, and why other ways would be worse.
- 9: a second copy only where a check holds it equal, for now; the founder would rather a manual
  drew from its owner directly, or a check held the two matched.
- 10: frozen history stays, in an area of its own whose README says why it exists and how it is
  counted.
- The executor constitution's section f: done, a research session pushes nothing to Loom or
  Zengine.
- The cold reader (the founder, 2026-11-19): a cheap reader (Sonnet, low effort, reading only)
  asked what a passage says, before and after, and as a self-audit, in part or whole; Ceecee
  decides when and how much, and what the answers mean; tokens counted where shown. Rule 11's
  exception is stated in the prompt itself: the rule, its home, that it does not hold for the
  session, and the rules for the reader's use.

Decided (the founder, 2026-11-19), on the trial's five decisions:

- 1: a rule spans files when other files rely on it, so TIMER-05 stays a law.
- 2: "input actor" for the hand that presses and types; "room" gets no proper name, and each use
  says what it means, laws included (the Vision constitution's two done).
- 3: the shrink is a goal, never a requirement: "as long as it does its job better, I will
  consider that a win"; clear and small encouraged, not forced.
- 4: no `CLAUDE.md`; Claude Code reads `AGENTS.md` where none stands (since v2.1.277).
- 5: the checks that only cap size pause during the rewrite, so the text can be reshaped freely;
  the checks that catch a mistake stay; the census counts code lines only.
- The rewrite in three passes: readable with one owner for each fact (a comment there only
  because a name is poor is marked, for the second pass); names (the language pass); compression
  and order, ideas building on one another.
- Accepted as Ceecee made them: the worked example on a real passage, `timer-binding.md` merged
  into `timed-weaves.md`, the glossary at `docs/glossary.md`.

Records: the founder's direction of 2026-11-19 (complete sentences, a comment earned, agent and
human pages merged without bloat, the executor constitution made a public contributor's guide;
smaller encouraged, never forced); the survey's numbers, in the design's "Today"; the trial's
record, `reportbacks/doc-design-trial/`.
