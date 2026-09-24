# Inventory command presets and reusable views

**Status:** accepted through Zengine #55: command presets (#50), portable views/hotkeys (#51), Terminal acquisition (#52), interaction authoring (Loom #14 / Zengine #53), toolbox persistence (#54) and independent Info views (#55).\
**Selected:** named nested Inventory folders, after the founder merged #55; implemented for review in
[Zengine #58](https://github.com/Krealsion/Zengine/pull/58) ([report](../../reportbacks/zengine-inventory-named-folders-RB.md)).\
**Owner:** [Workshop goal map](../goals/workshop.md#near-term-order-and-purpose).\
**Current executor packet:** [Named Inventory folders](../../prompts/zengine-inventory-named-folders.md).\
**Foundation:** [Reusable demo setups](workshop-comfort-and-test-setups-plan.md).

## Purpose and first complete story

Make saved commands useful material that a maker can reshape, instead of rebuilding each form.
The path works in either direction: start blank and add values, or start with a complete command
and remove the arguments that should vary. Existing inventory slots earn more general use before
new presentation types expand the UI.

Complete command → independent named preset → unset selected values → save incomplete draft →
reopen in Compose → fill gaps from a saved typed result through Info → review → explicit run.
Preserve the original on the copy route. An explicit live update keeps identity and checks its
revision. Names are presentation; neither a list row nor the next slot occupant is an identity.
A real owner reply can supply saved-result data without a general Terminal history feature.

Removing a field means removing its value while preserving the schema field and its requirements.
An unfinished preset is legitimate data, but not a complete message ready for dispatch. Keep absence
separate from false, zero, empty text and empty containers. Do not persist hidden excluded values
as if they were removed. Typed field acquisition should avoid manual transcription, including a
scalar where useful, and compose through shared meaning rather than command-specific adapters.

## Source preflight and decisions delegated

The implementation started from fetched main `a7f4648933d71f3941c2ab4ed95ef84cdeb23dc5`
(PR #49). A complete `StoredDraft` envelope carries one existing Library entry, preserving its
original schema closure and missing values. Inventory admission remains strict. `FieldValue`
carries a selected typed branch and structural path using that same codec, without sibling values.
Info requests current actor acquisition permission; Compose checks the complete current type
agreement and requires separate permission at explicit submission.

Compose Ctrl+B stores blank or incomplete presets; Ctrl+S stores complete commands. Info Ctrl+B
forks a preset copy, Ctrl+U unsets a value, Ctrl+S saves, and Ctrl+G picks up a typed field to place
in Compose. Copy and conditional live-save paths retain their prior custody. The maintained
`presets` demo layout shows Inventory, Info, Loaded and Compose together and resets both editors.
SDL repetition across visible Reset preserved saved entries; the shared TUI story also passed.
The [report](../../reportbacks/zengine-inventory-command-presets-RB.md) owns verification details.

Live Inventory identity remains process-local; toolbox save/restore supplies explicit durability.
Stored role context is an observation, never routing or authority. Required gaps, incompatible types and retained stale
revision arguments refuse rather than defaulting, silently refreshing or retrying an effect.

## Terminal and answer acquisition

The accepted story starts with actual Terminal command/reply data, stores named copies,
then removes a command field in Info and fills it from a saved reply through Compose. Ordinary
primary dragging acquires a copy; the secondary menu offers pick-and-place. This completes the
selected source connection without widening Terminal's vocabulary or guest execution authority.

Loom #13 now owns exact observation retrieval with separate 64-item authored and received windows.
Zengine #52 maps numbered wrapped rows to terminal instance/observation identities and authorizes
retrieval at Workshop's current actor boundary. Metadata records historical source facts separately
from the pure item. Capturing never reparses text, reruns a command, restores old authority or
recreates a pending conversation. Evicted/unavailable and oversized payloads refuse.

The [phase report](../../reportbacks/zengine-terminal-inventory-capture-RB.md) owns verification.
SDL, TUI and a warm SDL rerun proved capture/preset reuse and refusal without invocation authority.
The loaded-pane witness separately proves explicit maker-authorized hotkey delivery exactly once.
The founder merged #52; the subsequent authoring phase replayed the same story in SDL and TUI.

Independent Info views now keep a command and its result visible together. Named nested folders
are selected next; general view retirement remains a separate seam. No second retained-payload
cache is needed for organization.

## Several views over the same inventory

Single-entry boxes, rows/columns, contextual hotkeys, naming and added/name/type sorting are
accepted capabilities, along with explicit toolbox persistence. Named folders are selected next;
search/filtering and placement locks remain possible extensions for demonstrated tasks.

The direction is multiple views over shared owned entries, with independent selection/layout and
Info drafts. A view is not another authoritative copy of every stored item. A single view may
show a copy/snapshot or explicit live reference when that is the chosen operation; make the
binding visible. Removing or changing an entry must not redirect a stale view to a new occupant.

Keep three meanings distinct when these stories are selected:

- Collection identity and content: owned by Inventory; names/folders help organization.
- Slot placement and future locks: view configuration; bindings already follow entry identity.
  Sorting a collection must not silently rebind a pinned hotbar item.
- Invocation: command-specific explicit action using current authority; plain data and unfinished
  drafts remain inspectable/draggable, and are not secretly runnable buttons.

The accepted portable-view contract below owns boxes, strips and explicit contextual hotkeys.
Folders now have a selected collection story; a general multi-pane framework remains unselected.
Multiple Info views already preserve independent draft state and conditional saves.

## Next maker stories

The founder accepted independent Info views by merging #55 and selected named Inventory folders
next. The [folder packet](../../prompts/zengine-inventory-named-folders.md) carries implementation
and proof together, with a cheap owner/compatibility preflight in the same session.

### Selected next: named Inventory folders

Make a growing toolbox navigable through named nested folders: open a folder to see its immediate
children, climb to its parent, and return to root or an ancestor with a visible location. This is
Explorer-like traversal, not a filesystem or a requirement for a complete Explorer clone.

Create and rename folders, move entries and subfolders without changing entry identity, and
preserve nesting in saved toolboxes. Previously shipped flat files load at root. Empty-folder
deletion is enough; nonempty removal may refuse rather than delete stored material. Tree cycles,
invalid destinations, stale gestures and malformed restore candidates refuse without losing the
existing usable state. Pending work binds to the destination it began with, not the folder now
being viewed.

Folder membership and portable placement remain distinct. A box/strip does not become a second
owner, and moving or displacing its entry has a defined reachable home. Bindings continue to follow
entry identity; folder navigation grants no authority, changes no activation context and executes
nothing. Info links/drafts remain attached to their entries as folders are renamed or rearranged.

Reuse the filled inspection workbench: organize samples and command drafts, retrieve them through
nesting, combine fields in independent Info views, save, restart and restore. Zengine owns folder
behavior and integrity; a short ELH story demonstrates it in SDL and TUI. Record maker actions,
agent commands, remote asks and attributable host work separately. Search, tags, Back/Forward
history, multiselect, recursive deletion and folder-specific hotkey contexts remain unselected.

**Implemented for review ([Zengine #58](https://github.com/Krealsion/Zengine/pull/58)).**
`zengine.inventory` owns folders and membership beside entry names; folder identity is `{owner,
folder}` and membership never changes an entry's revision, so linked drafts still save. The pane
browses one folder with a location row, crumbs and `[Up]`; a second press or Enter opens a folder;
drops on folders file entries while placement stays a separate fact; toolbox files are version 2 and
version 1 files restore at Root. The organized workbench (`phase=organize`, `phase=folders`) repeats
in fresh SDL and TUI processes. The
[report](../../reportbacks/zengine-inventory-named-folders-RB.md) lists twelve overridable choices;
notably the second-press rule differs from Files.

<a id="selected-next-independent-info-workbench"></a>

### Accepted: independent Info workbench

[Zengine #55](https://github.com/Krealsion/Zengine/pull/55) is merged. Four Info views (the default
pane plus three reusable value-view slots) retain independent subjects, structural selection,
drafts and requests. Visible controls support saving, copying, refreshing, linked-value watching
and explicit source sampling. Typed fields can move between views and into a command draft.

The corrected adoption policy freezes conflicting edits during replacing reads, provides Stop
without declaring remote failure, preserves edits made during saves, and releases watch custody
including late approvals and reused slots. Broader incarnation identity, invalidation fanout and
Info's class split remain P-WORK-27/BL-WORK-03 work, not hidden prerequisites for folders.

The maintained `inspection-workbench` toolbox, `workshop/workbench` tool and `workbench` setup
are the reusable starting point. The [original report](../../reportbacks/zengine-independent-info-workbench-RB.md)
and [corrections report](../../reportbacks/zengine-independent-info-workbench-corrections-RB.md)
own validation, measurements and remaining seams. The legacy section anchor above preserves
existing navigation into this plan.

### Selected: keep a toolbox across restarts

Save useful typed entries and their configuration, stop Workshop, restart, and explicitly restore
them. This makes sessions accumulate work instead of ending as demonstrations. The founder merged
[Zengine #54](https://github.com/Krealsion/Zengine/pull/54), with
explicit named snapshots, distinct from same-shape reload continuity. The
[report](../../reportbacks/zengine-inventory-persistence-RB.md) owns validation and measurements.

Persist schema-bearing data and deliberate configuration, never old grants, pending operations
or a claim that an old live reference is valid again. Source absence, schema/version changes,
damaged storage, destination re-resolution and shortcut activation need explicit behavior.
The chosen boundary is one save/restore operation over collection data and portable slot/binding
configuration. Screen geometry retains its existing setup owner. File access needs a separate
guest toolbox power. Restore validates the complete candidate, fences concurrent writers and
starts hotkeys OFF. Old references embedded in user data remain historical; only toolbox-owned
placements reconnect through saved entry keys. Automatic boot/quit writes, schema migration and
multi-writer synchronization are not selected. Bags are not a prerequisite.

The real restart proof saved eleven entries and reused a saved command in fresh SDL and TUI
processes. Each restore is one ELH ask with no input session. Recorder attribution still exposes
publication, offers and redraws behind it; a one-request interface is not a one-message host.
Saved view identities reconnect existing setup files. Without offer retirement, restoring a
different collection of views can exhaust the twelve-id union: refuse before committing and
use a fresh Workshop. Retiring offers belongs with the future view-lifetime story.

### Enabling work and boundaries

Discoverable menu action identities would remove current ELH dependence on known action order.
Consider that bounded improvement when the selected story needs new context actions. Cross-pane
carry completion should let a source clear obsolete status without making it own the receiver.
View retirement/configuration cleanup is related to adding views; the broader fixture split stays
trigger-driven under P-BUILD-08. Flow UX and presentation research continue independently.

Each selected packet owns its complete story and proof. Compare maker actions, agent calls,
remote asks and attributed host work. Screenshot transport optimization is a separate question.

BL-WORK-01 remains active through legible UI and public tools/guides. BL-WORK-02 remains preserved.
BL-DEF-06 was accepted with #49 and removed from the live backlog; its evidence remains in Git and
the prior report. BL-VERIFY-01 stays parked unless its specific Builder witness is touched.

## Accepted portable-view contract

One Inventory-owned entry has one portable placement; default dragging moves that placement
between these views or returns it to
main Inventory. A filled single box returns its displaced entry without deleting data. Other
receiving panes still get a copied value. Explicit duplication creates independent data, with an
immediate name editor or the next available numbered name.

Bindings travel with entry identity. A duplicate retains the source key and explicit target, but
starts disabled. Main Inventory and newly created view contexts start OFF. Both the item and its
context must be enabled; activating conflicting contexts refuses without replacing the incumbent
binding. Execution always needs the current input actor's exact destination/shape authority.
Data, observational metadata and stored configuration never contain an execution grant.

[Portable-slot packet](../../prompts/zengine-inventory-portable-slots.md) owns this phase's scope.
The [phase report](../../reportbacks/zengine-inventory-portable-slots-RB.md) owns verification;
the [exploration log](../../reportbacks/zengine-inventory-portable-slots-exploration.md) records the
investigation. Named folders are selected next; focus-dependent scopes and user-designed box
faces remain later work. Terminal payload acquisition is now accepted separately.

### Pressure for the next selection

- Extra view identities currently remain offered after closing a window. Empty views can be
  reused, but retiring offers and reclaiming the twelve-view bound need an explicit lifecycle
  story before unrestricted workspace editing. Info's views in #55 stay bounded by reusing four
  fixed slots rather than by retiring offers; general offer withdrawal remains open.
- Explicit activation persists when a window closes. Focus-dependent contexts and readable
  user-authored context names can build on the two existing switches without redefining data.
- ELH can inspect pane rows and current view state, but menus still require known action order.
  Discoverable menu action identities would remove that remaining script ceremony. #55's
  `PanePointRequested` lets a tool press a painted control by its label, so the workbench tool
  avoids menus. Menus themselves are unchanged.
- Generic commands report queueing and recognized acknowledgements/refusals. Domain-specific
  completion remains the receiving weave's contract; a queued message is never reported as done.
- Configured bindings for unavailable entries consume the bounded configuration list. Explicit
  retirement should remove configuration only, never silently retarget it to a new occupant.
- Folders (#58, for review) are organization only: a folder is not a hotkey context, and a
  per-folder context would be view configuration keyed by folder identity. The same retrieval took
  1 maker action flat and 7 through two folder levels in the four-entry workbench; organization
  pays only as collections grow, so search or a flat "all entries" view are the next candidates
  if use shows that cost.

The acquisition and interaction-authoring reports own their run-specific request counts. They
vary with scrolling and screenshot transport; they are evidence routes, not a fixed cost contract.
