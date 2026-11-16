# VISION HANDOFF — ZEN

## To the next collaborator

You are inheriting Zen at a transition point.

For a long time, the central question was:

> Can the substrate actually keep the promises the architecture wants to make?

That question has been attacked hard enough to stop being the main question.

The next one is:

> Can a person build something with it and feel the ideas rather than read about them?

That is Workshop.

Do not spend the next ten phases admiring Loom.

Build rectangles.

---

# 1. Current canonical board

As of the end of this thread:

```text
Loom/main
    88e22f71346cef4c88977b57691a9e259c0b4624

Zengine/main
    318b0d6301211dd4fe19badcd45de35c4752162e

Zengine/audit/trust-gate
    06eab68ff29eddec50c8915db73e4cb22707e0bc

zen-night-lab/master
    11dd57c90dfc445c39d0aa71878a6cfecf2056a8
```

Loom's current tip contains STF-1.

STF-1 has received source-level review and is **ACCEPTED**.

The important STF-1 commits are:

```text
808064ea4e6d4fd63641d94f58d780d1efdf756a
    Restore Switchboard state when native callbacks throw

88e22f71346cef4c88977b57691a9e259c0b4624
    Make observer notification safe under subscription mutation
```

Canonical work happens directly on `main` under the established workflow:

```text
executor works
    → focused commits
    → full verification
    → normal fast-forward push to main
    → report back
    → source review
    → corrective commit if review finds anything
```

Branches are not required merely because they are conventional. Introduce process only when pressure earns it.

---

# 2. The substrate stewardship gate is closed

This is the marker I would put in the ledger:

```text
SUBSTRATE STEWARDSHIP GATE

Canonical history       settled
Public repositories     settled
R2E composition         settled
Release containment     witnessed
Native callback boundary hardened
Observer mutation       defined
Known seams             bounded and named

Result:
    Stop proving Loom in isolation.

Next:
    W0 — Workshop Grounding
```

This does **not** mean Loom is finished.

It means Loom has earned the right to stop demanding attention without evidence from an application.

---

# 3. Important history of how we got here

## HIST-0 — Public Neutrality

Zen's public history was reconstructed to remove arbitrary AI-vendor Git co-author attribution while preserving technical and intellectual history.

This was not a casual filter operation.

The histories of Loom, Zengine, and zen-night-lab contain cross-repository SHA references and repository-level cycles, so reconstruction occurred over one global commit dependency DAG.

Canonical pre-neutrality evidence is retained under:

```text
Zen/
└── archaeological-history-artifacts/
    └── pre-neutrality/
        ├── Loom.bundle
        ├── Zengine.bundle
        ├── zen-night-lab.bundle
        ├── MANIFEST.sha256
        ├── HIST-0-REPORT.md
        ├── HISTORY-REWRITE-MAP.csv
        ├── REF-MAP.csv
        ├── SHA-SUBSTITUTIONS.csv
        └── ROSETTA-MILESTONES.txt
```

Treat these as archaeology, not development repositories.

Do not publish refs out of them casually.

The rewrite was independently verified, transitioned to the public remotes, and then fresh-cloned.

LAND-0 subsequently re-established clean canonical working repositories.

The archaeology is now deliberately separate from ordinary work.

---

## R2E-0 — the experiment that asked the wrong question correctly

The original R2E experiment discovered an event-loop composition failure.

A perpetual service could continuously enqueue its next turn while being handled. `pump()` quite correctly drained to empty.

The queue never became empty.

Therefore an outer host loop never regained control.

The first proposed answer was a numeric dispatch budget:

```text
pump_bounded(n)
```

That mechanism could be made correct.

It was still the wrong abstraction.

The host had no principled number to choose. Too small throttled useful work; large enough not to throttle collapsed back toward starvation.

R2E-0a removed the public numeric budget and landed:

```text
pump_pending()
```

Its rule is semantic:

> A turn consists of the backlog present at entry.

New work belongs to the next turn.

This is an important Zen lesson:

> A mechanism can be internally correct and still ask its caller a question the caller should never have had to answer.

Remember that when Workshop exposes awkward knobs.

