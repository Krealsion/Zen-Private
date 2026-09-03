# Zen Workshop Goal Map

**Status:** PRIVATE LIVE GOAL AUTHORITY  
**Refreshed:** 2026-08-29  
**Strategic authority:** `private/zen-strategic-map.md`  
**Current direction:** EDIT-1 — Choose What to Edit  
**Current execution state:** EDIT-R1 complete; EDIT-1 implementation-ready but not authorized by this map  
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

That is a real development environment, but source acquisition is still captive to Builder. EDIT-1
is the next product boundary.

## 3. Current ownership model

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

Project means the launch directory unless an explicit path for a particular project file says
otherwise. WUX-3 removed accidental CWD ownership from user config/state; it did not abolish CWD as
the current project identity. EDIT-R1 found that this project root exists only as documented prose,
not as one captured production value.

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
trees. Workshop's former 30k-line test translation unit is six semantic suites plus shared support,
so Linux parallel verification is about 9 seconds rather than about a minute without losing the
population contract.

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

## 6. EDIT-1 — Choose What to Edit

### Product completion sentence

With no useful Builder source selected, a maker can open Project Files, navigate inside the project
root, open a source through the Editor's one path door, edit it, save it, and then use Builder
independently.

### Implementation-ready architecture from EDIT-R1

1. **Capture project truth once.** The host reads the launch directory in error-code form into
   `HostContext::project_dir`. Failure becomes an explicit absence; no fallback guess.
2. **Factor one open door.** The Builder-agnostic tail of `edit_source` becomes a private
   `open_source(path, mail)` seam. It retains reveal, dirty refusal, bounded read, byte admission,
   trial seating, epoch, viewport, focus, and notices.
3. **Normalize identity at entry.** Every caller supplies one resolved absolute,
   lexically-normal spelling with one separator convention. Display is a projection; it never
   becomes identity. Windows case-folding remains an explicit residual until platform evidence
   earns more.
4. **Add Project Files as an ordinary fourth pane.** It gets picker participation, arrangement,
   setup persistence, and context rows through the catalog rather than special casing.
5. **Keep rows small.** A row is `{exact name, file|directory}`. Current directory is a stack of
   entered names below the root. Path meaning derives at activation; rows hold no build facts,
   editor state, handles, or ownership guesses.
6. **Refresh at explicit truth points.** Recompute on pane open/seat, navigation, explicit Refresh,
   and a finished `BuildStatus`. Never enumerate on every paint; no watcher or polling.
7. **Use existing interaction patterns.** Files becomes the second catalog-declared keyboard-taking
   built-in, which earns a catalog `takes_keyboard` fact. Up/Down, Return, parent, Refresh, wheel,
   press-select plus Return/second-press all fit existing routes. Double-click is not representable
   and must not be promised.
8. **Builder becomes one caller.** Its recipe discovery and its current recipe-kind refusals remain;
   the resolved path enters the same door Project Files uses. Project Files never learns recipes.
9. **Persist nothing new.** The pane row already persists. Browser directory, cursor, scroll, and
   Editor source path remain session/presentation state until use earns otherwise.

One pre-existing path defect must be handled face-up: relative `single_source` spellings resolve
against CWD in Editor/preflight but against the generated workspace in the build. Normalizing the
Editor entrant fixes duplicate document spellings, not generated-CMake meaning. EDIT-1 must either
resolve both against project truth or state/refuse the relative case; it may not keep claiming the
edited and built files are necessarily identical for that spelling.

### Decisions to settle in the production prompt

These are bounded product choices, not architecture research:

- directories-first versus one bytewise ordering;
- whether hidden names are shown, filtered, or made toggleable;
- refuse entry into link-directories versus allow it and state that the physical target may be
  outside the root; if refusal is chosen, witness NTFS junction behavior;
- pointer activation rule: select-then-Return/second-press versus immediate picker-style open;
- remove the write-only `EditorState::recipe` or give it one truthful presentation use;
- add `--project` now or keep the launch directory as the only project-root authority for this
  phase.

Non-ASCII names should remain visible as marked, sanitized rows but refuse activation while path
custody is narrow-string and the Editor is byte-column based. Unsupported file contents are the
Editor's refusal, not the browser's.

### Explicit exclusions

No tabs, recent files, recursive index, fuzzy search, file create/delete/rename, file watching,
whole-filesystem browsing, VFS, generic tree widget, language registry, syntax highlighting,
provider-declared file list, source ownership inference, build ownership in Editor, hot reload, or
live replacement.

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

Its clean growth path is:

1. contextual `Edit Code` resolves a path and calls the same `Editor.open(path)` door;
2. the host resolves pane/provider -> recipe/source from authored provenance, without teaching the
   Editor build topology;
3. Builder produces the artifact through its existing recipe route;
4. the realization owner decides whether this is a waiting initial load or an already-live artifact;
5. already-live replacement remains refused until provider/weave custody, state continuity,
   authority, rollback, and failure semantics are explicitly earned.

Do not let Project Files store the future joins. It should remain an honest file navigator even if
the build/reload architecture later changes.

## 8. Live pressure and deliberate restraint

The nearest product pressures are:

- pane default height and one-cell keyboard resizing are still tedious;
- pane Inspect needs a general inspectable subject rather than the current object-only selection;
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

1. Start from current source, routed law, the accepted predecessor, and the smallest relevant
   pressure—not from this map's old phase names.
2. Use Prompt Contract v1: one stop-condition list, standing rules by reference, explicit baseline,
   proportional lane, split substantial report/evidence.
3. Use research or source preflight before a production prompt that changes ownership, authority,
   lifecycle, public architecture, cross-subsystem contracts, or a new maker capability.
4. Keep executor context bounded to the current capability and the laws it could violate.
5. Review the decision-layer report against current source and load-bearing tests. Founder
   acceptance precedes private-strategy movement.
6. Update this map only for product direction or durable product law. Put proof and chronology in
   reports; put open observations in `private/pressure.md`; put knowingly owed deferred work in
   `private/backlog.md`.

## 11. Current one-page view

```text
PURPOSE
    let a person build with Zen and feel the ideas rather than study a private architecture course

CURRENT CAPABILITY
    authored project plan + build recipes
    inspectable arrangement and power stack
    persistent, arrangeable desk in TUI and SDL
    one action/key/context truth
    standing Attention distinct from event notices
    one competent source editor
    maker-driven edit -> save -> build -> realize -> inspect loop

CURRENT LIMIT
    Builder is still the only source referrer the Editor can use

NEXT DIRECTION
    EDIT-1: captured project root + Project Files + one normalized Editor open-by-path door

COMPLETION FALSIFIER
    no useful Builder source selected; maker still navigates, opens, edits, and saves a source

NEXT LONG LOOP
    pane -> source provenance -> edit -> build -> initial realize or explicit live replacement

DO NOT PROMOTE YET
    tabs, VFS, watcher, provider file protocol, language IDE, generic Flow UI, hot reload framework

CORE EXPERIENCE
    boundaries remain; they stop being cliffs
```
