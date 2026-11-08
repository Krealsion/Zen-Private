# Main green: what it would cost

Vision, 2026-11-07, for the founder's decision on the process brainstorm's first item. Three parts,
each with what it buys, what it costs, and what we would lose.

## A correction first

I pitched "build Loom once and reuse it". Measured on V4's run at `1a4655c7`: Loom takes 0.7 to
1.1 minutes a job. Zengine's compile takes 20 to 34 and the tests 12 to 41. ccache is already in
`ci.yml`, and `reportbacks/fast-builds-research-RB.md` designed the rest. There is no cheap speed
win here I can stand behind, so it is out of this item. Speed still matters below: every extra CI
pass costs 40 to 73 minutes.

## A. No test reads the real clock

**Buys**: the end of a whole class of flakes. Today Flow's double click went red six times; before
it, the Timer suite on MinGW (P-BUILD-16) and the tower-defense story's 0.5 s wait (story_journey
U7). Tests could also skip their waits instead of sitting through them.

**Costs**:
- The work: about a dozen places read the OS clock themselves (P-WORK-85: the Timer, Neovim's
  bounds, Workshop's interaction time, the Input office's `Now`, Flow, Info's and Inventory's
  timestamps), and four suites step virtual time in 10 ms beats (P-BUILD-23). Medium to large; it
  is the frame clock round's ground anyway.
- A check that fails a test reading the clock, with its exceptions named.

**We would lose**:
- Real time at the edges, tested by default: the window's real double click, a child process's real
  latency (Neovim), real timeouts. Those need a small labeled set of real-time cases, which can
  still flake, so they should not gate a merge.
- Slowness that only shows in real time. The 600 s budget a case still measures real time, so gross
  slowness shows; a subtle latency regression would not.

**Order**: with or after the frame clock round. Before it, we would build seams the round replaces.

## B. Main green by construction

Three ways, cheapest first.

**B1. Today's way**: when lanes collide or one flakes, you order the merges and the rest rebase.
- Costs your attention every time.
- Two PRs green alone can still be red together; not seen yet that I know of.

**B2. "Require branches to be up to date before merging"** (a branch rule the repos can use as they
are): a PR merges only after it is rebased onto the newest main and its CI passed there.
- After each merge every other open PR is out of date: a rebase and a full run each, one at a time.
  Three lanes landing the same evening is hours of serial reruns.
- The advisory MSVC would not count.

**B3. GitHub's merge queue**: you press merge; GitHub tests the PR on top of main and everything
ahead of it in the queue, and merges only if green.
- Only for repositories owned by an organization: Loom and Zengine would move into one. GitHub
  redirects the old addresses, but CI's canonical Loom, the package names and attestations, links
  in pages, the nightly and UnknownWorkers' access each need checking.
- Every merge runs CI once more on the combined commit, 40 to 73 minutes (a batch shares a run).
- A flaky required check stalls the whole queue, so A comes first.
- A plus: an organization's teams give agent accounts like UnknownWorkers cleaner limits.

## Vision's lean

A first, as the frame clock round's rule. Stay with B1 until A lands; then B2 if few PRs land a
day, B3 if many.
