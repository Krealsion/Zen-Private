# Inventory command presets and reusable views

**Status:** implemented and locally verified; PR review and founder acceptance pending.\
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

The founder's fuller story starts with a completed Terminal command, removes values, and fills it
using saved command results, potentially inspected beside it. This is the recommended next source story after acceptance of the preset path.

Preflight confirmed Terminal's `TranscriptShown`/`ShownEntry` seam supplies rendered facts
rather than typed payloads/stable acquisition handles. Loom TerminalSession retains bounded incoming data, but its Submitted records carry no original
command payload. Completing outbound acquisition therefore needs an explicit retained-payload,
retrieval-authority and eviction contract at that owner. Display text is not a serialization
format. A copied historical message carries content and optional observational metadata, not an
old sender, grant, reply relationship or pending operation. Evicted/unavailable records remain
unavailable; do not re-execute them to reconstruct their data.

If this requires independent Loom retention/retrieval work, complete the generic preset story
first and report the exact seam. A second Info instance is a presentation/lifetime question,
not a prerequisite for using saved values as inputs. No compulsory phase split when a clean,
bounded extension can finish in the current implementation session.

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

These are design constraints and future stories, not approval for a hotbar, folder system,
multi-pane framework, hidden automation, hotkey grammar or persistence mechanism in this phase.
Multiple Info windows should preserve independent draft state and conditional saves when earned.

## Order and proof

1. Review and accept the implemented reversible preset story in existing Inventory/Info/Compose,
   using the maintained `presets` setup, visible Reset and reactive ELH proof. Its data/authority
   boundaries are ready for the next source to reuse.
2. Close any remaining typed Terminal command/result acquisition gap, grounded in retained data
   and authority. Include independent Info views when simultaneous inspection demonstrably helps.
3. Try one alternate inventory view, likely a single slot or small hotbar, against an actual task.
   Earn locking/binding semantics there; add folders, sorting and hotkeys when they simplify it.

This order is dependency-led, not a mandatory PR count. The executor may finish a bounded adjacent
source path while implementing the first story. Compare maker actions, agent calls, remote asks
and attributed host work. Keep large screenshot transfers and truncated recording separate.

BL-WORK-01 remains active through legible UI and public tools/guides. BL-WORK-02 remains preserved.
BL-DEF-06 was accepted with #49 and removed from the live backlog; its evidence remains in Git and
the prior report. BL-VERIFY-01 stays parked unless its specific Builder witness is touched.