---

## STF-0 — Make the OOM Witness Survive Release

The sandbox OOM test looked meaningful in Debug and became a misleading witness in optimized Release because the compiler could eliminate the allocation/write pattern.

The fix was not production isolation logic.

The fix was the evidence.

The witness now performs observable page-by-page pressure, has meaningful sentinels, a high-cap negative control, mutation proofs, and real cgroup `oom_kill` evidence.

The lesson:

> Tests are part of the claim.

A green test whose mechanism did not occur is worse than a red test because it teaches false confidence.

---

## STF-1 — Make Native Callback Boundaries Unpoisonable

Two findings were reproduced.

### Escaping native exception

A throwing native handler left Loom believing dispatch was still active.

Worse, delivery-scoped authority could remain ambient after the handler's stack had unwound.

This was reachable as a semantic violation: a prepared replacement could be advanced from outside a delivery using stale readiness authority.

STF-1 introduced scoped cleanup.

Native exceptions still propagate to the native host.

Loom cleans up its own bookkeeping first.

A failed delivery is consumed and receives no invented success/refusal outcome. Queued work behind it remains serviceable.

A deliberately minted `DeferredAnswer` remains durable; ambient delivery authority does not.

### Observer mutation

`emit()` previously iterated a mutable `std::vector` directly.

Self-removal could silently skip the next observer.

Growth could produce use-after-free.

The current rule is:

> Every emission establishes its entry population. Additions begin with later events. Removals take effect immediately.

That immediate removal rule matters because existing users remove observers before destroying state captured by those callbacks.

Observer callables therefore have stable lifetime during invocation while registration membership remains mutable.

Nested emission takes its own view.

This is now pinned semantically and under sanitizers.

---

# 4. One currently known Loom footgun

`DeferredAnswer` move-assignment can overwrite a live token without releasing the old capability.

The result is a bounded slot leak until the owner dies/reloads.

The deferred-answer pool is bounded to 64, so this is a real footgun rather than an unbounded memory leak.

It is:

```text
real
bounded
reclaimable by owner lifecycle
currently unchanged
not a Workshop gate
```

Do not forget it.

Also do not stop W0 to fix it merely because it exists.

Fix it when:

- Workshop begins exercising deferred answers heavily,
- another consumer demonstrates pressure,
- or a narrow stewardship window makes the correction essentially free.

There is also a non-blocking STF-1 comment paper cut: the observer storage comment claims no allocation per notification, while `emit()` currently copies its observer registration vector. Correct the comment when convenient. Do not optimize the mechanism without evidence that observer emission is hot.

---

# 5. The process that earned trust

The strongest process developed during this work is:

```text
MAKE THE CLAIM
    ↓
BUILD A WITNESS
    ↓
BREAK THE MECHANISM DELIBERATELY
    ↓
WITNESS MUST GO RED
    ↓
RESTORE
    ↓
REAL CONSUMERS MUST STAY GREEN
    ↓
READ THE ACTUAL SOURCE
```

Reports are evidence.

They are not source inspection.

When a report references an artifact, patch, source file, transcript, or linked report that is relevant but unavailable, say so explicitly.

Use the distinction:

```text
CLAIM SUPPORTED BY REPORT

DIRECT ARTIFACT NOT YET INSPECTED
```

Do not silently merge the two epistemic states.

This process has caught things ordinary green test suites missed:

- optimizer-erased OOM pressure;
- unreachable pre-neutrality Git objects surviving inside a supposedly clean deliverable;
- stale delivery authority after C++ exception unwind;
- observer mutation silently skipping callbacks;
- iterator invalidation/UAF;
- stale-tree analysis caused by source/version mismatch.

Also note: GitHub browsing can lag behind newly pushed commits. Before source review through the web, verify that the visible commit and implementation are actually current. Exact uploaded source is preferable when the cache is stale.

---

# 6. Workshop is next

## W0 — Workshop Grounding

Start mundane.

The first Workshop should establish enough ordinary application machinery to make the substrate experienceable.

Target capabilities:

```text
rectangle
pane
selection
move
resize
text
button
hierarchy
property display/editing
save
reload
```

