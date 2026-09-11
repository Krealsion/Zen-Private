# Zen Workshop Goal Map

**Status:** PRIVATE LIVE GOAL AUTHORITY  
**Refreshed:** 2026-09-11  
**Strategic authority:** `private/zen-strategic-map.md`  
**Current direction:** resolve Editor's document/presentation commitment before resuming PR #23 implementation; the IDE loop remains the product road
**Current execution state:** the commitment investigation is reported; Vision is developing a presentation-manager discussion draft before selecting a lower-level mechanism (§7)
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
document custody. Actual presentation extraction is an option, not selected production work.

### Failure and supervision

Authored weaves may fail, remain silent or stay pending indefinitely. Those are valid program
behaviors; the architecture does not owe universal successful completion. Zengine's shipped
components should preserve work and make failures or unfinished operations attributable to the
relevant intent, participant and observed stage. Absence of an answer is not a diagnosis.

Managers supply external observation and recovery policy within their authority. They may help
the application continue without solving the original operation; they too remain authored
participants that can fail. Establish the high-level owner and what it can actually know
before treating a missing interaction as evidence for a new substrate primitive.

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

Its clean growth path, with status as of 2026-09-06:

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

Files, Builder, Attention, Info, and Terminal have landed as pane weaves. Terminal's review
corrections are accepted with PR #22; it supplies `PaneCaret` ahead of the Editor. **Editor is
the final extraction in this arc.** Layouts, Pane Manager, and the maker pane remain host-owned
under the arc's current boundary, not as exceptions to the long-term peer-tool direction.

**Current selection: investigate Editor's document/presentation commitment.** The founder
accepted the [integration preflight stop](../../reportbacks/editor-sender-refusal-integration-RB.md)
and selected a focused design study with a small executable witness. Loom PR #5 is merged at
`f20f32df01e36ae672cef8013ea4499b76e3954c`; Editor PR #23 remains unaccepted at
`9cbf5a5ac8d4751472dc891371401d93a25e03cc`. The fresh merged-Loom preflight reproduced the
wrong source at the claimed commitment, loss of A's legitimate paste, and the 257th valid
text event being dropped. A queued reveal also survives Editor reload after its pending
operation is lost. Passing official tests did not establish the required outcome.

**Fixed opening outcome:** success has the intended source installed, presented and focused
at a defensible commitment boundary. Failure preserves the prior document, including
legitimate intervening work for it, and leaves no setup/focus change attributable to the
failed operation. Later independent maker actions may change presentation.

The [commitment investigation](../../reportbacks/editor-commit-investigation-RB.md) proposes
protected publication of owner-prepared values and compares it with provisional application
coordination. The founder has not selected a production root/SDK/ABI contract. The current
exploration starts with presentation-manager ownership, provider lifecycle and attributable
failure; Vision's [discussion draft](../drafts/presentation-manager.md) and its source research
are proposals for brainstorming, not accepted product law or an execution prompt. Preserve
weave-owned source and movable presentation ownership while evaluating the remaining need for
joint commitment. [BL-WORK-03](../backlog.md#bl-work-03--resume-the-editor-extraction-after-sender-fate)
tracks the still-owed extraction and dispatch-refusal integration. Implementation follows a
reviewed design and its own scope.

Input preservation remains a Zengine correctness requirement. The observed 257-event loss
uses ordinary one-character text events, not huge loading payloads. Trace the actual pending interval;
rapid traffic from multiple participants may extend it across dispatch/frame boundaries.
Bound resources while preserving admitted input, its order and subject, and unrelated pane
usability. An arbitrary larger cap or indefinite retention is not a repair. Large loading
operations may reasonably take time; optimize against actual interaction needs and measured
bottlenecks, without turning this investigation into a bulk-data performance campaign.

Merged dispatch refusal reports selected pre-handler failures; it does not establish this
application commitment or settle every conversation abandoned after delivery. Progress/closing
answers (VD-20) and the authority workflow (VD-21) remain separate selected work.

The extraction must preserve the current document's ownership/lifetime guarantees and the
component behaviors previously supplied by the host. Route through `Zengine/agents/workshop.md`,
`agents/panes.md`, and `agents/verification/fixtures.md` rather than copying their checklists here.
The Terminal findings specifically earned request-context checks, staged late answers, and
preservation of undo/normalization behavior across the move.

The founder's ceremony audit belongs alongside the development: assess the number and complexity
of actions needed for a concrete intent, including what the maker must know to choose them.
This is product pressure, not authorization for a new interaction framework. New-weave production
and Flow are not selected by this consolidation; a future task supplies its own scope and evidence.

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
