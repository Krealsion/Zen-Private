# Comfortable panes and reusable test setups

**Status:** implemented and locally verified in [Zengine PR #49](https://github.com/Krealsion/Zengine/pull/49), commit `e8fddf072d1791e7544392b0c437a65f220bb1a1`. Founder acceptance remains pending.\
**Selected:** 2026-09-22, founder request.\
**Owner:** [Workshop goal map](../goals/workshop.md#near-term-order-and-purpose).\
**Predecessor:** [Inventory/Compose and timed motion](inventory-compose-motion-plan.md).

## Outcome

Open a pane and have enough room to use it. Load a named demonstration with one agent command,
try the story, press Reset and try again. Retain the setup as a maintained starting point for
later tests and demos. Measure the work hidden behind that convenience as well as the visible
number of actions.

Interpret the founder's “1 or 2 default panes to load into” as one or two named **pane setups**,
built from existing tools. These are early workspace candidates, not a new workspace framework
or a request to replace the maker's normal startup desk.

## Starting evidence and implementation gate

The founder merged Zengine PR #48 and authorized implementation. The branch was created from
freshly fetched `origin/main` at `13e29602f6cddbf345d1773866325ba43fdbb227`; a delivery-time fetch
still resolves there. The [phase report](../../reportbacks/zengine-comfortable-demo-setups-RB.md)
and [evidence](../../reportbacks/zengine-comfortable-demo-setups-evidence.md) own the result.

The following source observations record the planning baseline, before implementation:

- `workshop/pane_vocabulary.hpp`: `PaneOffered v1` carries pane/name/summary, with no size request.
  `PaneRoom` reports actual body rows/columns resolved with the current medium's text metric.
- `workshop/screen.hpp`: reactive stack panes share `kStackRows = 9` canvas rows. Canvas rows
  are not necessarily text rows. `setup.hpp` seats through shared stack capacity, while explicit
  authored placement is a different path. A larger size hint alone will not repair seating.
- [Setups](../../Zengine/docs/workshop/setups.md) already persist pane references, arrangement
  and size. A named layout does not make new provider instances or checkpoint pane working data.
  `--isolated` avoids reading/writing per-user Workshop state; it is not a security sandbox.
- The [previous live driver](../../reportbacks/zengine-inventory-compose-motion-live.py) authors
  setup/admission/session files, starts both hosts, then runs two Escape tools and a restore tool
  before the demo. That is concrete preparation ceremony to remove, not the desired public API.
- The maintained [ELH package at the reviewed head](https://github.com/Krealsion/Zengine/blob/2f39c3c97ff637d171e7b17aacd34ffa124fe076/external-host/tools/workshop/loom-tool.json) already
  contains capture, collection, inspection and Compose stories. Loom sessions supply reusable
  runs, discovery and history. Reuse these rather than making another runner.

## 1. Comfortable initial sizes

Audit the shipped pane offers and choose a modest initial size for each tool's actual work.
Do not impose a common rectangle, equal row counts or a new tiling system. A small provider-owned
preferred-space declaration is the leading approach; Workshop resolves it using its actual
display, borders and available workspace. Keep the exact message shape open to source preflight.

- For item lists, budget **three actual items**, then add header, footer and omission rows.
  A list region showing one earlier/later marker needs four rows; a middle window with both
  markers needs five. For example, Inventory's current one-row heading and one-row footer imply
  seven body rows when both markers are present. Borders/title space are additional.
- Choose widths that make the ordinary labels, fields and primary action understandable.
  Forms need useful field/value space; Terminal needs output plus its command line; editors and
  Flow need room appropriate to their work. Record the short per-pane choice and verify it live.
- Express text needs in body text units where appropriate, not guessed SDL pixels. Canvas
  providers may express different needs. Check SDL and TUI at their real font/cell metrics.
- Explicit saved sizes and maker resizing take precedence. Preferences guide initially
  unresolved/default geometry; re-offering or content changes must not continually resize a
  pane. Preserve the existing meaning of an explicit “reset size to default” action.
- Update seating and resolved bounds together. Handle a small viewport honestly with usable
  degradation or the existing explicit waiting/refusal behavior. Do not claim three visible
  items when chrome consumed them, reserve invisible space, or force a larger window on the maker.
- Keep older providers usable through the existing fallback. A new message contract must obey
  schema identity/version rules; do not append fields to an existing version in place.

Initial comfort is a default preference, not a new hard minimum forbidding small authored panes.
This phase does not require collision-free automatic layout of every combination of panes.

## 2. Two named starting setups

| Setup | Panes and starting material | Ready means |
|---|---|---|
| Value inspection | Inventory + Info; a few small typed fixture entries, including a structured value | Visible list and inspector; copy/edit/save and fresh-read story can begin immediately |
| Command reuse | Inventory + Loaded + Compose; fixture values for the existing rename-command story | Current target discoverable, fresh form/catalog state, enough visible room for the complete drag/review/submit story |

Ship the first completely before adding the second; two is the maximum for this detour, not a
reason to leave either incomplete. Use safe disposable fixture data and the existing product
operations. Derive live identities after connecting; stored process IDs are not reusable setup
identities. Keep scene layout, required providers, fixture preparation, readiness checks and reset
instructions together under a discoverable recipe, referencing existing formats where possible.

Provide one discoverable agent command to **prepare/load a named setup**. With the documented
build/install prerequisites and pre-approved authority present, it should start an isolated demo
Workshop if needed or reuse its existing instance and ELH session. Return the setup identity,
live endpoint/instance, readiness result and artifact locations. A second invocation must have
defined behavior: ensure an already-ready setup without silently resetting completed work;
reset is a separate explicit action.

Start with dedicated demo instances. Layouts share provider state, so switching layouts inside
an arbitrary working Workshop is not safe isolation. Do not retarget a maker's active session,
replace their work or change their default startup files merely to prepare a test. First-time
installation/build and operator-granted authority remain named prerequisites, not hidden inside
a “fast load” time. No ELH self-approval or new permission bypass.

## 3. A real Reset button and matching command

Each setup exposes a visible **Reset demo** action, also reachable through one ELH tool call.
It runs the same recipe/reset workflow in both cases. Use an existing action/run surface if it
fits, otherwise a small optional demo participant; do not hard-code these stories into the host.
Test policy belongs to the ELH package, and changes to product state use its ordinary owners.
If the UI depends on the attached harness, make that dependency and an unavailable harness visible.

Reset restores this recipe's arrangement, known fixture values and relevant transient pane/form
state. It releases test-owned input before preparing the next run, waits for owner results and
reports ready, pending or the specific failure. Repeated resets should produce the same usable
starting state; they need not recycle object IDs or erase session history and evidence.

Keep unrelated inventory entries, files and unsaved work outside the reset boundary. Never use
two Escape presses as a universal reset contract. Refuse and explain when an owner cannot safely
reset affected work; partial completion is not success or an implied transaction. Discover the
small missing owner operations during preflight and add only those this story needs. A cold
restart of the owned isolated Workshop may be an explicit recovery option, but must be labelled
and measured separately from the required warm reset. It is not general undo of external effects.

## 4. Measure ceremony and latency at three layers

Take a baseline from the existing maintained story and its preparation, then repeat with the new
route on the same build/configuration. Count bootstrap/configuration work as well as steady-state
calls; bundling a large script into one command does not by itself show less total work.

| Layer | Report |
|---|---|
| Agent → ELH | Invocations/actions to prepare, run and reset; discovery calls and required manual setup listed separately |
| ELH → Workshop | Requests, replies/outcomes and round trips by operation/shape; distinguish input events batched in one request, polling, inspection and screenshot chunks |
| Inside Workshop | Observed operation-related deliveries, fan-out and longest attributable message chain; name the expensive/repeated paths and any unobserved portions |

Reuse Loom Recorder/Logger and run records with explicit retention sufficient for the sample.
ELH `Crossed` history observes the remote boundary; it cannot establish Workshop's internal
delivery counts. Collect those at Workshop's bus, and do not treat its application notice
journal as a complete message trace. Identify roots/correlations where available; label timer,
paint and other concurrent traffic separately. Mark incomplete retention/causal coverage as
incomplete, not zero. Count failures and retries too. Avoid creating a second logging subsystem.

Measure cold instance start-to-ready, warm setup load/ensure, warm reset-to-ready and the story
itself separately. Use monotonic elapsed time, owner/readiness evidence instead of fixed sleeps,
and a few repeated runs (for example five warm runs with median and range). Publish raw samples,
machine/build/viewport, measurement boundaries and recording overhead/limits. Keep screenshots
as explicit evidence work so their transfer cost is visible. Do not invent a speed target before
the baseline exists or spend this detour on broad benchmarking infrastructure.

The fixed interaction target is one command to prepare a ready setup and one button/command to
reset it. Reduce redundant discovery, reconnection, refresh and polling where the measurements
justify it. Preserve result checks, authority and ordinary owner contracts when reducing traffic.

## Delivery and proof

One goal-oriented implementation phase: trace and measure the old path; add comfortable sizes;
deliver one complete setup/reset route; reuse it for the second if bounded; prove and document.
These are checkpoints inside the work, not mandatory separate executor prompts.

Acceptance includes:

- Fresh panes with readable content; lists at beginning/middle/end; saved and hand-resized sizes
  preserved; older/no-hint providers; small viewports and real SDL/TUI metrics.
- A fresh documented environment reaching ready through the public command, then repeated warm
  load/ensure and reset on the same hosts. No leaked input, duplicate fixtures or stale targets.
- Missing provider, denied authority, lost connection and reset refusal/partial-failure results
  that identify the failed step. No accidental claim that the untouched maker's work was reset.
- A complete existing Inventory story run from the shipped setup, Reset through the visible
  button, and a successful repeat. Include screenshots on the PR and the three-layer metrics.
- Compact public help: prerequisites, list/describe/load/reset, scope, result and recovery.
  Zengine owns Workshop setup/tool guidance; Loom owns generic sessions/history. Future story
  tests extend these maintained recipes rather than copying a private launch script.

Follow the constitution's current-main branch, verification and buildable handoff rules. Keep
exploration/ceremony findings and evidence in the phase report. Implementation selects the exact
hint contract, reset action route and numbers from live checks; these are not settled product APIs.

## Roadmap and backlog disposition

This detour precedes named/incomplete command presets. Its purpose is to remove repeated setup
and cramped presentation from every later experiment. Return to the [Compose continuation](inventory-compose-motion-plan.md#after-the-setup-detour)
afterward: presets, missing-field completion and field acquisition through a real command story.
General workspaces, durable bags, persistence, undo and an animation framework remain outside.

BL-WORK-01 is active here: the public setup route must make the behavior understandable.
BL-WORK-02 remains preservation work; inspect the small provider witness when changing offers,
without turning demo recipes into a plugin SDK/project-template phase. BL-DEF-06 wakes if the
implementation edits pane-controls/pane-menu docs or the named tests; include that bounded wording
cleanup then. BL-VERIFY-01 remains parked unless its specific Builder field check/driver is reused.

## Implemented outcome and next use

Providers now offer version-2 body row/column preferences. Workshop resolves them through the
medium's text metrics and seats defaults by the same height it draws. Explicit sizes win; v1
providers retain the fallback. The two recipes use authored layouts in dedicated instances.
`external-host/demo.py` is the maintained list/start/status/reset/stop route. Python owns recipe
policy; an optional Demo weave exposes Reset and its attributed state. Workshop and providers
own setup application and transient reset. Reset preserves non-fixture inventory entries and
refuses pending owner work; it is intentionally not transactional or an undo system.

Windows SDL and terminal stories passed, including the visible reset and another edit/save.
The command story passed twice in the same SDL session. Five warm samples measured roughly
0.6 seconds to ensure readiness and 1.1–1.2 seconds to reset. Direct preparation is 7/8 owner
requests (values/commands), with service and requester coordination counted separately. Full
numbers and retention limits belong to the phase evidence, not the live roadmap.

After founder acceptance, use the `commands` setup for the selected named/incomplete-preset
story. Extend this existing recipe to expose missing fields, acquire a compatible value and
review/submit. Capture one before/after ceremony baseline without cloning process-launch code.
Choose persistence in that preflight; no cross-process inventory guarantee is implied here.

Pressure kept outside this detour: screenshots are expensive evidence transfers; complete-command
story run records can exceed their retained ask window. Broader supervision, arbitrary maker-desk
isolation, undo, collision-free tiling and packaged installers need their own concrete story.
These are observed limits, not newly authorized backlog work. BL-DEF-06 was awakened and its
bounded wording cleanup is implemented, awaiting founder acceptance at the backlog owner.
