# Built apart

A goal of *the Workshop split* on the [roadmap](../roadmap.md); how this file works:
[README](README.md).

The founder's picture (2026-11-20): "completely separate nodes, all connected through one central
node, Loom." The running program holds it; the build does not. The research measured why
(`reportbacks/built-apart-research-RB.md`): tests are 64% of the cold build's compile time, the
44 units of the Workshop fixture 47%, because the fixture compiles Workshop in; and a unit pays
for every shape it can see, used or not.

Done when (the founder, 2026-11-20):

- [ ] a weave builds against Loom, the vocabularies it speaks and its own code, and nothing else,
  and a check holds that direction by topology
- [ ] a test talks to the weaves it tests as the running program does, loaded through Loom, not
  compiled in
- [ ] the gains measured against today's build (cold 46.2 min at `-j2` on the laptop, one unit's
  peak 3.75 GB, 51 units over 2 GB, the tree 5.2 GB and the sanitizer tree 20 GB)

Tasks:

- [x] the research, `prompts/built-apart-research.md`, run and reviewed 2026-11-20
- [ ] slices 3 and 1, `prompts/unrun/built-apart-census-fixture.md`, cold: the law on its public
  page and the census's rows; the fixture compiled once; the two defects; the laptop's row in
  `machine_facts.md`. After the quarry's move merges
- [ ] slice 2, `prompts/unrun/built-apart-lazy-shapes.md`, cold: a shape's field list lazy, in a
  Loom pull request under Loom's whole lane
- [ ] slice 4, the panes suite with no Workshop in it
- [ ] slice 5, Workshop's suites load Workshop, reading it by message
- [ ] slice 6, the seam vocabularies to their contracts, internals out of weaves; each folder
  after its documentation slice
- [ ] slice 7, the topology: each package's own include root, the tree root nobody's; after 4 to 6
- [ ] slice 8, the host's own weaves loaded (one-host's rounds)

Decided (the founder, 2026-11-20), on the research's six decisions:

1. The law of five kinds and one direction, as `rule.md` writes it, with Vision's refinement: a
   library holds no state and no authority (a function of its arguments); a part that holds
   state or answers others is a weave.
2. Its consequences accepted, each part sorted by that refinement.
3. Workshop's suites read it by message, through a reading vocabulary that grants nothing and
   that a weaver's tools would use too; no door for tests alone.
4. The census's rows first, beside the fixture compiled once; then Loom's lazy shapes.
5. Loom's lazy shapes in a Loom pull request, its whole lane run under it.
6. The weave SDK's bus split for topology alone, when Loom's next round touches the SDK.

Open, each with Vision's lean:

1. How slice 5 reads what Workshop holds. Its suites read `Session` (`workshop/screen.hpp`), a
   plain struct none of whose parts is a shape; Loom's poke reads only a declared state shape's
   scalar fields (`ZEN_EXPOSE`). Lean, by kind: what Workshop shows, through the desk reading;
   what it holds as authored intent (the layout, the bindings), as a declared state shape that
   live replacement, inspection and tests read alike, if poke learns structured fields; its
   gestures' machinery as libraries tested on their own. Settled when slice 5 is designed.

Records: `reportbacks/built-apart-research-RB.md` and its folder; `pass-tools/build-coupling/`;
`reportbacks/fast-builds-research-RB.md`; `reportbacks/kit-build-memory-RB.md`.
