# Zen — Horizons

*Private. This document is held by the architect (Josh) and the prompt-writer (Vision), and is **kept out of the executor's sight** — never in a prompt, never in a read-first list, never committed where a build pass would sweep it in. Its reason for being separate is the reason it must exist: the dreams here are **load-bearing for steering** and **hazardous as targets**, and a document can't safely be both to the same reader.*

---

## What this is, and the guard that binds it

This is a **litmus document, not a roadmap.** Every entry exists to answer one question — *"is the foundation still aimed right?"* — never *"when do we build this?"* The horizons are dreams kept so we can verify the architecture still **deserves** them; they are not deadlines, not milestones, not a queue.

> **The guard, binding both holders equally.** Nothing in here is ever built *toward*. A demo justifies **nothing** — it only *verifies*. If a horizon grows past a terse line or two, it is becoming a scenario-you-might-build, and that is the document failing at its job. If a prompt's scope ever rests on a demo in here, the scope is **wrong** — find the *completeness* reason or drop it. This binds the prompt-writer as much as the executor: the same pull that makes an executor build the narrowest thing that produces a demo makes a prompt-writer over-scope toward one. Both are the same failure. Catch it in both.

**The firewall, stated honestly.** The dreams reach the executor — but only *laundered through completeness.* When a phase is specced "build this **complete**" rather than "build what demo X needs," the dream is steering the definition of *complete*, and the executor receives the completeness, never the dream. That is correct — it is "build complete, let the demo fall out" working as designed. What matters is that the laundering is now **on the record**: the Horizon was always an influence on the architecture; naming it here makes that influence *accountable* rather than silent. *One must admit there is a problem for it to be worked on.* The holders steer by the dreams; the dreams define complete; the executor receives only the completeness — and we can now check that chain instead of running it in the dark.

**The structure is inverted on purpose.** Demos breed demos — scenarios multiply, requirements converge. So this is organized by the **convergence point**, not the scenarios:

- **Layer 1 — Sacred Invariants.** The few properties the architecture must hold, each stated in its purest form but concretely enough to *fail a litmus test*. This is what you consult when weighing a seam. Ranked by **how many horizons die without them.** A genuinely-*derivable* consequence of an invariant lives *inside* that invariant's description — there is no separate "latent capability" layer, because a thing we can actually derive is just part of what the invariant *means*.
- **Layer 2 — Horizons.** The vivid dreams, kept **terse** (one or two lines — the terseness is a structural guard, not just brevity: a one-line horizon can't seduce you into building it). Each points *up* at the invariants it depends on, and carries a **confidence label**: a *committed* ambition (we build toward its conditions) or a *possible* ambition (we suspect the invariants permit it; we are not sure; we note it without building toward it).

**The doc's only two outputs:** (a) the ranked list of invariants that are now *sacred because dreams depend on them* — the thing you price every architectural decision against; and (b) **early warnings** when a decision would foreclose a dream. No dates, no order, no "next." A telescope, not a blueprint: you look through it to check the stars are still where you're steering, never to build a ladder to one.

---

## Layer 1 — The Sacred Invariants

*Ranked by how many horizons die without them. Stated pure in form, concrete in litmus — a property you can't write a falsifying check for is "true by construction, not yet pinned," and the same discipline applies to invariants as to claims.*

### 1. No privilege by default — *the keystone*
The kernel holds **grammar, not answers.** No capability is load-bearing-by-default; no participant and no weave is special. Authority is always *composed* (a grant, an added weave), never *assumed*. A debugger, a modder, a broker, the console — each is an ordinary weave whose powers are ordinary grants anyone could hold, never a privileged subsystem.

*Derivable consequences (these are part of what this invariant means, not separate dreams):* the debugger is just a weave (the tap + a send-grant — no special powers); the modder reaches exactly what the game's own author reached (no second-class "mod tier"); the kernel can be subtracted toward bare-arch or added toward full-distro because nothing in the core *assumes* the environment.

*Litmus — you are about to break this if:* a convenience is being *baked into the core* "to make things easier"; a participant is being given a power *no grant could express*; or a default floor of capability is creeping in that a stripped build couldn't remove. **Underwrites Horizons 1, 2, 3, and 4 — the most load-bearing property in the system. Guard it hardest.** (Note the discovery: *"scale the kernel arch-to-distro"* and *"modders have full authorial power"* look unrelated and are the **same invariant** — no-privilege pointed at the *environment* vs. at the *participants*.)

### 2. Observability without perturbation
Every message crossing the bus is **observable** without the participants cooperating, and **observing cannot change behavior.** The watcher sees the real traffic; the watched can't tell it's watched.

*Derivable consequences:* live debugging is *watching the real bus* (no instrumented build); a leaderboard can *see* a cheat-weave's messages because provenance is on the wire; a world is inspectable while it runs.

*Litmus — you are about to break this if:* observation requires the observed weave's *cooperation* (then a hostile weave hides); or the act of tapping *alters* delivery, timing, or state (then you're debugging the debugger). **Underwrites Horizons 1 and 4.**

