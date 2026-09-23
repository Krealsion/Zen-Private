# Inventory reuse and timed movement

**Status:** PR #48 and the subsequent comfortable-pane/demo setup PR #49 are merged. Reversible command presets are selected next.\
**Owner:** [Workshop goal map](../goals/workshop.md).  
**Phase:** [scope](../../prompts/zengine-inventory-compose-motion.md).

The inventory collection and copy/live Info paths are merged through Zengine #47. This phase
earns Compose as a receiving tool: compatible typed arguments or a complete command can be
copied into a form, reviewed, stored and explicitly submitted with the initiating actor's
authority. A drop never executes a command. Workshop remains an opaque transfer coordinator.

Input owns elapsed-time pointer motion. A pure linear/cubic Bezier sampler exposes the same
math for future animation, without creating an animation manager now. The external-host demo
reads current visible pane rows, requests motion, and verifies owner state. It supplies story
logic; it does not decode product geometry or implement transfer semantics.

## Recommended next phase

The [comfort/setup detour](workshop-comfort-and-test-setups-plan.md) is accepted with #49.
Its maintained command desk is the starting point for
[reusable presets built forward and backward](inventory-command-presets-plan.md).

## After the setup detour

The [preset/view plan](inventory-command-presets-plan.md) owns the selected scope: start from a
complete command, remove values without changing its schema, save the unfinished draft, refill
it from saved typed data and explicitly run. It also records Terminal command/result acquisition,
independent Info views and later single-slot/hotbar presentations. The current collection gets
more general use first. This completed motion phase owns no competing continuation checklist.

## Outside the completed motion phase

- Undo of external effects: owners need explicit inverse/conditional operations or checkpoints;
  pointer replay and a saved form cannot undo an already executed command.
- Durable bags, cross-process inventory persistence, unavailable-source resolution, automatic
  dependency building and toolbox launch buttons. Current inventory state is process-local.
- General field grabbers and scalar transfer envelopes, partially filled command presets,
  automatic command history and right-click Run. Complete commands can be stored explicitly.
- Animation scheduling, easing catalogs, arc-length curve traversal, GPU transitions and the
  accordion layout story. Only reusable geometry/time sampling is earned here.
- Universal semantic selectors, canvas/OCR introspection and exclusive remote input leases.
  The new query is a bounded visible-text reading; physical input may still intervene.
  Session close releases a held button at its last position, so cancellation is not atomic
  rollback of a partial gesture. A dedicated cancellation/lifetime signal deserves a later
  owner-led story if stronger abort guarantees become necessary.

## Process and backlog

BL-WORK-01 is addressed through a maintained public story and discoverable tool entry.
BL-WORK-02 remains preserved; BL-VERIFY-01 was not awakened by this scope. The subsequent #49
setup phase completed BL-DEF-06, now accepted and removed from the live backlog.
The constitution now requires a verified current-main branch, screenshots on visual PRs,
and a complete branch/build handoff. Keep compaction and exploration friction in the report,
not in growing agent memory. No automatic merging.

The live story also earned Loaded viewport scrolling without changing selection. The visible-pane
query refuses overlaps and panes reaching into status bands; richer partial-visibility queries
can wait for a story needing them. The current Compose preview substitutes unsupported text bytes
while retaining their original data; a richer text renderer is a separate presentation improvement.
