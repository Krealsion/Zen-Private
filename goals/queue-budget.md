# A contained weave's hold on the host (private)

A goal of *security* on the [roadmap](../roadmap.md); how this file works: [README](README.md).

Done when:

- [ ] a sender's waiting messages are bounded whole, so no weave -- native, isolated or boxed --
  can hold the host's memory past a known bound (P-LOOM-32; P-LOOM-34 assessed beside it): in
  messages (1,024), cells (`4 * kMaxDecodedCells`) and payload bytes (64 MiB) per sender, one unit
  holding all three (`PendingSpeech`), and the value windows bounded in the memory they keep
  (32 MiB each). Built and reviewed (2026-11-16) on `security/pending-cells-per-sender` at
  `8217387`, in the advisory's private fork `Krealsion/Loom-ghsa-2672-h8r2-r33r`
- [ ] a spent room refuses at the door before decoding in every unit: today `PendingSpeech::refuses`
  refuses a spent cell room outright but lets a zero-payload send past a spent byte room, so
  `refuses_now` answers nothing there and a byte-spent sender's sends are decoded, then refused at
  the bus (the bound on what is held stands; the decode is the cost)
- [ ] the fix merged in its private fork, and the advisory published, both halves in it (the cells
  the research measured, and the payload bytes the round found)

Tasks:

- [ ] the byte room's door check, a continuation in the fork before the merge (the founder,
  2026-11-18): an explicit refusal of a spent byte room in `refuses`, as the cells have, and a
  door case with only the byte room spent. Its prompt once its lanes' home is settled (Open).
- [ ] the founder merges the fork's pull request and publishes the advisory
- [ ] the round's clones in `scratch/private-queue-budget/trees/` kept until the merge: the kit's
  `left-behind.py` reads an advisory fork's pull request as none and marks them to go

Open:

- Where the continuation's lanes run, with no machine that builds them: the advisory's fork runs
  no Actions (GitHub lets no integration reach it), so either a private repository of the
  founder's own carries the branch and `ci.yml` (a Loom run is about 137 of the 2,000 private
  minutes a month: 88 Linux, 24 Windows at twice the rate, measured on `9f3db68`'s run), or the
  round waits for the PC. Lean: the private repository.
- The advisory covering both halves. Lean: yes, as the round wrote it; without the bytes it would
  describe a queue bounded in structure alone.
- The branch's five commits squashed at the merge. Lean: yes, so Loom's `main` keeps one clean
  commit, as the founder prefers; the correction from cells to memory stays in the report.
- The two keepers left open, P-LOOM-37 (the relay's held occurrences) and -38 (a bridge client's
  pending replies). Lean: a private round of their own next, the relay's first.

Records: `prompts/private-queue-budget.md`; `reportbacks/private-queue-budget-RB.md` and its
evidence, reviewed 2026-11-16. Measured 2026-11-14: a 25-byte value can decode to 65,536 cells
(6.8 MB, 11.5 ms); the host admits a message before queuing it (`src/kernel/kernel.cpp` 529);
1,024 waiting per sender (`kMaxPendingPerSender`) let one sender hold about 7 GB for about 12 s; a
box reaches it (`wasm_box.cpp` 408) and so does an isolated child. Reproduced at START by the
round in both units (8 whole values queued; 12 one-cell values of 8 MiB, 96 MiB waiting), refused
at END; the cost of weighing every send, +0.033 us a one-cell send and +1.5 % a whole value.