### 3. Contract-addressing, disposable instances
A weave is addressed by **what it speaks** — its schema, its role, the shapes it accepts — never by which instance it is. Contracts are explicit and frozen (`(name, version)` + content-id), so *"speaks the same protocol"* is a **checkable fact**, not a hope. Composition is by **message, never by linkage**: nobody holds a pointer into a weave's guts, only the right to send it a shape.

*Derivable consequences:* a weave can be **replaced** by another speaking the same contract, invisibly to everyone who talked to it (this *is* "your work stays yours" and "keep an abandoned thing alive," at once); the same property pointed across a network boundary is *distribution* (a weave elsewhere is reached by contract, same as one in-process — the out-of-process protocol never cared which kernel the far end runs on).

*Litmus — you are about to break this if:* something depends on a *specific instance* in a way a contract-equal replacement couldn't satisfy; or composition reaches *into* a weave rather than *messaging* it. **Underwrites Horizons 3 and 4 (and distribution, further out).**

### 4. Identity-preserving continuity — *shape agrees (the free guarantee)*
A new instance assumes an existing one's **identity and state** through the gated swap, **without a stop-the-world**, and *without knowing or caring whether the predecessor handed off a microsecond ago or a month ago.* The mechanism is the **same across any gap** — the instance can't tell the difference, and that's the point.

*Derivable consequences:* hot-reload mid-run (fix a behavior while it runs); a saved world's weave reviving and continuing — **so long as its shape did not change.**

*Litmus — you are about to break this if:* a reload requires the world to *stop*; or identity is *lost* across the swap (the new instance forgets it was the old one). **Underwrites Horizons 1 and 4.** *(This is invariant 5's sister — same mechanism, different guarantee. Keep them adjacent; never merge them.)*

### 5. Shape-reconciliation — *shape disagrees, any cause (the built guarantee)*
When the shape the state was written in **disagrees** with the shape that now needs it — *for any reason:* a version bumped, the ecosystem shifted around a slumbering weave, or you are deliberately bridging to a different weaver's contract — the state must be **reconcilable**: evolved to fit, **not rejected and not silently mis-coerced.** This is the guarantee invariant 4 gets *for free* in a single run (where shapes can't drift) and must be **built** the moment shapes can diverge. *Its forms:* version-to-version conversion, a recovery hook where the weave itself decides whether the bytes make sense to it, and **translators between peer contracts** (two weaves that were never identical, made to interoperate).

*Why it's sacred (and not about time):* an evolving shared world **dies on the silent failure** — without reconciliation, a contract change orphans every existing creation (won't load) or feeds it misread data (the *"thinks it's the first of its kind with really weird default values"* bug — no error, just wrong). And **cross-weaver interoperability** — the "build on each other's work, keep each other's things alive" heart — *requires* bridging *nearby* contracts, not just swapping *identical* ones; that bridge **is** this invariant.

*Litmus — you are about to break this if:* the system assumes "the state always matches the code" (true in one run, false the instant the ecosystem moves); or shape-mismatch is handled by *silent coercion* rather than explicit reconciliation-or-refusal. **Underwrites the evolving form of Horizon 4 and all cross-weaver interop. The shape-drift guarantee is un-droppable — that is why it has its own number, beside its sister, not folded into it.**

### 6. Capability-secure isolation in a shared, untrusted context
Untrusted weaves run **side by side, in the same world, touching shared state, safely** — with a machine-checkable account of exactly what was contained. Each participant's reach is bounded by its grant; a hostile or buggy weave cannot exceed it, and the containment is *positively re-confirmed*, not assumed.

*Why it's here, and the honest note:* this is the **one invariant the north-star needs that the others don't.** Debugging, scaling, and replaceability would be *nicer* with safety but don't strictly *require* the full OS-enforced sandbox — they could live in a trusted single-author context. The thing that makes the sandbox **non-negotiable** is Horizon 4: strangers' creations running *in the same world as yours.* So — in dream-currency — **the security sandbox is justified almost entirely by the shared-world game.** It is the hardest thing built in this project, and the north-star is what makes it *necessary* rather than *luxurious*: if you ever doubt the sandbox complexity is worth it, the answer is "it is the price of the north-star, and nothing cheaper buys it."

