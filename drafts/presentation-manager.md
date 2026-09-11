# Presentation as a managed service

**Discussion draft — 2026-09-11.** Incorporates the founder's direction on initial ownership,
authored continuity and inspect/repair/continue. Concrete transitions and experiments remain
proposals; no implementation, protocol version, new Loom facility or extraction scope is selected.
The [source research](presentation-manager-research.md) separates current mechanisms from proposals.

The working bet: give presentation one understandable owner, built from the same material as
the tools it presents. Workshop supplies application policy and connects the participants.
The presentation manager turns their contributions into a coherent place to look and act.

## 1. What failure means here

A weave is allowed to be mistaken, silent, or permanently pending. A manager is also an authored
program and can be wrong. The architecture should make these behaviors attributable and give
other authorized participants useful ways to respond. It cannot promise correct authored code.

For Zengine, we aim to implement those responsibilities well: preserve work, tell the truth,
and make an unfinished operation inspectable. A refusal, a handler that failed, an output
provider's reported problem, and an unanswered request are different facts. Waiting is a valid
state; lack of progress is not evidence of its cause. Existing realization law already permits
an unanswered load to remain loading indefinitely. [E1](presentation-manager-research.md#e1-unanswered-work-and-existing-management)

External architecture supplies a place to observe, decide and recover. It need not make the
original operation succeed. Choosing another output provider may restore a useful Workshop
while the first provider's unfinished operation remains honestly unresolved.

## 2. Put these responsibilities together

“Presentation manager” names a responsibility, not a new mandatory base class, Kernel manager,
or the existing Pane Manager tool. The founder's initial direction is one application-facing
service owning composition and output selection, with clear internal ownership of layout,
input and provider lifecycle. Splitting source files and splitting authoritative owners are
separate choices; neither must turn this first step into several services.

Replaceability is the design test. A successor manager should be able to take over through
named contracts and authored handoffs. Composition and output selection should have an
identifiable future separation, without requiring a separate protocol for every internal part
today. If a later change needs cooperating consumers to change, that is permitted: make the
affected contracts and dependencies discoverable so migration, adapters, regeneration or maker
intervention can follow them. Intelligent propagation may be partial and require correction;
it must expose unsupported joins instead of claiming that every dependent was repaired.
This is a criterion for design review, not a proposal to build an automatic dependency updater.

```mermaid
flowchart TD
    W[Workshop: application policy and connections] --> P[Presentation manager]
    T[Tools: documents, builds, terminal sessions] -->|Contributions and observations| P
    I[Input readers] -->|Platform events| P
    P -->|Subject-bound gestures| T
    P -->|Selected picture and output configuration| O[Output provider]
    O -->|Extent, capabilities, reported output condition| P
    P -->|Lifecycle requests| L[Existing realization and lifecycle owners]
    L -->|Observed outcomes| P
    P -->|Inspectable operation state| D[Attention, inspector, journal]
    L -->|Independent host observations| D
```

| Owner | Its authoritative facts |
|---|---|
| Workshop | Project intent, policy, grants, which services are connected, and allowed recovery choices |
| Presentation manager | Admitted contributions, arrangement, selection/focus, semantic input routing, active output binding, and its presentation operations |
| Tool weave | Its document, build, terminal session or other subject; what gestures mean and whether a requested change is admissible |
| Output provider | Its device/resources, actual extent and metrics, output capabilities, and what it can truthfully report about producing output |
| Input reader | Platform event capture and the units/source attached to those events |
| Lifecycle owner | Artifact admission, concrete participant identity and the lifecycle changes it actually performed |

A manager holds admitted projections with their origin and revision, not a second editable
copy of a tool's truth. A pane showing a build result still does not own the build. The current
“a presentation owns no facts” decision guards against that duplication; it does not forbid an
owner of arrangement, focus or output selection. [E2](presentation-manager-research.md#e2-where-presentation-lives-now)

The shipped Skins are already loadable weaves around native media. Here, “output provider”
names that service role; it is distinct from an artifact's operator-provider export. The new
work is managing the relationship, not making SDL into a weave for the first time.

Input capture and output remain independently composable. The manager decides where a gesture
goes; the recipient decides what it does. Swapping a renderer must not silently replace the
reader, reinterpret old coordinates using new metrics, or transfer a pending paste to another
document. The medium's clipboard and desktop facts remain medium-owned. [E3](presentation-manager-research.md#e3-media-input-and-resource-ownership)

## 3. Several truths, each named for what it establishes

The manager's authoritative presentation is the admitted logical picture and its interaction
state. Physical output is separately observed. A truthful record might say: “picture 42 is
selected; provider X last reported accepting picture 41; later output is unconfirmed.”

| Fact | What it establishes |
|---|---|
| Requested output | What the maker wants; it may differ from what is active |
| Loaded participant | Lifecycle admission succeeded; it says nothing by itself about usable graphics |
| Prepared output | This exact candidate reported meeting the stated preparation conditions for this operation |
| Active binding | The manager selected this provider for this particular surface |
| Submitted / acknowledged picture | A particular revision was sent / the provider made a defined claim about it |
| Observed failure | A named source reported a specific failure at a specific step |

An acknowledgment proves only its defined claim and provenance. A provider may claim it
submitted a frame to its platform; that is not proof that a person saw it. Devices with no
truthful acknowledgment can remain unconfirmed. The manager can preserve useful logical state
without claiming that frozen pixels are current.

This distinction is needed today: `SurfaceReady` is a greeting, emitted before the Skin calls
its medium. SDL initialization or later window creation can fail, and the diagnostic currently
goes to stderr. Neither the greeting nor the frame counter establishes successful output.
This needs an explicit manager-facing conversation if we want managed output transitions.
[E4](presentation-manager-research.md#e4-loaded-and-ready-do-not-establish-working-output)

## 4. Walk through changing output

### Continuity belongs to the application

Choosing the implementation for new work, changing a running instance, transferring its state,
and retiring its predecessor are distinct decisions. A handoff may be authored into the middle
of replacement; it need not be a universal prelude performed before any replacement work starts.
The founder's spell example illustrates legitimate choices:

| Authored policy | What the application must account for |
|---|---|
| Refuse replacement while in use, or wait for current work | Who determines that use has ended, what happens to new requests, and how waiting is shown |
| Transfer remaining work to the successor | Which state and obligations transfer, their boundary, and what a refused transfer leaves behind |
| Update an effect already in progress | Which running instances change and how their current meaning is transformed |
| Let old effects finish; use new code for new effects | Separate routing for existing and new instances, plus retention of the old code and resources until their work ends |
| Discard state that does not matter to this application | The domain's explicit discard meaning and what affected participants are told |

These are alternatives and may be combined. Zengine should choose a small, understandable
policy for its own tools without elevating it into the one permitted weave lifecycle.
Loom's authored-handoff pattern already leaves continuity and post-boundary behavior to the
domain. Today's prepared replacement nevertheless seals the incumbent when the successor is
admitted: keeping that old service running afterwards is not an automatic property of that
ceremony. Switching a factory/default while retaining old instances needs an explicit routing
and lifetime arrangement. Transferring data alone also does not keep an old message protocol
usable or transfer its answer rights. [E5](presentation-manager-research.md#e5-lifecycle-boundaries-and-continuity)

### One candidate policy for output

Suppose a maker chooses output provider B while A is active. This example aims to preserve
viable output during preparation; other applications may choose a different transition.

1. The manager records the request and starts one identifiable transition. A continues serving
   if it remains viable. The existing lifecycle owner loads or prepares B under the host's
   authority; the manager does not acquire arbitrary loading power by being presentation code.
2. B is asked to prepare for a specified surface and picture revision. Its answer includes the
   capabilities and actual conditions relevant to selection. Candidate reports do not resize
   the active desk, take its input, publish over its picture, or seize its role merely by arriving.
3. The manager reconciles B's conditions with current logical presentation. A resize or edit
   during preparation can require a fresh candidate picture or a refusal. Recheck the relevant
   revision and exact participant at selection; an old ready answer cannot authorize new work.
4. The active output binding changes at an explicit selection event. Subsequent output and
   applicable input routing identify that binding. Late reports from the former binding
   remain attributable to it and cannot rewrite the new active state.
5. Retire A when the selected policy permits. If B subsequently fails, expose that new fact and
   decide recovery explicitly. Do not rewrite history as though selection never happened.

That is a proposed sequence, not a claim that today's role swaps implement it. Prepared
replacement offers useful participant/admission machinery; choosing where its role transition
and the manager's active binding agree remains a design obligation. [E5](presentation-manager-research.md#e5-lifecycle-boundaries-and-continuity)

There is a resource constraint: some candidates can prepare alongside the incumbent; others
need exclusive use of the same window, terminal or graphics resources. For the latter, the
manager must describe the required interruption or refuse a seamless switch. “Keep A until B
works” is conditional on that coexistence being possible. A sealed weave can still execute
native code and create resources; sealing is not a side-effect sandbox.

If B never answers, the transition may remain pending. Keep a bounded record and do not pile
up candidates automatically. A maker may choose another attempt if its admission and resource
policy allow it. Abandoning a wait does not retract an already-queued command. A superseded
attempt must not later select output or change the active binding; loading and resource
acquisition already underway retain their own outcomes and cleanup obligations. Retirement
and cleanup can remain unresolved too; capacity exhaustion should be an explicit refusal.

## 5. Make the unfinished work reachable

The manager needs an inspectable record for operations it owns: requested intent, initiating
participant, affected subject, target participant/artifact, current stage, outstanding attempt,
and the last observed outcome with its evidence source. Link child operations to their parent
intent explicitly. A bus dispatch parent is not a complete causal history of asynchronous work.
[E6](presentation-manager-research.md#e6-evidence-and-attribution)

An example of the maker-facing reading:

> Switching output to B — waiting for B to prepare a surface.
> A remains selected. B loaded successfully; no preparation outcome has been observed.
> Inspect this operation · inspect B · read available diagnostics.

If creation instead refuses, identify that step, the candidate and the reported reason. If
only a handler failure is known, name that observation without inventing its cause. Source
navigation should use actual artifact/source provenance where available; missing provenance
is an explicit gap, not a guessed file path.

The founder's Genera-inspired target is to return to an interrupted activity later, inspect
what happened and what is waiting, repair what needs repair, and continue useful work. That
requires deliberate evidence retention: attributable messages, artifact/source identity,
operation context, and the state actually exposed or captured. A current inspection and a
snapshot from the failure must carry their different times and provenance.

The operation record is the manager's knowledge, not a transcript of everything in the system.
Keep bounded working state and use recorder/logger policy for the history worth retaining;
consider an explicit retained incident when a maker needs evidence beyond those ordinary
windows. Current facilities can forget metadata or payloads, and the durable logger records
only selected facts. Distinguish expired evidence from known pending work, and missing history
from a history in which nothing happened. Authentication identifies who said something, not
whether their internal implementation was correct. [E8](presentation-manager-research.md#e8-inspection-retention-and-repair-limits)

A loaded manager cannot automatically read host-only observations. The host can expose a
scoped, authorized observation path using facts it already knows; the exact door remains to
be designed. Avoid granting the presenter an unrestricted copy of bus traffic just to explain
one failed transition. Keep a diagnostic route outside the failing output path: current
stderr and the journal are useful foundations, even when no pane can draw the explanation.

If the presentation manager itself fails, Workshop's host/lifecycle owner must be able to
observe that boundary independently. Replacing it should reconstruct what is actually known
about participants and current output; a saved selection or pending flag cannot prove a
provider is still active or revive an expired answer right. The precise recovery contract
remains open, alongside recovery of the output provider.

### Several routes back to useful work

The recovery repertoire should remain open to authored tools:

- **Repair through a conversation.** A weave can expose diagnostic questions and deliberate
  repair messages, allowing its own logic to resume pending work. Discovering that surface
  does not grant authority to use it; ordinary authors need not implement every repair option.
- **Build and replace.** Inspect the available state and messages, edit the source, produce a
  new artifact, and use an authored continuity policy. The successor continues the domain work
  represented by that handoff; this does not imply resuming the predecessor's native stack.
- **Attach a debugging weave.** Give it the scoped observations and diagnostic conversations
  relevant to this participant. A debugger is another authored participant, not a title that
  confers unrestricted bus or memory access.
- **Examine a separate specimen.** Capture supported state and inputs for an isolated experiment
  while leaving the original running. The specimen must distinguish captured evidence from
  live connections. Its resource bindings, authority and external effects need an explicit
  plan; serializing state does not clone a device, a queued conversation or an execution stack.

These are directions for capability, not four facilities this phase must implement. A repair
tool should state what it will preserve, replace or discard. Late effects and observations
from the original attempt keep their identity; a successful repair does not make an unanswered
original request retroactively successful.

Some investigations can use declared state and messages; deeper ones need weave-authored
instrumentation or an appropriate native debugger. Loom's message surfaces are not a universal
view of arbitrary C++ internals. A silent handler that returns leaves the system able to run
its manager. A native handler that never returns can stall the shared thread, including an
attached debugging weave. External supervision or process isolation is a separate capability;
no in-process message protocol alone earns that recovery claim.
[E8](presentation-manager-research.md#e8-inspection-retention-and-repair-limits)

**Zengine is a place to start, not a place to end.** Ship a coherent default repair path and
leave room for makers to author better or domain-specific ones.

## 6. What this changes about Editor opening

The manager can own revealing a pane, its admitted content, room and keyboard destination in
one place. This can remove coordination among several presentation decisions. It gives pending
opening and output failures a useful owner and explanation.

Editor still owns the current source. Moving presentation into a manager does not automatically
make Editor's source installation and the manager's view change together. The selected open
contract remains: successful opening has B installed, presented and focused at a defensible
boundary; refusal preserves A and causes no attributable setup/focus change. It is not being
redefined as speculative opening or eventual agreement in this draft.

Protected publication remains a candidate for that remaining boundary. First map which facts
must actually change together after these owners are placed. Use the research to test the
residual need, rather than using presentation extraction to force all weaves into root-backed
state. A permanently pending preparation is allowed; it must not hold unrelated admitted input
hostage or silently change the input's subject. [E7](presentation-manager-research.md#e7-editor-commitment-and-the-research-limit)

## 7. A small next exploration

Start with an owner model and a diagnostic slice, before a new SDK/ABI. Use an existing Skin
path to distinguish artifact refusal, medium preparation failure, selection and unanswered
preparation, with an operation record reachable outside the renderer. Make one stuck operation
understandable when revisited later, showing retained evidence and declared gaps. Exercise one
authored intervention, including what the original attempt means afterwards. Then examine
candidate resource coexistence, obsolete reports, and input associated with an old output
binding. These are proposed experiments, not authorization to implement the manager or extract
another subsystem. A later review should test a second continuity policy before claiming the
design supports several; the first experiment need not implement the whole repertoire.

The first ordinary pane author should still supply content and handle its gestures. An output
provider author should learn a small preparation/output/reporting contract. Only authors who
need coordinated commitment should encounter that additional machinery. The ceremony check is
whether a novice can get from “my switch is stuck” to the relevant operation and participant
without understanding the entire architecture.

The founder has settled the initial service boundary and the need for authored continuity and
multiple repair paths. The remaining concrete choices are Zengine's own defaults: what output
selection promises (including whether a defined first-picture acknowledgment is required),
which intervention may run automatically under host policy, and what evidence a retained
incident keeps. These remain design questions; no one answer becomes a universal weave rule.

Judge the first implementation both by that useful maker loop and by the ability to change its
manager, continuity policy and diagnostic tools without surrendering ownership or hiding the
changes required of cooperating participants.
