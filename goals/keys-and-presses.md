# Keys and presses (V6, V7)

A goal of *the visual foundation* on the [roadmap](../roadmap.md); how this file works:
[README](README.md).

Done when (the founder's calls of 2026-11-02 and 11-03):

- [ ] the interaction contract first (the Grinch's gate, taken): gesture streams, a focus chain,
  dispositions, key routing from declarations against the settled pane-first rule
- [ ] a pane hears a key first, and what it does not consume goes up to Workshop; a pane may opt
  out of Workshop's defaults; a pane owns its own key (from outside it opens or selects the
  pane, inside it closes it)
- [ ] one action shape carrying its source (a click and its place, a key, an agent's); keymap ids
  scoped by their owner
- [ ] every pressable thing an action with one way in: a button its own declaration; a press
  declaring what it does (a message, the message a draft holds, or the pane's own code); a
  hotkey only a keymap binding; a command tile's press runs it
- [ ] V6: the press lambda stays in its pane, only its message's shape declared; a hotkey asks an
  action by its id, and that action's own press form runs
- [ ] V7: one way-out chord, Ctrl+Q by default, moved only by the weaver; the band shows it while
  a pane holds the keys; a notice says once where it went if the legend is hidden; a press
  reaches only the area under it, so the setups bar stays one
- [ ] jump hints with a mode each, press and focus first, a hint's letter triggering its action
- [ ] inputs, batched ones too, resolved one at a time against the state the last one left, the
  chord never waiting
- [ ] the double click's follow-ups (#120): a second press counted in the Terminal's word select
  and the Builder's list; `PointerTimingAsked` in V6's versions; `design.md` 2.5 and 1.8 saying
  the count goes on and is per hand

Tasks:

- [ ] the interaction contract, designed and agreed
- [ ] V6
- [ ] V7. The Workshop move holds on it.

Open:

- The interaction contract's design. Lean: a research first, since it reaches every pane.

Records: as the visual foundation's; `reportbacks/double-click-RB.md`.