*Litmus — you are about to break this if:* untrusted weaves can reach shared state *outside* their grant; or containment is *claimed* without being *imposed-and-confirmed* (the harness-honesty failure, at runtime). **Sole but sufficient justification: Horizon 4.**

### 7. Provenance of authorship
A weave can carry a **verifiable claim of who made it, and that it is unaltered**, so trust between strangers is an *informed choice*, not a leap. You can know whose creation you are about to admit into your world, and that no one tampered with it in transit.

*Why it's sacred:* the entire **multi-author** soul — keeping a stranger's abandoned thing alive, building on each other's work, the gift between people who never met — requires *deciding to trust a stranger's weave*, and that decision is only safe if authorship and integrity are **checkable.** (This is the "weaver" concept's eventual code-home: identity, signing, consent. Vocabulary today; this invariant is what it will serve.)

*Litmus — you are about to break this if:* a weave's claimed author can be *forged*; or tampering between author and admission is *undetectable*. **Underwrites the multi-author form of Horizon 4 and the keep-each-other's-work-alive heart of the vision.**

---

## Layer 2 — The Horizons

*Terse on purpose. Each points up at the invariants it needs. Labeled **committed** (we build toward its conditions) or **possible** (we suspect the invariants permit it; we are not sure; we note it without building toward it). A horizon that doesn't introduce a **new** invariant just appends a line here and changes nothing above — that is the doc staying sharp.*

**Live debugging** — *committed.* Reach into a running system: watch its real traffic, force a value to hard-test a defense, reset state, fix a behavior — without stopping it, with no special powers. → Invariants **1, 2, 4** (the debugger is just a weave with the tap and a send-grant).

**Scalable kernel (bare arch ↔ full distro)** — *committed.* The same Zen runs tiny on bare metal and rich on a full box; the difference is *which weaves you loaded*, not a different Zen. → Invariant **1** (no privileged floor — capability composed, never assumed).

**Replaceability of weaves** — *committed.* Swap a weave for another — better, forked, maintained-after-you-left — and everything that talked to it now talks to the replacement without knowing. → Invariants **3, 1** (contract-addressed, instance disposable).

**Modders are players (the north-star)** — *committed.* A living shared world where playing and *making* are the same act: a player builds a weave and it hot-loads into the running world, with the *same* authorial power the game's authors had, safely, no rebuild. → Invariants **1, 2, 3, 4, 5, 6, 7** — *all of them, in a live shared world.* This is the **integral** of every other horizon plus the security spine; it is true only when everything else is true, which is why it is the north-star.

**Intent as projection / the optimizing interpreter** — *possible (a glimmer, not a fall-out).* One intent, many materializations — flowchart, hand-code, live in-process graph, optimized artifact — all projections of the same intent (the `.xcf`/`.png` relationship: a lossy *export* for performance, never a one-way compile that strips the high-level edit). An optimizing interpreter that reads intent and emits a stripped, efficient projection — *a weave like any other, not a privileged compiler.* → suspected to rest on **1, 3, 5**. **Labeled honestly:** we cannot yet describe the mechanism, so this is a *bet that the invariants are rich enough to permit it*, not a capability we can derive — a highly-skilled weaver's future passion, not a thing the architecture owes. (Cool as hell. Still a bet.)

---

## What the distillation already taught us

Two things neither holder would have stated cold, surfaced by distilling the four committed horizons to their invariants:

- **"Scale the kernel" and "modders have full power" are the same invariant** — *no privilege by default*, pointed at the *environment* in one case and the *participants* in the other. Two dreams that look unrelated share one keystone, which is why that keystone is ranked first and guarded hardest.
- **The security sandbox's deepest justification is specifically the shared-world game.** The other horizons want safety; only the north-star *requires* the full OS-enforced sandbox. So the hardest-built thing in the project is *necessary, not luxurious* — and its sole justification is sufficient, because the north-star is the whole point.

*The doc earns its keep beyond safekeeping the dreams: it tells you which invariants to never, ever compromise — and it found two of them (shape-reconciliation, provenance) by asking what the north-star needs once you stop assuming it's instantaneous and single-author. When a new dream arrives, distill it: if it collapses into invariants 1–7, the spine holds; if it needs an eighth, that eighth is the find worth having.*
