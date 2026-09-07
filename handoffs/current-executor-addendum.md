# Zen — Current Executor Handoff

**Status:** PRIVATE LIVE EXECUTION CARD  
**Refreshed:** 2026-08-29  
**STALE (marked 2026-09-06):** this card predates EDIT-1's landing and the build-then-load arc. Its
§1 heads, §2 route, §3–§5 state and §9 report focus describe 08-29. Current state is
`Zen-FCO-v2.md` §6 and `handoff-2026-09-06.md`; current direction is the maps. §6–§8 (laws, Prompt
Contract v1, the acceptance boundary) remain true. A rewrite is owed at the next consolidation.  
**Current product direction:** EDIT-1 — Choose What to Edit  
**Current execution state:** EDIT-R1 research complete; no EDIT-1 production prompt is selected by this handoff  
**Scope authority:** the current phase prompt always wins

This is the compact bridge from strategy to a future executor. It is not a substitute for a phase
prompt, repository law, or source inspection.

## 1. Current repository observation

Observed clean and level with upstream during the private-roadmap refresh:

```text
Loom       main    9c4fe305fc48460fb44a46facacd5f96f943ffc3
Zengine    main    7ac1d53277a388131048f32c00bc47abbe377fc2
Night Lab  master  32fd548ea4e615fe05f2134d1130e32796a1f89d
Arena      main    28d424f81481bd60fd65251d2b8008db4f7e90be
```

These are refresh observations, not a reusable acceptance board. Before a phase, query live Git and
compare it with the baseline stated by that phase prompt or the accepted predecessor's END. Never
reset a working tree merely to match this card. `REPOSITORIES.md` owns paths, roles, branches, and
remotes only.

## 2. Read-first route

For EDIT-1 or adjacent Workshop work:

```text
current phase prompt
Zengine/AGENTS.md
Zengine/agents/workshop.md
Zengine/agents/verification.md
Zengine/docs/workshop/editor.md
Zengine/docs/workshop/limitations.md
reportbacks/EDIT-R1-RB.md
reportbacks/EDIT-0-RB.md
private/goals/workshop.md              relevant extract only
```

Read `Zengine/agents/realization.md` only if the phase touches Builder/realization. Read
`Zengine/agents/surface.md` only if it touches Surface/media vocabulary. Read Loom's router and
exact laws before drawing substrate conclusions or changing Loom.

Reports are evidence and navigation. Current source and load-bearing tests decide what exists.

## 3. Current product truth

Workshop can now keep a maker through:

```text
authored load plan
    -> inspect arrangement and powers
    -> arrange a persistent desk
    -> discover/contextualize actions
    -> open one Builder-named source
    -> edit and save
    -> build
    -> realize a waiting artifact
    -> inspect
    -> edit again
```

The remaining immediate defect is source acquisition: Builder is still the only way to name what
the Editor opens.

WUX, CTX, ARR, EDIT-0, the ZOOM build/test work, and Loom SDL removal are accepted current source.
Do not reconstruct them from their phase reports unless a claim needs archaeology; spend routed law.

## 4. EDIT-1 implementation shape

EDIT-R1 concluded no further research is owed.

```text
host captures launch directory once
    -> HostContext::project_dir

Builder discovery --------+
Project Files activation -+-> open_source(normalized absolute path, mail)
future Edit Code ---------+
```

Required product outcome:

> With no useful Builder source selected, a maker can open Project Files, navigate within the
> project root, open a source, edit it, save it, and then use Builder independently.

Production boundaries:

- factor the existing Builder-agnostic open tail; do not rewrite its dirty, byte, seating, epoch,
  focus, viewport, or notice laws;
- one normalized absolute path spelling enters the door from every caller;
- relative single-source recipes are already inconsistent: Editor/preflight use CWD while the
  generated project uses its workspace. The phase must resolve both against project truth or
  state/refuse the relative case; Editor normalization alone is not a build-path repair;
- Project Files is an ordinary fourth catalog pane and rows carry only exact name plus file/directory
  kind;
- current directory is a stack below the captured root; parent navigation pops and cannot lexically
  escape;
