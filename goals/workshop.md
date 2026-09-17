# Zen Workshop Goal Map

**Status:** PRIVATE LIVE GOAL AUTHORITY  
**Refreshed:** 2026-09-17\
**Strategic authority:** `private/zen-strategic-map.md`  
**Current direction:** everyday use and a replaceable desktop with useful inspection, then expressive presentation and protected experimentation
**Current execution state:** Neovim PR #33 is merged. Everyday interaction, PR #34, is in correction and awaits review/acceptance. The bounded desktop/launcher foundation is selected next in §7; each prompt owns its execution scope.
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
- open/save an authored object document and name/save/restore a separate pane setup;
- load an explicit authored project plan and inspect both the resolved arrangement and the live
  power stack;
- keep unresolved pane intent without silently rewriting it;
- arrange overlapping panes on a fine lattice with shared paint/hit geometry, recovery, canonical
  front order, and independent-axis settlement;
- use the same application meaning through TUI and SDL media;
- discover and remap one keyboard action truth used by dispatch, help, and contextual presentation;
- right-click a room, pane, or object (or use the keyboard door) to see actions meaningful to that
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

The object-document canvas remains implemented, but its retirement is now selected direction.
Section 7 separates that removal from the pane desktop and from the later UI-editing overlay;
none of those planned capabilities is claimed as present here.

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

The selected consumer is a replaceable desktop/root presentation with a pane launcher, default
interaction policy and useful failure explanations. This application root is distinct from the
fixed hosting/authority root. The desktop can explain unavailable tools while it is running;
failure of the desktop or its display needs recovery through the baseline Loom host/console.
The earlier opening manager establishes coordination boundaries, not an already extracted desktop.

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
Layouts, Pane Manager and other remaining host-owned behavior are candidates for the shell work
below, not permanent exceptions to the peer-tool direction.

Everyday interaction is on PR #34, following merged Neovim PR #33. Its Escape correction is
in progress; implementation or green checks alone do not establish acceptance. The
[correction prompt](../../prompts/zengine-everyday-interaction-corrections.md) owns that work.
Later execution starts from the accepted result, refreshing live Git rather than copying a
development head into this roadmap. Preserve the demonstrated editor capability.

### Near-term order and purpose

The founder's follow-up selects the old object canvas for retirement and gives shell replacement
a concrete consumer: inspect and reshape the real running Workshop. This revises the order without
making a complete UI authoring system a prerequisite for useful editor improvements.

| Order | Outcome | Purpose and boundary |
|---|---|---|
| Now | Finish and review everyday interaction, including the Escape correction | Close the current usable-interaction packet before treating it as the foundation. |
| Next | Replaceable desktop, pane launching, default interaction policy and a narrow real-pane inspector | Give remaining shell behavior a useful owner; retire the old canvas/picker paths as their responsibilities are deliberately removed or rehomed. |
| Alongside that foundation / immediately after | Local inspection, screenshots and authorized input/control | Make the visible result and failed operations observable; supply the smallest useful path before another large UI pass. |
| Then | Expressive Neovim/shared presentation and bounded standard-editor improvements | Make everyday editing comfortable; do not wait for a general source-editing overlay. |
| Following those foundations | UI-editing overlay and broader Info subjects; protected draft/publication work | Connect a visible subject to configuration or source. Stage draft protection before promising safe experimentation or publication to originals. |
| Later, through concrete consumers | General schema/composite authoring, deeper configuration/setup, reusable effects, Python, GPU and multi-host work | Extend demonstrated owners rather than prebuilding their possible frameworks. |

These are capability boundaries, not mandatory research/implementation handoffs or arbitrary PR
counts. Each executor packet should carry its bounded goal through preflight, implementation and
proof. Independent editor fixes can proceed when they do not depend on an unsettled presentation
contract. Full overlay authoring, all standard-editor features and protected storage need not
land together. Service retirement and generic changed-schema migration remain separate work.

### Part 1 — Everyday interaction (selected for execution)

Make Terminal and returning to Workshop comfortable enough for repeated use:

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

The [Part 1 prompt](../../prompts/zengine-everyday-interaction.md) owns implementation and proof.
This packet does not absorb every editor enhancement below. One executor should research, plan,
implement and demonstrate the full bounded outcome in one session, recording ceremony and
important discoveries throughout, including any context compaction.

### Part 2 — Replaceable desktop and pane launching (next execution arc)

Replace the prototype object's role as Workshop's default workspace with an application desktop
whose behavior can participate and be replaced. The target is the old rectangle/object-document
canvas and its shell commands, not the useful concept of a desk, pane arrangement or saved layout.
The fixed host retains its authority and recovery responsibilities; a participating desktop does
not inherit immovability merely because it is the parent of the other panes.

The first packet should demonstrate a coherent, bounded end-to-end result:

- Open or focus Terminal and Pane Manager through declared, configurable launch actions. Restore
  Ctrl-T as the proposed Terminal default; give Pane Manager its own discoverable default. Keep
  launch intent distinct from toggling a tool away or unloading its provider.
- Move the picker/launcher and hotkey presentation toward ordinary participating tools. Read one
  authoritative action/binding truth for dispatch, help and remapping. A tool's in-pane actions and
  its launch action have different lifetimes: launching cannot depend on already focusing it.
  Explain missing/unavailable targets without silently loading an unauthored artifact.
- Let the desktop handle input available to it and own its application defaults. Explicit global
  bindings have declared precedence and collision rules; neither an unanswered message nor an
  ignored key is automatic permission to act. A default can be replaced or disabled while the
  pane's more specific operation remains its own.
