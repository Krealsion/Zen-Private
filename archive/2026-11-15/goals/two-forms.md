# Two forms and Flow

**Status:** broader design horizon; the interpreted/generated Flow foundation has landed\
**Current direction:** [Strategic Map](../zen-strategic-map.md) and [Workshop Goal Map](workshop.md)

Design answer (Joshua, with Vision), 2026-09-05, reached while reviewing Zengine PR #10.
Current baseline refreshed 2026-09-19: Flow now consumes `maker/` for live interpreted execution
and supports native generation in the standalone workbench (PR #40); Workshop has a graphical
authoring consumer (PR #41). [Current Flow contracts](../../Zengine/docs/reference/flow.md)
own those mechanisms and the limited generated-code recovery claim. The
[Workshop roadmap](workshop.md#flow-ux-research-and-hierarchical-authoring) selects the next UX
research. The broader ideas below remain horizon, particularly arbitrary-code deconstruction
and generic changed-shape development. They do not authorize implementation by themselves.

**The decision: both forms, one bridge.**
- **The live form** is the definition, interpreted by `maker/`: rapid, inspectable to the last
  moving part, admitted as inert data, runs on any host with no toolchain. Edits are a
  `swap_state` or a succession, never a build.
- **The durable form** is a generated C++ weave against the Loom ABI, built by the Workshop's
  Builder: optimized, unrestricted, able to keep a secret inside itself while its messages stay
  visible on the bus. A veteran may write it by hand against a plain library surface and never
  learn the definition grammar.
- The maker always knows which form they are editing. "Completion" — the act that generates the
  durable form — needs a name that carries its terminating condition (repository-conventions).

**Why both** (Joshua's reasons). All-interpreted makes secrets very hard to keep; its grammar is a
Zen-only language, and a veteran may simply want a library surface and to run wild in C++;
someone who needs a new operator must never be stuck. Codegen-only loses the program-itself
liveness, the laid-bare interior, and sharing with a stranger who has no compiler. The vision's
"two views of the same thing" is satisfied by a bridge, not by a single form.

**Flow is the bridge, in both directions.**
- *Generation is total.* Every definition generates, and the generated code carries its
  definition (embedded or beside it, hashed): untouched generated code flowcharts perfectly by
  construction, not by cleverness.
- *Deconstruction is partial and improving.* Flow reads code into its world as far as it
  understands and draws a raw node where it does not; it is not its responsibility to understand
  everything. Its handles are the ABI: `Accept<>`/`on` handlers (an external input enters and
  starts its own graph section), `Emit<>`/sends (flow backward from what is emitted), `ZEN_SHAPE`
  state. The floor is total: the handler-level graph — inputs, emits, state fields — is derivable
  from declarations alone and, for a running weave, from the bus (`accepted_schemas`, the grant,
  `PokeStructure`). A raw node is only ever an interior.
- *State change is a Flow node* — a before/after comparison where the weave exposes suitable
  state and observation captures both boundaries. This can serve the durable side too, but a
  bus event alone does not expose arbitrary native internals, preserve a continuation, or
  guarantee that the cause of a compiler-related failure appears in the captured state.
  Missing snapshots remain visible gaps.

**Raw nodes — a hypothesis, recorded as one, not law.** A raw section may be treated as an
operator iff it has no bus access, directly or through anything it calls. Two confidences:
- a node the maker authors and the Builder compiles against the operator ABI is bus-free *at the
  door* by construction — registration by value, `operator/primitives.hpp` 47–50: an operator
  cannot be handed a Bus, a Kernel or a Workshop — but not *in the room*: ambient globals remain,
  and the tree says no hostile-code claim is implied;
- a section the deconstructor carves from existing code needs a static, transitive check.
The test that would earn a law: deconstruct the tree's own compiled weaves and count how much
interior is bus-free. Flow becoming exceptionally good at sending messages is what would make
interiors mostly bus-free; Joshua hesitates to make this law before it is shown, and this note
keeps that hesitation.

**The definition format is the fixed point; tools are replaceable.** Generators and
deconstructors consume and produce definitions. As deconstruction's ceiling rises, so do the
tools against degradation; a better deconstructor may arrive as someone's shared tool, be adopted
like a beloved mod, and become the default (the vision's "same stuff", "find what others made").

Flow should also be able to participate in the founder's
[inspect/repair/continue direction](workshop.md#authored-continuity-and-repair): help a maker
reach an operation, inspect the evidence available in either form, and choose an authored repair.
It is one possible tool for that loop; neither Flow nor the interpreted form is a prerequisite
for message-based diagnosis, native debugging or rebuilding with an authored handoff.

**Landed foundation and remaining roads.**
- Standalone generation and generated-source recovery now exist under the current Flow
  contracts. Broader Builder integration follows its own consumer; the earlier sketch of a
  generator is not an outstanding instruction to rebuild it.
- General deconstruction beyond verified generated source, including a handler-level graph
  from arbitrary native declarations or a running bus, remains a separate capability.
- `DownloadAndConfigureCMakeWeave` for a recipient without a toolchain: a recipe that fetches
  and runs a compiler is the most powerful thing a recipient is asked to trust — provenance
  first (the vision's seventh line; the identity phase).

**Implications for a future Flow phase, when selected.** The operator ladder is a requirement, not a footnote:
writing and mounting a raw node must be as smooth as snapping one, or the wall returns through
the side door. Today that requirement fails at the provider: a C++ leaf written in the Editor is
built by Builder and mounted by the plan, but a rebuilt provider is never remounted
(`Zengine/agents/realization.md`), so a raw node is as smooth as a snapped one only once a provider
can be remounted ([Flow's powers](../../reportbacks/zengine-flow-powers-RB.md), 2026-09-30). A
visible indicator of the form being edited. The definition kept as the artifact
after completion, so the live view is never lost.

See [identity design](identity-phase.md) for the author-identity and re-consent rules both forms will meet.
