# Inventory command presets and reusable views

**Status:** selected next phase; prompt prepared, implementation not started.\
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

Verified merged main: `a7f4648933d71f3941c2ab4ed95ef84cdeb23dc5` (PR #49), tree-equal to its reviewed
product tip. Refresh again at execution. `message-draft::Draft` already supports unset and partial
state; `Library` preserves original schema closures with a private presence projection. Inventory
pairs correctly require complete admission. Compose saves only complete messages, and its local
presence toggle is not yet a stored-preset editing route. Info has scalar editing but no unset UI.

The executor chooses a representation and bounded shared edits after tracing these owners. Prefer
existing draft/library support; the stored preset must itself be valid typed data. Ordinary item
admission stays strict, and projected optional shapes never become runtime message contracts.
Scope the first lifetime to current process-local Inventory. Durable bags are not silently promised
because the lower draft library can serialize data. Store target observations separately from
current routing and authorization. A reused command is always the current actor's new act.

Keep destination/schema agreement, required-field checks, stale-revision refusal and authentic
owner answers visible. A drop never executes. Missing data, changed schemas or expired source
references produce an attributable outcome, not a default value or an automatic effect retry.

## Terminal and answer acquisition

The founder's fuller story starts with a completed Terminal command, removes values, and fills it
using saved command results, potentially inspected beside it. This is the preferred follow-on
source and may land in the same session if the owner contract is already sufficient.

At the checked baseline, Terminal's `TranscriptShown`/`ShownEntry` seam supplies rendered facts
rather than typed payloads/stable acquisition handles. Preflight must inspect the actual retained
record and its retrieval authority before promising drag-out. Display text is not a serialization
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

1. Deliver the reversible preset story in existing Inventory/Info/Compose, using the maintained
   `commands` setup, visible Reset and a small reactive ELH proof. Pin incomplete roundtrip,
   typed acquisition, copy/live custody and explicit execution.
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
