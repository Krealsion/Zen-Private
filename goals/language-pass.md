# The language pass

A goal of *readability* on the [roadmap](../roadmap.md); how this file works:
[README](README.md).

Done when (the founder, 2026-11-15):

- [ ] function names are verbs that say what happens; parameters say what they hold; numbers are
  named locals the compiler folds away; comments say only what the code cannot, nothing said
  twice; helpers make the path people naturally take the clear one
- [ ] across Zengine and Loom, a slice at a time, each pull request carrying a rename map

Tasks:

- [ ] the founder's call on cold readers
- [ ] the first slice: `graphics/` and the tile defense, with the tile defense's names and the
  arranger's rename, and the ports' helpers. Holds on W1.
- [ ] the slices after it (day one: their order)

Open:

- Cold readers: readers given only a function's code and comments say what it does and flag what
  repeats; it needs an exception to Ceecee's rule 11. Lean: a small model, scoped and capped,
  reading before and after each rename; Ponder the outside read once a slice merges.
