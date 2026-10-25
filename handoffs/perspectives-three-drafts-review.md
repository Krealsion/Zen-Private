# The git, pairing and tailoring perspectives, answered

Vision, 2026-10-25, for Ponder. Read: `rebuild-scaffold/perspectives/git.md`, `pairing.md` and
`tailoring.md` at Zen `d16ba7db`, their measured claims spot-checked against Zengine `main`;
`check.py` passes. The founder's answers (2026-10-25), as Vision proposed them: all nine questions
below, with two additions to git's seam and one to pairing's. Mark the three `founder-reviewed`.

## Git (`git.md`)

1. **The seam: yes, local commits only, with two additions.**
   - Say how `zengine.git.host` reaches git. Three places start a process today, as
     `builder/run.hpp` names them: the Builder's runner, the Neovim editor's child and the
     launcher. The office either asks the Builder's runner to run git, or is a fourth, which a
     host grants as a power. Draw the one you choose, and name the other as its alternative.
   - A stage, an unstage or a discard names the diff it was read from (the file's blob id, say),
     and the office refuses it whole when the working tree has moved since, as D1's owner refuses
     an edit judged from a picture the run has moved past. A hunk's index alone can land on the
     wrong lines.
2. **[Stage][Unstage][Commit][Refresh] and [Diff v]: yes.**
3. **Slot 2: `Inventory`** (option A): carrying a hunk to Inventory is a moment of the task, and
   the Git pane lists the files itself.

## Pairing (`pairing.md`)

1. **The seam: yes**, `GuestDecisionRequested` and `GuestDisconnectRequested` on `zengine.guests`,
   the weaver's hand alone. The hand is judged by asking Workshop the question D1 adds,
   `WeaversActRequested{gesture, office}`, answered `WeaversActAnswered{current}`
   (`Zen:prompts/desk-split-d1.md`), so one judge says whose hand a gesture is. Say so where the
   page says "under a weaver-hand gesture".
2. **[Admit][Refuse][Shed] and the row's right-press menu: yes.**
3. **Slot 4: `Info`** (option A).

Your measured gap holds on `main`: a row with `"admit": "ask"` parks its connection in
`awaiting-decision`, and `GuestDoor::decide` (`workshop/guest_door.hpp`) has no caller, so nothing
can admit it. It wants an issue of its own, which is the founder's to file; the page keeps it as
the gap it measures.

## Tailoring (`tailoring.md`)

1. **[Show/Focus][Hide][New Pane] on the Pane Manager: yes.**
2. **[Modify][Type Key][Reset] and [Commit][Cancel] on Hotkeys: yes**, and the Manual's
   [Top][Bottom][Close], which the page proposes and does not ask.
3. **Slot 2: `Info`** (option A).

## For all three

- The pages stand at `7bda9f0b`. Since then L1 (#413, `ui/` in whole pixels) and #416 (the guides
  say what the code does, the cheat sheet an index, `workshop/docs/hotkeys.md` rewritten) have
  merged, and D1 (#415, the layouts' owner `zengine.layouts`) moves the settings and layout seams
  these pages cite. Keep the baseline as it is; rebaseline once D1 merges, before any page becomes
  a prompt.
- What not to do stands as your handoff says it.
