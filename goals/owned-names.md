# Owned shape names

A goal of *the Workshop split* on the [roadmap](../roadmap.md); how this file works:
[README](README.md).

Done when (decided 2026-11-09; Loom #3, P-LOOM-08):

- [ ] every vocabulary declares its owner once, `ZEN_VOCABULARY("<owner>")` or
  `ZEN_VOCABULARY_BARE()`, and one declaring neither does not compile
- [ ] nothing is renamed, so no name or content id moves; published versions stay bare, an owned
  version carrying the number on; an older name read forward by each reader, no alias at Loom's
  gate
- [ ] Loom checks an owner's spelling; Zengine refuses an owner on a namespace with no shapes of
  its own; today's bare vocabularies pinned, so a new one takes an owner unless a reviewed pin
  says otherwise
- [ ] an owner is the vocabulary's own name after its package's spelling, never a role's; Loom
  spells itself `loom.`

Tasks:

- [ ] Loom's round (Loom #3's done-when)
- [ ] Zengine's round. Both in a gap between the pane contract's rounds, before the first pane
  outside Zengine.
- [ ] short names, only where a person types and nothing is stored: optional, after

Records: `reportbacks/owned-shape-names-research-RB.md`, its census and spike.
