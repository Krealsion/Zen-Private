# Zen Workshop Goal Map

**Status:** PRIVATE LIVE GOAL AUTHORITY  
**Refreshed:** 2026-10-03 UTC\
**Strategic authority:** `private/zen-strategic-map.md`  
**Current direction:** improve complete maker stories through typed inspection, authorized reuse and reusable ELH tools, alongside understandable Flow composition and replaceable presentation
**Current execution state:** Inventory foundations through named folders (#58), independent Info (#55), toolbox persistence (#54), Editor typed transfers (#59), the tower-defense creation story (#60) and event-driven ELH observation (Loom #16, Zengine #62) are accepted. [The tally panel](../../reportbacks/zengine-flow-powers/proving-story.md), accepted 2026-09-30 from [Flow's powers research](../../reportbacks/zengine-flow-powers-RB.md), is built in three reviewed stages: find (merged as #82), compose (merged as #84) and show (merged as #85), and the View Builder is worked by hand (merged as #86, 2026-10-03). The founder's order of 2026-10-03 (§7) began with the View Builder's polish, merged as #87 (pan, snap, side handles, the view's size and the weaver's grid), the quick desk fixes, merged as #88, and an executor process phase, merged as #89 (2026-10-04): a primary build folder, a helper kit, setups that carry their checks. The whole pixel (BL-WORK-05) is merged: stage 1 as #90 (2026-10-04), an authored place measured from the room, stage 2, what Workshop still paints itself, as #91 (2026-10-05), and stage 3, arranging by hand, as #92 (2026-10-05); agents reading the desk by messages (BL-WORK-24) is merged, in two stages as #93 and #94 (2026-10-06); the text panes on the canvas (BL-WORK-06) is merged, in four stages: the cell caret and the panes that list and show as #95 (2026-10-06), the medium's own ground and four more panes as #96 (2026-10-07), Info and Inventory and a terminal's own text colour as #97 (2026-10-07), and the Editors with the managed opening carrying a picture as #98 (2026-10-07), so every pane Zengine ships draws on its canvas; settings (BL-WORK-36) is next, researched first; the trial of waiting for hosted CI in place of the local MinGW-w64 lane passed and is the standard delivery (the founder, 2026-10-04). Flow composes; a UI builder beside it builds views; they meet at shapes. Tools, retained learning and repeatability outrank polish. UI update research and independent pane/editor UX remain parallel work. Conventional coding stays first-class; Flow is a consumer, not a prerequisite.
**Role:** current Workshop product truth, next capability boundary, and goal-local design laws

This map is forward-looking. Reports and Git retain phase history.

## 1. Product thesis

Workshop is where Zen becomes visible, useful, learnable, and authorable.

It should let a maker move among project declaration, live runtime, source, build, presentation,
diagnostics, and failure without each boundary becoming a different conceptual universe. The
boundaries remain because they protect ownership and truth; they stop being cliffs.

The workshop and the work are peers. Workshop may compose and present powers, but it receives no
ambient authority and should be built from the same materials it offers makers.

The beginner and the expert should perform the same underlying act. Convenience may remove
ceremony; it must not hide a different privileged mechanism.

Since 2026-09-06 the peer sentence above is direction, not aspiration (VD-19): every pane a maker
sees inside Workshop should become a participating weave loaded from the plan. Workshop
currently implements room and focus alongside realization and roots. A built-in pane written
as C++ inside the host is the debt this arc pays, one pane at a time.

## 2. Current maker capability

A maker can currently:

- launch the same Workshop install from different project directories while per-user config and
  state follow the maker rather than the CWD;
- use `--isolated` for a run that reads and writes no per-user Workshop state;
- restore the previous desk, normal window size, desktop position, and maximized state;
- name/save/restore pane layouts and inspect a real pane independently of selection or focus;
- load an explicit authored project plan and inspect both the resolved arrangement and the live
  power stack;
- keep unresolved pane intent without silently rewriting it;
- arrange overlapping panes on a fine lattice with shared paint/hit geometry, recovery, canonical
  front order, and independent-axis settlement;
- use the same application meaning through TUI and SDL media;
- discover and remap one keyboard action truth used by dispatch, help, and contextual presentation;
- right-click a room or pane (or use the keyboard door) to see actions meaningful to that
  subject, without pointing becoming selection;
- see standing conditions in Attention while transient event reports remain on the notice row;
- choose an authored build recipe, build it, and offer its artifact to the live realization owner;
- see a pending project frontier and realize it without skipping authored order;
- compose and submit a message from a selected target's actual accepted shapes;
- open the one source named by a selected single-source recipe, edit it normally across lines, save
  exact admitted bytes, build, realize, inspect, and return to editing.

Since 2026-09-05 (EDIT-1; build-then-load, Zengine PRs #11–#14) a maker can also:

- open Project Files inside the captured project root and open any source through the one
  Editor-owned `open(path)` door — Builder is no longer the only source referrer;
- rebuild a live weave-only artifact and have it **reload in place**, state kept, on the same
  `WeaveId`, through the realization owner's one conversation with the Manager (`zen.ReloadWeave`);
  arm "load when built" before the build or press "load now" after it — one action, one button;
- **promote** the reloaded image to the default the next launch loads (a same-bytes atomic write),
  or **revert** to the previous image; until promoted the row says so — nothing is upgraded silently;
- **pick a buildable** (an explicit gesture that enumerates once; a `.cpp`, or a configured CMake
  tree) and, by choosing it, author a recipe row; **load it** authors the minimum plan row with a
  role the maker types; a project catalog and a project plan at the project root are the truths
  in force at the next launch, so the maker's rows survive a restart without flags;
- read a realize refusal whole in the `--log` journal (it has no reader yet — see the pressure board, P-WORK-14).

The subsequent accepted work closes pane-to-source acquisition and the Workshop development
launch: a maker can reach a pane's code, build its owning artifact, and develop the participating
Workshop behind a separate host. The standalone Loom/admission-policy arc is also merged.
Evidence and boundaries are in the [pane-to-source correction report](../../reportbacks/zengine-pane-to-source-loop-corrections-RB.md),
[development-launch correction report](../../reportbacks/zengine-workshop-development-launch-corrections-RB.md),
and [standalone-host correction report](../../reportbacks/loom-standalone-usability-corrections-3-RB.md).

The founder reports the live standard/Neovim switch working as envisioned. Its
[report](../../reportbacks/zengine-neovim-live-switch-RB.md) describes active-document handoff,
unsaved edits, caret/representable selection, and baseline Loom use through a second terminal.
This is an implemented editor-specific replacement consumer. It does not establish a generic
changed-schema development workflow. The founder merged PR #33 on 2026-09-17 as
`7f553c3858083da37bb64a7de73e3a6680810fca`; its tree matches the report head `9046fdd`
exactly. This records founder acceptance and merge, without claiming an independent full review.
Read live Git for current disposition.

The prototype object-document canvas and old picker are retired by accepted PR #35. The
desktop weave owns application defaults, Pane Manager and Hotkeys; Info inspects real panes.
The broader UI-editing overlay remains future work (§7).

External-host input/capture/inspection is available through the admitted loopback connection
and reusable probe from PR #38. Flow now supports standalone authoring/native generation (#40),
a graphical Workshop pane with reusable typed drafts (#41), and measured native text, a black
ground and safe resize previews (#42). Node dragging and pan/zoom already exist. The founder
reports that the overall authoring experience is confusing; merged functionality does not
establish learnability or resolve changed-motion rendering cost. The current
[Flow guide](../../Zengine/docs/workshop/flow.md) and
[external-host guide](../../Zengine/docs/workshop/external-host.md) own the working interfaces.

## 3. Current ownership model

### Application authority and presentation ownership

Workshop coordinates its application within the authority supplied by the hosting process.
It currently implements presentation ownership: room, pane arrangement and focus. That implementation location is not a permanent
ownership constraint. The founder favors keeping presentation movable into its own weave,
with Workshop connecting the participating subsystems and applying application policy.
Name the application authority, presentation owner and document owner separately when a
design crosses them. Moving presentation must not require surrendering the Editor weave's
document custody. For the first manager design, keep composition and output selection together
with a clear potential separation. Replaceability does not promise that every future change is
local: expose the affected contracts so cooperating changes can propagate through authored
migrations, adapters, tools or maker intervention, including honest partial results. Avoid
requiring all those tools or service splits in the first implementation. Actual presentation
extraction is now part of the selected architectural direction: "gut the shell" means make
remaining fixed application behavior replaceable. Each production phase still names the owner it
moves and the consumer that needs the seam. The minimal host/authority root remains outside
application-controlled replacement or relaunch; application behavior should not gain that
immovability merely by being implemented there today.

The desktop is now a replaceable participant with a pane launcher, declared application
defaults and attributable unavailable-tool feedback. It remains distinct from the fixed
hosting/authority root. Workshop still owns application coordination, room, arrangement and
focus. Optional tool failures leave the desktop available; essential desktop/display failures
retain the host/console diagnosis and relaunch boundary documented by the accepted phase.

### Failure and supervision

Authored weaves may fail, remain silent or stay pending indefinitely. Those are valid program
behaviors; the architecture does not owe universal successful completion. Zengine's shipped
components should preserve work and make failures or unfinished operations attributable to the
relevant intent, participant and observed stage. Absence of an answer is not a diagnosis.

Managers supply external observation and recovery policy within their authority. They may help
the application continue without solving the original operation; they too remain authored
participants that can fail. Establish the high-level owner and what it can actually know
before treating a missing interaction as evidence for a new substrate primitive.

### Authored continuity and repair

The application chooses what replacement does to current work: refuse or wait, transfer it,
update a running instance, let old instances finish while new instances use new code, or discard
state the domain does not need. A handoff may occur within that authored transition. New-work
routing, running-instance lifetime, state transfer and retirement are separate decisions;
Zengine's default is not the only valid policy. Supported mechanisms must earn the particular
policy's promises rather than assume that loading a successor provides them.

The founder's recovery direction is inspect, repair and continue useful work, even when a maker
returns to the failure much later. Retain attributable evidence by deliberate policy, show its
gaps, and keep the relevant operation and participant reachable. Repair may use a diagnostic
conversation, a rebuilt artifact with an authored handoff, an attached debugging weave, or an
isolated specimen for investigation. These are options to enable as needed, not mandatory
features for every weave. Inspection and intervention receive only their granted authority;
preserved data does not by itself restore a native continuation, resource or answer right.

Zengine is a place to start, not a place to end. Its useful defaults should leave makers room
to author different managers, continuity policies and debugging tools. The
[presentation-manager draft](../drafts/presentation-manager.md) explores these principles;
its source research distinguishes current support from capabilities still to be built.

### Project and user files

```text
project truth
    object document
    named pane setup
    load plan
    build recipes
    source files

user config
    keymap
    preferences

user machine state
    last session / the layout run and which one was live / viewport / window placement

installation truth
    executable and shipped default plans/recipes/artifacts
```

The host captures the launch directory once as `HostContext::project_dir`; a failed capture is
explicit absence. User config/state have their own roots. Relative recipe sources resolve against
that captured project before either Editor or Builder uses them. Current law and witnesses:
`Zengine/agents/workshop/project.md` (WL-PROJ-01, WL-PROJ-02).

### Authored, resolved, and presented

```text
authored setup
    PaneRef + sparse place/size override + canonical front rank

live owners resolve
    provider/catalog presence
    medium capability
    canvas room
    clipping and overlap

Workshop presents
    one ordered pane geometry for paint, hit, state, recovery, and provider room
```

A pane reference identifies intent. It is not a WeaveId, loaded image, provider lifetime, or proof
of availability. One PaneRef still mounts at most once.

### Build and realization

```text
recipe catalog        how an artifact can be produced
load plan             how an artifact participates
artifact stem         the only authored join
live realization      what has actually settled in this process
```

Builder owns production procedure and operation status. The realization owner owns authored order,
eligibility, load outcomes, and the waiting frontier. A successful process exit is not proof that an
artifact exists, and a produced artifact is not permission to load or replace it.

### Editor

The current holder of the Editor office owns its document state. The standard editor has one
document and reusable buffer mechanics; Neovim owns its buffers and editor-specific behavior.
Workshop coordinates opening, presentation commitments and supported office replacement without
becoming a second document owner. Current contracts live in Zengine's routed `editor`, `opening`,
`editor-switch` and `neovim` owners and the public editor-switch reference.

The standard editor's exact admitted-byte model remains narrower than Neovim's. Switching carries
the active document's edits, caret and representable selection; unrepresentable transfer is said
or refused as documented. Other state may reset under the explicit loss/consent policy. Frequent
editor swapping is a demonstration/experimentation use, not the assumed normal workflow.
Ordinary dirty-work and quit protection remains separate. The editors serve different audiences
and should grow distinct strengths; cooperation does not require feature parity.

## 4. Laws the next phase must preserve

- **A source may suggest a document; the Editor owns opening and editing it.**
- **Each editor owns its document lifecycle.** Standard-editor tabs are a selected follow-on,
  not permission for the host to mirror documents or require identical editor features.
- **Presentation never owns document lifetime.** Removing, hiding, or arranging the Editor pane
  cannot discard the buffer.
- **The same geometry draws and hits.** This applies to panes, menus, text, selections, and file rows.
- **Workshop owns room; a provider owns meaning within the room it was granted.**
- **Pointing names a subject for one request. Selection is ongoing maker state.**
- **Open remembers identity; spend re-asks the owner.** Do not cache liveness or applicability in
  contextual presentation.
- **An action is one truth.** Menus reference action identity; they do not duplicate labels,
  gestures, callbacks, or availability policy.
- **Standing conditions and event reports have different lifetimes.** A condition retracts when
  its source fact stops being true; it is not a toast or unread history.
- **The keymap may promise only gestures every supported backend can actually deliver.**
- **A deferred editing operation is pinned to both document identity and edit sequence.**
- **Build and realization are maker gestures.** No automatic build-on-missing, per-paint disk probe,
  directory scan, or implicit hot reload.
- **Refuse unknown or unsupported values whole.** Preserve authored intent through current inability
  to project it.
- **A pane declares its actions; the host assembles the keymap.** One action truth is one
  identity, not one file: rows arrive with the pane weave, the host joins them at load and runs
  the collision law then. A pane's rows act only while the pane has the keyboard; no command-mode
  key acts on a migrated pane's subject from anywhere — the maker points at the pane first
  (VD-22). Buttons, hover, or the host mapping a key to a weave's action are later UX, not defaults.
- **A plan row asks for authority.** It confers none; the host's policy decides, may refuse, and a
  refused weave is told.
- **The pane protocol grows from demonstrated consumers.** A pane needing something it cannot
  truthfully express can justify a shared contract; migration is no longer its only consumer.
  Preserve replaceability without erecting a speculative plugin framework.

## 5. Completed capability arcs, compressed to their surviving results

### Grounding and legibility

Workshop proved ordinary object creation, selection, editing, persistence, and truthful refusal
without new privilege. Graphical and terminal media now carry one application meaning. Semantic
type, bounded prose, panels, dynamic extents, messages, and introspection are current product
material rather than future scaffolding.

Target acceptance discovery and Message Composer demonstrated a general rule: the target owns its
vocabulary, and discovery and enforcement spend the same schema truth. `SUBMITTED`, delivered, and
semantic success remain separate facts.

### Operators, providers, and authored project structure

Typed operators are synchronous value computation, neither Messages nor Senses. Primitive power is
native only when Zen cannot express it; composites reuse the host's live catalog. A loaded provider
may supply many panes, operators, or weaves without those logical surfaces becoming identical.
Durable references keep provider/operator identity; invocation resolves and holds the current
implementation at spend.

Authored load plans replaced compiled-in project participation. Provider overlays are reversible and
their provenance is inspectable. The Builder later added a separate authored recipe catalog and a
bounded route from build success to realization. Project structure is explicit list, never ambient
directory scan.

### Product custody and continuity

Workshop now separates project files, roaming user config, and machine-local session state.
Named setups preserve maker intent; the last session returns the DESKS automatically -- every
layout the maker authored, in their order, under their names, standing on the same one (WUX-10) --
while a named setup file still holds exactly one desk; the document remains an explicit open. Window placement is observed and validated by the graphical medium, not
guessed by Workshop. The TUI claims no desktop placement and preserves the remembered graphical
value.

### WUX

WUX left five product truths:

1. graphical prose uses the medium's actual type metrics while TUI retains an honest cell
   projection;
2. pane geometry lives on a fine shared lattice and every resize preserves the opposite anchor;
3. independent axes settle independently, while an axis-local anchored position/extent pair is
   atomic;
4. Workshop behaves like an installed application with per-user roots, isolated runs, durable
   preferences, and display-aware placement restoration;
5. Attention owns current standing conditions; the notice row owns completed events.

### Build/test optimization and Loom SDL removal

Compile-judged tests no longer configure or regenerate the main Zengine build tree. They use an
isolated fixture tree and serialize only that writer. Two concurrent build operations use two build
trees. Workshop's tests are split by semantic ownership with shared support. The repository
verification routes own the current population and lane measurements.

Loom removed its unused SDL executor, demo, tests, FetchContent graph, and licensing edges only
after proportional type metrics and the medium-agnostic outline law moved into portable coverage.
The installed Loom surface is unchanged; Zengine remains the SDL product consumer.

### Context and arrangement

Context is a projection of actions meaningful for a subject kind. It carries no second command
system. Pane actions spend explicit PaneRefs; object actions spend object IDs; owners judge live
applicability. Right-click changes neither selection nor keyboard focus. Move/size became one
pane-local Arrange state, and the whole desk is a second scope over the same vocabulary.

### EDIT-0

The source editor is a competent conventional multiline editor: caret/selection, preferred-column
movement, word/document navigation, multiline clipboard and undo/redo, mouse placement/drag,
viewport following and wheel scroll, exact tab geometry, atomic save, dirty refusal, and deferred
paste sequencing. It edits one source document and intentionally does not imitate Vim, provide
language tooling, or create a generic multiline widget hierarchy.

## 6. EDIT-1 — Choose What to Edit — LANDED

With no useful Builder source selected, a maker can navigate Project Files within the captured
project root, open a source through the Editor's one path door, edit and save it, then use Builder
independently. Editor and build share the resolved source path; dirty refusal and byte custody
remain the Editor's responsibility.

Current owners: `Zengine/agents/workshop/project.md`, `editor.md`, and `files.md`.
The old production checklist and its decisions are history in the EDIT-1 reports and Git.

## 7. The next maker loop after EDIT-1

The development loop remains the product spine:

```text
point at a running tool -> Edit Code -> edit -> save/build -> realize or replace -> inspect
```

Pane-to-source acquisition and Workshop development launch have landed. The Neovim integration
demonstrates an editor-specific authored replacement; a generic changed-shape rebuild/handoff
workflow remains later work. Build recipes, load plans, document custody and realization keep
their separate owners. The next goal is to make this environment comfortable to inhabit,
understand and reshape. The founder selected this roadmap on 2026-09-17 after hands-on use.

### Pane extraction: current status and next work

Files, Builder, Attention, Info, Terminal and Editor are pane weaves. The selected extraction and
bounded interaction repairs through Files action identity are accepted and merged. Their reports
and Git retain the acceptance history; the live source and routed laws own exact mechanics.
Pane Manager, Hotkeys and application defaults now belong to the desktop weave. Layouts and
remaining host-owned presentation remain candidates for later shell work, not permanent exceptions
to the peer-tool direction.

Everyday interaction PR #34 is accepted and merged on 2026-09-17 as
`be1231112c20a3bbcb13f0012ec1042f85c99744`, with the same tree as reviewed head `633f778`.
The [correction report](../../reportbacks/zengine-everyday-interaction-corrections-RB.md)
routes the Escape correlation repair and its evidence. Refresh live Git before execution;
preserve this interaction behavior and the demonstrated editor capability.

### Near-term order and purpose

The retired object canvas supplied useful interaction ideas; its former document and host
ownership stay retired. Hands-on Flow use and the founder's 2026-09-21 discussion now join around
complete maker stories: start from a stated setup, create something, inspect it and improve the
route. Shared inspection and authority work supports Flow and agent participation without
serializing unrelated pane/editor or UI-update work.

| Order | Outcome | Purpose and boundary |
|---|---|---|
| Accepted foundations | Desktop #35, schema admission Loom #8 / Zengine #36, external control #38, pane UX #37, Flow #40/#41/#42 and reusable sessions Loom #10 / Zengine #39 | Reuse existing ownership, schemas, drafts, authorized connections and sessions. A merged mechanism does not establish intuitive UX or every downstream authority promise. |
| Accepted maker story | ELH Workshop improvement, Loom #11 / Zengine #44 | Reusable recipe-authoring route, maintained tool checks, native interaction evidence, loaded-module identity and continued session context. Multi-config recipe authoring resolves P-WORK-16. See the [completion report](../../reportbacks/zengine-elh-workshop-improvement-completion-RB.md). |
| Accepted inventory foundation | Capture, collection and Info editing through #47 | Owned typed data and separate metadata, stable process-local identities, copy dragging and secondary live-reference editing. |
| Accepted maker story | [Inventory to Compose and timed motion](../../reportbacks/zengine-inventory-compose-motion-RB.md), PR #48 | Fill compatible forms, store complete commands and explicitly submit with actor authority; demonstrate through state-reactive ELH orchestration. |
| Accepted maker story | [Comfortable panes and reusable test setups](../../reportbacks/zengine-comfortable-demo-setups-RB.md), PR #49 | Per-pane initial comfort, one-command demo setup, visible warm reset and measured agent/ELH/host ceremony; reuse existing Inventory/Info and Compose stories. |
| Accepted; #50 merged | [Reusable command presets and field acquisition](../../reportbacks/zengine-inventory-command-presets-RB.md) | Start blank or work backward from a complete command, unset values, retain incomplete drafts, fill gaps from saved typed records and explicitly run with current authority. |
| Accepted; #51 merged | [Portable inventory views and contextual hotkeys](../../reportbacks/zengine-inventory-portable-slots-RB.md) | Single boxes and row/column strips over owned entries; move/reorder/displace without data loss; duplicate independently; retain copied bindings disabled; explicit activation and per-invocation authority. |
| Merged; Loom #13 / Zengine #52 | [Terminal acquisition](../../reportbacks/zengine-terminal-inventory-capture-RB.md) | Retrieve real typed command/results at their retention and authority owner. Independent Info views, folders and durability follow demonstrated tasks. |
| Accepted; Loom #14 / Zengine #53 merged, CI green | [Easier interaction authoring](../../reportbacks/zen-interaction-authoring-RB.md) | Shared request mechanics, one explicit native grant owner, attributable missing replies and an exercised loaded-pane guide. Application policy and pending remain explicit. |
| Merged; #54 | [Durable toolboxes](../../reportbacks/zengine-inventory-persistence-RB.md) | Explicitly save and restore typed data and portable configuration across restarts; reduce executor fixture setup to one owner operation. Fresh live references and inactive restored hotkeys preserve authority boundaries. |
| Accepted; #55 merged | [Independent Info workbench](../../reportbacks/zengine-independent-info-workbench-RB.md) | Keep sample and draft views side by side, transfer typed fields, watch linked entries without losing edits, sample supported sources explicitly and reuse a filled toolbox. Visible controls and bounded view lifetime make the story usable. |
| Accepted; #58 merged | [Named Inventory folders](../../reportbacks/zengine-inventory-named-folders-RB.md) | Organize growing toolboxes through nested names, immediate-child views, parent/root navigation and identity-preserving moves; retain hierarchy across save/restore and reuse entries through Info, Compose and portable slots. |
| Accepted maker story; #60 merged | [Tower defense creation story through ELH](../../reportbacks/zengine-tower-defense-creation-story-RB.md) | Complete creation/play/reload route and durable tools, with the reviewed reliability repairs and positive maker-authorized toolbox witness. The [second correction report](../../reportbacks/zengine-tower-defense-creation-story-corrections-2-RB.md) retains evidence; preserve the original experiment's declared boundary deviations. |
| Accepted; Loom #16 / Zengine #62 merged | [Event-driven ELH observation and monitors](../../reportbacks/elh-event-driven-observation-RB.md) | A reusable ELH run subscribes with authority, follows its Builder operation, then monitors gameplay and returns completion/deviation with evidence. Latest claims, occurrences and history stay distinct, and operation identity survives gaps, waits and cancellation. |
| Accepted maker capability; #59 merged | [Editor typed transfers](../../reportbacks/zengine-editor-typed-transfers-RB.md) | Both editors participate in typed reuse: incoming text/commands, selected-text capture, explicit C++ generation and saved file locators. Conventional coding remains first-class; no Flow dependency. |
| Find (#82), compose (#84) and show (#85) merged, 2026-10-02 | [The tally panel, in three stages](../../reportbacks/zengine-flow-powers/proving-story.md), from [Flow's powers research](../../reportbacks/zengine-flow-powers-RB.md) | **Find:** one read-only discovery door over the live catalog, prose carried in each contribution, Flow's palette over the door, Powers browsing through it and the Terminal asking it. **Compose:** the evaluation budget first, then operator references, with Add able to place a node before the one selected, the bounded fold loop, Flow's carry receivers, emit authoring and integer addition. **Show:** a view description, view host, renderer and UI builder beside Flow, joined to it by shapes. Each stage is reviewed on its own. |
| Merged; #86 (2026-10-03) | [The graphical View Builder](../../prompts/view-builder-canvas.md) | The View Builder becomes a tool worked by hand: a palette to drag element kinds from, an element list, and a design canvas drawn by the view's own renderer, with drag to create, move and resize, a hover highlight and click to select; values edit in fields with boxes. A canvas pane drags values out and hears the pointer hover. |
| Merged; #83 (2026-10-02), between the tally stages | [Default pane menu](../../prompts/zengine-default-pane-menu.md) | A right press in a pane's body never vanishes: the pane acts or offers its rows where it has something there, and the standard pane menu opens everywhere else. A pane's own rows sit above the standard rows in one menu. Taking a pane off the desk is called hide, and a row that opens another menu ends in ` >`. |
| Merged; #87 (2026-10-03) | [The View Builder's polish](../../prompts/view-builder-polish.md), with [the view's size](../../prompts/view-builder-size.md) ([BL-WORK-07](../backlog.md#bl-work-07--the-view-builders-polish)) | A middle-button drag pans the design canvas; a place by hand snaps to other elements' and the view's edges, and to a grid only when the weaver sets one, Alt setting every snap aside; each side has a handle. A view has a size it is drawn in and asks its pane for, its notice rows beneath it. |
| Merged; #88 (2026-10-04) | [Quick desk fixes](../../prompts/quick-desk-fixes.md) ([BL-WORK-08](../backlog.md#bl-work-08--quick-desk-fixes)) | The window opens whole on the screen and centred; Layouts is on every desk; Escape deselects as every pane's default; `demo.py` says a start and a stop truly; Inventory holds 36 views and 512 hotkeys, all of them on at once, and a desk 96 panes. |
| Merged; #89 (2026-10-04) | [Executor process](../../prompts/executor-process.md) | From #88's measured wall clock: one primary build folder kept between phases, a maintained helper kit (`pass-tools/executor-kit/`), and setups that carry replayable walks (`demo.py walk`). The Windows trees gain a compile cache in its follow-up. |
| Merged; #90, #91 and #92 (2026-10-04 to 2026-10-05) | [The whole pixel](../backlog.md#bl-work-05--workshops-unit-becomes-the-whole-pixel), and what Workshop still paints itself | Stage 1, the unit and canvas panes in pixels ([prompt](../../prompts/whole-pixel-1.md)); stage 2, what Workshop still paints; stage 3, arrangement snapping, and a launched pane that always lands where the weaver can see it (the founder, 2026-10-04 and 2026-10-05). Stage 1 merged as #90 (`2c06da5`, 2026-10-04), with an authored place measured from the room ([prompt](../../prompts/whole-pixel-1-room.md)); stage 2 merged as #91 (`5901b39`, 2026-10-05) with three review findings (BL-DEF-09) and nothing kept for the Pane Creator; stage 3 merged as #92 (`567f983`, 2026-10-05) ([prompt](../../prompts/whole-pixel-3.md)), with BL-DEF-10 and its review's fixes ([follow-up](../../prompts/whole-pixel-3-fixes.md)). The hosted-CI trial rode with stage 1 and is now the standard delivery: the executor reads the hosted run to its end in place of the local MinGW-w64 lane (the founder, 2026-10-04). The pixel becomes Workshop's unit. The grey workspace behind the panes goes, Attention's indicator moves into its pane, the Pane Creator retires into described views ([BL-WORK-04](../backlog.md#bl-work-04--the-pane-creator-retires-into-described-views)) and arrangement mode snaps (P-WORK-10). |
| Merged; #93 and #94 (2026-10-06), in two stages ([stage 1](../../prompts/desk-by-messages-1.md); [stage 2](../../prompts/desk-by-messages-2.md)), ordered fourth since 2026-10-05 so the rest proceeds smoother | [Agents read the desk by messages](../backlog.md#bl-work-24--agents-read-the-desk-by-messages), with [agents acting by intent](../backlog.md#bl-work-25--agents-act-by-intent) beside it, ongoing | A canvas pane answers too, so BL-WORK-06 keeps every pane it moves readable. An agent works from messages alone: stable IDs, with places and sizes as numbers in pixels that tests prove match what is drawn. It states an intent in one dense message carrying the whole idea, and each story makes more intents solid. |
| Merged in four stages, 2026-10-06 to 2026-10-07 ([stage 1](../../prompts/text-panes-canvas-1.md), as #95; [stage 2](../../prompts/text-panes-canvas-2.md), as #96; [stage 3](../../prompts/text-panes-canvas-3.md), as #97; [stage 4](../../prompts/text-panes-canvas-4.md), as #98); settings next, researched first | [The text panes on the canvas](../backlog.md#bl-work-06--the-text-panes-draw-on-the-canvas), then [settings](../backlog.md#bl-work-36--settings-what-a-pane-can-set-kept-with-each-layout) (the founder, 2026-10-07), then [what that unlocks](../backlog.md#bl-work-09--what-the-canvas-unlocks-for-every-pane) | Every pane draws in pixels. Then what a pane can set is kept with each layout and edited by message, so a fork can be a setting rather than a choice. Then every pane can have a hover cue on what a press activates, a `?` for its guide, and a tutorial mode that outlines its own parts. |
| Ordered 2026-10-09, ahead of BL-WORK-09 (decision 18, in part); stages 0, 1 and 2 merged as #150, #151 and #158 (2026-10-09), stages 3a and 3b after the documentation overhaul's folder move and stages 4a and 4b ([BL-ADOPT-05](../backlog.md#bl-adopt-05--the-documentation-overhaul-a-man-page-on-each-weave-a-tutorial-for-each-step)) ([stage 0](../../prompts/agent-desk-0.md), [stage 1](../../prompts/agent-desk-1.md), [stage 2](../../prompts/agent-desk-2.md)) | [Agents and weavers on one desk](../backlog.md#bl-work-38--agents-and-weavers-on-one-desk), stage 0, then stages 1 to 3b, from [its research](../../reportbacks/agent-desk-research-RB.md) | Stage 0 closes the open path first: on a weaver's host no door of the desk takes a guest's bytes, source, keys toward an editor or the Terminal, typed text or a file write. Stages 1 to 3b then let an agent read the desk whole as text, follow it by notices and act through one judged door, so the phases after them are built by agents on the desk. Where BL-WORK-36's later stages fall is decision 18's, still open. |
| Ordered 2026-10-09, beside the desk's stage 2; the guide up for review as Zengine #159 and Loom #38 (2026-10-09), the founder's answers taken the same day: links into `agents/` kept, a claim told in status comments, an outside contributor authoring as themselves, the weave-first principle in `AGENTS.md` ([continuation](../../prompts/agent-guide-2.md)) | [A guide to taking an issue, and best practices](../../prompts/agent-guide.md); [faster builds, researched first](../../prompts/fast-builds-research.md) | The founder's working window runs to 2026-10-26: a release proposed for 2026-10-24, features frozen 2026-10-23, the work then carried on in small pieces. Agents take bounded issues from the repositories alone, with best practices beside the cheat sheet; and a pane rebuilt alone against its vocabulary and Loom, loaded into a running Workshop, from a cached and shared build. |
| Ordered 2026-10-03; sixth since 2026-10-05 | [Accordions and anchors, researched first](../backlog.md#bl-work-16--accordions-and-anchors-researched-first) | A research phase, then the work: a weaver shows and hides the parts of a pane, or the pane itself, with an accordion, and anchors a pane's place to another pane or an edge so placement follows. |
| Ordered 2026-10-03; seventh since 2026-10-05 | [Files answers a request for a path](../backlog.md#bl-work-17--files-answers-a-request-for-a-path) | A file picker of Workshop's own: a pane asks and Files answers with the path the weaver chose, with a typed path line, the marks as quick places in an accordion, filters and a name line for saving. |
| Ordered 2026-10-03; eighth since 2026-10-05 | [Info rebuilt as a one-slot inspector](../backlog.md#bl-work-10--info-rebuilt-as-a-one-slot-inspector) | Info takes anything dropped on it or picked in its selection mode, and edits it in fields with boxes. It shares each pane's parts and boxes with the tutorial mode. |
| Ordered 2026-10-03; ninth since 2026-10-05 | [Images](../backlog.md#bl-work-11--images) | The canvas draws an image, and a view description holds one; a terminal shows a fallback. |
| Ordered 2026-10-03, tenth | [Load metadata, researched](../backlog.md#bl-work-26--load-metadata-researched) | What a weave was loaded from, by whom and when, discoverable through its contract, each fact with its owner; metadata grants nothing. |
| Ordered 2026-10-03, eleventh | [A dead weave's last state, inspectable](../backlog.md#bl-work-27--a-dead-weaves-last-state-inspectable) | The owner still holding a dead weave's last state offers it, typed, saying what kind of value it is; looking never restores. These two close the current arc. |
| Ordered 2026-10-03, later | [Multiple windows](../backlog.md#bl-work-12--multiple-windows), [GitHub from Workshop](../backlog.md#bl-adopt-04--github-from-workshop), [Python scripts as participants](../backlog.md#bl-work-13--python-scripts-as-participants), [an app of its own, edited live from Workshop](../backlog.md#bl-work-35--an-app-of-its-own-edited-live-from-workshop) and, at the very bottom, [undo and time travel](../backlog.md#bl-work-33--undo-and-time-travel) | Each after its own research, when the founder selects it. Undo and time travel come last of all: undo of real effects, then full undo and time travel for demos. |
| Parallel product/research | UI update optimization, pane UX and expressive editors | Measured rendering work, with the view renderer as UI update's first consumer, and independent pane/editor improvements. Shared input/authority contracts need coordination; unrelated improvements continue. |
| Following concrete dependencies | Full UI-editing overlay, protected experimentation/publication and broader schema/migration work | Typed inspection is useful before complete UI authoring. State custody and enforcement must exist before promising protected originals. |
| Backlog; not implemented or selected | [Terminal command scripts (`.zenscript` idea)](../backlog.md#bl-work-23--terminal-command-scripts) | Repeat commands as if sent through Terminal, with explicit authority and completion/failure behavior. The name is a proposed convenience, not an existing language or part of the Editor packet. |
| Later consumers | Deeper setup/configuration, reusable effects, Python, GPU and broader multi-host work | Demonstrated stories earn scope; no universal framework or complete renderer is a prerequisite. |

These are capability boundaries, not mandatory research/implementation handoffs or arbitrary PR
counts. Each executor packet should carry its bounded goal through preflight, implementation and
proof. Independent editor fixes can proceed when they do not depend on an unsettled presentation
contract. Full overlay authoring, all standard-editor features and protected storage need not
land together. Service retirement and generic changed-schema migration remain separate work.

### Complete maker stories and reusable information

The founder selected complete 0-to-demo stories as a unit of development: stated setup,
useful creation, a reusable route and evidence another maker can check. A session can research,
implement and prove its bounded goal; preserve the exploration timeline, important discoveries,
ceremony and context-compaction findings. GUI, TUI and structured ELH routes reach the same
semantic owners. Scope and proof can support autonomous story work; shared meaning, authority,
persistence and replacement decisions remain founder-directed.

The maker-story arc's remaining research is in the backlog: load metadata
([BL-WORK-26](../backlog.md#bl-work-26--load-metadata-researched)) and a dead weave's last state
([BL-WORK-27](../backlog.md#bl-work-27--a-dead-weaves-last-state-inspectable)). The
[inventory capture report](../../reportbacks/zengine-inventory-capture-RB.md) holds its first story.
Resolve a selected pane subject to its actual data owner and supported
schema/value retrieval. A temporary info box can follow the source, become a pinned view,
yield an independent copy or save typed content for later. Reuse message-draft traversal and
schema-bearing libraries; distinguish live replies, observations and recovery snapshots.

Research metadata in the weave contract: author descriptions and host-observed loaded file,
requesting/loading actor, load time and incarnation. Name each fact's owner and lifetime;
do not infer human identity or mutate schema identity with per-load observations. Inspection
and cross-pane use are maker actions, with separately granted ELH equivalents. Preserve the
originating actor through privileged UI; approval requires its own Weaver/operator authority.
Any development bypass is compiled out of default builds. Exact mechanisms remain research.

The founder selected inventory as the concrete home for captured material on 2026-09-22. First,
one weave slot stores a pure typed item paired with a separate automatically collected list of
typed metadata, including nested structured observations. Item and metadata retain their own
decoding schemas; unavailable optional facts stay absent. Set replaces the pair together, and
Get yields independent data without executing actions or reviving the source's authority.
Capture, collection and Info editing own process-local live state. The merged toolbox phase
(#54) adds explicit disk save/restore; automatic recovery remains unselected.
The [implemented Compose phase](../../reportbacks/zengine-inventory-compose-motion-RB.md)
extends reuse without changing the pair/authority boundary.
The [preset](../../reportbacks/zengine-inventory-command-presets-RB.md),
[portable-view](../../reportbacks/zengine-inventory-portable-slots-RB.md) and
[acquisition](../../reportbacks/zengine-terminal-inventory-capture-RB.md) reports hold the accepted
behavior; Inventory's next options are backlog items BL-WORK-18 to BL-WORK-22. Several views should refer to the same owned
entries while keeping their own arrangement and editing state. Slot placement, collection identity
and execution remain distinct; sorting must not silently redirect a pinned hotkey. Typed Terminal
acquisition now uses its actual retention/authority owner. Independent Info views now provide
separate editing state, routed replies and bounded lifetime; named nested folders are accepted in #58.
The [creation story](../../reportbacks/zengine-tower-defense-creation-story-RB.md) (#60) put these
tools to work on a playable tower defense game and a reusable demonstration of how it was made.
The longer-term inventory can organize code/data/schemas into bags, represent unavailable sources
and saved actions, and support dependency discovery/build/load. Drag-out follows the same transfer
meaning as dragging from a pane. The accepted generic preset path now supplies the first portable-view story.

### Flow UX research and hierarchical authoring

**Accepted 2026-09-30** ([Flow's powers research](../../reportbacks/zengine-flow-powers-RB.md)): Flow composes, and only
composes: operations, and a participant's reactions, with one semantic edit model and the
discovery of what to compose. Discovery asks one read-only door over the live catalog; each
operator's prose rides in its own contribution; the maker's folders are Inventory folders of kept
references; Powers is repurposed to browse through the same door. Examples are Inventory's typed
values, carried in and out. A presenter/view pair is an assembly of a Flow-made presenter and a
builder-made view: UI building belongs to a UI builder beside Flow, and participants never become
nodes in an operator graph. A loop is an evaluator-owned form that runs an operator reference,
bounded per loop and by a per-evaluation spend budget that lands first. The
[power map](../../reportbacks/zengine-flow-powers/power-map.md) and [pattern map](../../reportbacks/zengine-flow-powers/pattern-map.md) hold the
reasons; the tally panel stages in the table above hold the order.

**Decided 2026-10-02:** the Pane Creator (WL-MAKER), a pane of static text regions that Workshop
paints and the research missed, stays beside described views and retires into them after the
graphical View Builder; described views already draw on the canvas in whole pixels ([BL-WORK-04](../backlog.md#bl-work-04--the-pane-creator-retires-into-described-views)).
A pixel-first Workshop, its terminal picture derived from the window's, is ordered third and
fifth in the table above ([BL-WORK-05](../backlog.md#bl-work-05--workshops-unit-becomes-the-whole-pixel),
[BL-WORK-06](../backlog.md#bl-work-06--the-text-panes-draw-on-the-canvas)).

**Selected:** make the first useful Flow understandable and directly manipulable, then support
reusable operations with inspectable interiors. The founder asks for a folder-like palette with
input/output previews, drag-out creation and connection, movable nodes, and navigation into
composites. [The Flow UX plan](../drafts/flow-ux-research.md) owns the detailed task journeys,
candidate layout, capability gaps, milestones and unresolved decisions. It is a research/design
plan, not an approved implementation of every proposal. The
[initial research](../../reportbacks/zengine-flow-ux-research/research-result.md) now includes an
isolated live journey, source/terminal audit and interactive study. It recommends independent
operation composition alongside message-driven authoring, with one shared semantic command
model. Terminal participation is an explicit completion requirement; the present FlowEdit
schema alone does not establish it. Human validation and consequential semantic decisions remain.

The founder's refinement selects a 1920×1080 landscape ideal, drag-first placement without Move
left/right buttons, hover details, explicit Store boundaries, operator tags and native-source
traversal. [Building blocks and reusable UI pairs](../drafts/flow-building-blocks.md) keeps the
presenter/view rule profile; the pair itself is now an assembly of a Flow-made presenter and a
builder-made view, and the recycling list is the view renderer's. The [maker-story section](#complete-maker-stories-and-reusable-information) states shared
inspection, metadata and actor-authority requirements. Flow consumes those typed transfers;
agents use the equivalent semantic edits under their own grants. Presenters process data without drawing; views own rendering/local display state
and report typed intents. Enforcement claims distinguish participant grants from trusted native
code and logical helper boundaries. These are selected outcomes with proposed contracts, not
capabilities already implemented by the study.

Distinguish palette organization, visual grouping, callable composite definitions and their
occurrences. A folder changes discovery; a group changes presentation; a composite changes
reusable behavior. Enter/leave a composite with a stable occurrence path and restored viewport.
Expose shared-edit impact and an independent-copy path. Native leaves route to available contracts,
provenance and source instead of pretending every implementation can be decompiled into nodes.

The current graph executes in authored order, including unused nodes, and has a single result.
Arbitrary extraction, multiple outputs, reordered execution, shared-definition updates and deeper
runtime observation are explicit capability decisions. Existing node dragging should become
discoverable; saving incomplete drafts and deliberate Run/Apply must remain intact. Research
input/schema, state and emission authoring as well as the graph canvas. Preserve one semantic edit
owner for GUI, keyboard and messages, and keep effects and authority with their existing owners.

Research starts with real tasks and low-fidelity prototypes, then selects a coherent delivery
packet: direct authoring, hierarchy/reuse and live understanding. Keep the exploration/ceremony
log, including wrong assumptions, backtracking and important discoveries. ELH replay helps
reproduce interactions; human first-use evidence judges whether those interactions make sense.
Reuse the old workspace's successful interaction grammar only where it fits current contracts.

### UI update optimization research

**Selected side research:** let a pane describe its view independently of particular dimensions,
then let a replaceable view renderer resolve it against geometry and observable data changes.
[The UI update research plan](../drafts/ui-update-research.md) owns source routes, the VarStorage
connection, experiment matrix and decision criteria. Distinguish description, layout, paint and
presentation costs; fixed content and percentage geometry have different invalidation needs.

Investigate explicit or read-tracked dependencies, asynchronous data bindings, coherent evaluation
snapshots, cache lifetime and provider replacement. Paint and hit testing must spend the same
resolved presentation. Dirty scheduling must preserve input order, timely gesture invalidation
and the existing settlement/capture promise. Failure or stale data stays attributable.

This is an opportunity to make presentation more replaceable and inspectable, not permission to
embed application policy or arbitrary cross-weave calls in a getter. The observed drag pressure
wakes claim-specific measurement under BL-ADOPT-03; no general benchmark campaign is selected.
Its first production consumer is the view renderer of the tally panel's show stage: a view
description is retained by construction and each binding names its dependency. Let measured
results guide substantial presentation changes without blocking independent usability repairs.

### Part 1 — Everyday interaction (accepted foundation)

The accepted behavior to preserve as ownership changes:

- Scroll the transcript, including wrapped content, while keeping the command line usable.
  Indicate retained content above at the top and below at the bottom; distinguish offscreen
  content from entries evicted from the record. Preserve a reading position when new output
  arrives and give the maker a clear return to the live tail.
- Up/Down browse command history when no command is actively being composed. Browsing remains
  browsing while Up/Down are pressed, even though a recalled command is visible. Any different
  command key leaves history navigation and returns arrows to completion behavior. Enter and
  Tab are special: they lock the recalled command in for editing and do nothing else on that
  press, with no submission or completion. Other editing keys do their ordinary work once.
  Later Enter/Tab presses have the normal editing-mode meaning. The mode must be legible.
- Complete real currently discoverable addresses and IDs, through their actual owner; retain
  existing shape/field completion. Discovery neither grants authority nor promises later delivery.
- Make Escape-to-deselect usable in Workshop while respecting a more specific pane operation,
  especially Neovim's Escape. Do not infer an external pane's non-consumption from silence or
  implement editor-specific mode knowledge in the host. Explain a reachable way back from panes
  that retain Escape.
- Make the already-supported Neovim user/init-file selection easy to find and diagnose. A new
  configuration framework is not required for that existing capability.

The [Part 1 prompt](../../prompts/zengine-everyday-interaction.md) records the original scope;
current mechanics belong to the repository's routed laws. Richer editor presentation remains
the separate work below.

### Part 2 — Replaceable desktop and pane launching (accepted foundation)

PR #35 is accepted and merged on 2026-09-18 as
`90d709f65aa510520bdc5a1a2e20b9824f4662f5`, following review of `ce61deb` and the founder's
hands-on use. The [continuation report](../../reportbacks/zengine-desktop-foundation-continuation-RB.md)
and [cleanup report](../../reportbacks/zengine-desktop-foundation-cleanup-RB.md) retain evidence;
current behavior belongs to Zengine's routed laws and public Workshop guides.

Preserve these accepted boundaries:

- The desktop weave owns the Pane Manager, Hotkeys, declared launch/default actions and room
  backdrop. Workshop judges application operations and publishes the pane inventory; the
  minimal hosting/authority root stays outside application-controlled replacement.
- Info holds a real pane as its subject independently of focus/selection, including itself,
  and edits supported properties through their owners. The old object canvas and picker are
  retired; broader component/composite/schema subjects remain future work.
- Declarations receive attributed verdicts and later withdrawal notices, with recovery owned
  by the declaring participant. This completes BL-WORK-04; dispatch refusal remains a different fact.
- Optional tool-load failure is attributable without ending the running desktop. A failed
  desktop/display retains host/console diagnosis and relaunch limits; automatic live return to
  skipped plan rows is not supplied. P-WORK-22 now tracks only the remaining recovery pressure.
- Lost pane choices remain lost across replacement. Creator operations distinguish known
  non-delivery from delivered silence; no timer invents an answer or retry.
- Same-contract reload is supported. Changes to accepted messages and the unreleased inventory
  shape used a matched rebuild and fresh runtime, preserving the old runtime and authored data.

The mixed-schema repair is accepted and merged as Loom #8 and Zengine #36. Emitted and nested
definitions now join admission agreement natively and across ABI v9 / manifest v5; valid schema
identity survives the manifest boundary. The shared-graph traversal and its timeout witness were
also corrected. [P-LOOM-07](../pressure.md#p-loom-07--declared-schema-agreement-is-incomplete)
routes the evidence. External capture/control and expressive editors can build on this result;
generic migration remains separate.

Keep future configuration choices separate: selection eligibility, keyboard focus,
pointer interception/click-through, placement and presentation preferences. The accepted desktop
does not promise every such configuration or the complete UI-editing overlay. Preserve the
simple external-pane learning artifact (BL-WORK-02).

### Part 3 — Expressive editors and presentation

**Accepted parallel packet (#59):** [Editor typed transfers](../../reportbacks/zengine-editor-typed-transfers-RB.md).
Extract only an established selection, through right-click > Extract or a drag beginning
inside its highlight; ordinary selection drags keep their meaning. Copy text to Inventory,
insert saved text/commands, and retain file locations that reopen through the active editor.
Optional C++ generation is a separate explicit action for C++ documents and must account for
real type/header/API requirements. Coding remains useful on its own, while these interactions
supply concrete evidence for what Flow should simplify. Worktree/runtime isolation keeps this
packet independent of the ELH creation story; it does not impose that story's tool restrictions.

- Faithfully display Neovim search, syntax and matching-brace highlighting, selections and
  mode-appropriate caret shape/blinking. The founder accepted the minimal initial GUI; these
  are desired capabilities, not retroactive defects in that proof. Neovim supplies its meaning;
  shared presentation carries it without rebuilding editor semantics in Workshop.
- Improve the standard editor for its own audience: open-file tabs, middle-button scrolling,
  line numbers and Git changed-line indications. Tabs need explicit document lifecycle; changed
  lines need a named comparison base. Gutter actions for rollback and publishing edits connect
  to protected drafts below and must state what they change.
- Offer a reversible hidden-comments view with visible concealment and correct source positions.
  Keep file bytes unchanged and use language-aware information; support code readability and
  identification of opportunities for self-documenting code.
- Rework the application bar, potentially replacing the platform bar with an authored one.
  Preserve the window behavior a maker relies on. This is a scoped follow-on, not a requirement
  to finish every desktop extraction or the UI-editing overlay before Neovim gets useful highlighting.

### Inspectable control — an external Loom host

The initial external-host consumer is merged in Zengine PR #38. The
[working guide](../../Zengine/docs/workshop/external-host.md) owns the admitted loopback
connection, input sessions, screenshots, inspection, connection inventory and reusable probe.
An agent can retain its own host-side tools and history while interacting with Workshop. Each
host keeps its own authority. The following boundaries govern reuse and further development;
automatic discovery, remote-machine transport and a general federation are not implied.

**The reusable test package is the first consumer, Loom end to end.** Load the package into the external
host, connect to Workshop, exercise an input queue/session and an inspection or application door,
capture the presented result, and inspect successful, refused and interrupted attempts. Package
orchestration and assertions live in ordinary participants consuming supported installed surfaces,
not hard-coded host routines or a separate automation engine. Platform-specific helpers and later
GitHub watchers can be further packages; neither a watcher service nor package distribution is
required for this first consumer.

**Use Loom's Recorder and Logger.** The external host configures their existing selection and
retention policies, including keeping more instances or payloads for particular test messages when
needed. Recorder supplies bounded working history; Logger preserves selected durable records.
Do not create a parallel logging/recording subsystem. A useful reader and owner-supplied observation
requests may be needed, but they consume those owners. Remote evidence retains its source host,
session and operation identity; receiving evidence locally is not observing its remote execution.
Retained, omitted and forgotten evidence remain distinguishable. See
[Loom's history contract](../../Loom/docs/reference/history.md) for the mechanisms and limits.

**Workshop displays connected hosts.** Supply a participating view of current connections with
enough attributable identity and connection state to tell which external host is present. Keep a
clear admission decision seam on the default inbound path so a later Workshop surface can approve
or refuse a new connection. A popup for each new connection is the founder's likely interface,
not a required popup implementation in this arc. The decision belongs to the host's policy; the
popup would present it. Appearing in the list, knowing a schema, and being able to connect grant
no application authority. Admission, capability grants, observation and disconnection are distinct.

Input admission, processing, application completion and presentation are separate facts. The
selected rule is to preserve the agent as actor through injected input and direct requests,
including privileged approval UI. Current Input republishes injected and platform events without
downstream origin distinction; receiving-side guest admission alone does not enforce that rule.
The [maker-story section](#complete-maker-stories-and-reusable-information)
states the research and default-off compile-time bypass requirement. Preserve the ordering needed
to request a screenshot after relevant input and a subsequent presentation. A
picture is evidence of presentation, not proof that asynchronous work finished. A disconnect after
submission can leave the outcome unknown; silence does not prove failure or authorize blind replay.
Requests for richer Workshop history remain subject to its own observation policy.

Inspect concrete facts: identity, current owner, accepted messages, configuration, authority,
source, pending work and attributable outcomes. Metadata routes to truth; it does not confer
authority. Reuse existing discovery and owner contracts before introducing new reflection. Loom
owns general communication and authority mechanics; Zengine owns its input, capture and application
meaning. The external host owns test policy, package composition and local retention choices.

Reuse the implemented admitted-connection path rather than reopening the former Bridge
selection as unfinished work. Additional transport, discovery or human identity requirements
need their own consumer and policy. Coordinate with parallel pane UX at input/presentation
boundaries and preserve its custody.

### Event-driven ELH observation — accepted

Loom #16 and Zengine #62 merged the [event-driven observation arc](../../reportbacks/elh-event-driven-observation-RB.md)
(2026-09-25 and 26).
Its first proof follows Builder's existing structured outcomes; the second lets a Python package
monitor gameplay events in an explicit play state and report a deviation or completion with
retained evidence. Latest claims, occurrence-sensitive events and history have distinct semantics.
Subscribe with explicit authority before acting, retain identity across waits, and expose gaps,
reconnects and cancellation. Generic mechanism belongs in Loom; application meaning stays with
its owner and test policy with the ELH package. Structured text/TUI reads and selective graphical
captures complement subscriptions. The accepted #60 replay remains the comparison and regression
baseline. Inventory's unaccepted domain replies (P-WORK-33) are a following command-outcome
consumer, not a reason to conflate answers with events.

### ELH usability and extension documentation

The founder selected an explicit ELH-improvement strand on 2026-09-21. Treat the external
harness as a tool that makers can learn and extend: give each relevant phase's report its own
ELH improvements/ceremony section, and maintain a compact capability and extension map with
links to deeper owners. The [experiment arc's documentation direction](../../reportbacks/elh-workshop-improvement-arc.md#elh-improvements-and-a-compact-reader-entry)
defines the reader journey and that bounded continuation's scope. The
maker-story arc's last step follows the next stories: turning demonstrated setups, fixtures,
journeys and checks into reusable ELH packages.

Generic session, run, history and tool-authoring guidance belongs in Loom. Workshop-specific
setup, control and reusable tools belong in a separately organized Zengine external-host guide
group. Package manifests own individual tool help; the entry routes to those descriptions and
states availability, required authority and important limits. Keep it small and discoverable
through normal docs/package routes, useful to humans and agents without private phase history.
Update affected documentation with capability changes. The merged experiment supplies a public
setup/journey guide, a small build fixture and maintained tool checks. Reuse that route; further
harness changes need concrete ceremony or capability pressure from the next story.

The founder's 2026-09-22 [setup detour](../../reportbacks/zengine-comfortable-demo-setups-RB.md) supplies
that pressure: choose comfortable initial pane sizes and maintain one or two named demo setups,
initially value inspection and command reuse. One agent command prepares a ready environment;
a visible Reset action and matching command restore that demo's declared starting state. Reuse
the admitted ELH session and ordinary state owners, preserve unrelated work, and distinguish warm
reset from a cold restart. Layouts alone do not checkpoint pane data. Measure agent invocations,
ELH/Workshop crossings, attributable internal messages and cold/warm/reset latency separately.
Future demos extend these maintained setups; a universal workspace system is not required.

### UI-editing overlay and a broader Info pane

The replacement for the prototype authoring canvas is an explicit editing overlay on the actual
running panes. Point to a UI subject, inspect its authored and resolved facts, change supported
configuration, or reach the source responsible for it through the existing edit/build/replace loop.
Editing mode must make clear whether a gesture inspects the UI or activates the underlying tool.
Keep target identity and applicable revision/provenance explicit across changes; consult P-WORK-25
when defining that selection, without requiring a universal history protocol in the desktop packet.

The [typed-inspection arc](#complete-maker-stories-and-reusable-information)
made owner-supplied information reusable through linked views, copies and saved values.
It can serve pane, component, composite and schema subjects before the complete editing overlay.
Info presents their descriptions and operations. The presentation does not acquire universal write authority. Each
owner validates its own edits and reports their fate; looking does not author. Preserve subject
binding and draft behavior already earned by Info's extraction and targeted-commit repairs.

Source availability is required for source editing, but it does not require placing the overlay
inside the host. A replaceable tool can route to the existing source/build owners. A rendered row
or schema declaration alone does not identify an editable source location; richer source mappings
must be supplied and diagnosed when absent. Begin with a concrete pane/component, then composites;
general schema editing connects to the selected Flow investigation; changed-shape migration
still needs its own owner and scope.

The full editing overlay follows the inspection foundation and useful editor presentation.
Typed information acquisition and reuse need not wait for the complete overlay. Protected
drafts may land before or alongside it when its experiments need durable isolation. Opening source
and ordinary explicit edits do not require that whole storage arc. An overlay-generated edit must
name the version it addresses and pass through the document owner; claims that experiments cannot
modify originals require the promised custody/enforcement first.

**Accepted 2026-09-30:** the overlay is the entry and the inspector for UI subjects. For a
described view it opens the [UI builder](../../reportbacks/zengine-flow-powers/ui-builder.md) at the element pointed at;
for a coded pane it routes to the Editor through the existing source loop. The builder and the
overlay share element identity, the authored/resolved distinction, the inspect-or-activate mode
and picture identity (P-WORK-25). Shape authoring is one model shared by Flow and the builder.

### Protected experimentation — a substantial separate arc

Preserve live edits durably in a working copy, with permission to write originals granted at
explicit save/publication. Dynamic Git worktrees are the founder's proposed mechanism; research
the smallest appropriate worktree, overlay or draft-store solution before committing its form.
Keep a base identity, detect competing changes to originals, make changes reviewable, and let
builds/experiments name the version they actually consume. Draft preservation, publication to
original files, Git commit and runtime activation have distinct meanings even if a tool offers
a combined workflow.

Storage separation alone is not write-authority enforcement. Native editors/plugins must be
behind a boundary that actually prevents bypass if the product promises originals are protected.
Standard-editor rollback and "confirm changes into main code location" should use this owner,
without introducing another source of document truth. Any persistent draft custody must be
explicitly reconciled with the active editor's live ownership.

### Further shell extraction, reusable effects and playful consumers

"Gut the shell" means move anything currently static and immovable in application behavior into
replaceable participating weaves. Keep the minimal hosting/authority root fixed. Pursue concrete
extractions alongside their consumers, with explicit ownership and authored composition. Part 2
names the first concrete consumer and the old canvas's retirement; remaining layout, presentation
and shell work follows actual use. Avoid rebuilding a god-file or demanding every extraction
before the next useful feature.

Build a reusable library of GUI transformations and animations from real examples. The first
target is configurable accordion expansion/contraction attachable to a pane. It preserves anchor
paths so dependent placement follows correctly; painting, hit-testing, clipping and granted room
agree, and hiding is not silently unloading or discarding state.

Keep a simple Python mascot pane as a small creative consumer: a character in its own box reacts
to mouse position and knows nothing else. Let that bounded purpose determine the Python and
presentation seams it needs. GPU integration remains a direction whose concrete scope (rendering,
compute, resource custody) should be chosen from an actual consumer.

### Configuration and independent setup

Programs designed for configuration should be configurable without replacing their code. Explore
discoverable configuration and generation with explicit owners, formats, validation, application
and recovery behavior. Neovim profile selection and the desktop's declared defaults are immediate
examples. Neither selects a universal configuration service; use the owning configuration surface
for supported properties and source editing where the program actually requires code.

Make dependencies and setup obtainable from a baseline Loom: detect missing tools, explain what
is needed, and support authorized acquisition/configuration, with CMake a concrete example.
Keep manual build/setup guides sufficient for a maker starting without helper weaves. Installation
scope, provenance, versions, progress and failure belong in the eventual consumer's contract;
this roadmap does not preselect a package manager or dependency solver.

### Supporting architecture and boundaries

Progress/closing answers, attributable refusal and recovery remain relevant where these consumers
need them. The merged standalone/admission work is the authority starting point, not evidence
that all human trust or filesystem containment is solved. Check relevant backlog wake conditions
per phase; do not convert every horizon into immediately owed work. General queued-picture
provenance and service retirement remain distinct work; the selected Flow and UI update
investigations above must preserve the relevant input/presentation guarantees.

### Managed opening and continued work

**Accepted opening outcome:** before joint publication, A remains the current readable and editable
document and B is only prepared state. Publication changes the Editor's and presentation owner's
claims together. Success requires both owners to apply that publication, with the intended source,
admitted presentation, room and focus agreeing. Physical rendering follows the admitted state.
A refusal before publication preserves A, including legitimate intervening work, and leaves no
setup/focus change attributable to the refused operation. Later independent maker actions stand.

**Publication is not application.** After publication, Pending remains pending; Declined, Failed
and Lost are attributed to the actual participant. An application failure does not undo publication
or promise the prior document was preserved. The terminal answer reports what happened; a repaired
owner that declines its predecessor's publication is not a successful open. Loom records these
facts; Zengine owns the focused manager, its bounded policy and the maker's explanation.

Document custody remains in the Editor weave. Workshop currently implements presentation and
retains application authority; the presentation owner stays movable. The native opening manager
coordinates through ordinary conversations and explicit host-minted authority. Preserve the old
Editor-address door's full promise and answer provenance. Another subsystem extraction, loaded
manager, service-retirement policy or general recovery framework is not a prerequisite.

Input preservation remains a Zengine correctness requirement. The repaired 257-event loss
used ordinary one-character text events, not huge loading payloads. In future work, trace the actual
pending interval;
rapid traffic from multiple participants may extend it across dispatch/frame boundaries.
Bound resources while preserving admitted input, its order and subject, and unrelated pane
usability. An arbitrary larger cap or indefinite retention is not a repair. Large loading
operations may reasonably take time; optimize against actual interaction needs and measured
bottlenecks, without turning ordinary interaction work into a bulk-data performance campaign.

Merged dispatch refusal reports selected pre-handler failures; it does not establish this
application commitment or settle every conversation abandoned after delivery. Progress/closing
answers (VD-20) remain separate work; VD-21 continues from the merged standalone/admission
policy rather than the former allow-any application baseline.

Future changes must preserve the extracted document owner's lifetime guarantees and the
component behaviors that moved with it. Route through `Zengine/agents/workshop.md`,
`agents/panes.md`, and `agents/verification/fixtures.md` rather than copying their checklists here.
The Terminal findings specifically earned request-context checks, staged late answers, and
preservation of undo/normalization behavior across the move.

The founder's ceremony audit belongs alongside the development: assess the number and complexity
of actions needed for a concrete intent, including what the maker must know to choose them.
This is product pressure, not authorization for a new interaction framework. The Flow
authoring consumer has since landed; its UX research now applies the same audit to discovery,
composition and runtime understanding. Each execution packet still supplies its scope and evidence.

### Roadmap disposition of service retirement

The founder considers the [retirement research](../drafts/service-retirement-research.md)
sufficient to preserve the option of letting old work finish while a successor serves new work.
No current development requirement depends on implementing that policy. Further loaded-worker
experiments, live output-provider coexistence and dependency-version retention are parked.

For Zengine lifecycle cases, waiting for incumbent work to finish is the preferred starting
option where the domain has a meaningful completion condition; explicit refusal may also fit.
Neither an empty queue nor elapsed time proves completion. This preference does not weaken
Editor's current input-preservation or document/presentation commitment requirements.

Managed opening and its scoped dispatch-refusal consumption are accepted. Continue to judge
IDE-loop and ceremony work against the manager's clear ownership, attributable pending/failure
and replaceability. Further progress and authority work must start from the merged contracts
and receive a consumer-grounded execution scope.
Keep the more elaborate continuity options possible without requiring their implementation now.
Revisit overlapping retirement when a concrete consumer needs to admit successor work before
the incumbent can finish, or a proposed change would close that option unnecessarily.

## 8. Live pressure and deliberate restraint

The founder's actual use now supplies the editor and Terminal pressure previously waiting on
adoption. Section 7 owns its disposition and order. The [pressure board](../pressure.md) carries
observations and triggers; the [backlog](../backlog.md) carries knowingly owed deferred work.
No standalone "stabilize everything" prerequisite precedes the next maker capability.

Scope each phase by its outcome. Shared rendering, draft storage, configuration, automation and
remote control have concrete consumers on the roadmap, but that does not authorize building all
their possible frameworks. Keep independent editors, baseline Loom use and replaceable application
owners viable as these contracts grow.

## 9. Success signals

Workshop is moving in the right direction when:

- a maker naturally stays inside it for another edit/build/inspect turn;
- a new surface reuses existing action, schema, provider, or realization truth rather than copying
  it;
- a refusal names the owner and the remedy without inventing success;
- application pressure deletes framework ideas as often as it creates them;
- onboarding friction is either removed as accidental ceremony or taught as a real concept;
- an outside maker can reproduce a project from durable authored intent without founder-local
  knowledge.

Warning signals are growing special privilege, cached mirrors of live owner facts, lifecycle policy
inside Builder or Editor, phase chronicles in current law, widening public contracts for one demo,
or verification volume standing in for a claim-specific witness.

## 10. Phase generation

1. Start with the [architectural-fit review](../../zen-orientation.md#architectural-fit-comes-first):
   the maker outcome, the complete ownership model, and the effect on selected next work. Trace
   its premises through current source, routed law, the accepted predecessor, and real pressure.
2. Use Prompt Contract v1: one stop-condition list, standing rules by reference, explicit baseline,
   proportional lane, split substantial report/evidence.
3. Use research or source preflight before a production prompt that changes ownership, authority,
   lifecycle, public architecture, cross-subsystem contracts, or a new maker capability.
4. Keep executor context bounded to the current capability and the laws it could violate.
5. Review the implemented whole against the vision and that design argument, then its behavioral
   evidence. Local passing cases cannot excuse making later work needlessly harder. Founder
   acceptance precedes private-strategy movement.
6. Update this map only for product direction or durable product law. Put proof and chronology in
   reports; put open observations in `private/pressure.md`; put knowingly owed deferred work in
   `private/backlog.md`.

## 11. Current one-page view

- **Purpose:** let a person build with Zen without first studying a private architecture course.
- **Capability:** choose a source, edit/save, build, realize or reload a same-shape weave,
  inspect it, and explicitly promote or revert. See §2 for the complete current capability.
- **Accepted story:** [tower-defense creation through ELH](../../reportbacks/zengine-tower-defense-creation-story-RB.md),
  merged #60: live editing, build/reload/play, durable workspace/toolbox/tools and a repeatable
  demo. Its repairs and maker hotkey witness are accepted; evidence preserves the original
  experiment's limits. Folders (#58), Info (#55), persistence (#54), Editor transfers (#59)
  and event-driven ELH observation (Loom #16 / Zengine #62) are accepted foundations.
- **Built:** [the tally panel](../../reportbacks/zengine-flow-powers/proving-story.md), in three stages: find (a
  discovery door that Flow, Powers and the Terminal share; merged as #82), compose (the evaluation budget, then a
  bounded loop over an operator reference; merged as #84) and show (a UI builder beside Flow; merged as #85, and worked by hand as #86). Flow composes;
  the UI builder builds views; they meet only at shapes.
- **Selected next:** the founder's order of 2026-10-03 in §7. The View Builder's polish, the
  quick desk fixes and an executor process phase are merged as #87, #88 and #89; the whole
  pixel ([BL-WORK-05](../backlog.md#bl-work-05--workshops-unit-becomes-the-whole-pixel)) comes
  next.
- **Parallel work:** UI update research, with the view renderer as its first consumer, and
  independent pane/editor improvements. Conventional coding remains first-class; Flow is not
  required. P-WORK-29 to P-WORK-49 keep the measured story/tooling pressure visible.
- **Selected sequence:** the pane status and founder's current order have one home in §7.
- **Success:** a maker understands what acted, what failed, and what to do next without losing
  their authored work. Each production task states its own completion evidence.

No horizon or old implementation checklist on this page selects a production task.
