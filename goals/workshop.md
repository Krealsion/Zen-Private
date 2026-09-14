# Zen Workshop Goal Map

**Status:** PRIVATE LIVE GOAL AUTHORITY  
**Refreshed:** 2026-09-14\
**Strategic authority:** `private/zen-strategic-map.md`  
**Current direction:** continue the IDE-loop road after the accepted pane extraction; progress/closing answers and the authority workflow remain selected downstream work
**Current execution state:** PR #28 Info repair accepted; Files action identity selected, then the pane-to-source loop (§7); service retirement remains parked
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
- read a realize refusal whole in the `--log` journal (it has no reader yet — see §8).

Source acquisition is no longer captive to Builder. What remains captive is provenance: a maker
cannot yet reach a source from the pane that draws it, and a changed-shape rebuild is still refused
rather than replaced.

## 3. Current ownership model

### Application authority and presentation ownership

Workshop is the host and authority for its application. It currently implements presentation
ownership: room, pane arrangement and focus. That implementation location is not a permanent
ownership constraint. The founder favors keeping presentation movable into its own weave,
with Workshop connecting the participating subsystems and applying application policy.
Name the application authority, presentation owner and document owner separately when a
design crosses them. Moving presentation must not require surrendering the Editor weave's
document custody. For the first manager design, keep composition and output selection together
with a clear potential separation. Replaceability does not promise that every future change is
local: expose the affected contracts so cooperating changes can propagate through authored
migrations, adapters, tools or maker intervention, including honest partial results. Avoid
requiring all those tools or service splits in the first implementation. Actual presentation
extraction is an option, not selected production work.

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

`EditorState` owns one current document: path identity, admitted representation, saved state, dirty
comparison, viewport, epoch, and lifecycle. `EditorBuffer` owns reusable editing mechanics. The
pane is presentation only.

Source admission is intentionally bijective: LF/CRLF convention, final newline, tabs, and ordinary
ASCII round-trip exactly. Mixed endings, bare CR, control bytes, and non-ASCII are refused whole
until Workshop can place and edit them truthfully. Atomic save protects the last good file. Dirty
source refuses replacement and orderly quit until the maker saves or explicitly discards.

## 4. Laws the next phase must preserve

- **A source may suggest a document; the Editor owns opening and editing it.**
- **One current document remains enough.** A file browser does not imply tabs or a document service.
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
- **The pane protocol grows one demonstrated contract at a time.** A migrating built-in that needs
  what a provider cannot say is the only reason a shape is added; it never becomes a plugin
  framework.

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

The target loop is worth preserving:

```text
right-click pane
    -> Edit Code
    -> choose/open source
    -> edit and save
    -> build
    -> realize or reload the owning artifact
```

Its growth path after the accepted pane extraction (2026-09-13):

1. contextual `Edit Code` resolves a path and calls the same `Editor.open(path)` door — **not built**;
2. the host resolves pane/provider -> recipe/source from authored provenance, without teaching the
   Editor build topology — **not built** (P-WORK-06);
3. Builder produces the artifact through its existing recipe route — **built**, and "pick buildable"
   authors the recipe row when none exists;
4. the realization owner decides whether this is a waiting initial load or an already-live artifact —
   **built**: a live same-shape artifact reloads in place, state kept, promotion explicit, revert
   available;
5. changed-shape replacement remains refused until provider/weave custody, state continuity,
   authority, rollback, and failure semantics are explicitly earned — **still the wall**; Loom's
   prepared replacement and authored handoff are the mechanism, and Workshop does not drive them yet.

Roads recorded, not built: a timed auto-revert once keep and revert are habitual; a modal that warns
on closing without promoting — the pressure for a general popup/modal feature; a reader for the
`--log` journal; `config` asked by the chooser only when the tree's generator is multi-config.

Do not let Project Files store the future joins. It should remain an honest file navigator even if
the build/reload architecture later changes.

### Pane extraction: current status and next work

Files, Builder, Attention, Info, Terminal and Editor have landed as pane weaves. **The selected
extraction arc is complete.** Layouts, Pane Manager and the maker pane remain host-owned under
this arc's boundary; that does not change the long-term peer-tool direction.

