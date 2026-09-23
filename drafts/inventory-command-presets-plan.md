# Inventory command presets and reusable views

**Status:** command presets accepted and merged in Zengine #50; portable inventory views and contextual hotkeys accepted and merged in [PR #51](https://github.com/Krealsion/Zengine/pull/51). Terminal command/result acquisition is implemented for review in [Zengine #52](https://github.com/Krealsion/Zengine/pull/52); its Loom #13 dependency is merged.\
**Selected:** 2026-09-23, founder refinement after Zengine #49 merged.\
**Owner:** [Workshop goal map](../goals/workshop.md#near-term-order-and-purpose).\
**Executor packet:** [Reusable command presets](../../prompts/zengine-inventory-command-presets.md).\
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

The current review story starts with actual Terminal command/reply data, stores named copies,
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
Review and founder acceptance remain distinct from these results; #52 is open.

Independent Info windows, durable bags/folders and view retirement remain later selections. A
second Info instance could let the maker keep a command and its result visible together; current
reuse works with one. Preserve these seams instead of building a second retained-payload cache.

## Several views over the same inventory

The founder proposes single-entry boxes behaving as draggable buttons; rows or columns of slots
like a game hotbar; and hotkeys mapped to slots, with locking, sorting and folders. These are
valuable later arrangements of the same toolbox. Use generic inventory behavior first to discover
which layouts remove actual work.

The direction is multiple views over shared owned entries, with independent selection/layout and
Info drafts. A view is not another authoritative copy of every stored item. A single view may
show a copy/snapshot or explicit live reference when that is the chosen operation; make the
binding visible. Removing or changing an entry must not redirect a stale view to a new occupant.

Keep three meanings distinct when these stories are selected:

- Collection identity and content: owned by Inventory; names/folders help organization.
- Slot placement and locks: view configuration; sorting a collection should not silently rebind a
  pinned hotbar item. Decide whether each hotkey binds a slot or an entry and display that policy.
- Invocation: command-specific explicit action using current authority; plain data and unfinished
  drafts remain inspectable/draggable, and are not secretly runnable buttons.

The selected portable-view phase below now authorizes boxes, strips and explicit contextual
hotkeys. Folders, durable storage and a general multi-pane framework remain future stories.
Multiple Info windows should preserve independent draft state and conditional saves when earned.

## Order and proof

1. Command presets and portable views are accepted through #51, including compact shared-border
   tiles, naming on arrival and contextual hotkeys.
2. Review and land the implemented typed Terminal command/result acquisition in #52, grounded in
   retained data and current actor authority.
3. Complete the selected [interaction-authoring phase](interaction-authoring-plan.md) before the
   next dependent maker story: reduce repeated request bookkeeping, diagnose missing reply grants,
   repair the contributor route and measure build friction.
4. Add independent Info views when simultaneous inspection demonstrably helps. Expand organization
   or durable bags only against an actual task. Folder and locking policy
   should simplify the existing identity model rather than replace it.

This order is dependency-led, not a mandatory PR count. Each selected packet owns its scope;
unrelated Flow and pane UX work can continue. Compare maker actions, agent calls, remote asks
and attributed host work. Keep large screenshot transfers and truncated recording separate.

BL-WORK-01 remains active through legible UI and public tools/guides. BL-WORK-02 remains preserved.
BL-DEF-06 was accepted with #49 and removed from the live backlog; its evidence remains in Git and
the prior report. BL-VERIFY-01 stays parked unless its specific Builder witness is touched.

## Selected portable-view phase

The founder selected single boxes and row/column strips next. One Inventory-owned entry has one
portable placement; default dragging moves that placement between these views or returns it to
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
investigation. Durable folders/bags, focus-dependent scopes, user-designed box
faces and Terminal payload acquisition remain later work; this phase does not require them.

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

### Terminal-story pressure for a following phase

- Two simultaneous Info views would reduce source swapping while composing from saved replies.
  Choose this if the next story involves comparing or combining several stored values.
- The maintained story uses 80 hand requests before cleanup on its first run. SDL's two screenshots
  raise the total to 261 link asks (TUI: 85); a warm SDL run uses 282 because locating older rows
  adds scrolling. These are observations, not a request to optimize transport in this phase.
- General menus still require a known action order in the ELH story. Discoverable action identities
  and screenshot transport efficiency belong to the ELH improvement seam already identified.
- Info's source-side field-carry notice can remain after another pane receives the copy. A later
  carrier-completion signal could make cross-pane status clearer without making Info own Compose.
- Broad seam/test-fixture headers make Windows iteration costly. The selected
  [interaction-authoring phase](interaction-authoring-plan.md) measures this friction alongside
  repeated request mechanics and the missed native reply grant. Bounded dependency improvements
  need evidence; a build-system rewrite is not selected.
