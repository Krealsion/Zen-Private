# Zen Workshop Goal Map

**Status:** PRIVATE LIVE GOAL AUTHORITY  
**Refreshed:** 2026-09-06  
**Strategic authority:** `private/zen-strategic-map.md`  
**Current direction:** the pane-weave arc on the IDE-loop road — the built-in panes become participating weaves (VD-19); send fate and row-requested authority precede it (VD-20, VD-21)  
**Current execution state:** EDIT-1 landed; build-then-load landed (Zengine PRs #11–#14); `PaneActions` (PR #15) and Files as a weave (PR #16) landed 2026-09-07 — the first migration of the pane-weave arc; the Builder migration is next; new-weave research landed, its production waiting behind the arc; nothing else is authorized by this map  
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
sees inside Workshop is a participating weave loaded from the plan, and Workshop itself keeps
room, focus, realization and roots. A built-in pane written as C++ inside the host is the debt
this arc pays, one pane at a time.

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

## 6. EDIT-1 — Choose What to Edit — LANDED

Landed 2026-09; the completion sentence below is now true. Kept as the record of what was chosen;
the surviving law is `Zengine/agents/workshop/project.md` and `editor.md`.

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

**The arc before the remaining joins (2026-09-06, VD-19).** The built-in panes migrate onto the
pane protocol as participating weaves, in the order the research measured by smallest protocol
delta. Landed 2026-09-07: `PaneActions`/`PaneActionRequested` (Zengine PR #15, Powers the first
consumer) and Files as a weave (PR #16 — three host doors, rows re-declared per mode, saved
references converted at read, the built-in gone, −80 KB of host). Next the Builder, carrying
`RecipeCatalog` v2 for the catalog-source row it lost (P-WORK-20); then Attention, Info, the
Editor last (caret and selection are the contract it pulls). Layouts, the Pane Manager, the Terminal
and the maker pane stay host this arc. Replacing a migrated pane with a differently-shaped one is
item 5 above with a case. New-weave production follows the first migrations. Attention landed
(PR #19, one new sentence: `StandingConditions`). Info's first stage landed (PR #20: the host
owns the document, `DocumentShown` is the picture, four acts are asks) and stopped on the
reserved side column; the founder retired the reservation (VD-23): room is the whole screen, a
shipped default setup opens Info at the right edge, and the geometry PR precedes Info's second
stage. The geometry landed (PR #21): the room is the screen, the right column is a place a desk
row may name, the one-time resize of %-shares accepted by the founder. The Terminal migrates too
(VD-24) — it pulls the caret shape ahead of the Editor and wears a boundary by construction; the
stays-host list is now Layouts, the Pane Manager and the maker pane. Order: Info stage 2, the
Terminal, the Editor.

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
    authored project plan + build recipes, both authorable from inside Workshop
    inspectable arrangement and power stack
    persistent, arrangeable desk in TUI and SDL
    one action/key/context truth
    standing Attention distinct from event notices
    one competent source editor, reachable from Project Files and Builder
    maker-driven edit -> save -> build -> reload in place (state kept) -> promote or revert
    pick buildable -> author a recipe row -> load it -> author a plan row

CURRENT LIMIT
    a source is not yet reachable from the pane that draws it; a changed shape is refused, not replaced

NEXT DIRECTION
    the pane-weave arc (VD-19): PaneActions (#15) and Files (#16) landed 2026-09-07. Next the
    Builder migration, carrying RecipeCatalog v2 (P-WORK-20); then Attention, Info, the Editor.
    Preconditions in parallel: send fate then obligation (Loom, VD-20); the plan row as authority
    request, the Weaver seat and its approval modal (VD-21). New-weave production (VD-18, research
    landed) follows the first migrations. Still on the board: pane -> source provenance
    (P-WORK-06); the changed-shape rung (P-WORK-07), now with a case -- a differently-shaped pane

COMPLETION FALSIFIER
    none selected; the next prompt states its own

NEXT LONG LOOP
    pane -> source provenance -> edit -> build -> reload in place or explicit replacement

DO NOT PROMOTE YET
    tabs, VFS, watcher, provider file protocol, language IDE, generic Flow UI, hot reload framework

CORE EXPERIENCE
    boundaries remain; they stop being cliffs
```