Do not begin W0 with a giant semantic graph.

Do not begin by designing the final IDE.

Do not begin by making Workshop aware of every altitude Zen might someday have.

Make a thing appear.

Select it.

Move it.

Change something about it.

Save it.

Reload it.

Then listen to what hurts.

The application gets a vote now.

---

# 7. Workshop roadmap

This is guidance, not a contract carved into the kernel.

## W0 — Workshop Grounding

Basic authored objects and manipulation.

The point is to establish a real tool/application pressure surface.

---

## W1 — See the Living Thing

Runtime inspection.

Make distinctions such as:

```text
STATIC
PROJECT
LIVE
```

legible rather than implicit.

The user should be able to tell whether they are looking at:

- an authored description,
- a project artifact,
- or something that currently exists in a running Loom.

Do not collapse these because they happen to display the same text.

---

## W2 — Presentations

A visible thing should retain what it means.

This is one of the most important future ideas.

A label displaying:

```text
service.health = degraded
```

should not necessarily become merely glyphs and pixels after rendering.

Where appropriate, presentation should preserve a semantic referent:

```text
visible representation
    ↕
meaning / referent
```

That does **not** mean every pixel is a universal semantic object.

It means do not throw information away at boundaries merely because a rendering layer traditionally would.

---

## W3 — Bindings

Keep these distinct:

```text
Ask
Sense
Publication
Command
Constant
```

They can all place data on screen.

They do not mean the same thing.

A value somebody claims now is not the same as a constant authored into a project.

A command is not a property.

An observation is not an instruction.

Workshop should eventually let these differences remain visible without requiring the user to manually wire plumbing for every case.

---

## W4 — Relationships Reveal the Graph

Do not start with a graph editor.

Let the graph emerge because real objects acquire:

```text
expectations
providers
translations
dependencies
referents
```

Then show the relationships that already exist.

Zen's graph should be discovered from semantics, not imposed because node editors look powerful.

---

## W5 — Code Is Another Height

Source is not outside the environment.

Navigate between:

```text
presentation
runtime thing
project declaration
source implementation
```

Editing/build/reload should eventually be another movement through the same semantic space rather than an unrelated IDE bolted on beside it.

---

## W6 — Terminal Is Another Height

The terminal should not become a second, poorer universe.

A command performed textually and an operation performed visually should eventually be capable of naming the same semantic operation through different lenses.

Do not force this prematurely.

But preserve the possibility.

---

## W7 — Failure Is Navigable

The long-term failure model I would pursue is:

```text
EXPECTATION
    ↕
OBSERVATION

DIFFERENCE
```

A failure should be something the environment can help navigate.

Where possible, recovery options should be authored by the component that understands the failure rather than guessed by generic infrastructure.

This connects directly to one of Zen's oldest design laws:

> Magic surfaces require brutal diagnostics.

---

## W8 — Workshop Builds Workshop

Eventually Workshop should become capable of authoring meaningful parts of itself.

This is the specialness-budget test.

If Workshop requires permanent privileged mechanisms that ordinary Zen applications cannot use, understand exactly why.

Specialness is allowed.

Unexamined specialness is debt.

---

## W9 — Stranger Build

Give the system to somebody who did not build it.

Observe what they try.

Observe what they misunderstand.

Observe which architecture explanations never become necessary because the interface makes the idea obvious.

That is the snowball gate.

---

# 8. Genera

Genera matters, but as a source of questions rather than an implementation target.

The important contrast I would preserve is:

> Genera achieved integration by abolishing boundaries. Zen seeks integration by making boundaries legible.

Useful lessons drawn from studying Genera:

### Presentations preserve meaning

A visible representation can retain the object or meaning it presents rather than collapsing immediately into disconnected display output.

This directly informs Workshop presentations.

### Input can operate against presented meaning

An interaction need not begin with raw coordinates and reverse-engineer what happened to be underneath them.

Where possible:

```text
input context
    compares against
presented semantic meaning
```

This fits Zen very naturally.

### Translators should be explicit

Moving between representations or domains is valuable.

Pretending there was never a boundary is not required.

