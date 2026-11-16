# Drawing inside a frame

A goal of *drawing for real-time games* on the [roadmap](../roadmap.md); how this file works:
[README](README.md).

Done when (the real-time drawing research's rounds, 2026-11-14):

- [ ] the window works out once what a change covers, not kept nodes against changed ones (W1)
- [ ] a refusal's words are built only when Loom refuses, and fields are read by position (the
  drawing's L1, in Loom)
- [ ] D1 and W2 in Zengine (day one: their requirements, from the research report)
- [ ] Loom carries a value's admitted bytes through the host, building its value tree only for a
  reader that asks (the drawing's L2, P-LOOM-31)
- [ ] a whole area at the bound draws inside a 16 ms frame in Release, measured in a real host's
  frame and not one drawer alone (today 26 to 30 ms)

Tasks:

- [ ] W1, about 25 lines. Holds on drawing order and names (the same store code).
- [ ] the drawing's L1, about 60 lines. Holds on the queue budget's fix (the same
  message-checking code).
- [ ] D1 and W2
- [ ] the drawing's L2, its order beside the data plane's read from the two reports (day one)
- [ ] the measure in a real host's frame, once game time's frame clock is in

Records: `reportbacks/realtime-drawing-research-RB.md`, `realtime-drawing-second-RB.md`,
`realtime-drawing-disputed-RB.md`.
