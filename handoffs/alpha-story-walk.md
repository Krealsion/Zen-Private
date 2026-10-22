# The alpha story, walked on main (Vision, 2026-10-21)

The founder's full story for the alpha: make a view, wire its inputs, author its logic in Flow,
wire its outputs back, detach the view into a window of its own, close Workshop, the view still
running, open Workshop and connect to the authored host's window; bonuses: the logic changed in
the Editor, the authored host merged back as a pane. Walked from the source and the manuals at
Zengine `main` `3fa139a1` and Loom `main` `3afe9e3`. Nothing was run.

## Step by step

| step | state | what is there | what is missing |
|---|---|---|---|
| 1. make a view | works | the View Builder: labels, number fields and buttons placed in pixels, run by the view host as a participant of its own (`view/docs/zengine.view.builder.md`) | a live look on `main`: the tutorial's pictures date from 2026-10-14, before G1's window defaults |
| 2. wire its inputs | works | a button's intent, `tally.panel.Count`, dragged onto Flow and declared accepted (`view/docs/view-builder.md`, "Drag shapes between the builder and Flow") | -- |
| 3. author the logic in Flow | works | a fold of `math.add`, emitting `tally.Total`; covered by `tests/test_flow_pane.cpp` and `tests/test_flow_graph.cpp` | -- |
| bonus: the logic in the Editor | not built | a workspace saves as Loom bytes (`.flow-workspace`); a definition has a JSON projection (`definition_json`, `flow/docs/flow-reference.md`) | an Editor round trip |
| 4. wire the outputs back | works | `tally.Total` dragged onto the label: `shows tally.Total.total`; the running view waits until told, then shows it (`tests/test_view.cpp`) | -- |
| 5. the view in a window of its own | missing | the pieces below | something that runs a view and a flow outside Workshop's process, an arranger for its window, and a way to start it |
| 6. Workshop closed, the view runs on | follows from 5 | a second process outlives the first | a witness of it |
| 7. Workshop opened, connected to the authored host | partial | Loom links, Workshop's guests file, the Connections pane | dialing again when Workshop comes back; what a connected host is to the weaver beyond a row |
| bonus: merged back as a pane | missing | the view keeps its field text, focus and told values across an apply; Flow keeps state across an apply | a handoff across hosts |

Steps 1 to 4 are the tally tutorial, end to end, today.

## Step 5: what a view in its own window needs

**Why it cannot happen today.** The view host and the Flow host run only inside Workshop:
Workshop's weave composes them (`agents/view.md`, "Workshop composes the host beside the Flow
host"), the Flow host's manual says "Workshop mounts it; it is not a file you load", and
`zengine-view` and `zengine-flow` are header-only libraries. No other process can run a view or an
interpreted flow.

**What another process can already load:** the operator providers (`zengine-operators-basic`),
the graphics directory and the OS window (`zengine-graphics`, `zengine-window-sdl`), the Timer.
The pattern exists: `zengine-snake` is an application made of weaves in a host of its own, its
operator weave the arranger of its window (`examples/snake/README.md`), though its window is the
terminal's.

**The ways to get there:**
- **(a) The app is a plan.** The view host and the Flow host become artifacts a plan loads; the
  authored host loads the operators, the graphics directory, the OS window, the two hosts with the
  view's and the flow's files, and a small arranger that places the view's area. What runs it:
  a Zengine host that holds an operator catalog and mounts providers, which today is only
  `zengine-workshop`, desk and all; so either a desk-less mode of it, or a small app host.
  Recommended: the weaver's creation becomes a plan of weaves, which is Loom's own answer.
- **(b) A second Workshop** launched with a one-pane setup. The least new code, but it is
  Workshop, chrome and all, not the weaver's own app.
- **(c) The flow generated as C++.** Refused for any fold ("a fold is spent by the evaluator, so
  this definition is not generated as C++ and runs interpreted", `flow/docs/zengine.flow.md`), and
  the tally flow folds.

**Starting it.** Zengine starts an operating-system process in one place, the Builder's runner,
and it runs only the host's CMake (`builder/run.hpp`, `builder/runner.hpp`). The demos entry needs
the same thing for `demo.py start --setup <name>`. One catalog-limited start serves both: the app
host with an app folder, `demo.py` with a listed setup, nothing a message can widen. The plainer
alternative: the export writes a launcher the weaver runs.

**Detach itself** is then a View Builder command: write the app folder (the plan, the view, the
flow workspace) and start it, the copy in Workshop stopped.

## Step 7: connecting

- A Loom host's plan can hold a `links` row to another running Loom, such as Workshop; the far
  host's policy decides, here Workshop's guests file (`--guests <file>`). An unreachable link stays
  mounted and answers `unlinked`; `links connect <name>` dials again, a new session (Loom
  `docs/guides/running-loom.md`, section 10).
- Workshop's Connections pane shows each connected host as the guest door reports it
  (`external-host/docs/zengine.connections.md`).
- Missing: the app dialing again by itself when Workshop returns, and what the weaver can do with a
  connected app from Workshop. Today a link carries the app's asks to Workshop's offices, under its
  guests row's grant; nothing in Workshop reaches into the app.

## The first five minutes

- Workshop starts on `workshop-plan.json` in the folder it was launched from, else
  `default-load-plan.json` beside it, which shows the desk in the terminal window; the OS window is
  `graphical-load-plan.json` (`workshop/docs/load-plans.md`). Until G2's stage 8 makes the window a
  choice, the release's launcher names the graphical plan.
- The way to the story today: `ctrl+p`, then `n` for the View Builder; Flow from the Pane Manager;
  the walk is `view/docs/view-builder.md`. A first-run screen can open the two side by side at its
  first step.

## The order to build it in

1. Steps 1 to 4 witnessed live on `main` in the OS window: no product change, and it confirms the
   half that exists.
2. A read-only probe for step 5 (Ceecee): option (a)'s cost, the two hosts as artifacts, the
   operator catalog in a host without the desk, the arranger, and the catalog-limited start shared
   with the demos entry.
3. Step 5 built, likely two phases, then step 7's dialing again.
4. The first-run screen pointing at it.

Steps 1 to 3 need no build slot until 3; the probe can run beside G2.

## Not walked

- Anything run: every state above is the source's and the manuals' word.
- The bonus merge-back's design: Loom's replacement guide (`docs/guides/replacing-a-service.md`)
  is where it starts.