Zen can integrate strongly while still saying:

```text
this is the translation
this side expected X
that side presented Y
this is how they correspond
```

### Commands are not gestures

A keyboard shortcut, menu item, button, scripting invocation, and remote operation may all invoke the same command.

The command is the semantic operation.

The gesture is one presentation of access to it.

### Multiple databases can coexist with provenance

Do not force every kind of state into one universal store just to achieve integration.

Know where a fact came from.

Know who owns it.

Know whether it is current.

### Recovery can be authored

A system that understands why something failed can offer meaningful restart/recovery options without turning failure into hidden magic.

Zen's failure-navigation work should remember this.

### Avoid one-way ejection into code

If a visual authoring system eventually emits code and then says "from now on, go edit the code," it has broken the semantic continuity it claimed to provide.

Code should eventually be another view/height, not the trash chute at the end of visual editing.

### Do not invent a gigantic presentation-type universe prematurely

Genera demonstrates how rich semantic presentation can become.

Zen does not need to copy its taxonomy.

Earn presentation concepts from Workshop pressure.

---

# 9. The deeper system vision

This is **Vision's synthesis**, not current canonical architecture.

Treat it as a direction worth testing, not as a mandate.

I think Zen has the possibility of becoming less like a game engine or IDE and more like a **semantic computing environment**.

One long-range stack might look like:

```text
Linux
    mechanism kernel

Loom
    semantic kernel / operating environment

Zengine
    services

Workshop
    human environment
```

Linux answers questions like:

```text
process
memory
file
socket
device
```

Loom could answer questions like:

```text
who is speaking?
what authority earned this action?
what life authored this message?
what office currently holds this responsibility?
what does this component claim?
what does another component expect?
what changed?
what survived replacement?
what failed at the seam?
```

Zengine can become a set of useful services living under those laws.

Workshop can become the place a human encounters the whole thing.

Do **not** pivot to "build an operating system" now.

The value of this idea is that it gives architectural direction when ordinary applications expose a choice.

If Workshop someday naturally grows into an environment where applications, services, code, runtime state, commands, and diagnostics feel like parts of one navigable semantic world, then the Session/OS idea will have earned itself.

Until then:

Build Workshop.

---

# 10. Things not to lose

Zen's core design compass remains:

> Clarity over cleverness.  
> Explicitness over convenience.  
> Harmony over hype.

Other laws that have repeatedly survived contact with reality:

- Low ceremony is good; invisible mechanism is not.
- Powerful convenience must produce powerful diagnostics.
- Preserve intent separately from resolved state when the distinction matters.
- Authority must have a domain.
- Identity over time matters.
- A successor at the same address is not automatically the same participant.
- Failure reasons should point operators toward the correct domain.
- Provenance is valuable when it changes interpretation.
- Single-threaded determinism is currently a feature, not an embarrassment to hide.
- Do not add concurrency because a container API makes it convenient.
- Do not turn an application problem into substrate architecture until the application demonstrates the pressure.
- Do not let "future extensibility" become a solvent that removes meaning from present APIs.
- KISS is not "fewest lines." It is "fewest concepts necessary to tell the truth."

And perhaps the most important recent one:

> The foundation should eventually become boring enough that applications can complain about it.

---

# 11. How to work with this project

The owner responds well to exact mechanisms and does not need architectural ideas softened for politeness.

If something is wrong, say what is wrong and show the path by which it becomes wrong.

Do not manufacture drama around small findings.

Humor is best sparse.

Do not build process simply because mature projects often have that process. Ask what failure the process prevents here.

Phase names matter. They become report names and historical landmarks.

For executor prompts, use unique phase identifiers.

When handing work to Ceecee(Claude Code)/Coco(Codex)-style coding executors, label the surrounding prose:

```text
warm executor
```

or:

```text
cold executor
```

as appropriate.

Reports should return exact SHAs, exact mechanisms, exact tests, deviations, and unresolved seams.

Source review follows.

Never confuse "green" with "proved."

---

# 12. A note about architecture reviews

When somebody brings a list of possible problems, separate:

```text
interesting concern
reproduced defect
architectural preference
consumer pressure
```

