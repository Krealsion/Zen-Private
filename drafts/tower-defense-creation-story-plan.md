# A complete creation story through ELH

**Selected:** founder discussion, 2026-09-24.\
**Owner:** [Workshop goal map](../goals/workshop.md#near-term-order-and-purpose).\
**Executor packet:** [Tower defense creation story](../../prompts/zengine-tower-defense-creation-story.md).\
**Accepted:** founder merged Zengine [#60](https://github.com/Krealsion/Zengine/pull/60)
on 2026-09-25 as `c02b88a463e6c937e0a1416a989149742aeaedf1`. The
[second correction report](../../reportbacks/zengine-tower-defense-creation-story-corrections-2-RB.md)
retains the repaired replay and the positive maker-authorized stored-command witness. The
[original report](../../reportbacks/zengine-tower-defense-creation-story-RB.md) retains the
experiment's boundary deviations; acceptance does not rewrite that history. The next phase is
[event-driven ELH observation](elh-event-driven-observation-plan.md).

## Outcome and priority

Use an agent to create a small playable tower defense game entirely through its external Loom
host, preserving useful tools and turning the creation route into a repeatable, adjustable-speed
demo. Durable tools, learning and repeatability outrank game polish or completion by bypassing
the environment. Continue toward a complete game; this priority is not permission to stop at
a proposal or a toolkit without trying its intended consumer.

This is one assignment from preflight through implementation and proof. Compaction and natural
milestones stay inside the session. The founder prefers Neovim's motions, line jumps, macros and
editing controls as the initial authoring route; actual use should test that hypothesis.

## Boundaries

Declare installed hosts, toolchains and a clean task-local environment as bootstrap. No game,
task-specific product fix or hidden final workspace is supplied by bootstrap. Once established,
project reading, editing, compiling, testing and observation happen through ELH. Game and
Zengine source authoring exercises the live Workshop editor; build/load uses the normal owners.
ELH-local file/process helpers remain explicit, scoped and attributable. This is an experimental
discipline, not a claim of OS enforcement.

Zengine improvements are activated through eligible weave rebuild/reload in the same running
Workshop. Compilation is still needed. The fixed hosting process, unsupported services and
changed-shape continuity are not silently made replaceable. A necessary change beyond that
boundary requires a founder decision. Neovim's own active-process reload refusal remains valid.
Record actual self-editing if useful repairs earn it; do not manufacture a change for a checkbox.

Recoverable interruptions are retained as distinct runtime segments. A restart cannot establish
an in-place reload claim. Fresh verification runs are expected and use a declared versioned
baseline. The game can introduce its own artifacts; new instances and retained state remain
distinguishable. Broad host extraction, authority redesign and migration are not prerequisites.

## Story and retained material

Aim for one map, a fixed enemy path, tower placement/resources, several waves, win/loss and
restart. Let that goal choose the implementation and weave boundaries. Simple presentation is
sufficient. Establish a usable workspace, create/load visible milestones, play, improve, and
retain useful commands/material in durable Inventory folders and controls.

Build small reusable tools when actual repetition earns them. Maintain a full exploration
timeline plus a condensed successful demo. Repeated commands may become named operations;
abandoned edits/undos may disappear from the demo only when its required state and later
effects remain correct. Keep evidence and a mapping back to the exploration. The demo is an
honest curated reconstruction, not a verbatim replay claim.

The demo recreates the project, workspace, commands and play loop from a clean game directory.
Authored source may be versioned replay input through the editor, with meaningful construction
milestones. Restoring finished files/binaries/toolboxes alone does not prove creation. Resolve
current subjects, controls and identities, and wait for operation completion rather than fixed
delays. Playback speed affects presentation pacing, not actual build deadlines or game time.
Pause/resume and single-step at safe action boundaries suffice. Full undo/time travel is later.

## Acceptance and learning

Deliver source, setup/toolbox, reusable ELH tools and manifest help, an executable creation demo,
reset/repeat instructions, an artifact index, and exploration/evidence. Verify fresh processes
and clean project paths at watchable and fast paces, the playback controls, useful failure and
cancellation behavior, and the playable result. Apply normal checks to surfaces actually changed.

Measure agent calls, ELH runs/asks, attributable host work where observable, time and manual
interventions. Separate bootstrap, exploration and repeat costs. Retention must outlast bounded
run/build histories. Log compaction and expensive re-entry as ceremony findings. Current guidance
belongs with maintained tools and public owners; reports retain the phase's evidence.

The preceding Inventory arc is accepted through folders (#58), independent Info (#55) and
durable toolboxes (#54). Use these foundations rather than adding Inventory features by default.
The controller growth triggers (P-WORK-28, BL-WORK-03), Builder witness BL-VERIFY-01 and authority
pressure are checked only as their surfaces become relevant. Flow/presentation work remains
parallel. Follow-on scope should come from this story's measured obstructions and useful outputs.

## Review disposition and selected follow-on

Independent review reproduced unsafe handling of an unsaved new buffer, false Builder completion,
position-dependent catalog selection, loss of cancellation reach after a wait timeout, and false
forced-shutdown claims. A clean replay failed on a preceding `.nvimlog`; after an explicit ELH
selection correction, the remaining milestones and five-wave game completed. Fresh graphical
and terminal launches, including inactive toolbox restoration, also passed. The correction
packet owns the detailed reproductions and acceptance evidence still required.

Preserve the original report's disclosed direct-shell reads after compaction. Those qualify the
original ELH-only experiment; successful later replay does not rewrite that history. The repair
packet is a separately identified ordinary development pass, with acceptance creation replay
still going through the editor and build/load owners. BL-VERIFY-02's positive maker invocation
is part of acceptance; guest refusal alone does not establish it.

After #60 acceptance, the selected [event-driven ELH observation arc](elh-event-driven-observation-plan.md)
follows Builder outcomes directly and then adds an autonomous gameplay monitor. Reduce routine
polling, captures and agent turns while keeping events, latest claims and history distinct.
The game remains a useful consumer; a generic automation or subscription framework is not a
prerequisite for fixing this story's current defects.