- Inspect one real pane and change a supported property through its actual owner. Keep the
  inspection subject independent of selection/focus, so entering the inspector does not retarget
  it and self-inspection remains possible. This proves a useful seam without requiring a general
  component tree, schema editor or arbitrary source-rewriting engine.
- Demonstrate an unavailable tool with an attributable explanation and a reachable recovery path.
  P-WORK-22 matters here: the current boot refusal can end the host before a desktop is available.
  Preflight must trace both launch paths and distinguish essential startup from recoverable tool
  failure before choosing policy. Continuing blindly after every failed row is not the outcome.
  If the desktop/display fails, prove what the baseline console can actually diagnose or repair;
  do not claim a fallback that depends on the failed component itself.

Audit and retire the old canvas, its object-specific shell commands and redundant picker UI as
part of this arc. Retain any useful property/document primitives under their owners. Account for
existing authored files explicitly; do not delete the maker's files or silently reinterpret old
documents as pane setups. Removal need not wait for the complete future overlay. Info is retained,
with a useful real-pane subject as its old default document consumer goes away. Pane Manager's
inspection responsibilities can move into Info; launching/participation and placement remain
operations judged by their respective owners. Do not preserve two authoritative pane inventories.

Keep an initial configuration inventory beside the eventual owning contracts: default Escape
behavior and its disabling/replacement; launch bindings; selection eligibility; keyboard-focus
eligibility; pointer interception/click-through; and default placement/presentation preferences.
Selection, focus and click-through are distinct choices, not one interactive/noninteractive bit.
This inventory guides the first necessary properties; it does not require every configuration
or a configuration framework in the first packet.

Check P-WORK-02, P-WORK-03, P-WORK-19 and P-WORK-22 at preflight. Declaration admission and
provider-visible rejection have a concrete upcoming consumer in launch/default registration:
scope the relevant BL-WORK-04 work when that surface changes. Preserve BL-WORK-02's small example.
These dependencies belong to this arc, not to the current Escape correction.

### Part 3 — Expressive editors and presentation

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

### Inspectable control — bring local capability forward

A substantial introspection/metadata pass should make concrete questions answerable: identity,
current owner, accepted messages, configuration, authority, source, pending work and attributable
outcomes. Metadata describes and routes to the relevant truth; it cannot confer behavioral
authority or turn a declaration into an observed fact. Terminal completion, the launcher and
real-pane inspection are early consumers. Use their questions to bound the first metadata work;
general reflection and schema mutation are not prerequisites.

Bring a local micro-console and screenshots forward to support development and testing. Agents
need both authorized input injection for interaction tests and direct requests to owning weaves
for semantic operations. The agent remains the actor, rather than silently becoming the user.
Screenshots must reflect the presented result, not substitute for evidence of command success.
Both control paths should work through ordinary contracts. Networking need not precede a useful
local tool. Bring the smallest useful capture/control path alongside the desktop foundation or
immediately after it, before a large visual pass; do not require an agent-control platform before
testing one pane. Distinguish physical/backend input, semantic requests and displayed evidence.

The multi-host continuation adds discoverable hosts and requests to connect. Discovery,
authentication, session admission and permission to perform actions remain separate. The baseline
Loom console/harness is the starting consumer. Cross-host communication is selected direction,
not an already implemented remote desktop or an automatic unrestricted grant.

### UI-editing overlay and a broader Info pane

The replacement for the prototype authoring canvas is an explicit editing overlay on the actual
running panes. Point to a UI subject, inspect its authored and resolved facts, change supported
configuration, or reach the source responsible for it through the existing edit/build/replace loop.
Editing mode must make clear whether a gesture inspects the UI or activates the underlying tool.
Keep target identity and applicable revision/provenance explicit across changes; consult P-WORK-25
when defining that selection, without requiring a universal history protocol in the desktop packet.

Info can present pane, component, composite and eventually schema subjects through owner-supplied
descriptions and operations. The presentation does not acquire universal write authority. Each
owner validates its own edits and reports their fate; looking does not author. Preserve subject
binding and draft behavior already earned by Info's extraction and targeted-commit repairs.

Source availability is required for source editing, but it does not require placing the overlay
inside the host. A replaceable tool can route to the existing source/build owners. A rendered row
or schema declaration alone does not identify an editable source location; richer source mappings
must be supplied and diagnosed when absent. Begin with a concrete pane/component, then composites;
general schema editing belongs with the later schema-builder/Flow and changed-shape work.

This arc follows a working desktop/inspection foundation and useful editor presentation. Protected
drafts may land before or alongside it when its experiments need durable isolation. Opening source
and ordinary explicit edits do not require that whole storage arc. An overlay-generated edit must
name the version it addresses and pass through the document owner; claims that experiments cannot
modify originals require the promised custody/enforcement first.

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
provenance, service retirement and Flow remain distinct work.

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
This is product pressure, not authorization for a new interaction framework. New-weave production
and Flow are not selected by this consolidation; a future task supplies its own scope and evidence.

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
- **Next outcome:** finish everyday interaction, then the replaceable desktop/launcher and narrow
  real-pane inspection, with local capture/control close beside it; expressive editors, the
  UI-editing overlay and protected drafts follow the dependencies in §7.
- **Selected sequence:** the pane status and founder's current order have one home in §7.
- **Success:** a maker understands what acted, what failed, and what to do next without losing
  their authored work. Each production task states its own completion evidence.

No horizon or old implementation checklist on this page selects a production task.
