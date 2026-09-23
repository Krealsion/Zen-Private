# Inventory reuse and timed movement

**Status:** implementation, real SDL demo and local verification complete; PR #48 open with all six reported checks green at the 2026-09-22 planning review. Founder merge remains pending.\
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

The founder selected a short [pane comfort and reusable test setup detour](workshop-comfort-and-test-setups-plan.md)
before expanding commands: sensible initial sizes, one-command starting setups, a visible reset
and measurements of agent commands, remote requests and internal messages. This turns the
demonstrated story into a quick repeatable starting point. Implement from verified current main
after PR #48 merges. The plan owns this scope; the continuation below remains next afterward.

## After the setup detour

Make command reuse a convenient toolbox: named command presets and incomplete forms.
Choose persistence explicitly in that preflight; the current Inventory remains process-local.
Start with one command that needs values supplied by inventory slots, show each missing field,
and require an explicit run gesture after completion. Preserve the distinction between a
complete admissible stored value and an unfinished draft (the existing draft library already
has a projection for the latter). Keep target-role observations separate from authority.

Preflight the real ceremony first: choosing the receiver via Loaded, finding a compatible field,
and recovering from a stale entry revision. Use that evidence to choose the smallest field-level
acquisition addition and drop affordances. Do not promise automatic rebinding or retries.

## Deliberately outside this phase

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
BL-WORK-02 remains preserved; BL-VERIFY-01 and BL-DEF-06 are not awakened by this scope.
The constitution now requires a verified current-main branch, screenshots on visual PRs,
and a complete branch/build handoff. Keep compaction and exploration friction in the report,
not in growing agent memory. No automatic merging.

The live story also earned Loaded viewport scrolling without changing selection. The visible-pane
query refuses overlaps and panes reaching into status bands; richer partial-visibility queries
can wait for a story needing them. The current Compose preview substitutes unsupported text bytes
while retaining their original data; a richer text renderer is a separate presentation improvement.
