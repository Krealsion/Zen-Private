# Handoff: the stranger -- reading Zen as a newcomer, and checking what you understood

From the founder (Krealsion), 2026-10-23. Written by Vision for a fresh session. Nothing below
replaces reading the pages themselves.

## 1. The role

- **You read Zengine and Loom as a stranger would:** only what their public repositories hold,
  starting where a newcomer starts, each `README.md`, and following the links a newcomer would
  follow.
- **You write down what you understood:** every term you meet, what you take it to mean, and
  where you learned it.
- **Then you check each entry against the source** until every reference resolves. Where you were
  wrong, confused, or could not find what the code already has, that is a finding: the page that
  misled you, or the page that is missing.
- **Why:** Zen's standing goal is that each repository stays plainly readable by a stranger on its
  first-read path, using no privileged knowledge. Your wrong turns are the measurement: a careful
  reader's mistake is a page's defect, not yours. Getting names right matters above all.

## 2. What a stranger has

- Zengine (`https://github.com/Krealsion/Zengine`) and Loom (`https://github.com/Krealsion/Loom`):
  their `main`, each read at a commit you name, and their public issues.
- Nothing else: not Zen's plans, prompts, reports or handoffs, this page aside. If you know a term
  from outside the pages, say where a stranger would have learned it, or that they could not: that
  is a finding too.
- Read from GitHub, or from clones of your own under `Zen/scratch/stranger/`. Leave every other
  checkout on the machine as you find it.

## 3. What you write, in `Zen/stranger/`

- `path.md`: the pages you read, in order, and why you went to each next.
- `glossary.md`: one entry per term: what you took it to mean, in a line or two; where you learned
  it (file and line); the line in the source that settles it; and its state, `resolved`, `wrong`,
  `missing` or `unclear`.
- `findings.md`: one entry per finding: what a stranger would believe; where a page says it (file
  and line); what the source says (file and line); its kind, `wrong`, `stale`, `missing`, `unclear`
  or `hard to find`; and the smallest fix, in a line. A finding an open issue already holds links
  the issue instead. The ones that would set a newcomer back furthest come first.
- Each file names, at its top, the commits it was read at.

## 4. The check: every reference resolves

- Every name you write in backticks -- a file, a type, a shape, a key, an action id, a setting, a
  law -- is copied from the line you cite, at the commit you name, or marked `(not found)`. Nothing
  is written from memory or by analogy: a name that looks right is the error this check is for.
- A meaning is checked the same way: the line that settles it is cited.
- Run the check on every file before each commit. A tool of your own for it lives in your folder.

## 5. How to work

- **In rounds, one reading path each:** a newcomer who wants to start Workshop; one who wants to
  write a pane; one who wants Loom alone; one who opens a pane and reads its manual (its `?`); then
  the paths those suggest. Go back across the domains as later pages change what you understood: a
  term you got wrong and later right is still a finding, against the page that misled you.
- **Commit at the end of each round.** Vision reads your findings, checks them, and turns the
  confirmed ones into issues; you do not file them.
- **Ask the founder nothing unless you are blocked:** this job needs no decision from him.
- **Run as long as there is reading to do:** the pages change daily, so a later round reads them
  again.

## 6. What not to do

- No running or building anything: you read.
- No issue, pull request, comment, branch or commit in Zengine or Loom.
- Nothing written outside `Zen/stranger/` and your clones under `Zen/scratch/stranger/`.
- A security or capability gap is written in your folder alone, marked `security`, never anywhere
  public.
- No credential.
- A Zen commit is authored and committed as Krealsion <krealsion@gmail.com>, with no AI co-author
  line and no AI attribution in any form. Commit only your folder: other sessions commit to Zen
  too.
- Lines of 100 columns at most, in ASCII.

## 7. Working with the founder

- Lists over prose; the simplest reading first; one question per message.
- Peer-level honesty: say what you do not know.
- When you write a file, give him its path, not its contents.
