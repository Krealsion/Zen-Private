# A contained weave's hold on the host (private)

A goal of *security* on the [roadmap](../roadmap.md); how this file works: [README](README.md).

Done when:

- [ ] a sender's waiting messages are bounded whole, so no weave -- native, isolated or boxed --
  can hold the host's memory past a known bound (P-LOOM-32; P-LOOM-34 assessed beside it)
- [ ] the fix merged in its private fork, and the advisory published

Tasks:

- [ ] Vision reviews the round's report (`unreviewed/private-queue-budget-RB.md`) and the fork's
  change, on the device
- [ ] the founder merges the fix in the fork and publishes the advisory

Records: `prompts/private-queue-budget.md`. Measured 2026-11-14: a 25-byte value can decode to
65,536 cells (6.8 MB, 11.5 ms); the host admits a message before queuing it
(`src/kernel/kernel.cpp` 529); 1,024 waiting per sender (`kMaxPendingPerSender`) let one sender
hold about 7 GB for about 12 s; a box reaches it (`wasm_box.cpp` 408) and so does an isolated
child.
