# Inventory command presets and reusable views

**Status:** accepted through Zengine #53: command presets (#50), portable views/hotkeys (#51), Terminal acquisition (#52), and the interaction-authoring foundation (Loom #14 / Zengine #53).\
**Selected:** 2026-09-23, founder refinement after Zengine #49 merged.\
**Owner:** [Workshop goal map](../goals/workshop.md#near-term-order-and-purpose).\
**Current executor packet:** [Independent Info workbench](../../prompts/zengine-independent-info-workbench.md).\
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

Inventory remains process-local. Serialization does not promise durable bags. Stored role context
is an observation, never routing or authority. Required gaps, incompatible types and retained stale
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

Independent Info windows, durable bags/folders and view retirement remain later selections. A
second Info instance could let the maker keep a command and its result visible together; current
reuse works with one. Preserve these seams instead of building a second retained-payload cache.

## Several views over the same inventory

Single-entry boxes, rows/columns, contextual hotkeys, naming and added/name/type sorting are
accepted capabilities. Search/filtering, named bags, placement locks and durable storage remain
possible extensions. They should solve actual collection or workspace tasks.

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
Folders, durable storage and a general multi-pane framework remain future stories.
Multiple Info windows should preserve independent draft state and conditional saves when earned.

## Next maker stories

The founder reviewed persistence favorably and selected independent Info views next, with useful
visible controls, observation and extra correctness work for a new executor. Persistence #54 is
still open at preparation; its merge precedes development from fetched current main. The
[Info packet](../../prompts/zengine-independent-info-workbench.md) carries the full next story.
Organization remains a following choice.

### Selected next: independent Info workbench

Keep a saved result in one Info view and a command draft in another. Inspect them side by side,
drag a compatible field into the draft, and save or reuse the filled command through Compose.
Changing focus or another pane's selection must not replace a pinned subject or erase its edits.

Current Info has one InventoryEditor, room and fixed pane id; Inventory's boxes/strips already
demonstrate multiple pane ids from one provider. Use that existing seam as a starting point,
not a commitment to clone whole weaves or build a universal window framework. Current Info drops
open a subject; targeted field insertion into an existing draft needs implementation/preflight,
not an assumption that a second visible window provides it automatically.

Each view owns its selection, draft, pending operation and reply destination. Two live drafts of
the same entry are independent drafts, not independent owners: saving one must leave the other
intact, and a stale revision must refuse without discarding local edits. Copying a view must not
silently duplicate Inventory data. Copy/live-reference mode and unsaved work must remain visible.

Include a bounded create/close/reopen story and deliberate handling of dirty or pending views.
Closing a view must not delete its stored item; a late reply must not modify a reused view.
Clarify visibility versus retirement so creating views does not quietly exhaust permanent offers.
Use distinct PaneRefs if appropriate; this does not select duplicate windows for one PaneRef.
The existing general Info inspector must retain its pane-property behavior; multiple typed-value
views do not imply multiple independent instances of Workshop's current property-inspection owner.

Expose useful controls for Save, Save Copy, Refresh, Watch/Pause and creating a view. Fork, Sample
Source and Close can use compact secondary controls. Give views useful names, visible copy/link
and dirty/pending status, stable structural field selection and an understandable last observation.
Buttons and keyboard actions share behavior and authority; small rooms remain usable in SDL/TUI.

Watch a linked Inventory value with bounded, explicitly authorized observation. Dirty drafts never
silently adopt new content or revisions. Keep the last good value on failure, isolate a slow view,
and stop scheduling on pause/close. A timer is not a fresh user gesture: scoped observation custody
must be established in preflight, with no borrowed pane grants or stale gesture replay.

Separately, Sample Source obtains a new observation through at least one supported read-only
provider contract. Historical capture metadata helps explain a source; it neither authorizes
sampling nor makes arbitrary stored commands safe to replay. New observations keep fresh metadata;
the saved original remains unchanged until an explicit store action. Source disappearance and role
replacement must be legible. Automatic original-provider watching is not required.

Carry the complete story through implementation and SDL/TUI proof in one execution packet.
Reuse typed transfer/schema agreement, conditional Inventory writes and the new request helper.
Keep behavior in Zengine and the ELH story short and state-reactive. Compare the maker's source
switching and agent/host message counts against the existing single-Info story. Leave a named,
filled, documented toolbox and setup that another executor can restore in a fresh session. The
constitution now makes useful toolbox upkeep a regular development habit, without an entry quota.

### Alternative: organize a growing toolbox

Find a useful saved command/result among many entries, collect related items into a named bag or
filtered view, and arrange a hotbar without rebinding its keys. Search and grouping add something
beyond existing sorting. Keep entry identity independent of names, ordering and membership;
removing a placement or collection must not accidentally delete its data.

Select this first if finding material has become more costly than combining it. The exact
membership/folder model needs a concrete collection story; arbitrary hierarchy is not required.

### Selected: keep a toolbox across restarts

Save useful typed entries and their configuration, stop Workshop, restart, and explicitly restore
them. This makes sessions accumulate work instead of ending as demonstrations. The implementation
is ready for founder review in [Zengine #54](https://github.com/Krealsion/Zengine/pull/54), with
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
investigation. Durable folders/bags, focus-dependent scopes and user-designed box
faces remain later work. Terminal payload acquisition is now accepted separately.

### Pressure for the next selection

- Extra view identities currently remain offered after closing a window. Empty views can be
  reused, but retiring offers and reclaiming the twelve-view bound need an explicit lifecycle
  story before unrestricted workspace editing.
- Explicit activation persists when a window closes. Focus-dependent contexts and readable
  user-authored context names can build on the two existing switches without redefining data.
- ELH can inspect pane rows and current view state, but menus still require known action order.
  Discoverable menu action identities would remove that remaining script ceremony.
- Generic commands report queueing and recognized acknowledgements/refusals. Domain-specific
  completion remains the receiving weave's contract; a queued message is never reported as done.
- Configured bindings for unavailable entries consume the bounded configuration list. Explicit
  retirement should remove configuration only, never silently retarget it to a new occupant.

The acquisition and interaction-authoring reports own their run-specific request counts. They
vary with scrolling and screenshot transport; they are evidence routes, not a fixed cost contract.
