# Inventory capture: data paired with typed metadata

**Status:** initial capture implemented; collection and Info reuse merged through Zengine #47.
Current sequence: [Compose and motion](inventory-compose-motion-plan.md), then [pane comfort and test setups](workshop-comfort-and-test-setups-plan.md)\
**Selected:** 2026-09-22\
**Owner:** [Workshop Goal Map](../goals/workshop.md#near-term-order-and-purpose)\
**Executor packet:** [one-slot inventory capture](../../prompts/zengine-inventory-capture.md)

## Outcome and boundary

Capture a real typed item, automatically collect a separate list of typed metadata, store the
pair in one inventory weave slot, then retrieve and interpret both through ordinary messages.
The item is the pure data the maker wanted to keep. Metadata records what was known about it
at capture. The two are acquired together and remain associated through Set/Get.

This replaces the earlier first-story proposal of Loaded inspection followed by a drafted state
read. It gives reusable information a concrete home first. One message-only inventory weave is
sufficient; no new pane, generalized inspector or drag-and-drop is needed for this phase.

The founder's longer-term inventory can contain code, data, schemas and action descriptions;
organize them into bags; describe unavailable sources; and help discover/build/load dependencies.
Custom buttons may represent opening a workstation or playing music. Dragging from inventory
should eventually use the same transfer semantics as dragging from another pane. Those consumers
guide the seam but are not immediate acceptance requirements.

## The stored pair

- **Item:** an owned snapshot of the requested data with its schema and referenced definitions
  needed for interpretation. Decoding never depends on optional metadata or the source staying
  alive. A runtime-selected schema does not require recompiling inventory.
- **Metadata:** a separate list of owned typed observations, with their own schema definitions;
  entries may have different shapes and nested structured values. Capture code derives facts
  from the retrieval and actual owners, rather than inventory inventing provenance. A snapshot
  of actual start-command data is a useful example when available.

Observed facts, supplier claims and inference retain their distinction and origin. Unknown
optional facts stay absent. A declared launch recipe is not necessarily the command issued;
several observations need not be simultaneous. Missing enrichment need not prevent a valid
capture. Malformed supplied metadata is different: the entire replacement pair must validate
before the old one changes.

One slot is empty or contains one associated pair. Set replaces both together; Get reports empty
or returns the pair. Failed Set preserves the old pair. Copies, including nested data and returned
snapshots, remain independent of supplier mutation/removal and subsequent slot replacement.
The required lifetime is the current inventory instance. Disk persistence, replacement handoff
and restart recovery are later work unless a real consumer selects them.

Captured metadata does not certify truth merely by being stored. Names, locators and participant
references carry no grants, original sender identity or renewed answer rights. Get retrieves;
executing a saved action, rebuilding dependencies or loading code remains separately authorized.

## Existing material and implementation judgment

Loom `Value` supplies runtime-described values; it claims a schema and still needs admission.
Native serialization carries schema identity, while decoding requires its actual definition.
Zengine Draft/Library already demonstrate independent copying, schema closure and codec reuse.
Library's incomplete-draft projection must not silently relax complete inventory data.

The missing representation choice is the public heterogeneous carrier. A fixed Message field
requires a particular nested schema, and a list has one declared element type. An envelope of
descriptors and encoded values is plausible; its outer admission does not admit embedded data.
Ceecee should choose the smallest coherent encoding using existing facilities. No new Any kind,
raw-pointer transport or general storage framework is selected.

Legacy VarStorage adapts different sources to one chosen output type; it does not supply runtime
schema discovery or independent custody. Preserve its source-adapter idea for a later live
reference consumer, not its borrowed callbacks as stored inventory contents.

## Execution and proof

Use one warm session for source preflight, implementation, verification and documentation. Start
from merged Loom `4b4667904888c26cda862fcce6725549c97d7141` and Zengine
`8048c058ca6b2f245017921b3a3f78e3de8308c4`, refreshing accepted newer work. Canonical local
checkouts were behind those merges during drafting. Preserve parallel Flow/pane/editor work.

The prompt owns exact acceptance evidence. Its core is an actual typed capture plus automatically
derived structured metadata, two item shapes through the same Set/Get door, schema-driven reading
without compiled sample knowledge, independent nested ownership, truthful empty/replacement/refusal
behavior and ordinary bounded authority. Use the maintained ELH facilities for the reusable route;
a graphical journey and a whole-Workshop input-authority overhaul are not prerequisites.

Capture and inventory operations need explicit permission and attributed answers. Existing guest
inspect/input grants do not imply arbitrary state or storage access. If a UI route is touched,
its actor continuity still matters; direct authorized messages suffice for this phase. Broader
loader metadata, subject resolution and input-origin research stay selected in the larger arc.

Log important discoveries, ceremony and compaction costs. Put durable answers with public contract
owners and a small ELH tool/example; report backlog dispositions without sweeping unrelated work.
The founder performs all PR merges.

## Following consumers

Next, acquire these pairs from real pane subjects and drag them out through the same typed transfer
contract, under the originating actor's authority. Add richer inspection, bags, follow/pin views,
source/dependency resolution and persistence when each has a concrete use. The previous
[maker-story direction](maker-story-development.md) remains the wider goal: people and agents
improve Workshop using its own understandable, reusable, authorized capabilities.
