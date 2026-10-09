# Handoff: Zen Night Lab, era 2

From the founder (Krealsion), 2026-10-09. Written by Vision, the Zen thread, for the session that
will run Night Lab's own thread: design its experiments, write its prompts, review its runs and
curate what they find.

## The question

"Can agents create new panes and setups that are efficient for both them and the human user?"
(the founder, 2026-10-09)

- An agent, on its own host, reads and drives a Workshop through the agent's desk (BL-WORK-38):
  the desk said as text, notices of change, one judged door for acts.
- It makes panes, and setups (a desk's layouts, with each pane's settings).
- Each result is judged twice: what it costs an agent (tokens a look, steps an act) and what it
  costs a person (the founder judges from pictures and from use).

## When

- The founder's order: the agent's desk first, then the documentation rewrite, then the lab's runs.
  The new docs matter here too: the lab reads them as a stranger would.
- The question needs at least the desk's stages 1 to 3b (the desk read whole, notices, one door,
  the owners' checks). Stage 4a (documents) and 7d (a build slot) help. Stage 2 is running now.
- The preparation below needs nothing from Zen, and can start now.

## What Night Lab is

- Repository: `G:\programming\cpp\Zen\playground\zen-night-lab`, which is
  github.com/Krealsion/zen-night-lab, branch `master`. **It is public.**
- Eras: `original/`, `marathon/`, `workshop-marathon/` and `followups/` are frozen evidence about
  the Zen they ran on, never updated. `current/` is the Loom-only era of ZNL-R to ZNL-06 (August
  2026): seven small applications built on an installed Loom. Its last four runs opened no new
  friction entry. It ran dry, which is why era 2 asks a new question.
- The house rules (`current/README.md`), kept: only installed packages, never a source tree;
  nothing writes to Loom or Zengine; no shared framework between experiments; a labelled fake is
  allowed, an unlabelled one is not; sightings nominate, they do not authorize; each claim in
  EVIDENCE has its WITNESS, SCOPE and DOES NOT PROVE; `substrate.lock` is a record, never an input.
- Read: `Zen/private/raw-vision-deltas.md` (its 2026-08-06 section),
  `Zen/reportbacks/ZNL-R-REPORT.md` and `Zen/reportbacks/ZNL-06-RB.md`, and the lab's
  `current/README.md`, `FRICTION.md` and `EVIDENCE.md`.

## The wall

The founder agreed to these measures (2026-10-09). Set them up first.

A dedicated WSL distribution, the lab's own:
- Made fresh from a clean Ubuntu image, never a copy of the founder's distribution, which holds
  Ceecee's build trees and mounts his drives.
- Its `/etc/wsl.conf` turns off drive automount, Windows interop and the Windows `PATH`, and names a
  default user of its own. It then sees no Windows drive and runs no Windows program. A separate
  Windows user would not do this alone: a second drive such as G: usually grants every user write.
- The executor runs inside it (Claude Code installed there), so every tool it uses stays inside.
- Zen comes from GitHub, pinned: each run builds Loom and Zengine at exact commits into a fresh
  prefix and records both in `substrate.lock` (the lab's Loom rule, extended to Zengine).
- GitHub: a fine-grained token that reaches only `zen-night-lab`, made by the founder and put into
  the distribution by the founder. Loom and Zengine are public, read-only.
- Its Workshop is a development host (`host: development` in its own guests file): the agent
  builds and writes there, and nothing of the founder's is reachable.
- Said limits: the founder's WSL uses mirrored networking, a setting for every distribution, so the
  lab shares Windows' loopback and can reach anything listening on Windows' localhost. And it
  shares CPU and memory: run when nothing else builds, until stage 7d's build slot.
- Verify each setting on the machine before the first run (no `/mnt/c`, no `cmd.exe`). The founder
  runs anything that needs an administrator or one of his accounts.

What the wall means for the lab: it cannot read `Zen/`. Its prompts, rules and reports live in the
lab repository, and Zen's executor constitution does not reach in, so the lab keeps a short
constitution of its own. Inside the wall the executor starts with no memory: write cold prompts,
or let the lab keep its own memory in its repository.

## Findings

The founder's arrangement:
- Each run's raw findings stay in the lab repository, in the run's own experiment folder:
  FRICTION, EVIDENCE, `substrate.lock`, pictures.
- An `experiments/` folder holds the curated record. Per experiment: the best findings explained
  plainly, what was left unfinished, and suggestions for the next experiment.
- The repository is public. A finding that lets someone do what they should not is never written
  there: it goes to the founder, for a private security advisory.
- Promotion: sightings still only nominate. A finding the founder promotes becomes a GitHub issue
  on Zengine or Loom, filed by deep review in the issue form (outcome, fences, a test that fails
  before), or, when it is architectural, goes to the Zen thread's plans.

## Prompts and reviews

- The founder's prompt rules: the outcome, the fences and what not to do; as few conditions as
  possible; the executor decides the how; the what-not-to-do list binds; a STOP is honored.
- The first line names the run; a `Memory:` line; wrapped at 100 columns.
- The temperature goes in your chat message beside the prompt's path, never in the prompt: hot (a
  continuation), warm (a fresh session with its memory), cold (no memory at all).
- The old ZNL prompts ran to about 1,800 lines. Keep era 2's short: one standing prompt reused
  each night is the target, run as a scheduled task once the founder says go.
- A review reports the checks run out of the checks planned. Un-run is unverified.

## How the founder works

His saved preferences apply. In short:
- Lists; the simplest explanation first; at most one question a message; for anything he must do,
  explicit steps and what "done" looks like; for a file you write, its path only.
- He does not read reports word for word, so a summary must stand on its own.
- Peer-level honesty; say so when reasoning runs backward from a wanted conclusion.
- Never: AI attribution in commits or pull request text; handling credentials; deleting what he
  did not ask to delete; merging, which is his.

## First tasks, in order

1. Read the above and the files it names.
2. Set up the wall with the founder: the exact commands for his machine, each verified.
3. Era 2's README, the lab's short constitution, and the form of `experiments/`.
4. Refresh `current/FRICTION.md`'s ten entries against today's Loom: which are fixed, which live.
5. The standing prompt for era 2.
6. Wait for the founder's go, after the agent's desk and the documentation.

## The Zen thread

- Vision owns Zen's plans (`Zen/private/`), the prompts in `Zen/prompts/` and the agent's desk.
  This thread owns Night Lab. A lab finding that should change Zen's plans goes to the founder, who
  brings it to the Zen thread.
- Where things are: the Zen workspace is `G:\programming\cpp\Zen`. The agent's desk:
  `Zen/private/backlog.md` (BL-WORK-38) and `Zen/reportbacks/agent-desk-research-RB.md` with its
  folder (`design.md`, `stages.md`, and `experiments.md` on an agent's own host; decision 17 is
  isolation). The issue lane: `Zen/private/backlog.md` section 1 and
  `Zen/private/handoffs/issues-handoff.md`.