The founder confirmed [PR #23](https://github.com/Krealsion/Zengine/pull/23) merged on 2026-09-13
as `26ae2dd9a63a8cf5feac2eebb0fd9eddff4066cd`. Its tree matches the reviewed `50c279b` exactly.
It consumes accepted Loom `a08499f` (ABI v8). BL-WORK-03 and BL-DEF-04 are closed: Editor extraction,
managed opening and removal of the dead Loom SDL dev override are accepted. The
[final corrections report](../../reportbacks/zengine-managed-open-quit-notice-corrections-RB.md)
and [completed roadmap](../drafts/editor-pr23-roadmap.md) retain the evidence and sequence.

The accepted result also refuses a quit when the host observes that its question could not reach
a participant, naming the participant and reason while preserving work and restoring interaction.
A delivered unanswered question can remain pending. Builder and Files publish the clearing of a
spent notice. Files' independent click-mapping repair is accepted in PR #24 at merge `3c8d6bc`;
its [pressure entry](../pressure.md#p-work-23--pane-notices-must-agree-with-actions-and-hit-testing)
tracks the bounded notice/interaction follow-ups. The founder confirmed [PR #25](https://github.com/Krealsion/Zengine/pull/25)
merged as `968a2578476d3876dc6b0026271b00b373aefaa7`; its tree matches reviewed `9c4242c`.
Workshop now supplies actual prior ordinary-key routing on v2 presses, Files retains activation
policy, and v1 compatibility is conservative. Hidden-title selection survives the room update,
and the keyboard legend reflects actual routing. Host version inspection does not guarantee
delivery through holder turnover; an attributable refusal is valid, without duplicate retries.
The [implementation report](../../reportbacks/zengine-files-focus-implementation-RB.md) retains
the evidence. P-WORK-24 and its enumerated documentation residue (BL-DOC-01, landed in PR #27)
are closed.

The founder confirmed [PR #26](https://github.com/Krealsion/Zengine/pull/26) merged as
`3bf888c378655933ba2aa403faf776dfb99a0876`, tree `297a532c9d860054627cccd85c2b066af787d1e5`,
identical to reviewed `a22dced`. Its [notice audit](../../reportbacks/zengine-pane-notice-audit-RB.md)
closes the named Info/Terminal/Attention candidates: ignored input preserves a notice, consumed
actions publish its removal without requiring a new document picture, and Info maps clicks against
the notice-bearing rows it shows. Ownership remains in each pane.

PR #27 is accepted and merged as `b42fe353467994f762d3470121eccadf3acdceae`, tree
`1c280311e8380b33d1d8a95a08bc8019cb39e134`, identical to reviewed `407ca15`. Its
[corrections report](../../reportbacks/zengine-pane-interaction-cleanup-corrections-RB.md) retains
the evidence. Info preserves drafts and later edits, sends one commit at a time, and accounts for
answers without claiming writes away. Builder/Files ignored ids and Attention's hidden-state
wording are repaired. P-WORK-23, BL-DEF-02 and the enumerated BL-DOC-01 work are closed.

PR #28 is accepted and merged as `afdc2423d76ba9eb49a0c916b20c665bb9408376`, tree
`7cf781e7c135a48f2ddc0b9d8b7af1cd03790dc3`, identical to reviewed `c012085`. Its
[implementation report](../../reportbacks/zengine-info-targeted-commits-RB.md) and
[documentation follow-up](../../reportbacks/zengine-info-targeted-commits-doc-followup-RB.md)
retain the evidence. Workshop binds the commit's applicable subject; Info settles known send
refusals and preserves legitimate drafts. P-WORK-26 and BL-DOC-02 are closed. The disclosed
host state-swap limitation waits for a real Workshop replacement consumer; mixed-version
diagnostics remain deferred. Neither selects further Info repairs now.

The current sequence, following the founder's accepted direction on 2026-09-14:

1. **Files action identity:** [the selected repair](../../prompts/zengine-files-action-identity.md)
   closes BL-DEF-05: browsing, chooser selection and authoring submission keep distinct operation
   meanings when queued input crosses a mode change. Files owns the modes; Workshop keeps its
   existing declaration/keymap join. This is the remaining selected interaction repair.
2. **Pane-to-source:** contextual `Edit Code` joins a running pane to its authored source/recipe
   through the host, then reuses Editor, Builder and realization. This is the next substantial
   maker capability, not another general stabilization pass.
3. **Ceremony throughout that loop:** measure actions, decisions, required knowledge and recovery
   for a real visible modification. Keep the small example pane useful for dissection. Success is
   a maker reaching a running change they understand and choosing to make another.
4. **Progress and authority:** scope progress/closing answers and the Weaver workflow from Builder,
   realization and permission needs. These remain the next supporting architecture arc; their
   precise execution packets are not implied by this sequence.

New-weave authoring, changed-shape handoffs and Flow remain later capability expansions. General
[queued-picture provenance](../pressure.md#p-work-25--queued-presses-do-not-identify-the-picture-they-targeted),
presentation extraction and service retirement remain separate. Necessary repairs protect the
maker loop and have explicit exits; they do not make exhaustive correctness a prerequisite for
the next product capability.

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
answers (VD-20) and the authority workflow (VD-21) remain separate selected work.

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
and replaceability. VD-20's progress/closing answers and VD-21's authority workflow retain their
selected direction and each require a consumer-grounded execution scope.
Keep the more elaborate continuity options possible without requiring their implementation now.
Revisit overlapping retirement when a concrete consumer needs to admit successor work before
the incumbent can finish, or a proposed change would close that option unnecessarily.

## 8. Live pressure and deliberate restraint

The nearest product pressures are:

- pane default height and one-cell keyboard resizing are still tedious;
- pane editing needs a contextual acquisition door and richer spatial facts (P-WORK-02);
- search is the first likely conventional editor demand after real use;
- Unicode source editing needs a representation/geometry answer, not merely a UTF-8 decoder;
- provider-contributed context rows require a deliberate protocol extension;
- source-to-artifact provenance and live replacement are the gates on the self-hosting loop;
- a second independent read-only provider remains useful evidence for generality, not permission to
  add input, arbitrary drawing, unloading, or multiplicity.

Do not build a widget set, generic document service, plugin framework, notification system, layout
solver, shell, dependency solver, or Flow editor merely because Workshop now resembles an IDE.

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
- **Remaining IDE joins:** pane-to-source provenance and changed-shape replacement (§7).
- **Selected sequence:** the pane status and founder's current order have one home in §7.
- **Success:** a maker understands what acted, what failed, and what to do next without losing
  their authored work. Each production task states its own completion evidence.

No horizon or old implementation checklist on this page selects a production task.
