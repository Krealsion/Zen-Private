# The language pass

A goal of *readability* on the [roadmap](../roadmap.md); how this file works:
[README](README.md).

Done when (the founder, 2026-11-15):

- [ ] function names are verbs that say what happens; parameters say what they hold; numbers are
  named locals the compiler folds away; comments as the documentation's design says
  ([doc-design](doc-design.md): complete sentences, each comment earned; the founder,
  2026-11-19); helpers make the path people naturally take the clear one
- [ ] across Zengine and Loom, a slice at a time, each pull request carrying a rename map

Tasks:

- [ ] the founder's call on cold readers
- [ ] the first slice: `graphics/` and the tile defense, with the tile defense's names and the
  arranger's rename, and the ports' helpers. Holds on W1.
- [ ] the slices after it (day one: their order)

Open:

- `RunningRecipe::look()` (`builder/run.hpp`) takes the output it reads, and its name says it only
  looks; the builder race of 2026-11-19 grew from that (Zengine #179,
  `reportbacks/builder-look-race-RB.md`). Lean: a name that says it takes.

- Cold readers: readers given only a function's code and comments say what it does and flag what
  repeats; it needs an exception to Ceecee's rule 11. Lean: a small model, scoped and capped,
  reading before and after each rename; Ponder the outside read once a slice merges. The founder,
  2026-11-19: the documentation's trial uses one, its exception stated in the prompt
  ([doc-design](doc-design.md)), and its setup is archived after it for reuse. Lean now: the same
  setup in each slice's prompt, once the trial has shown what it is worth.
