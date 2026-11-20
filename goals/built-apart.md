# Built apart

A goal of *the Workshop split* on the [roadmap](../roadmap.md); how this file works:
[README](README.md).

The founder's picture (2026-11-20): "completely separate nodes, all connected through one central
node, Loom." The running program holds it; the build does not. Vision's rough measure
(`Zen/pass-tools/build-coupling/`): Workshop written as one class in headers, the test fixture that
compiles Workshop and every pane into each test, drawing code in headers, the seam vocabularies in
`workshop/`, and Loom's weave SDK carrying the in-process bus.

Done when (the founder, 2026-11-20):

- [ ] a weave builds against Loom, the vocabularies it speaks and its own code, and nothing else,
  and a check holds that direction by topology
- [ ] a test talks to the weaves it tests as the running program does, loaded through Loom, not
  compiled in
- [ ] the gains measured against today's build: a cold build, peak memory, a typical change's
  rebuild, disk

Tasks:

- [ ] the research, `prompts/unrun/built-apart-research.md`, cold, on the laptop: the map, each
  nexus's cost, probes on scratch branches, the rule and its check, the plan in slices. It runs
  now, ahead of its direction (the founder, 2026-11-20)
- [ ] the plan's slices, once the research is reviewed

Open, each with Vision's lean:

1. Where it runs among the lanes: the research now, beside the documentation's rewrite, which
   builds little. Lean: its slices follow the plan's order, the test fixture first, since it holds
   most of the cost.

Records: `pass-tools/build-coupling/README.md` (2026-11-20); `reportbacks/fast-builds-research-RB.md`;
`reportbacks/kit-build-memory-RB.md`; `pressure.md` P-BUILD-08, taken here.