- refresh on open/seat, navigation, explicit Refresh, and finished `BuildStatus`; never per paint;
- non-ASCII names remain visible but marked and not activatable while current path/editor custody
  cannot represent them truthfully;
- unsupported contents are refused by the Editor, not filtered by the browser;
- persist nothing beyond the pane row that setup persistence already owns;
- Builder keeps recipe discovery and becomes another caller of the door.

The production prompt must settle six bounded choices: ordering, hidden entries, link-directory
policy, pointer activation, the write-only recipe field, and whether an explicit project override is
earned now.

## 5. Do not absorb into EDIT-1

```text
tabs or multiple documents
search / fuzzy finder / recent files
create / delete / rename
recursive project index or watcher
whole-filesystem browsing or VFS
generic tree widget
language/file-type registry or syntax highlighting
provider-declared files
source-to-artifact ownership inference
build or realization ownership in Editor
right-click pane -> Edit Code
hot reload / live replacement
```

The next long loop is preserved by keeping `Editor.open(path)` reusable and browser rows free of
build topology.

## 6. Load-bearing current laws

- No privilege by default; Loom owns substrate grammar, Zengine/hosts own application policy.
- The actor remains the actor; a Weaver changes authority and performs nothing for a Session.
- Authored intent and resolved state remain separate.
- Provider route, pane identity, loaded instance, and presentation are not aliases.
- Workshop owns room, clipping, ordering, paint/hit, and recovery; providers own meaning inside the
  grant.
- Pointing names a request subject; selection is ongoing state.
- Context stores identity; owners re-judge existence/applicability at spend.
- Dispatch, help, remapping, and menus use one action truth.
- Build recipe and load-plan row are separate authored truths joined by artifact stem.
- A successful process, an artifact, a realized row, and a replaced live artifact are separate facts.
- One source document; presentation cannot discard it; dirty state blocks replacement and quit.
- Unsupported representation is refused whole rather than normalized or partially accepted.
- TUI and SDL spend one application meaning; backend reach is stated honestly.
- Verification is proportional; quote the repository's official lane, not a bare green.

## 7. Process and Prompt Contract v1

The phase prompt is scope authority. It should:

1. enumerate stop conditions once and reference them everywhere else;
2. reference standing execution rules rather than copying them;
3. state expected repository heads or name the accepted predecessor END;
4. use QR for bounded known repairs and production shape for ownership/authority/lifecycle/public
   architecture/cross-subsystem/new maker capability;
5. preflight a large production prompt whose premises were not just source-traced;
6. request `<PHASE>-RB.md` as decision layer and `<PHASE>-evidence.md` as exhaustive proof, unless a
   small QR fits one compact report.

Before commit, fan factual corrections out by meaning. For counts, search the number, phase name,
and derived arithmetic. A relevant known gap outside scope pauses for founder direction; a gap found
after push is repaired forward without rewriting honest history.

## 8. Acceptance boundary

```text
executor
    performs only the authorized phase, preserves unrelated work,
    reports START/END and evidence, does not self-accept

Vision / strategic collaborator
    reviews decision-layer claims against source and load-bearing tests,
    recommends disposition, updates private continuity only after acceptance

founder
    accepts, rejects, redirects, or requests follow-up
```

The executor does not edit private authorities or `REPOSITORIES.md`. A mechanically bounded review
cleanup is permitted only when it changes no behavior, schema, ABI, authority, persistence,
interaction, layout law, or public API.

## 9. Required report focus for EDIT-1

In addition to SC status and normal identity/evidence:

- exact owner and failure behavior of captured project root;
- path normalization and document-identity falsifiers;
- explicit disposition and witness for relative `single_source` edit/build semantics;
- root/link/non-ASCII/hidden/ordering decisions actually shipped;
- proof Builder and Project Files reach the same open door;
- proof dirty refusal and source-byte round-trip did not regress;
- proof refresh does not poll or enumerate during paint;
- live TUI and SDL navigation/open/save witness;
- no new persistence, watcher, VFS, document service, build topology, or provider contract;
- pressure exposed for the later pane-to-code/build/reload loop, without implementing it.