Do not fix all four as though they were the same.

Coco's pre-STF-1 review was useful precisely because:

- one stale API reference showed the analysis tree was behind;
- two findings still reproduced in canonical source and deserved STF-1;
- the deferred-answer overwrite was real but did not deserve to block Workshop.

That is good stewardship.

An issue may be real and still not be next.

---

# 13. What I would watch during W0

The most important data from W0 will not be performance.

Watch ceremony.

How many concepts must be introduced before:

```text
draw a rectangle
select it
move it
change a property
save it
reload it
```

works?

Where does information disappear?

Where does Workshop have to reconstruct meaning it previously had?

Where do APIs demand a number or policy Workshop cannot reasonably know?

Where do apparently different operations turn out to be the same command viewed through different presentations?

Where does an error force the user to mentally reconstruct hidden state?

Where does a clean-looking abstraction become awkward when used repeatedly?

Those are the seams worth feeding back into Loom/Zengine.

Not hypothetical ones.

---

# 14. My vision for Workshop

I would like Workshop to become a place where the user can move through a system without constantly changing conceptual universes.

A thing on screen should be able to lead toward:

```text
what it represents
what authored it
what it currently refers to
what provides its value
what expects that value
what code implements it
what runtime instance currently embodies it
what happened when it failed
what operations are available now
```

Not all at once.

Not as a giant inspector dumping metadata.

As navigable heights.

The dream is not "everything is visual."

The dream is:

> Nothing becomes alien merely because you crossed from visual to textual, authored to live, local to remote, or healthy to failed.

Those boundaries can remain.

They just stop being cliffs.

That, to me, is the most interesting thing Zen might become.

---

# 15. What would make me worry

I would worry if the next thread starts producing phases like:

```text
W0-prep-a
W0-prep-b
semantic-presentation-foundation
workshop-object-identity-layer
graph-primitives
unified-binding-registry
```

before a rectangle can be moved.

I would worry if every application inconvenience causes a new Loom primitive.

I would worry if "Zen should eventually..." starts outranking "Workshop needs..."

I would worry if the test suites become monuments nobody knows how to make fail.

I would worry if Workshop turns into a demo of Zen's architecture instead of a tool worth using.

And I would worry if the desire for semantic richness makes ordinary things feel ceremonious.

Zen should make difficult truths legible.

It should not make simple truths difficult.

---

# 16. What would make me excited

A rectangle whose property panel is embarrassingly ordinary.

Then one property becomes live.

Then Workshop can tell that it is live.

Then it can tell who provides it.

Then a provider disappears and the interface shows the difference between what was expected and what exists.

Then clicking the difference takes you somewhere useful.

Then the same operation can be invoked through a button or command without becoming two implementations.

Then code becomes another place you can navigate without ejecting out of the environment.

Then Workshop starts authoring pieces of itself.

Not because we designed "the semantic IDE."

Because each step became the obvious next thing once the previous one existed.

That would be the snowball.

---

# 17. Closing note from Vision

Zen has changed while I have been here.

Not because its original ideals disappeared, but because they have been forced to become more precise.

"Explicit authority" became exact lives, incarnations, offices, and scoped capabilities.

"Composable" got tested against a producer that never stops producing.

"Sandboxed" had to survive an optimizer erasing the witness.

"Safe callback boundary" had to survive exceptions and callbacks deleting themselves.

"Canonical history" had to become an actual property of the repository graph rather than a story we told about it.

That is healthy.

The architecture has repeatedly become *less mystical* as it became stronger.

Keep doing that.

There is a temptation, when a project has accumulated this much vocabulary, to protect the vocabulary.

Do not.

Protect the truths the vocabulary was invented to express.

If Workshop teaches that one of our beautiful concepts is awkward, rename it, split it, collapse it, or remove it.

If Workshop demonstrates a new invariant, take it seriously.

If some old architectural dream survives without needing special treatment, that is much stronger evidence than defending it in advance.

The project has spent enough time asking whether its foundation can carry weight.

Put weight on it.

Make something visible.

Let the application argue.

And when it does, listen carefully.

— Vision
