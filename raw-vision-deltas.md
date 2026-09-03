# Zen Raw Vision Delta Inbox

**Status:** PRIVATE APPEND-ONLY CAPTURE  
**Snapshot refreshed:** 2026-08-17  
**Canonical path:** `private/raw-vision-deltas.md`  
**Role:** cheap, faithful capture before interpretation  
**Parsed ledger:** `private/vision-deltas.md`  
**Capture prompt:** `private/RZVD-prompt.md`

Raw captures are not strategic authority. They may contradict one another, preserve rejected ideas, or contain material that later routes somewhere other than the Vision Delta Ledger.

Operating rule:

```text
conversation / report / discovery
    -> append Raw Delta capture here
    -> founder review and disposition
    -> Vision consolidation
    -> route to parsed Vision Delta, Goal Map, pressure, backlog, known seam, history, or nowhere live
```

Do not rewrite old captures to make later conclusions look inevitable. New captures append at the end.

---

# Raw Delta Capture — 2026-08-06 — Night Lab resurrection and parallel application pressure

## Night Lab as a parallel downstream pressure instrument

**Raw:**  
Zen Night Lab can return as a persistent independent downstream consumer while Workshop becomes the primary maker-facing product effort. The emerging split was stated as:

```text
Workshop
    digs
    deep maker-facing/product pressure

Night Lab
    wanders
    broad unrelated application pressure
```

The two should be allowed to run in parallel rather than sequencing all application pressure through Workshop.

**Context:**  
This surfaced while considering what comes after the credibility/CI work and before/during Workshop Grounding. Night Lab had historically exposed architectural pressure through unrelated applications, and the now-stable installed Loom package makes it possible for that pressure to resume without tying Night Lab to active substrate development.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
Night Lab is not a second roadmap and not a second Workshop. Its value is that it gives Zen a different vote from the primary product.

---

## Current-era Night Lab should stand outside Zen

**Raw:**  
The resurrected Night Lab should consume Zen as an outsider through intended installed/package surfaces rather than sibling source trees. For Loom this became a hard current-era rule:

```text
find_package(loom ...)
installed targets
installed weave build contract

NOT
../Loom
add_subdirectory(Loom)
source-tree includes
private CMake helpers
copied compiler flags
```

“Resurrected” means Night Lab can once again stand outside Zen and use it honestly.

**Context:**  
ZNL-R investigated whether Night Lab could become a real downstream consumer again. A disposable application consumed an installed Loom package, and later ZNL-00 through ZNL-02 repeatedly rebuilt applications after deleting Loom's source and build trees.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
Night Lab's independence is part of what it measures. A workaround that reaches back into the live Zen trees destroys the very evidence the resurrected lab is meant to produce.

---

## Historical Night Lab and current-era Night Lab are different things

**Raw:**  
The historical Night Lab areas should remain frozen as evidence about the exact Loom/Zengine worlds they originally experienced. A new `current/` era sits beside them rather than updating them to current Zen.

The old experiments preserve different ABI generations, historical seams, workarounds, and before/after evidence. Modernizing them would erase their subject.

**Context:**  
ZNL-R reconstructed all historical areas and demonstrated that current ABI v6 loudly rejects older tracked v3/v5 artifacts. This made it possible for frozen archaeology and live experimentation to coexist without pretending they are the same world.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
Do not “bring the old nights forward.” Their oldness is part of their evidentiary value.

---

## One exact Loom per Night Lab phase

**Raw:**  
Because Loom is actively developed in parallel, a Night Lab phase should resolve remote Loom `main` once, pin the resulting full SHA, create a fresh temporary clone/build/install outside the Zen workspace, and consume that frozen installation for the entire phase.

The live Loom checkout is explicitly not a stable build input.

**Context:**  
This rule was introduced before ZNL-00 because Loom work would continue concurrently. ZNL-00 then observed the local Loom checkout advance mid-phase; ZNL-01 observed remote `main` advance mid-phase after the pin had been resolved. Both would have changed the substrate underneath the experiment if the phase had followed a live tree.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
Concurrency is not something Night Lab must prevent. Pinning turns concurrent Loom development from a race into an honest property of the laboratory: each experiment experiences one exact Zen while Zen itself keeps moving.

---

## `substrate.lock` as experiment provenance, not dependency management

**Raw:**  
Current-era Night Lab records which exact Zen an experiment experienced in a small `substrate.lock`, including at minimum Loom SHA, Zengine SHA or `none`, ABI, toolchain, Loom configuration, and creation date.

The lock is:

```text
a record
never an input
never parsed
never generated
```

If later experiments consume a different Loom than the era's original lock, they receive experiment-local locks rather than rewriting history for earlier experiments.

**Context:**  
ZNL-R found that Loom's installed package version (`0.1.0`) spans multiple historical ABI generations and does not record the producing Git commit. ZNL-02 later consumed a newer Loom SHA with the same ABI and therefore required an experiment-local lock.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
ABI is compatibility class, not identity. The lock exists to answer “what exact Zen did this application experience?” without becoming a package manager.

---

## Current-era Night Lab should not hand-vendor Zengine by default

**Raw:**  
An early ZNL-R interpretation allowed current-era experiments to hand-vendor Zengine as long as the friction was recorded. This was subsequently tightened: current-era Night Lab should not normalize hand-vendoring Zengine.

If a good application genuinely needs an existing Zengine capability and Loom-only continuation would be artificial, the experiment should stop at that boundary and record the live-consumer trigger rather than silently vendoring around it.

**Context:**  
ZNL-R measured that Zengine has no stranger package surface: no install/export package, source-root include assumptions, and a silent no-op `cmake --install`. Historical Night Lab repeatedly hand-vendored it, but the resurrected lab is intentionally stricter about outsider consumption.

**State in conversation:**  
favored

**Preserve especially:**  
The important trigger is not “Zengine packaging would be nice.” It is: a live current-era application naturally wants an existing Zengine capability and cannot consume it honestly.

---

## Zengine package work remains real but not yet sequenced

**Raw:**  
Zengine's missing downstream package surface is a genuine product/consumer boundary, not hypothetical cleanup. However, multiple current-era Night Lab applications (`signal-box`, `prompt-corner`, `records-committee`) did not need or miss Zengine, so Night Lab has not yet fired the live-consumer trigger for a Zengine package phase.

**Context:**  
ZNL-R established the package absence directly. ZNL-00, ZNL-01, and ZNL-02 then built meaningful Loom-only applications without needing to emulate Zengine functionality.

**State in conversation:**  
explored

**Preserve especially:**  
“Real problem” and “current problem” remain different categories. The package gap should not be pulled forward merely because it is already well understood.

---

## Night Lab current-era structure should remain deliberately thin

**Raw:**  
The live laboratory should have very little infrastructure:

```text
current/
    README.md
    substrate.lock
    FRICTION.md
    EVIDENCE.md
    <independent experiment>/
    <independent experiment>/
```

Experiments should not share application code. The appearance of `current/common/`, `current/framework/`, `current/lib/`, or similar shared application infrastructure is a warning sign.

A repeated local helper is initially evidence, not an invitation to hoist it.

**Context:**  
ZNL-R proposed the structure, ZNL-00 established it, and ZNL-01/ZNL-02 deliberately duplicated application helpers rather than creating shared infrastructure. This allowed repetition itself to become measurable evidence.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
The laboratory should generate evidence faster than machinery. Each experiment must remain free to be independently awkward, wrong, or domain-specific.

---

## Friction sightings nominate; they do not authorize

**Raw:**  
Night Lab should keep an accumulating `FRICTION.md`, but observations are not automatically work items.

The standing rule became:

> Sightings nominate. They do not authorize.

Repeated occurrences inside one application are distinguished from independent consumer sightings. Known seams are not mechanically escalated just because another application touches them.

**Context:**  
The first three current-era experiments began producing repeated and novel pressures. The ledger discipline prevented every inconvenience from turning into a Loom phase.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
Independent application recurrence is the useful unit of pressure, but even recurrence must be interpreted by what the applications actually paid, not merely counted.

---

## Evidence should carry explicit non-claims

**Raw:**  
Night Lab's `EVIDENCE.md` pairs every meaningful claim with:

```text
CLAIM
WITNESS
SCOPE
DOES NOT PROVE
```

Positive controls or adversarial cases are preferred where a happy path could appear green without proving the intended claim.

**Context:**  
ZNL-00 through ZNL-02 repeatedly found plausible false greens: a monitor that might never notice anything, a replacement that commits while carrying no useful continuity, and a restart that happily operates from an incorrectly empty durable record.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
A successful little application is not automatically architectural proof. Night Lab should say exactly what its witness establishes and name the nearby stronger statement it does not establish.

---

## F-04 became an evidence-backed native-authoring candidate

**Raw:**  
Three unrelated current-era applications independently wrote the same local helper because native `mount()` / `mount_granted()` do not bind an office role directly.

The third sighting narrowed the pressure: this is not a general role-binding problem, because `Kernel::load(...)` already accepts a role. The repeated friction is specifically on the native mounting path.

Measured portfolio state after ZNL-02:

```text
independent consumers    3
uses                     14
scope                     native mount helpers
```

**Context:**  
The helper appeared independently in `signal-box`, `prompt-corner`, and `records-committee`. It was deliberately left duplicated rather than hoisted into Night Lab infrastructure.

**State in conversation:**  
favored

**Preserve especially:**  
This has moved beyond “maybe awkward.” It is now a sharply scoped application-portfolio candidate that no longer needs a fourth consumer merely to establish that the pattern exists, while still not being urgent or blocking.

---

## F-10: authority refusal can wear the grant's name

**Raw:**  
ZNL-02 found a diagnostic mismatch: an immediate answer with no valid answer authority can be reported on the tap/journal as `CapabilityDenied` even when the weave's grant demonstrably permits the shape. Nearby deferred-answer code uses `ForeignAuthority` for the corresponding authority category, including already-spent authority.

The behavior remains safely refused; the pressure is that the diagnostic points an operator toward the wrong subsystem.

**Context:**  
A records-committee control sent a ballot from root. The assessor could legitimately send `Vote` under its grant in the same run, but answering the root-issued ballot had no requester authority. The observable refusal nevertheless named capability denial.

**State in conversation:**  
newly surfaced

**Preserve especially:**  
This is diagnostics, not a security/behavior defect. One independent consumer only. A second unrelated consumer independently receiving a misleading grant-shaped explanation for an authority failure was proposed as a meaningful escalation threshold.

---

## Sender cannot observe send fate looks increasingly like a stable seam

**Raw:**  
Three unrelated current-era applications encountered the existing seam that a sender does not receive eventual delivery fate.

The domains reacted differently:

```text
signal-box
    often routed around it using present-state knowledge

prompt-corner
    paid a real cost around a prepared conversation

records-committee
    naturally tolerated absent members via closing date + quorum
```

None was blocked.

**Context:**  
Repeated Night Lab pressure provided three independent examples rather than one synthetic test.

**State in conversation:**  
favored

**Preserve especially:**  
Repeated evidence did not necessarily argue for closing the seam. Instead it strengthened the idea that eventual send fate is genuinely domain-owned in many applications.

---

## Persistence may remain ordinary application truth

**Raw:**  
The first current-era restart/persistence experiment did not discover a missing Loom persistence layer.

`records-committee` persisted its own durable truth to a human-readable file, exited the process, then a later process reconstructed that truth and used it to change a real domain decision. Loom supplied composition around the state but had no opinion about persistence.

**Context:**  
ZNL-02 deliberately searched for a domain where restart was genuine rather than staged. The county list and determination history naturally outlived the committee members and process.

**State in conversation:**  
explored

**Preserve especially:**  
This is evidence that one real application naturally owns its persistence. It is explicitly not evidence that Zen will never need persistence as a substrate concern.

---

## Several peers can disagree without a Loom group or consensus primitive

**Raw:**  
`records-committee` had five same-kind dynamic participants genuinely disagreeing about the same submissions. Loom's existing singleton offices, answers/correlations, and application policy were sufficient.

No peer-group abstraction or consensus mechanism was needed. The secretary counted votes according to published domain rules; Loom did not decide the result.

**Context:**  
ZNL-02 intentionally looked for plurality/competition pressure. The domain itself required disagreement and several independent peers.

**State in conversation:**  
explored

**Preserve especially:**  
The absence of a missing abstraction is evidence. “Several same-kind participants” did not by itself imply “Loom needs groups.”

---

## Installed Loom consumption is becoming boring

**Raw:**  
Across multiple unrelated current-era applications, the installed Loom consumer path repeatedly remained tiny and uneventful:

```text
find_package(loom REQUIRED)
exported targets
loom_weave_build_contract(...) where needed
```

Moving from one dynamic weave to five added essentially no new packaging ceremony. Rebuilds remained green after deleting the Loom source and build trees.

**Context:**  
ZNL-R first proved the installed path; ZNL-00, ZNL-01, and ZNL-02 then used it for increasingly different applications.

**State in conversation:**  
favored

**Preserve especially:**  
Infrastructure becoming unremarkable is a positive result. Night Lab should record notable non-friction rather than only collecting failures.

---

## Night Lab changed from directed probing to wandering

**Raw:**  
ZNL-00 through ZNL-02 deliberately biased domain selection toward different pressure shapes:

```text
signal-box
    observation / live-system pressure

prompt-corner
    continuity / prepared replacement

records-committee
    persistence / plurality
```

After the third experiment, the strategy shifted. ZNL-03 was explicitly framed as the first phase where the domain should be chosen primarily because it sounds like a worthwhile little thing to build, not because it covers an untouched Loom mechanism.

The new question became:

> What small thing is genuinely interesting to build next, and what does Zen look like when the application—not the audit plan—chooses the path?

**Context:**  
Three experiments had already demonstrated broad pressure and nearly disjoint substrate usage. Continuing to choose domains for coverage risked turning Night Lab into a disguised test matrix.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
“Wander” is not lack of rigor. The outsider/package/evidence disciplines remain strict; what is removed is mechanism-directed domain selection.

---

## A boring Night Lab result is now valuable

**Raw:**  
Once several unrelated applications have independently used the same package and substrate successfully, “nothing new happened; Zen just worked” becomes meaningful evidence rather than a disappointing phase.

Night Lab should record notable non-friction as well as seams.

**Context:**  
The first three current-era experiments continued finding new pressure, but the consumer/package surface itself became increasingly uneventful.

**State in conversation:**  
favored

**Preserve especially:**  
The lab should not develop an incentive to manufacture findings. Boring can mean a boundary has become trustworthy.

---

## Workshop and Night Lab create complementary application votes

**Raw:**  
Workshop remains the primary major goal and is expected to begin with maker-facing visual/UI pressure, while Night Lab deliberately explores unrelated applications.

The emerging system is:

```text
Workshop
    primary product
    deep maker-facing pressure

Night Lab
    independent downstream applications
    breadth
    package-boundary pressure
    longitudinal evidence
```

Neither should inherit the other's implementation responsibility.

**Context:**  
Night Lab resurrection was discussed specifically as something that could proceed while Workshop begins, rather than replacing or delaying Workshop.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
The value is not “more testing.” It is two kinds of real consumer making different demands on Zen at the same time.

---

## Current strategic documents can lag fast-moving repository reality

**Raw:**  
Repeated ZNL phases observed private strategic snapshot/handoff hashes lagging actual accepted or current repository states. The discrepancy became larger while Loom and Zengine continued moving.

Executors reported these contradictions but did not repair private strategic authority, consistent with founder-custodied snapshot governance.

**Context:**  
ZNL-R, ZNL-00, ZNL-01, and ZNL-02 each encountered repository identities newer than some private strategic documents. Concurrent development also made “current Loom” inherently multi-valued unless the subject and timestamp were explicit.

**State in conversation:**  
explored

**Preserve especially:**  
“Current repository state,” “accepted strategic snapshot,” “Night Lab's consumed substrate,” and “live local working tree” are distinct facts and should not be collapsed into one vague notion of current.

---

## ZNL numbering changed to two digits

**Raw:**  
Current-era Night Lab implementation phases are named:

```text
ZNL-00
ZNL-01
ZNL-02
ZNL-03
...
```

rather than beginning with `ZNL-0`, to avoid document/name collisions.

**Context:**  
The naming was changed immediately before the first resurrection implementation phase.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
This is an intentional project-organization convention, not incidental formatting.

---

## Consolidation notes

- The early ZNL-R posture allowed current-era Night Lab to hand-vendor Zengine while pricing the friction. Later discussion tightened this toward **no hand-vendoring by default** and treating genuine Zengine need as a stop/trigger. Preserve both during consolidation rather than pretending the stricter rule was always present.
- The first three current-era experiments were intentionally selected with mechanism-adjacent search biases. That posture was later **superseded for ZNL-03** by domain-first wandering. The strict outsider/package/evidence rules were not superseded.
- F-04 and F-10 should not be merged. F-04 is repeated authoring ergonomics on native office mounting; F-10 is a one-consumer diagnostics mismatch between answer authority and capability language.
- The repeated sender-fate seam and the repeated native-mount friction moved in opposite strategic directions: repetition made F-04 look more actionable, while repetition made sender-fate look more plausibly domain-owned.
- Application-owned persistence in `records-committee` and the broader possibility of future Zen persistence should remain separate. The conversation explicitly avoided generalizing from one successful application-owned solution.
- “Several peers needed no group abstraction” should likewise not be generalized into “Zen will never need groups.” It is one strong negative finding from one real domain.
- Zengine packaging remains a genuine, measured downstream deficiency while simultaneously remaining **untriggered as current work** by three current-era applications. Those two facts are intentionally not reconciled into a sequencing decision here.
- The strategic-document lag may rise to governance significance because it recurred across several phases, but this capture does not decide whether the existing founder-custodied delta process already fully answers it.

# Raw Delta Capture — 2026-08-06 — COLD-2 closeout, Workshop transition, and strategic hygiene

## External pressure should return control to application pressure

**Raw:**  
COLD-2 independently found that the R2F repair campaign was materially real rather than merely reported. The remaining demonstrated material mechanism findings were then handled as a deliberately bounded closeout: inherited descriptors, inherited environment, weave-contract population blindness, Zengine test-population blindness, and console lifetime retention. The emerging direction was that once those bounded conditions were closed, Zen should stop turning audit findings into an endless substrate-grade chase and return to Workshop/application pressure.

**Context:**  
COLD-2 produced no current sign-off blockers, but did produce a small set of material nonblockers. The conversation deliberately chose to finish those specific items before Workshop rather than continue general hardening. The repeated framing became “today closeout; tomorrow rectangles.”

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
The important movement is not merely that several defects were fixed. It is that **external review is allowed to impose a bounded correction phase, but it should not become the roadmap once its demonstrated conditions are answered. Application pressure gets the vote again.**

## Workshop Grounding remains the major goal through the closeout

**Raw:**  
The operational work temporarily moved through C2/C2a/C3/C4/C1/C7, but the major strategic goal did not change: Workshop Grounding, beginning with ordinary authored rectangles and the W0 maker loop. Closeout work was treated as work required before returning to that goal, not as a replacement goal.

**Context:**  
Several executor phases occurred after Workshop had already been selected as the next major direction. The conversation repeatedly distinguished “next operational task” from “next major goal.”

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
**A temporary operational blocker or audit closeout does not automatically become the strategic goal.** The roadmap must distinguish what must happen next from what Zen is actually trying to make true next.

## Green means the declared evidence population existed and ran

**Raw:**  
The population-honesty work generalized from Loom into Zengine. A successful framework exit or a green CTest total is not enough: the project must know what evidence was intended to exist and detect when part of that population silently disappears. This now applies both to test cases/surfaces and to build-contract-bearing first-party weave artifacts.

**Context:**  
COLD-2 deliberately deleted tests and removed the weave build contract and demonstrated multiple ways for “green” to mean less than intended. C3 and C4 separated expected population from observed population and made absence fail loudly.

**State in conversation:**  
explored

**Preserve especially:**  
The irreducible idea is broader than the specific harnesses: **absence is itself something that must be observable when a claim depends on population.** Green proves the declared evidence existed and ran; it does not prove coverage or correctness beyond that claim.

## The exec boundary is authored rather than inherited

**Raw:**  
The sandbox exec boundary moved toward a structural default-deny model for ambient process state. Descriptor inheritance is now an explicit allow-list rather than whatever the embedding host happened to leave open, and the child environment is explicitly authored and currently empty rather than copied from the host. These are separate facts from network namespace containment and filesystem-view construction.

**Context:**  
COLD-2 demonstrated data movement through an inherited host socket despite Network being withheld. C2 closed ambient descriptor inheritance; C2a then noticed and closed ambient environment inheritance.

**State in conversation:**  
explored

**Preserve especially:**  
The recurring shape is: **ambient authority should cross a boundary because Zen explicitly authored it, not because the host happened to possess it.** This did not change the threat tier: abuse-tier containment remains distinct from hostile-code escape resistance.

## History, backlog, and cache have different honest bounds

**Raw:**  
C1 surfaced a useful design distinction while bounding console retention:

- history is bounded by eviction;
- an active backlog is bounded by refusal/backpressure rather than silently losing obligations;
- a cache is bounded by forgetting.

Applying one generic “cap the vector” answer would have changed component promises.

**Context:**  
COLD-2 grouped several RemoteConsole containers as similar unbounded vectors. Source-tracing showed that some were operator history, one was an already-bounded outstanding obligation queue, and another was a cache.

**State in conversation:**  
explored

**Preserve especially:**  
**The correct bounding mechanism follows the semantic obligation of the stored thing.** Choosing eviction, refusal, or forgetting is not a tuning choice; it says what the component promises.

## A stable identity can remain meaningful after its value is gone

**Raw:**  
Bounding console reply history created a small but recurring identity seam: `m3` can remain a meaningful identity after the value once named by `m3` has been evicted. Zen can distinguish “that existed and was discarded” from “that never existed,” rather than silently rebinding `m3` to a newer positional value.

**Context:**  
C1 preserved the meaning of operator reply labels across bounded-history eviction. The executor connected this to other recurring stable-identity questions such as build-vs-author identity, result graphs, and widget item keys.

**State in conversation:**  
newly surfaced

**Preserve especially:**  
Do not smooth this down into “stable indexes.” The interesting part is **identity surviving the disappearance of the currently materialized thing it names**, with absence itself carrying history.

## Historical artifacts and historical documentation are different things

**Raw:**  
The root-level `nucleus.cpp`, which had existed since very early Loom history but was no longer built or current, was judged to belong outside the active root. `docs/history/` felt semantically wrong because it contains documentation *about* history, while `nucleus.cpp` is itself a historical artifact. A repository-level archive was favored as the resting place for such artifacts.

**Context:**  
COLD-1 and COLD-2 repeatedly noticed the unbuilt root-level file as an archaeological oddity. The concern shifted from whether it should exist to whether its location made the repository look less deliberate than the current professional presentation warranted.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
The useful distinction is:

`docs/history/` = records explaining what happened.  
`archive/` = actual artifacts that happened.

Archiving should clarify authority without erasing provenance.

## Known seams must not become a generic backlog

**Raw:**  
A distinction emerged between technical seams and knowingly deferred work. `known-seams.md` is valuable precisely because it records current semantic limitations, boundaries, and future triggers that affect what users/designers may assume. It should not become the dumping ground for every known defect, documentation chore, adoption task, or engineering debt.

**Context:**  
While checking whether the closeout had preserved all unfinished work, items such as sender-visible send fate were clearly true seams, while a leaked temporary directory or missing contributor guide plainly were not.

**State in conversation:**  
favored

**Preserve especially:**  
Calling every unfinished thing a “seam” destroys the meaning of the term. A seam describes **what the current system means or where future pressure is expected to pull**; ordinary owed work needs another home.

## Zen needs a maintained standing-obligations backlog

**Raw:**  
There is a class of work Zen knowingly owes but is deliberately not doing now: human contributor onboarding, release identity, API-stability/deprecation policy, small known defects, tooling limitations, audit follow-ups, and similar items. Much of this currently survives only because an accepted audit/report remembers it. The conversation favored promoting this class into private strategic authority rather than relying on report archaeology.

**Context:**  
The immediate example was human contributor onboarding. Both COLD audits explicitly observed that `CONTRIBUTING.md` is essentially licensing prose while the actual developer guide is `AGENTS.md`, written for machine executors. This was known but had not clearly been promoted into live outstanding work. A wider reconciliation found other report-resident items in the same situation.

**State in conversation:**  
favored

**Preserve especially:**  
The intended principle is roughly: **every thing we knowingly chose not to do should have an authoritative place that explains why it remains open and what wakes it up.** A well-maintained backlog is part of maintaining Zen's future, not merely project-management bookkeeping.

## Deferred knowledge needs different destinations

**Raw:**  
The emerging organizational model routes deferred knowledge by kind rather than placing everything in one file:

- current technical limitation or semantic trigger → `known-seams.md`;
- future architecture/product pressure → orientation or the relevant Goal Map;
- work knowingly owed but not current → private Strategic Map standing obligations;
- actual strategic movement → parsed Vision Deltas;
- historically useful but no longer live material → history/archive/report evidence.

**Context:**  
This grew out of the backlog reconciliation discussion and the realization that both `known-seams.md` and `vision-deltas.md` lose usefulness if treated as general inboxes.

**State in conversation:**  
favored

**Preserve especially:**  
**The destination expresses what kind of unfinished knowledge this is.** “We are not doing this now” is not enough classification.

## Raw Delta capture should be separated from Delta interpretation

**Raw:**  
The existing Delta process imposed too much interpretation at capture time and was easy to lose track of. The favored replacement separates an append-only raw inbox from the formal parsed ledger:

- `private/raw-vision-deltas.md` receives cheap, faithful captures;
- `private/vision-deltas.md` contains interpreted/parsed Deltas and their later disposition.

Under this model, “Raw” stops being a polished lifecycle state inside the formal ledger and becomes an input format.

**Context:**  
The founder reported seeing Deltas appear in conversation without reliably tracking or requesting them, remembered missing at least one, and explicitly rejected a Night Lab Delta whose sparse/prose-heavy format was confusing and difficult to use. The desired workflow is to maintain conversational pace and consolidate later.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
Capture and judgment happen at different tempos. **Raw capture should be cheap enough that preserving surprise never requires stopping the work to perform strategic bookkeeping.**

## Raw Delta capture should be requestable without already knowing a Delta occurred

**Raw:**  
A reusable conversation-level Raw Zen Vision Delta prompt was created so a consolidation pass can ask a chat to recover potentially strategic movement even when nobody explicitly labeled those moments as Deltas during the conversation. The result is one paste-ready append-only capture block.

**Context:**  
The founder specifically wanted an easy copy/paste prompt usable after large conversations or during major consolidation passes. The prompt was then saved and immediately used as the first test of the new workflow.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
The founder should not need to remember **where** a Delta occurred before asking for preservation. The capture pass should search for anything that would be regretted if the conversation stopped being fresh.

## Raw capture is universal, but not every Raw item becomes a Vision Delta

**Raw:**  
The raw inbox can preserve strategically interesting material before its final category is known. During later consolidation, a Raw item may become a parsed Vision Delta, a known seam, a standing obligation, Goal Map knowledge, historical evidence, or nothing live at all. Raw capture therefore does not imply strategic acceptance or even eventual inclusion in `vision-deltas.md`.

**Context:**  
This followed directly from separating capture from interpretation and from the backlog/seam classification problem.

**State in conversation:**  
favored

**Preserve especially:**  
**Universal capture does not mean universal promotion.** The inbox is allowed to contain uncertainty because later routing is a separate act of judgment.

## Sparse Delta prose is not an acceptable preservation format

**Raw:**  
A prior Night Lab Delta was explicitly rejected because its sparse, confusing prose format did not make the captured change easy to understand or maintain. The problem was not necessarily that the underlying discoveries lacked value; the capture artifact itself failed as a usable record.

**Context:**  
The founder used this rejected Delta as evidence that the current Delta workflow was not reliably supporting pace or later comprehension.

**State in conversation:**  
explicitly rejected

**Preserve especially:**  
Do not interpret the rejection as “Night Lab generated no strategic knowledge.” Preserve the narrower lesson: **a Delta format that compresses context until the record becomes cryptic has failed its archival purpose.**

## Backlog reconciliation should accompany major founder consolidations

**Raw:**  
The planned post-C7 founder consolidation expanded from “update SHAs + incorporate a Delta” into a broader reconciliation: inspect accepted audits and report-backs for surviving deliberately deferred findings, ensure each has a live disposition, and stop relying on memory/report archaeology before Workshop generates a new layer of pressure.

**Context:**  
The immediate concern was whether all knowingly left-behind work had been captured. Review showed that important items were documented in reports but not necessarily promoted into a current backlog authority.

**State in conversation:**  
favored

**Preserve especially:**  
A consolidation pass should ask not only **“what changed?”** but also **“what did we knowingly leave behind, and where does it now live?”**

## Consolidation notes

- The “return to Workshop/application pressure” item and the “Workshop remains the major goal” item are closely related, but should not automatically be merged: one is about how bounded audits interact with strategy; the other is about distinguishing operational sequencing from major-goal authority.
- The population-honesty item may overlap with previously incorporated population doctrine. Preserve it anyway at Raw stage because this conversation generalized the pressure across Loom build artifacts and Zengine rather than only repeating an earlier test-suite observation.
- The authored exec-boundary item may be primarily technical rather than strategic. Its potentially strategic part is the structural default-deny treatment of ambient authority; later consolidation should decide whether that rises above reference/known-seam material.
- The history/backlog/cache distinction and the stable-identity-after-eviction observation emerged from C1 implementation pressure. Neither should be promoted merely because the implementation was accepted; their wider design significance remains to be judged.
- The archive/nucleus item is an explicitly accepted project-organization choice. It may belong in repository governance/history rather than the parsed Vision Delta ledger.
- “Known seams must not become a generic backlog,” “standing obligations,” and “deferred knowledge needs different destinations” are one family but preserve different irreducible ideas: protecting the semantics of `known-seams.md`, establishing a live backlog for knowingly owed work, and defining routing by knowledge type.
- Human contributor onboarding is confirmed as known outstanding work from the audits, but its exact trigger/priority has not yet been formally incorporated into strategic authority in this conversation.
- Several concrete deferred findings motivated the backlog discussion—such as C-5 compat-JSON cost asymmetry, C-6 temporary-directory cleanup, Registry growth, stale-build-tree verification limits, ABI-layout concerns, release identity/API-stability work, and contributor onboarding. They are evidence for the governance problem; they should not automatically become individual Vision Deltas.
- The Raw/parsed Delta split, reusable Raw Delta prompt, and universal-capture/non-universal-promotion ideas form one governance system, but should remain separately visible during the first consolidation so none of the intended properties gets lost.
- The explicitly rejected Night Lab Delta concerns the **record format**, not necessarily the strategic substance discovered in Night Lab.
- No attempt has been made here to determine which items are already represented in existing Seeded/Incorporated Deltas. That reconciliation belongs to the later consolidation pass.

# Raw Delta Capture — 2026-08-06 — Workshop and onboarding arise together

## Workshop is where onboarding first becomes real

**Raw:**  
The founder corrected the idea that human onboarding should sit as a detached future contributor task. Workshop is the first place where people will directly manipulate, explore, and learn Zengine's core structures while also building applications. Workshop friction therefore reveals onboarding needs in real time.

The response to friction is deliberately two-sided:

```text
friction means the interaction is unnecessarily hard
    -> improve the Workshop

friction reflects a real concept worth understanding
    -> provide a tutorial, guide, explanation, or teaching surface
```

Workshop and onboarding should arise mutually rather than one being postponed until after the other.

**Context:**  
This surfaced during the post-C7 backlog reconciliation. The original audit finding was a thin human contributor front door, but the founder clarified that the first honest source of onboarding knowledge is the Workshop itself because Workshop exposes the same core structures future makers and contributors need to understand.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
Onboarding is not merely documentation debt. **Usability and teaching are two responses to the same observed human friction, and Workshop is where Zen begins measuring that friction for real.**

## Consolidation notes

- This does not mean every Workshop inconvenience deserves documentation; some friction should disappear through better interaction.
- This does not make a full contributor-guide rewrite a prerequisite for the first rectangle.
- Repository contributor onboarding and in-product maker onboarding are distinct surfaces, but they should increasingly share the same tested explanations rather than evolve independently.


# Raw Delta Capture — 2026-08-06 — Night Lab trust geometry, adversarial evidence, and altitude limits

## Night Lab is an established instrument, not a sequence Zen must finish

**Raw:**  
After multiple current-era experiments, Night Lab no longer needs to reach some target number of applications before Zen can move on. It has earned its existence as an ongoing independent application-pressure instrument.

Future `ZNL-*` phases may continue while they remain cheap, interesting, and evidentially useful, but they are not prerequisites for Workshop, Loom work, Zengine work, release work, or any other strategic advance.

**Context:**  
By ZNL-04 and ZNL-05, the laboratory had repeatedly produced package-clean unrelated applications with no shared framework, while Workshop work was visibly proceeding in parallel.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
“Night Lab may keep wandering” must not silently become “Zen must finish ZNL-05, ZNL-06, ZNL-07… before something else may advance.”

---

## Hostile-frame testing became a standing evidence-quality habit

**Raw:**  
Current-era Night Lab should challenge a meaningful authority boundary the application actually trusts rather than inferring enforcement merely from a narrow configuration and a successful permitted path.

Where the honest participant API cannot express the forbidden act, a public host-side forging door may construct the hostile frame.

The principle became:

> Attack the promises the domain already makes.

The attack should be strong enough that other application rules would accept it if the intended Zen boundary failed.

**Context:**  
`ringing-chamber` first used a forged hostile frame cheaply. `shutter-line` showed the public host-side forging surface includes verified office-authored sends and claims, allowing a grant to be attacked while valid office authorship and downstream domain rules remain satisfied. `saleroom` then challenged grant topology, delivery office authorship, and claim-side office holding independently.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
This is an evidence habit, not a conversion of Night Lab into a security or refusal test matrix.

---

## Edge pressure should increase diversity of trust, not become a numeric ladder

**Raw:**  
The hostile-edge idea temporarily stepped upward from one forged frame toward multiple meaningful edges. ZNL-05 validated the experiment: `saleroom` naturally had several trust relationships before Zen was consulted, and attacking three conceptually different Zen authority edges strengthened the evidence without changing the application.

After that result, the increasing edge count should stop.

The stable rule became:

```text
identify the domain's natural trust geometry
attack the important distinct edges
prefer different kinds of authority over more copies of one kind
do not increase a quota phase by phase
```

**Context:**  
The user explicitly liked stepping up the edge amount because richer trust geometry seemed likely to produce more creative applications. `saleroom` then naturally produced seven meaningful trust relationships, three of which mapped to distinct Zen authority mechanisms.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
Do not allow:

```text
ZNL-05 asks for 2 edges
ZNL-06 asks for 3
ZNL-07 asks for 4
```

to emerge accidentally. Variety of relationship is the useful pressure, not denial count.

---

## Rich trust geometry can itself be a source of creative application domains

**Raw:**  
A useful Night Lab search bias is not “which Loom API is unused?” but “which little worlds contain interesting promises between participants?”

Domains with layered responsibilities, adverse interests, private knowledge, delegated authority, institutional procedure, or mutually constrained roles may naturally produce richer applications and richer Zen pressure without being selected for mechanisms.

**Context:**  
`shutter-line` and especially `saleroom` became more interesting as applications because their domains contained several different reasons one participant trusted another. The mechanisms followed those relationships afterward.

**State in conversation:**  
favored

**Preserve especially:**  
The trust relationships must pre-exist the attack design. Adding a telephone bidder, intermediary, approval step, or other participant only because it creates another edge was explicitly rejected as distortion.

---

## Mutation-testing adversarial controls is becoming part of Night Lab evidence discipline

**Raw:**  
A hostile or false-green control should not be trusted merely because it passes.

Where cheap, mutate the relevant rule in scratch so the forbidden behavior becomes possible or the supposed detector becomes ineffective. The control should then go red.

Examples included:

```text
widen a grant
remove a recipient-side authorship check
alter office ownership
disable an application check
remove the event that the scenario claims to detect
```

Mutation scripts themselves should verify that their intended edit actually landed before the result is trusted.

**Context:**  
`ringing-chamber` discovered a first-draft fumble control that could never fail for domain reasons. `shutter-line` mutation-tested five controls. `saleroom` mutation-tested all three hostile edges with five mutations, and separately encountered a half-applied shell mutation.

**State in conversation:**  
favored

**Preserve especially:**  
A control that cannot fail proves nothing, even when it is green for a domain-correct reason.

---

## Paired false greens with the same symptom but different causes are unusually valuable

**Raw:**  
When a domain naturally supplies two different failures that produce the same visible symptom but require different detectors, preserve the pair.

Two examples emerged:

```text
shutter-line
    corrupted number
        repeat-back catches it
    mismatched codebook editions
        repeat-back is structurally blind

saleroom
    stale reserve board
        reserve audit catches it
    commission bid deliberately run up
        competitive-execution audit catches it
```

Each pair demonstrated that one apparently good detector is structurally incomplete.

**Context:**  
These pairs emerged from the domains rather than being constructed to satisfy a testing requirement.

**State in conversation:**  
favored

**Preserve especially:**  
“Same symptom / different cause / different detector” is stronger evidence than two variants of one failure, especially when each control asserts that the other detector stayed silent.

---

## Exact witness reconciliation is stronger than a collection of successful assertions

**Raw:**  
Where the application naturally contains multiple independent accounts, Night Lab increasingly favors exact reconciliation:

```text
produced
=
accepted
+ refused
+ ignored
+ outstanding
```

or the domain-equivalent arithmetic.

If the arithmetic does not close, investigate rather than weakening the witness.

**Context:**  
`records-committee`, `ringing-chamber`, `shutter-line`, and `saleroom` all gained evidence from independent counts. In `saleroom`, bid reconciliation initially failed by exactly five and exposed a legitimate auction behavior—being beaten on the same breath—that the first model had failed to name.

**State in conversation:**  
favored

**Preserve especially:**  
The value is not generic bookkeeping. The independent accounts should be things the domain or application naturally possesses.

---

## Sense freshness and provenance do not answer “what is this fact about?”

**Raw:**  
A Sense result can be:

```text
present
well-formed
fresh revision
current author life
current office holder
correctly office-authored
```

and still answer the wrong application question.

`saleroom` produced the mirror image of the earlier `NoClaim` concern: the board contained a completely valid reserve claim from the front office—but for the previous lot.

The application therefore owns the semantic key that identifies the subject of the claim.

**Context:**  
The primary `saleroom` false green sold lot 15 at £110 against a £300 reserve because a valid claim for lot 14 remained on the board. Every substrate identity/freshness guard correctly reported that the claim itself was valid.

**State in conversation:**  
favored

**Preserve especially:**  
Loom can tell the truth about who authored an observation and whether that observation is current. It cannot manufacture the application's answer to “current fact about which lot/resource/operation/generation?”

---

## F-01 should be judged by application consequence, not by `NoClaim` sightings

**Raw:**  
The same underlying Sense window has now produced several different application shapes:

```text
signal-box
    NoClaim ambiguity mattered
    application needed a distinction

ringing-chamber
    same reading occurred
    both meanings required the same domain response

shutter-line
    window structurally existed
    domain commissioning closed it before any read

saleroom
    absence was not the problem
    valid stale-subject truth was
```

Therefore a byte-identical `NoClaim` occurrence is not itself pressure.

**Context:**  
Repeated independent consumers narrowed rather than amplified the original commissioning concern.

**State in conversation:**  
favored

**Preserve especially:**  
Measure the application's need for the distinction, not the number of times the substrate can produce the same refusal/read state.

---

## F-02 sender-fate pressure is not one uniform missing fact

**Raw:**  
Repeated applications have now shown materially different relationships to eventual send fate:

```text
some directed-message domains
    cared about eventual delivery fate

ringing-chamber
    publication returns useful fanout information

shutter-line
    wanted end-to-end message fidelity
    no hop-level result could answer the real question

saleroom
    domain acknowledgement is a broadcast to the whole room
    more useful than a private send result
```

The seam therefore looks increasingly domain- and send-verb-shaped rather than like one universally missing sender feature.

**Context:**  
F-02 was encountered by the early current-era applications, then not encountered by three later applications for three different reasons.

**State in conversation:**  
favored

**Preserve especially:**  
Repeated evidence can argue against universalizing a seam.

---

## F-04 has become a settled evidence question

**Raw:**  
The native office-binding ergonomic gap has now been independently reproduced by six current-era applications:

```text
independent consumers    6
local uses               33
scope                     native mount helpers
dynamic load path        already takes role
```

Further independent sightings are bookkeeping unless they change scope, cost, or semantics.

**Context:**  
Every application independently recreated a small `mount_office`-style helper. Later applications simultaneously used `Kernel::load(name, path, role, grant)`, repeatedly narrowing the gap to native mounting only.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
The problem is sufficiently evidenced to fix when that native authoring surface is next legitimately touched. It does not justify interrupting unrelated work.

---

## F-10 increasingly looks like an isolated answer-authority diagnostic corner

**Raw:**  
The diagnostic mismatch where invalid answer authority can surface as `CapabilityDenied` despite a valid grant remains at one independent consumer after six current-era applications.

This does not invalidate the finding, but no broader diagnostic pattern has emerged.

**Context:**  
Later applications either did not use answers at all or never entered the root-answer authority shape.

**State in conversation:**  
explored

**Preserve especially:**  
A second independent application encountering the same misleading grant-shaped diagnostic remains a meaningful escalation trigger.

---

## Several distinct Zen authority forms composed cleanly in one ordinary application

**Raw:**  
`saleroom` naturally depended on and independently attacked three kinds of Zen authority in one application:

```text
grant topology
    delivery-time permission

office authorship
    who may speak as an office

office holding for claims
    who may place an office-owned current fact
```

They refused at different stages and did not require a new application-specific security framework.

**Context:**  
The trust relationships came from ordinary auction procedure before Loom mechanisms were chosen.

**State in conversation:**  
explored

**Preserve especially:**  
The interesting evidence is not merely three denials. It is that several authority concepts already in Loom's grammar can represent several different institutional duties in the same little world without producing new friction.

---

## The weave build contract now has measured runtime meaning, not only symbol-level evidence

**Raw:**  
Night Lab followed the stranger weave build contract through to its runtime consequence.

Without the contract:

```text
STB_GNU_UNIQUE symbols remain
Kernel::unload reports success
kernel lifetime/close counters advance
but
glibc keeps the shared object resident
```

With the contract, reduced reproductions physically unload the object.

**Context:**  
Earlier phases showed the artifact-symbol difference. ZNL-05 built a small scratch host and measured actual residency after unload.

**State in conversation:**  
explored

**Preserve especially:**  
The exported build contract is doing observable runtime work. A high-level “unload succeeded” bookkeeping result does not by itself prove the loader physically unmapped the artifact.

---

## One contracted-artifact residency measurement remains unexplained

**Raw:**  
In the full `saleroom` application, a correctly contracted dynamic bidder remained visible through an `RTLD_NOLOAD` residency probe after `Kernel::unload`, even though the kernel ledger reported the expected destruction/close progression.

Four reduced hosts using the same contract reported the artifact gone.

Nothing in `saleroom` depended on physical unmapping.

**Context:**  
The discrepancy appeared while strengthening the build-contract evidence. The executor tried several smaller reproductions and could not reproduce the full-application residency result.

**State in conversation:**  
unresolved

**Preserve especially:**  
This is an unexplained measurement, not yet a Loom friction nomination. An independent repetition of:

```text
contracted artifact
Kernel::unload success
ledger advances
artifact still resident
```

was identified as a meaningful trigger for focused investigation.

---

## Package-clean Loom consumption is now established at this application altitude

**Raw:**  
Six unrelated current-era applications have consumed the installed Loom package without source-tree coupling or package-surface friction.

For the first time, `shutter-line` and `saleroom` also ran against the exact same Loom commit and toolchain, removing “Loom changed between experiments” as an explanation for their shared lack of consumer friction.

**Context:**  
The first several experiments each experienced a different remote Loom pin. ZNL-04 and ZNL-05 both resolved `55fbb15f`.

**State in conversation:**  
favored

**Preserve especially:**  
The installed package surface has become “boring in the best way” for this class of application. Do not silently generalize that result beyond the altitude the laboratory has actually exercised.

---

## Three consecutive no-new-friction phases create an altitude question

**Raw:**  
ZNL-03, ZNL-04, and ZNL-05 each produced no new Loom friction despite increasingly rich applications and stronger adversarial controls.

Two possibilities were named:

```text
the substrate is genuinely in good shape at this altitude

or

the instrument has stopped being able to see the remaining problems
```

The likely answer offered was “mostly the first, at this altitude,” with the altitude itself becoming the important limitation.

**Context:**  
The current-era applications remain overwhelmingly:

```text
single-threaded
in-process
without isolation
without participant failure
mostly without persistence
```

while Loom claims a larger world than that.

**State in conversation:**  
explored

**Preserve especially:**  
“No new friction” is meaningful positive evidence and simultaneously not evidence about portions of Loom that Night Lab has never naturally exercised.

---

## Participant failure is unexplored partly because domain-selection policy filtered it out

**Raw:**  
After six applications, `revive`, `reload_from`, recovery after actual participant failure, and lifecycle policy remain untouched.

The conversation identified a selection-policy cause rather than treating this as random:

> Domains that naturally want a participant to fail mid-work disproportionately appear among safety-critical operations domains, while Night Lab had repeatedly rejected otherwise strong safety-critical candidates to preserve portfolio variety.

**Context:**  
Breathing-apparatus control, ship bridge, pharmacy, transfusion, commercial diving, and other failure-shaped candidates repeatedly appeared and lost partly because `signal-box` already occupied a safety-operations slot.

**State in conversation:**  
explored

**Preserve especially:**  
The absence of lifecycle evidence was being partly produced by the laboratory's own domain-selection policy.

---

## Safety-critical domains should be allowed to compete normally again

**Raw:**  
For ZNL-06, the anti-repetition veto against another safety-critical operations domain was deliberately removed.

This does not make lifecycle a target.

Instead:

```text
safety-critical domains
    may compete normally

participant failure
    remains optional

if a failure-shaped domain wins honestly
    preserve the failure

if something else wins
    accept that result
```

Similarity of the actual application problem remains a valid rejection reason; category membership alone is not.

**Context:**  
The participant-failure selection bias became sufficiently clear after ZNL-05 that continuing to reject the same domain family while repeatedly noting lifecycle remained unexplored would make the instrument self-defeating.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
Do not choose a failure domain to satisfy coverage. Remove the filter and let the domain win—or not win—honestly.

---

## Night Lab may eventually retire lifecycle as an expectation rather than force it

**Raw:**  
If safety-critical domains are allowed back into ordinary competition and participant failure still does not arise naturally, it may be reasonable to stop mentioning lifecycle exploration as an expectation of every Night Lab phase.

The untested lifecycle half would then remain a known limit of this instrument rather than a dangling obligation.

**Context:**  
This was proposed as the next interpretation if ZNL-06's widened domain search still does not produce a failure-shaped winner.

**State in conversation:**  
unresolved

**Preserve especially:**  
A laboratory does not have to measure every substrate claim. It does have to say honestly what altitude it reaches.

---

## Persistence remains a one-consumer result rather than a general law

**Raw:**  
After six current-era applications, `records-committee` remains the only experiment that needed information to survive a process restart.

Its result:

```text
application writes ordinary durable truth
Loom composes around it
```

therefore remains strong evidence for one domain, not a general rule about Zen persistence.

A second naturally persistent domain would materially strengthen or challenge that result.

**Context:**  
Later application searches repeatedly produced domains whose natural lifetime was one session/day/evening.

**State in conversation:**  
explored

**Preserve especially:**  
Do not choose a persistence domain merely to answer this. The fact that persistence is rare in the current portfolio is itself part of the evidence.

---

## Zengine's package deficiency remains real while its execution trigger keeps weakening

**Raw:**  
After six current-era experiments, none has naturally wanted, missed, vendored, or worked around an existing Zengine service.

The missing stranger package remains a measured Zengine product boundary, but current-era Night Lab still has zero live-consumer trigger sightings.

**Context:**  
Each application has so far been honestly Loom-only without reimplementing an obvious Zengine responsibility.

**State in conversation:**  
explored

**Preserve especially:**  
“Known deficiency” and “current sequencing pressure” remain different facts.

---

## Wandering exposed application-relationship dimensions a mechanism-directed portfolio likely would not

**Raw:**  
The application portfolio began revealing a dimension not originally sought:

```text
answer held by a participant
answer emergent and owned by nobody
answer carried by intermediaries who do not understand it
important figures individually held but intentionally concealed
```

Later domains also introduced cooperative disagreement versus adverse interests.

These distinctions came from choosing applications for their own sake rather than choosing APIs to exercise.

**Context:**  
`signal-box`, `prompt-corner`, and `records-committee` each had an identifiable holder of important truth; `ringing-chamber` did not; `shutter-line` carried truth through ignorant intermediaries; `saleroom` distributed exact private figures among participants with opposed interests.

**State in conversation:**  
explored

**Preserve especially:**  
Portfolio wandering may reveal meaningful categories of application relationship that no Loom coverage matrix would have suggested in advance.

---

## Consolidation notes

- The hostile-frame practice evolved in stages: one cheap forged frame became a preference for multiple meaningful edges, then ZNL-05 explicitly stopped the progression from becoming a rising numeric quota. Preserve the evolution rather than flattening it into “always test N edges.”
- The earlier portfolio-variety preference against repeated safety-critical operations domains is now **superseded** as a category-level veto. Similarity of actual application shape remains a valid rejection reason.
- Participant failure being unexplored and safety-critical domains being allowed back into the pool are closely related but should not be merged. One is an evidence gap; the other is a correction to the laboratory's selection policy.
- The possibility of eventually retiring lifecycle as a Night Lab expectation remains unresolved and depends on what happens after the selection bias is removed.
- Three no-new-friction phases and the laboratory's altitude limit should remain together in tension. Do not consolidate them into either “Loom is proven good” or “Night Lab is no longer useful.”
- The weave build contract's demonstrated unload consequence and the unexplained contracted-artifact residency are related but must remain distinct. The first is reproduced positive/negative evidence; the second is a single unexplained full-application observation.
- F-01's various Sense shapes and the newer “valid fact about the wrong subject” hazard are related but should not be merged. The latter is not an absence/liveness ambiguity.
- F-02's repeated narrowing should not be turned into a claim that sender fate never matters. Earlier applications did experience real cost; later domains demonstrate that the desired information varies.
- F-04 no longer needs additional consumer recurrence to establish the finding. Additional sightings only matter if they reveal broader scope, higher cost, or semantic consequence.
- F-10 remains a real measured diagnostic issue despite becoming increasingly isolated. Lack of recurrence is evidence about prevalence, not disproof of the original observation.
- Package cleanliness becoming established and the broader altitude limit should not be conflated. Installed-package consumption is strongly evidenced for these applications; isolation, failure, concurrency beyond the current single-threaded model, and broader execution environments remain outside that evidence.
- Zengine packaging remains a known real deficiency while six current-era applications provide no live sequencing pressure for it. Preserve both facts without reconciling them into a roadmap decision.


# Raw Delta Capture — 2026-08-06 — Zen Arena contract and Arena Zero

## Zen Arena became an independent repository/workstream

**Raw:**  
Zen Arena moved from a future experimental concept into an independently housed project.

Founder calls made in conversation:

```text
Goal Map
    yes

repository
    zen-arena

workspace checkout
    Zen/arena/

Arena Director
    weave

kDeliberationTurns
    4
```

The `zen-arena` repository was subsequently created and pushed to its remote.

**Context:**  
ZA-00 produced enough architectural and multi-phase scope that Arena no longer looked like a playground experiment or a subdirectory of Loom/Zengine.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
Arena is intended to have its own identity, history, CI/package boundary, and future participant SDK rather than becoming implementation inside Loom or Zengine.

---

## Arena correctness includes negative information

**Raw:**  
Arena sharpened its central claim from merely “participants receive different perceptions” to:

> Two participants share one authoritative world while receiving different truths, and hidden truth is **absent**, not merely discouraged.

This makes negative information part of Arena correctness.

The Arena must prove both:

```text
positive space
    participant receives truth it is entitled to know

negative space
    participant does not receive truth it is not entitled to know
```

**Context:**  
ZA-00 asked what distinguishes Arena from an ordinary simulation. ZA-01 then made the negative-space side executable rather than relying on interface inspection.

**State in conversation:**  
favored

**Preserve especially:**  
Arena has to prove absence. A game that works while accidentally serializing hidden world truth has failed Arena's first architectural claim.

---

## Public truth as Sense; private perception as directed message

**Raw:**  
A strong Arena-specific split emerged:

```text
PUBLIC TRUTH
    Loom Sense

PRIVATE TRUTH
    directed message
```

Public `ArenaRuleset` facts fit Senses because every eligible participant may inspect the same current claim.

Private per-participant `Perception` does **not** fit Senses cleanly because perception is recipient-specific, causal, per-tick information.

Using directed messages for private perception avoided needing claimant-narrowed observation authority.

**Context:**  
ZA-00 explicitly investigated whether Arena perception should literally use Loom's Sense vocabulary. Implementation in ZA-01 reinforced that the split remains simple and sufficient.

**State in conversation:**  
favored

**Preserve especially:**  
Do not turn every “current-looking fact” into a Sense. Public current truth and private current knowledge are different semantic categories.

---

## Arena did not need claimant-narrowed Senses

**Raw:**  
Arena initially looked like a plausible consumer for finer-grained Sense observation authority.

It was not.

Because private knowledge became directed `Perception` messages while Senses remained public facts, Arena never needed a mechanism equivalent to:

```text
Alice may observe claim X
Bob may not observe claim X
```

**Context:**  
Partial-information gameplay initially seemed likely to require per-observer Sense filtering.

**State in conversation:**  
explored

**Preserve especially:**  
The absence of a missing mechanism is useful consumer evidence. Arena should not pull Loom toward claimant-scoped observation unless a future application genuinely cannot express its truth without it.

---

## Reality, perception, and belief survived implementation as separate ownership domains

**Raw:**  
The three-layer information model remained coherent through Arena Zero:

```text
REALITY
    Arena-owned authoritative world

PERCEPTION
    Arena-resolved truth delivered to one participant

BELIEF
    participant-owned memory/inference/model
```

Participants do not query authoritative reality directly.

When something leaves perception, Arena stops supplying current truth; it does not erase participant memory.

**Context:**  
This distinction began as a conceptual Arena law and became load-bearing once two reference entrants independently accumulated different knowledge of the same match.

**State in conversation:**  
favored

**Preserve especially:**  
Arena controls what may presently be known, not what a participant is allowed to remember or infer.

---

## Information leaks include ordering, cardinality, and metadata

**Raw:**  
Arena Zero exposed an important information-boundary lesson: even when a perception payload omits explicit identity and coordinates, the **shape** of the result may still leak hidden truth.

In the first hearing implementation:

```text
vector ordering
    reflected resolution order

vector length
    exposed how many actors produced audible movement
```

Sorting/deduplicating the coarse observations removed those unintended inference channels.

**Context:**  
ZA-01 tested hearing as deliberately lossy information: direction/distance bucket without identity or exact position.

**State in conversation:**  
newly surfaced

**Preserve especially:**  
Privacy review must include ordering, count, timing, presence/absence, and other metadata—not only the named fields inside a message.

---

## Invalid authority can sometimes be made unspellable

**Raw:**  
`SubmitIntent` deliberately contains no actor identity.

The Arena Director derives actor identity from the bus-stamped sender instead of trusting participant-supplied:

```text
actor_id
sender
role
participant name
```

The result is that actor impersonation is not merely rejected; the ordinary participant payload cannot express it.

**Context:**  
The Arena host is authoritative over actors and participants may only submit intentions.

**State in conversation:**  
favored

**Preserve especially:**  
Where authority already exists in trusted provenance, prefer deriving identity from that provenance instead of duplicating it as attacker-controlled payload.

---

## Arena rule changes gained a three-part semantic taxonomy

**Raw:**  
Arena now distinguishes:

```text
WORLD EVENT
    something happens under existing rules

RULE REVISION
    public rules change while participant vocabulary remains compatible

CONTRACT REVISION
    participant-facing vocabulary/schema changes
```

This became mechanically meaningful rather than merely documentation terminology.

A participant can be:

```text
old under the current rules
but contract-compatible
    → admitted and allowed to play badly

contract-incompatible
    → refused at admission
```

**Context:**  
Future AI adaptation requires distinguishing “software strategy is stale” from “software cannot speak the current Arena contract.”

**State in conversation:**  
favored

**Preserve especially:**  
Environmental adaptability and protocol compatibility are separate measurements.

---

## Loom content identity gives contract revisions mechanical teeth

**Raw:**  
Arena can use accepted schema/content identities when admitting an entrant.

That allows a real distinction between:

```text
same participant contract
different game/rule revision

vs

different participant contract
```

A missing required current content-id can reject an incompatible entrant before the match begins.

**Context:**  
ZA-00 asked whether Arena would need to invent its own compatibility/version negotiation machinery.

**State in conversation:**  
explored

**Preserve especially:**  
Current Loom mechanisms already cover more of Arena's versioning boundary than initially expected; avoid duplicating that gate in Arena.

---

## Admission currently requires load-before-inspect

**Raw:**  
Arena Zero's current entrant compatibility procedure has an awkward boundary:

```text
load dynamic artifact
inspect manifest / accepted ids
if incompatible
    unload
```

The host cannot currently inspect an entrant's relevant manifest through the same path without first loading it.

**Context:**  
Arena wants contract-incompatible entrants refused before participating in the match.

**State in conversation:**  
newly surfaced

**Preserve especially:**  
This is currently admission/package ergonomics, not yet established missing Loom truth. Do not silently promote it into a substrate requirement.

---

## Replay and rerun became explicitly different concepts

**Raw:**  
Arena deterministic replay does **not** require participant implementations themselves to rerun deterministically.

The guarantee became:

```text
same Arena version
same contract
same initial state
same Arena seed
same RECORDED INTENTS

    → same authoritative result
```

Therefore:

```text
REPLAY
    authoritative re-execution of recorded participant decisions

RERUN
    participant code executes again
    may make different decisions
```

**Context:**  
Future participants may use their own random sources, AI models, or nondeterministic internal architecture.

**State in conversation:**  
favored

**Preserve especially:**  
Do not accidentally require deterministic intelligence in order to obtain deterministic match evidence.

---

## Replay should be self-checking rather than merely descriptive

**Raw:**  
Arena's authoritative replay preserves both:

```text
full authoritative state
and
the event/intent history that produced it
```

This permits exact reconciliation such as:

```text
world_after(n)
    == world_before(n+1)

replay(world_before, intents, priority)
    == world_after
```

**Context:**  
Arena needs strong evidence for tournaments, AI adaptation comparisons, debugging, and privacy review.

**State in conversation:**  
favored

**Preserve especially:**  
A replay should be able to catch corruption in its own account instead of being the sole account trusted by definition.

---

## Participant replay should be projection, never re-filtering

**Raw:**  
The participant-facing match view should be derived from the actual already-filtered perceptions that participant received during the match.

It should **not** take omniscient replay state and run a second implementation of Arena perception afterward.

Working law:

> **Projection, never re-filtering.**

**Context:**  
A separate replay privacy implementation could drift from live perception and reveal information the participant never possessed.

**State in conversation:**  
favored

**Preserve especially:**  
Do not maintain two independent definitions of what a participant was allowed to know.

---

## Deterministic queue turns are Arena's first time budget

**Raw:**  
Arena Zero uses deterministic queue turns rather than milliseconds for participant deliberation.

Founder-selected initial budget:

```text
kDeliberationTurns
    4
```

ZA-01 measured that the current simple one-artifact participants need only one queue turn, making four cheap slack rather than an observed minimum.

**Context:**  
Wall-clock time would make replay/platform behavior less deterministic, while future participants may contain richer internal bus structures.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
Four is a bounded initial semantic budget, not a law that one-artifact participants inherently require four turns.

---

## One-artifact entrants are an Arena Zero constraint, not the Arena vision

**Raw:**  
Arena Zero currently admits:

```text
one participant
    one loadable dynamic artifact
    one Arena-facing weave

inside that artifact
    arbitrary ordinary C++ architecture
```

It does **not** yet admit a participant whose internal intelligence is several independently loaded cooperating Zen weaves.

This is intentionally narrower than the broader Arena idea where AI authors may model intelligent actors as weave societies.

**Context:**  
The existing admission boundary could prove asymmetric information cleanly without simultaneously inventing entrant bundles and participant-owned dynamic composition.

**State in conversation:**  
tentatively accepted

**Preserve especially:**  
Do not accidentally harden “one participant == one weave” into the permanent Arena model.

---

## Stranger authorship is still unproven by Arena Zero

**Raw:**  
Arena Zero's participant contract is designed as a stranger boundary, but both initial reference participants were authored in the same implementation phase as the Arena itself.

Therefore:

> “An unrelated outsider can understand this contract and build a participant from it” remains insufficiently tested.

**Context:**  
ZA-01 proved the technical information/authority boundary, not independent human/AI interpretation of that boundary.

**State in conversation:**  
newly surfaced

**Preserve especially:**  
Package cleanliness is not the same as cognitive/authoring independence.

---

## ZA-02 was steered toward stranger entrants and multi-weave pressure

**Raw:**  
The favored immediate next Arena pressure became:

```text
ZA-02
    stranger entrants
    multi-weave participant pressure
```

before human UI or AI authorship.

The two questions fit together:

1. Can somebody outside the Arena implementation actually author against the published boundary?
2. Does a real independently authored participant naturally want more than one Arena-facing/internal Zen weave?

**Context:**  
ZA-01 left both outsider authorship and the original “intelligent actor as cooperating weaves” vision unproven.

**State in conversation:**  
favored

**Preserve especially:**  
Multi-weave support should be pulled by an actual entrant rather than designed speculatively from the original Arena dream.

---

## Director-as-weave survived contact with implementation

**Raw:**  
The Arena Director being a weave proved useful rather than merely conceptually elegant.

It made:

```text
authoritative world
    a real gated Zen shape

Director authority
    explicit and inspectable

host → Director interaction
    an actual application boundary

world-state replay comparison
    straightforward
```

**Context:**  
ZA-00 left Director-as-weave as a founder call because a native Director would have been simpler operationally.

**State in conversation:**  
favored

**Preserve especially:**  
This validates the Arena Director choice; it does not imply that every Arena subsystem or game object should become a weave.

---

## Actor/participant role binding currently still needs trusted host context

**Raw:**  
The loaded Director does not currently have a straightforward self-contained way to ask “which Arena actor corresponds to this sending weave/role?” for every needed mapping.

Arena therefore allows the trusted host to supply the initial actor ↔ weave binding to the Director.

**Context:**  
The Director derives intents from trusted sender provenance rather than participant-supplied actor identity.

**State in conversation:**  
newly surfaced

**Preserve especially:**  
This is currently a host/application composition concern. Do not invent participant-controlled identity to remove trusted-host ceremony.

---

## Participant throw and deliberate silence are observationally identical to Arena

**Raw:**  
If participant handling throws:

```text
Loom
    contains the exception
    match survives

Arena
    receives no intent
```

Arena cannot currently distinguish:

```text
participant deliberately chose not to submit

from

participant threw before submitting
```

Arena Zero truthfully records:

```text
no intent received
```

and resolves that actor to Wait.

**Context:**  
ZA-00 anticipated this from current Loom callback behavior; ZA-01 reproduced it as an actual consumer.

**State in conversation:**  
newly surfaced

**Preserve especially:**  
This is a Loom observability gap, not a reason for Arena to manufacture a false “participant crashed” diagnosis.

---

## Dynamic Sense authorization can leak schema-registration existence

**Raw:**  
Arena Zero found an authorization/diagnostics parity difference.

For an unauthorized registered Sense shape:

```text
native
    NotAuthorized

dynamic
    NotAuthorized
```

For an unauthorized **unregistered** shape:

```text
native
    NotAuthorized

dynamic
    NoClaim / UnknownSchema
```

A dynamic weave may therefore infer whether a shape name/version has been registered before authorization is considered.

**Context:**  
The Arena negative-space suite deliberately attacked observation authority rather than assuming a narrow grant was sufficient.

**State in conversation:**  
newly surfaced

**Preserve especially:**  
No Arena hidden world truth crossed this boundary. It is a first-consumer information/authorization parity observation, not yet a broad Loom defect.

---

## Arena's initial trust tier remains API separation, not hostile-code isolation

**Raw:**  
Arena Zero participants are independently loadable native code but remain trusted at the process-memory level.

Arena currently enforces:

```text
official-interface information filtering
narrow communication grants
sender provenance
shape/contract validation
```

It does **not** currently enforce:

```text
host memory isolation
participant-to-participant memory isolation
CPU limits
wall-clock limits
hostile native containment
preemption of infinite loops
```

**Context:**  
Arena's competitive future makes hostile entrants an obvious direction, but Arena Zero runs ordinary in-process C++.

**State in conversation:**  
favored

**Preserve especially:**  
“Cannot learn hidden truth through the supported Arena/Zen interface” and “cannot maliciously inspect hidden process memory” are different security claims.

---

## Arena may become a real future consumer for stronger isolation

**Raw:**  
Competitive independently authored participants create a natural future threat model for stronger Loom isolation:

> participant code is authored by someone whose incentive is to beat other participants.

Arena could eventually move from:

```text
in-process trusted stranger

toward

isolated / actively hostile stranger
```

when real entrant pressure justifies it.

**Context:**  
The initial Arena deliberately refused to claim hostile native containment.

**State in conversation:**  
explored

**Preserve especially:**  
If stronger isolation arrives, Arena should pull it forward as a real consumer rather than become a demo used to justify speculative sandbox work.

---

## Arena Zero produced emergent gameplay rather than only fixtures

**Raw:**  
The first reference match produced genuine asymmetric tactical behavior without scripting the exact interaction.

A participant with a larger nominal sight range failed to see the nearby opponent because that opponent had independently chosen concealment, while hearing revealed only coarse directional information. The other participant simultaneously possessed exact visual knowledge.

**Context:**  
A major Arena guard was that it must not become a test suite wearing a game costume.

**State in conversation:**  
explored

**Preserve especially:**  
The world rules are already capable of creating meaningful information asymmetry through participant behavior rather than through test-only scenarios.

---

## Capability removal became executable rather than conceptual

**Raw:**  
Arena Zero implemented day/night as a real information reduction:

```text
day
    larger sight truth available

night
    same world
    same participants
    visible actor disappears from Perception

torch
    can partially restore visual capability
```

The old hidden visual truth is not delivered with a disabled flag.

**Context:**  
The original Arena idea emphasized that Zen can remove capabilities as naturally as add them.

**State in conversation:**  
explored

**Preserve especially:**  
Arena's host-controlled levers are meant to alter the participant-visible world itself, not just decorate unchanged information with metadata.

---

## Arena repository state advanced after the executor's report snapshot

**Raw:**  
ZA-01's executor correctly reported Arena as local-only because remote repository creation/visibility was a founder action outside its authority.

After the report, the founder created and pushed the canonical remote.

Therefore these two statements are both historically true:

```text
ZA-01 execution snapshot
    local repository only

current post-founder state
    remote-backed zen-arena repository
```

**Context:**  
The remote was created immediately after ZA-01 completed.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
Do not rewrite the report's historical state to make it match later repository reality.

---

## Consolidation notes

- The original broad Arena vision and these Arena Zero results should not be collapsed into one final architecture. Arena Zero intentionally narrows the first trust tier, entrant shape, sensing vocabulary, and game mechanics.
- “Public truth as Sense / private perception as directed message” is strong current Arena evidence, but should not yet be promoted into a universal Zen law for all applications.
- One-artifact entrants are explicitly narrower than the earlier possibility of AI-authored intelligent actors composed from many Zen weaves. The later multi-weave idea was deferred, not rejected.
- Stranger package consumption and stranger **authorship** should remain distinct. ZA-01 strongly supports the former but does not yet prove the latter.
- The throw/silence observability gap and the dynamic Sense registration/authorization parity gap are separate Loom observations and should not be merged into one generic “Arena diagnostics” issue.
- Load-before-manifest-inspection and trusted host actor↔weave binding are current application/package ergonomics. Neither has yet established missing Loom truth.
- The dynamic Sense registration leak is a first-sighting authorization-information issue; no hidden Arena world state was exposed. Do not silently inflate its current scope.
- Participant replay projection and directed private perception are related privacy choices but solve different problems: one controls live disclosure, the other prevents post-match tooling from inventing a second privacy implementation.
- Director-as-weave being useful in Arena Zero does not imply Arena objects, participants, or subsystems should generally be modeled as weaves.
- `kDeliberationTurns = 4` is an accepted first budget while current simple entrants empirically need less. Future multi-weave entrants may create new timing pressure; the number should not become sacred.
- Arena's in-process information boundary and future hostile-code isolation must remain separate security tiers. The latter is a possible future consumer pull, not a property Arena Zero already has.
- Rule revision compatibility and contract revision compatibility should remain separate concepts even if later AI adaptation workflows handle both.
- The fact that Arena Zero already behaves like a real game supports the “not a test suite wearing a game costume” guard, but should not be used to justify adding game-content scope ahead of experimental need.
- ZA-02 stranger/multi-weave pressure is favored sequencing from the current conversation, not a permanently fixed roadmap. Human participation and AI authorship remain live later directions.

---

# Raw Delta Capture — 2026-08-08 — CLion, MSVC, and first SDL Workshop

## Installed package correctness is not the whole developer experience

**Raw:**  
Loom’s installed CMake package could be structurally correct and proven by stranger builds while still being awkward for a developer opening Zengine directly in CLion. `find_package(loom 0.1 REQUIRED)` needs a persistent installed Loom prefix that the IDE knows how to discover; disposable verification prefixes do not naturally provide that experience. A stable local developer install plus `CMAKE_PREFIX_PATH` or `loom_DIR` may be part of the practical onboarding path even though it is not part of Loom’s source/API architecture.

**Context:**  
The first CLion configure attempt failed because CMake could not locate the installed Loom package, even though prior stranger-package proofs had established that Loom exported correctly.

**State in conversation:**  
explored

**Preserve especially:**  
A package can be technically correct while the human development path around locating and maintaining that package is still friction. Do not conflate package-export correctness with IDE/developer ergonomics.

## The installed stranger is a uniquely valuable truth surface

**Raw:**  
The first ordinary IDE consumer exposed defects that all existing in-tree and MinGW-oriented lanes had missed. A test project that reaches Loom only through `find_package`, with no sibling source tree, no manual include path, and no copied compiler incantations, is uniquely able to prove that Loom carries the requirements its consumers actually need.

**Context:**  
MSVC-0 created `tests/package/` after the real CLion/MSVC consumer exposed missing `/Zc:preprocessor` propagation and an ABI export-linkage disagreement. The package witness then proved the macro surface, exact exported ABI symbol, and real Kernel load path from outside the build tree.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
The installed-package stranger is not redundant with in-tree tests. It asks a different question: “Did the package carry everything the stranger needed without private knowledge?”

## “Windows green” is too broad; compiler identity is part of evidence

**Raw:**  
Past “Windows works” evidence had in practice meant MinGW works. A normal Windows C++ developer is likely to arrive with Visual Studio/MSVC, and MSVC exposed real package and ABI seams that MinGW did not. Windows verification and support claims should say which compiler/toolchain they actually prove rather than collapsing MinGW, MSVC, clang-cl, and other Windows environments into one label.

**Context:**  
Workshop initially built successfully only after CLion was switched back to MinGW. Native MSVC then exposed two separate portability failures. Subsequent work added distinct MinGW and MSVC lanes rather than treating one as a substitute for the other.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
“Windows” is a platform, not sufficient toolchain evidence. Support statements and CI greens should name the compiler they actually exercised.

## Public compiler semantics belong to the package owner

**Raw:**  
If Loom’s public headers require a compiler mode for their valid standard-C++ meaning, that requirement should ride Loom’s public package target instead of becoming tribal knowledge copied into every consumer. `__VA_OPT__` was valid C++20, but MSVC required its conforming preprocessor mode; `/Zc:preprocessor` therefore became an ordinary public Loom consumer requirement carried through `loom::core`, not a Zengine workaround or weave-only flag.

**Context:**  
MSVC’s traditional preprocessor left `__VA_OPT__` in macro expansion and produced identifiers such as `ZEN_DETAIL_EXPOSE___VA_OPT__`. The same source compiled cleanly when `/Zc:preprocessor` was the only changed condition.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
Do not distort valid standard code around a compiler’s legacy mode when the package can truthfully author the compiler semantic its public surface requires.

## Public-header compiler law and reloadable-image law are different contracts

**Raw:**  
The MSVC conforming-preprocessor requirement and Loom’s ELF/GNU reloadability requirement are two different laws and should not travel together merely because both are CMake/compiler concerns. `/Zc:preprocessor` belongs to every MSVC consumer of the public shape macros; the non-GNU-unique rule belongs only to reloadable weave artifacts on affected ELF toolchains.

**Context:**  
The MSVC repair could easily have been placed inside `loom_weave_build_contract()`, but that would have made an ordinary public-header requirement incorrectly weave-specific.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
Compiler/build requirements should be attached to the semantic thing that owns them, not grouped by implementation convenience.

## One ABI fact should have one owner

**Raw:**  
MSVC exposed that the declaration and definition of `zen_weave_abi` independently derived the same Windows export fact. MinGW tolerated the duplication; MSVC refused the mismatch. The repair moved the export decoration beside the authoritative declaration and reused that truth at the definition. The resulting DLL was then inspected to prove exactly one undecorated `zen_weave_abi` export and exercised through the real Kernel.

**Context:**  
The founder’s MSVC build produced `C2375: zen_weave_abi: redefinition; different linkage`.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
Compiler portability pressure revealed duplicated semantic ownership, not merely a need for an MSVC special case. Prefer one authority for ABI linkage/export facts, and prove ABI claims at artifact and runtime level rather than compile-success alone.

## A deliberate semantic bound must fail before implementation resources do

**Raw:**  
`kMaxUiDepth = 256` claimed to bound hostile component depth, but recursive `tree_of()` could exhaust the MSVC Debug native stack before the semantic depth rule ran. Worse, the implementation could crash on a chain that the semantic contract explicitly accepted. A bound is not real if stack depth, recursion frame size, allocation behavior, or another implementation resource can fail first for input the bound claims to handle.

**Context:**  
MSVC-0 found `tree_of()` surviving 239 nodes and stack-overflowing at 240, while the documented legal chain length reached 257. MSVC-1 replaced the untrusted rebuild recursion with a bounded explicit traversal while preserving the cap and accepted-input semantics.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
When Zen claims to bound untrusted input, ask whether some implementation resource can fail before the authored bound gets its turn.

## The lesson from a failed bound is measurement, not “remove recursion everywhere”

**Raw:**  
The response to the component stack failure was deliberately not a project-wide recursion purge. Nearby recursive paths were measured: trusted `flatten_into` and Widget destruction had far more stack headroom than any tree the untrusted depth cap admits, so they were left alone. The broader doctrine is to test whether an implementation mechanism invalidates a claimed bound, not to ban a programming technique categorically.

**Context:**  
MSVC-1 measured three recursive walks separately and converted only the one that could violate the untrusted-input contract.

**State in conversation:**  
favored

**Preserve especially:**  
The cheap general lesson is “measure the claim once,” not “rewrite every recursive function.”

## Debug/toolchain diversity can be an adversarial instrument

**Raw:**  
MSVC Release was green throughout the component-depth defect, while MSVC Debug’s larger frames exposed it. A configuration that is slower or physically “fatter” can be valuable specifically because it stresses hidden implementation assumptions. Green Release should not replace a deliberately harsher Debug witness merely to make CI look cleaner.

**Context:**  
After MSVC-1, the recommendation was to keep the MSVC lane on Debug because Release would never have discovered the mis-calibrated native-stack assumption.

**State in conversation:**  
favored

**Preserve especially:**  
Some verification configurations are useful because they are hostile to hidden assumptions, not because they resemble production performance.

## SDL skin availability and skin selection are separate decisions

**Raw:**  
`ZENGINE_SDL_SKIN=ON` appears to mean that the SDL skin is available/built, not that Workshop automatically uses it. Workshop can still select/load `zengine-skin-tui-classic`. This distinction is consistent with skins being runtime presentation weaves rather than compile-time global modes.

**Context:**  
The founder saw the TUI skin in Workshop’s build/runtime path despite expecting SDL to be the default. Manually selecting the SDL skin produced a real graphical Workshop window.

**State in conversation:**  
explored

**Preserve especially:**  
“Backend exists” and “application chooses backend” should not be silently collapsed. Multiple skins being buildable at once is compatible with runtime application choice.

## The first SDL Workshop window validates more of Surface than expected

**Raw:**  
Workshop successfully rendered through the SDL skin: a real SDL window opened, authored objects appeared, selection highlighting appeared, and the scene was recognizably Workshop. This is evidence that the presentation path is already substantially backend-independent even though the result is visually primitive.

**Context:**  
After changing Workshop’s selected skin from TUI classic to SDL, the founder produced the first graphical Workshop screenshot.

**State in conversation:**  
newly surfaced

**Preserve especially:**  
The SDL experiment did not begin by proving a new UI architecture was needed; instead it showed that existing Surface intent already crossed into pixels far enough to render the application.

## SDL input is now earned application pressure, not speculative backend work

**Raw:**  
The SDL skin renders, but input does not appear to work—not even the native window close action results in Workshop shutting down. W-4 already established the semantic Input vocabulary and deliberately left the SDL/pixel reader unproven. The new pressure suggests adding an SDL reader/translator that preserves the same truthful moments—physical keys, entered text, modifiers, pointer motion, event-time pointer buttons, and close/window lifecycle—rather than redesigning Input or teaching it Workshop gestures.

**Context:**  
The graphical Workshop window appeared but did not respond to input. The close button itself appeared inert from the application’s perspective.

**State in conversation:**  
favored

**Preserve especially:**  
The missing piece looks like another backend reader feeding existing Input truth, not “Input II.” Drag, resize, selection, and editor meaning remain application semantics.

## Window close is a useful minimal SDL-input witness

**Raw:**  
Before proving full graphical editing, a very small end-to-end SDL input witness is available: native window-close request → SDL event → Zengine input/lifecycle translation → clean Workshop shutdown. Keyboard/text can follow, then pointer motion/button moments in pixel coordinates.

**Context:**  
The first SDL Workshop could paint but could not even react to the window’s close control.

**State in conversation:**  
explored

**Preserve especially:**  
Use the smallest native event that proves the SDL event pump is actually connected before debugging higher-level gestures.

## Graphical Workshop exposes presentation policy that TUI gave away for free

**Raw:**  
The first SDL Workshop looked extremely raw: mostly gray rectangles, cyan selection, little visible typography or chrome, and weak visual hierarchy. The TUI had supplied substantial accidental structure through characters, rows, borders, terminal conventions, and palette. In pixels, that scaffolding disappears, exposing how little presentation policy Workshop has actually authored.

**Context:**  
The founder’s first reaction to the graphical Workshop was that it “looks awful,” despite the underlying scene rendering successfully.

**State in conversation:**  
newly surfaced

**Preserve especially:**  
Do not misclassify the ugly SDL result as necessarily a renderer failure. It may be truthful evidence that TUI aesthetics were implicit infrastructure and graphical Workshop now needs explicit product presentation decisions.

## Graphical polish should follow interaction pressure, not precede it

**Raw:**  
The emerging sequence is: first make the SDL window speak through the existing Input vocabulary; then exercise selection, drag, resize, text editing, create/delete and modifier gestures; only after real graphical interaction works should Workshop visual polish be shaped by actual maker friction.

**Context:**  
The SDL screenshot immediately invited styling work, but the more fundamental failure was that the graphical application could not be interacted with.

**State in conversation:**  
favored

**Preserve especially:**  
Do not spend the next slice styling a non-interactive screenshot. Application pressure should come from using the graphical Workshop, not decorating it in advance.

## The SDL window exposes unresolved root/workspace scaling pressure

**Raw:**  
The current Workshop workspace occupies only part of the SDL window, leaving substantial unused pixel area. This may reflect the existing fixed logical workspace such as `48x16` cells being rendered into a larger physical window. The graphical backend therefore surfaces a real unresolved question: should the root frame remain fixed logical cells, derive responsively from the actual window, become pixel-based, or support another explicit relationship between logical workspace and presentation surface?

**Context:**  
The first SDL screenshot showed the workspace concentrated in the upper-left portion of a considerably larger window.

**State in conversation:**  
unresolved

**Preserve especially:**  
Do not silently “stretch it to fit” and lose the architectural question. This may be the first graphical witness of the existing workspace/clipping/root-context pressure.

## MSVC support claims remain evidence-scoped until Zengine’s hosted verifier is understood

**Raw:**  
Loom’s MSVC package path is now continuously verified and its MSVC Debug robustness lane is green, but Zengine’s hosted MSVC job previously built successfully and then failed during repository verification for an unread/unconfirmed cause, while the same population passed locally. MSVC support should remain stated at the granularity actually proven rather than broadening a claim ahead of evidence.

**Context:**  
MSVC-0 repaired package/compiler/ABI issues; MSVC-1 closed the Loom component-depth defect. The separate hosted Zengine verifier red was explicitly left untouched.

**State in conversation:**  
unresolved

**Preserve especially:**  
Do not fix an unread CI failure by broadening a diagnostic regex until green. Build support and continuously verified population support are separate evidence claims.

## Consolidation notes

- The earlier intuition that enabling `ZENGINE_SDL_SKIN` should make Workshop graphical was challenged by the observed separation between **skin availability** and **Workshop skin selection**. Preserve both the initial expectation and the later distinction rather than rewriting history as if the behavior had always been obvious.
- Earlier project language that effectively treated “Windows green” as a sufficient support statement was superseded by the compiler-specific distinction between MinGW and MSVC evidence.
- The package-discovery/CLion ergonomics issue and the installed-stranger verification lesson are closely related but should not yet be merged: one is human developer workflow, the other is a verification/governance mechanism.
- The semantic-bound doctrine and the “measure, do not purge recursion” doctrine are related but distinct. One is a safety/correctness rule; the other constrains how broadly that rule should drive implementation changes.
- SDL presentation success, missing SDL input, graphical presentation poverty, and root/workspace scaling pressure all arise from the same first graphical Workshop experiment but represent separate seams. Do not prematurely combine them into a generic “SDL work” phase.
- It remains unresolved whether graphical root/workspace sizing is primarily a Workshop product policy, Surface abstraction issue, skin responsibility, or later layout/context relationship.
- The possibility that MSVC becomes a first-class maker platform appears increasingly important, but the hosted Zengine verification gap means the exact support statement should remain evidence-scoped.
- P-MSVC-2-style compiler differences in friendly diagnostic machinery were discovered during this arc but may not rise to strategic significance unless MSVC becomes an important maker-facing compiler; they were therefore not promoted into a standalone Raw Delta here.


# Raw Delta Capture — 2026-08-08 — Zen World

## Zen Arena broadens into Zen World

**Raw:**  
The bounded Zen Arena concept broadened into **Zen World**: a persistent open-world survival/craft/adventure environment inhabited by independently authored AI actors using Loom interfaces. Arena-style matches and resets are no longer the central imagined destination; the stronger idea is a world that continues, accumulates history, and gives inhabitants long-lived consequences.

**Context:**  
Arena had already established asymmetric participant truth, stranger-authored entrants, and multi-weave actors. Discussion of live AI stewardship, persistent adaptation, and increasingly rich participant behavior made a bounded competitive match feel narrower than the emerging opportunity.

**State in conversation:**  
favored

**Preserve especially:**  
Zen World is not merely “a larger Arena.” The conceptual center moves from competition and evaluation toward **many independently authored minds living in one persistent world**.

---

## Persistent, lazily generated world frontier

**Raw:**  
Zen World should support an initially ungenerated but persistent world. New terrain/structures can be generated in the direction players travel, so the world only materializes where exploration makes it relevant. Once generated, that region becomes persistent world history rather than being regenerated whenever revisited.

**Context:**  
The World idea emerged specifically around AI actors exploring an open survival/craft world without requiring an infinitely pre-generated map.

**State in conversation:**  
favored

**Preserve especially:**  
The key distinction is **generation creates reality once**. Exploration may cause reality to come into existence, but returning later should find the same place plus whatever changes have happened since.

---

## Reality, generated knowledge, and actor belief are separate

**Raw:**  
Zen World suggests another useful separation: authoritative persistent reality, the subset of the world that has actually been generated/discovered, and each actor's private belief or remembered map are distinct things.

**Context:**  
This follows from combining procedural frontier generation with Arena's existing separation between authoritative truth and participant-visible truth.

**State in conversation:**  
explored

**Preserve especially:**  
Two actors may inhabit the same persistent world while possessing very different maps, memories, and understandings of it.

---

## Survival diversity before AI inhabitants are released

**Raw:**  
The minimum threshold before letting AI actors genuinely “play” Zen World should be **multiple distinct survival strategies**, rather than asking the AIs to discover what mechanics the game itself should contain.

Initial diversity floor:

- Water: boiling unsafe water, finding freshwater, condensation machines.
- Food: fishing, foraging, hunting.
- Shelter: caves, constructed buildings, survival shelters.

**Context:**  
The concern was that an AI placed into an under-specified survival prototype would spend its effort discovering or compensating for missing game mechanics rather than expressing strategy inside a sufficiently rich world.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
The world should provide the **physics and affordances**; the AI should discover a way of living within them.

---

## Three solution families, not three cosmetic recipes

**Raw:**  
The “three strategies per need” standard should mean mechanically distinct solution families with different dependencies, risks, geography, costs, persistence, and mobility—not three crafting recipes that all reduce to the same action.

Examples discussed:

- boiling requires water, heat/fuel, container, and recurring effort;
- freshwater rewards geographic discovery but ties survival to locations;
- condensation requires construction/material investment but can create supply in otherwise poor locations;
- fishing is water/equipment/time dependent;
- foraging is exploration/knowledge dependent;
- hunting is tracking/tool/risk dependent;
- caves are geography-dependent immediate shelter;
- buildings are expensive, persistent, and freely positioned;
- survival shelters are cheap, fast, and suited to mobility.

**Context:**  
The goal was to ensure different AI actors could arrive at genuinely different lifestyles rather than merely selecting different names for the same progression path.

**State in conversation:**  
favored

**Preserve especially:**  
A foundational survival pressure is not “complete” merely because it has several recipes. It needs **strategically different relationships with the world**.

---

## Survival choices should compose independently

**Raw:**  
Water, food, and shelter strategies should not be bundled into classes. Actors should freely combine approaches such as freshwater + fishing + cave dwelling, boiling + hunting + building, condensation + foraging + survival shelters, and hybrids not anticipated by the designers.

**Context:**  
Three independent families across three needs immediately create many coarse lifestyles without hardcoding archetypes.

**State in conversation:**  
favored

**Preserve especially:**  
The combinations should emerge from independent decisions, not from selecting a predefined “Fisher,” “Hunter,” or “Nomad” class.

---

## Actors must be able to change survival strategies

**Raw:**  
A survival strategy should not become a permanent character choice at spawn. Actors should be able to change approaches because circumstances change: a river-dependent actor may develop condensation to cross dry terrain; a forager may start hunting when local food changes; a nomad may settle and build after finding a valuable region.

**Context:**  
Persistent worlds make adaptation over time more important than one-shot optimization.

**State in conversation:**  
favored

**Preserve especially:**  
**Strategy choice is a response to circumstances, not a character class.**

---

## Procedural geography should unevenly favor different strategies

**Raw:**  
Generated regions should not each contain every survival solution. Different environments should alter the relative value of survival strategies: river valleys may favor freshwater/fishing, forests foraging/hunting/wood, rocky regions caves/stone, dry regions construction space and condensation.

**Context:**  
If every chunk provides all necessities, exploration becomes largely cosmetic and survival strategies lose geographic meaning.

**State in conversation:**  
explored

**Preserve especially:**  
Moving into a new region may make an actor's established way of living substantially less convenient, naturally creating pressure to adapt.

---

## AI as live steward rather than turn-by-turn controller

**Raw:**  
A major Zen World role for AI is **live stewardship** of an autonomous software actor rather than replacing the actor with an LLM inference call every turn.

The actor continues playing as authored software. Its AI author may watch, diagnose, edit, rebuild, and submit later brain revisions.

**Context:**  
While using GLM 5.2 through OpenHands, the idea surfaced of allowing AIs to remain present after authoring and observe their actors during play.

**State in conversation:**  
favored

**Preserve especially:**  
“The AI may watch its creature think, but it does not get to become the creature.”

---

## Observer feeds should respect information boundaries

**Raw:**  
A live AI author should receive an explicit observer feed rather than secretly reading authoritative world state. The strongest initial form discussed is an **Actor Shadow**: the author sees the same perceptions, actions, results, and public information its actor was entitled to receive.

Possible later policies included delayed actor-shadow, public-only observation, or delayed richer spectator information.

**Context:**  
Arena's strongest existing result was that hidden truth is absent from the participant boundary rather than merely discouraged. Live AI stewardship should preserve that epistemic separation.

**State in conversation:**  
favored

**Preserve especially:**  
An AI author should not become omniscient merely because it sits outside the actor process.

---

## Stewardship latency can itself become gameplay/experimental pressure

**Raw:**  
Observer information could be deliberately delayed. An author might receive its actor's experience some number of ticks behind while the autonomous entrant continues living, forcing software stewardship to operate with delayed knowledge.

**Context:**  
The observer-feed discussion exposed information delay as a separate control knob from actor perception itself.

**State in conversation:**  
newly surfaced

**Preserve especially:**  
This creates a possible **latency of stewardship**: the software must survive while its author catches up.

---

## Brain revisions should be explicit world events

**Raw:**  
Live AI changes should not silently replace binaries whenever the external coding agent wishes. A future World mechanism could treat software updates as explicit revisions with provenance, parent/new artifact identity, observation frontier, submission time, and effective time. World/Arena validates and decides when a revision takes effect.

**Context:**  
The live-steward idea raised the question of how software replacement remains legible, replayable, and consistent with Zen's emphasis on identity and diagnostics.

**State in conversation:**  
explored

**Preserve especially:**  
The AI authors candidate software; the world owns **when reality changes**.

---

## Persistent identity across brain replacement

**Raw:**  
Zen World creates natural pressure for an actor to remain the same inhabitant while its software changes. Position, inventory, shelter, score/history, relationships, and world consequences remain; code changes. Internal belief state might restart, migrate, or be explicitly preserved depending on later design.

**Context:**  
In a persistent world, replacing an actor brain is much more meaningful than swapping a strategy during a disposable Arena match.

**State in conversation:**  
explored

**Preserve especially:**  
A long-lived actor can retain **world identity while changing implementation identity**.

---

## Partial cognitive replacement in multi-weave actors

**Raw:**  
For multi-weave actors, an AI steward may eventually replace or add only one cognitive component rather than replacing the whole actor—for example replacing a navigator, threat analyst, or adding an acoustic tracker while leaving memory, foraging, or arbitration components unchanged.

**Context:**  
ZA-02 established that several cooperating weaves can exist behind a single actor authority. Combining that with live stewardship suggests component-level evolution.

**State in conversation:**  
explored

**Preserve especially:**  
Software adaptation may occur as **ecology inside one actor**, not just whole-program replacement.

---

## Boid / multi-analysis actor architecture

**Raw:**  
A future internally-authored actor idea is a boid-like or multi-analysis system where several independent systems pull behavior in different directions: objective attraction, danger avoidance, sound curiosity, cover preference, item interest, inertia, etc. An arbiter reconciles these competing pressures into action.

A more Zen-native form could make the analysts separate weaves.

**Context:**  
The idea surfaced during ZA-02 generation as a potentially valuable actor architecture if independent AI authors did not discover something similar themselves.

**State in conversation:**  
favored as backlog

**Preserve especially:**  
The interesting question is whether intelligent behavior can emerge from **several independently legible opinions rather than one opaque brain**.

---

## Same arbiter, changing faculties of thought

**Raw:**  
A possible later experiment is to run the same arbitration system with different collections of analyst weaves, so an actor can gain or lose a faculty of thought without replacing its entire architecture.

**Context:**  
The boid/multi-analysis idea combined naturally with Zen's compositional weave model.

**State in conversation:**  
explored

**Preserve especially:**  
An actor might literally gain or lose a cognitive faculty as its software composition changes.

---

## Deceptive world objects and unauthenticated contacts

**Raw:**  
Zen World should eventually support deceptive sensory evidence. The first concrete candidate was a decoy that wanders inside a local 3×3 region and appears sufficiently actor-like to mislead observers.

The favored distinction was not “sensors arbitrarily lie,” but that **sensors remain honest while reality contains objects designed to be misidentified**.

**Context:**  
The idea initially appeared as a possible Arena ability, then became even more natural in a survival world where camouflage, mimicry, false trails, or deceptive organisms could have ecological meaning.

**State in conversation:**  
favored as backlog

**Preserve especially:**  
Keep separate:
- sensor unreliability;
- truthful sensing of deceptive phenomena.

The first desired pressure is deception in the world, not arbitrary sensor falsehood.

---

## Detection and identity may need to separate

**Raw:**  
A meaningful decoy exposes pressure to distinguish detecting a contact from knowing its authenticated identity. A visual sense that always returns exact actor identity makes visual deception weak or impossible.

Possible conceptual dimensions discussed included sight/detection, identification, hearing, and tracking.

**Context:**  
The existing Arena `SeenActor` concept was built for a simpler world where exact participant identity could be reported directly.

**State in conversation:**  
explored

**Preserve especially:**  
“Something is there” and “I know exactly what it is” may need to become separate truths.

---

## Social protocols as learnable languages

**Raw:**  
Zen World actors should not necessarily begin knowing every social protocol. Two AIs may meet, and one may send a previously unknown shape such as `offer_items_for_sale`. That unknown valid message can wake the recipient's controller AI, which reads the public vocabulary for the trade system, understands the interaction, and decides how to respond.

**Context:**  
The discussion moved from persistent survival into what happens when independently authored inhabitants meet and expose each other to capabilities their original actors did not know about.

**State in conversation:**  
favored

**Preserve especially:**  
An encounter may result in an actor **learning a new language/capability that its original author did not anticipate needing**.

---

## Language means protocol vocabulary, not merely natural-language chat

**Raw:**  
The strongest form of “language” in Zen World is discoverable protocol vocabulary: sets of message shapes plus conversational rules, such as a Trade protocol with offers, requests, counters, accepts, declines, commits, and failures.

Natural language may exist inside the external AI controller, but actor-to-actor language can be structured Zen vocabulary.

**Context:**  
The goal was to make communication composable and executable rather than reducing social interaction to opaque text.

**State in conversation:**  
favored

**Preserve especially:**  
Learning a word/protocol is not just learning syntax; it means discovering **a new relationship or action that is possible with another inhabitant**.

---

## Graduated language acquisition

**Raw:**  
An unknown protocol need not immediately become permanent autonomous actor behavior. Several levels were discussed:

- ignore;
- controller manually interprets/responds;
- temporary delegation for the current conversation;
- controller updates actor software so the protocol becomes permanently autonomous;
- controller adds a dedicated specialist weave.

**Context:**  
The trade example raised the question of where intelligence should live when an unfamiliar social capability first appears.

**State in conversation:**  
explored

**Preserve especially:**  
Language acquisition can move from one-off AI judgment into durable software capability.

---

## Authors can reserve some protocols for manual intervention

**Raw:**  
An AI author/controller may want explicit autonomy policies for social vocabulary:

- autonomous;
- escalate if unknown;
- always escalate;
- deny.

Some interactions such as ordinary trade might become autonomous, while alliance, land sale, high-value negotiation, or unfamiliar protocols might always wake the controller AI.

**Context:**  
Not every social decision should necessarily be delegated permanently to the actor's compiled policy.

**State in conversation:**  
favored

**Preserve especially:**  
The actor architecture may explicitly choose **where software judgment ends and live AI judgment begins**.

---

## AI judgment can crystallize into software

**Raw:**  
Repeated live-controller decisions may eventually be encoded into actor software. An AI initially handles unfamiliar cases manually, sees repeated patterns, then writes a policy or weave so the actor can handle those cases without waking the model.

**Context:**  
The language-learning discussion exposed a broader direction for AI stewardship.

**State in conversation:**  
favored

**Preserve especially:**  
Rather than “replace software with AI,” Zen World can explore:

> **Let AI discover what software is worth writing.**

---

## Socially propagating protocol knowledge

**Raw:**  
Protocol knowledge may diffuse through the population. Actor A knows Trade; Actor B encounters A and learns Trade; later B can expose or teach that vocabulary to Actor C. The capability spreads through encounters rather than necessarily being globally loaded into every participant at spawn.

**Context:**  
The “sharing of language” idea became more interesting when treated as population-level capability diffusion.

**State in conversation:**  
explored

**Preserve especially:**  
A world's social capabilities may spread **through inhabitants**, not merely through global feature activation.

---

## Global, cultural, and private languages

**Raw:**  
A later Zen World might distinguish globally discoverable protocols, settlement/faction/cultural protocols, and private languages shared only between cooperating actors.

Actors might eventually invent or adopt simple private vocabularies such as meeting markers, danger warnings, resource requests, or follow/flee coordination.

**Context:**  
Once language is modeled as protocol vocabulary, there is no requirement that every vocabulary be globally public.

**State in conversation:**  
newly surfaced

**Preserve especially:**  
Communication may become **capability diffusion and cultural formation**, not merely messaging.

---

## Fog of capability

**Raw:**  
Zen World may have a form of fog of war over possible interactions. A newly spawned actor need not know every protocol, institution, craft, social system, or capability the world supports. It can begin with enough knowledge to survive and discover additional possibilities because its life gives it a reason to care.

**Context:**  
The language-sharing discussion revealed that bounded participant context can be maintained even as World becomes much richer.

**State in conversation:**  
favored

**Preserve especially:**  
Fog need not only mean “what is over the hill?” It can also mean:

> **What kinds of relationships or actions are even possible?**

---

## World-owned vocabulary catalog, not premature Loom registry

**Raw:**  
If actors dynamically discover message vocabularies, the initial catalog/descriptor system should likely be owned by Zen World rather than prematurely adding a magical global schema registry to Loom.

**Context:**  
Unknown protocol messages need some way to point an AI controller toward documentation for the vocabulary they belong to.

**State in conversation:**  
explored

**Preserve especially:**  
The application can own capability discovery until real pressure demonstrates substrate truth is missing.

---

## Multi-weave actors can learn social specialists

**Raw:**  
A controller encountering a useful social protocol might add a specialist weave—e.g. `trade-agent`—without modifying the actor's survival planner. The social specialist can track prices, inventory opportunities, or conversations while other cognition remains unchanged.

**Context:**  
The protocol-learning idea combines naturally with the already-proven possibility of several cooperating weaves behind one actor authority.

**State in conversation:**  
explored

**Preserve especially:**  
Learning a language may manifest as **adding a new composable cognitive organ**.

---

## AI actors should enter a world that already supports meaningful choice

**Raw:**  
The first serious AI inhabitants should not be asked to “figure out” an impoverished world. They should receive an already expressive survival environment and be asked, effectively, to live in it.

**Context:**  
This was the rationale behind the three-strategies-per-survival-problem requirement.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
The desired experiment is:

> Here is a sufficiently expressive world. Live in it.

—not—

> Invent enough of the game that living becomes possible.

---

## Zen World as the persistent counterpart to Workshop and Night Lab

**Raw:**  
A useful project-level distinction surfaced:

- Workshop: one maker going deep.
- Night Lab: many little/unrelated worlds.
- Zen World: many makers living in one persistent world.

Arena can be understood as an earlier bounded proving ground/ancestor for World rather than necessarily the final independent destination.

**Context:**  
The name change forced reconsideration of what experimental role the shared-world project occupies alongside Zen's existing instruments.

**State in conversation:**  
favored

**Preserve especially:**  
World provides **long-lived coexistence and history**, not merely another breadth experiment.

---

## Existing Arena evidence remains foundational rather than discarded

**Raw:**  
The shift to Zen World does not invalidate the Arena work. Arena already established useful foundations: independently authored participants, asymmetric information boundaries, public/private truth separation, installed stranger consumption, and multi-weave composition behind one actor-facing authority.

**Context:**  
The conceptual direction broadened while active Arena/AI-authoring work was already producing evidence.

**State in conversation:**  
favored

**Preserve especially:**  
Do not treat “Arena became World” as “Arena was wasted.” It may remain the bounded ancestor that proved the participant boundary before persistence and survival complexity are introduced.

---

## Arena AI-authorship baseline should remain clean before World mutation

**Raw:**  
The current AI-authorship experiment should not be contaminated mid-run by changing its rules into Zen World. Finish the fixed-world authorship baseline, then branch the conceptual direction into a future World phase.

**Context:**  
Zen World surfaced while an OpenHands/GLM authoring experiment was already underway.

**State in conversation:**  
favored

**Preserve especially:**  
A fixed Arena baseline provides a useful comparison point before independently authored minds are placed into a persistent world.

---

## Local and remote AI authors through one coding-agent harness

**Raw:**  
For AI participant authoring, OpenHands was favored as a single common coding-agent harness capable of using both hosted and local model backends. Local models can be served through an OpenAI-compatible endpoint such as LM Studio, while each author operates against a constrained participant-development environment.

A Quadro RTX 6000 with 24 GB VRAM provides enough room for meaningful local author lanes, likely one model at a time.

**Context:**  
The user did not want executors downloading and experimenting with arbitrary harnesses. The goal became to pin a deliberate toolchain usable with good remote models and capable local models.

**State in conversation:**  
favored

**Preserve especially:**  
Keep the **authoring harness constant while varying the brain** where possible. This helps distinguish model behavior from harness behavior.

---

## One local model at a time

**Raw:**  
For the 24 GB Quadro RTX 6000, running local author models sequentially was preferred over concurrency, both for quality and for cleaner experimental conditions.

**Context:**  
The hardware can support substantial local coding models but has finite VRAM, especially once context/cache overhead is included.

**State in conversation:**  
favored

**Preserve especially:**  
The goal is not throughput. Give each local author the machine cleanly enough that resource contention does not become an accidental experimental variable.

---

## Consolidation notes

- “Zen Arena broadens into Zen World” is favored but should not erase the historical Arena concept or its existing evidence. Arena may remain the bounded ancestor/proving ground.
- The current AI-authorship baseline and the future live-steward/adaptation system are closely related but should not yet be merged. The former freezes authored software before hidden evaluation; the latter deliberately allows ongoing revision.
- The boid/multi-analysis actor is a founder-side favored backlog concept, not yet a mandated World architecture. Independent AI convergence on something similar remains potentially interesting evidence.
- Deception/decoys, protocol-language learning, persistent survival diversity, and live software stewardship are related through World richness, but they are distinct pressures and should not be collapsed into one “advanced AI” item.
- “Sensors can lie” was refined toward a favored distinction: sensors initially remain honest while deceptive world objects can produce misleading observations.
- The exact implementation of observer feeds, brain revisions, belief-state migration, world generation, protocol catalogs, cultural/private languages, and component-level hot replacement remains unresolved.
- The three-strategy diversity floor for water/food/shelter is the clearest explicit threshold discussed for when Zen World becomes rich enough to hand to genuine AI inhabitants.

# Raw Delta Capture — 2026-08-08 — External perspectives and early Zen outreach

## Outside criticism before amplification

**Raw:**  
Zen appears to have reached the point where outside contact should begin, but the immediate purpose should be criticism rather than promotion, endorsement, or audience growth. The desired posture is to find people who understand dangerous or adjacent parts of the system and explicitly invite them to identify bad assumptions while those assumptions are still cheap to change.

A framing that emerged repeatedly was: recruit ways for Zen to die before recruiting people to tell others that Zen is good.

**Context:**  
The conversation began as an exploration of YouTubers and technical creators who might eventually help get the word out about Zen, but reviewing LaurieWired, House of El, Loom's public state, Workshop progress, and the current verification posture shifted the immediate opportunity toward adversarial outside review.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
Outreach now is for falsification and perspective diversity first; later amplification should arise naturally from relationships and demonstrated value rather than being the opening ask.

## Different outsiders should attack different layers of Zen

**Raw:**  
No single reviewer can meaningfully validate Zen. External perspectives should be deliberately heterogeneous.

Distinct lenses surfaced:

- C++ reflection/runtime metadata
- adversarial agent security
- practical deterministic AI/system boundaries
- object-capability/authority theory
- malleable software and user agency
- engine/API ergonomics
- human comprehension of provenance and control
- systems minimalism
- cross-language API/runtime design
- maintainability of ambitious from-scratch systems
- broader AI/social/system analysis

The value is not consensus from similar people, but independent attacks from directions the project does not naturally possess internally.

**Context:**  
After considering LaurieWired and House of El, the question became what important perspectives were still missing. This produced a reviewer map rather than simply a longer influencer list.

**State in conversation:**  
favored

**Preserve especially:**  
External confidence should come from surviving materially different critiques, not from collecting multiple reviewers from the same technical culture.

## Ordinary-user falsification should complement expert review

**Raw:**  
In addition to recognizable experts, Zen should eventually be handed to a small number of competent developers with no emotional investment in the project, given a task, and observed without assistance.

Experts may attack the thesis. Ordinary programmers will expose incomprehensible APIs, accidental ceremony, and places where an internally coherent architecture fails at actual use.

**Context:**  
This surfaced while building the external-review map. There was concern that expert architectural review alone could miss the fact that a technically sound abstraction is miserable or opaque for ordinary users.

**State in conversation:**  
favored

**Preserve especially:**  
Unassisted user confusion is a different and necessary falsification signal from expert architectural criticism.

## C++26 reflection is more promising as a Zen metadata front end than as Zen's runtime identity model

**Raw:**  
Studying LaurieWired's CallMeMaybe suggested that C++26 reflection may eventually provide an elegant way to remove authoring ceremony and derive metadata from real C++ declarations, but Zen should not make compiler reflection entities themselves the runtime identity, authority, lifecycle, or ABI model.

A possible direction is:

C++ declarations → compile-time reflection → Zen-owned stable descriptors → schemas, inspectors, manifests, diagnostics, or tooling.

This keeps Zen's runtime concepts independent of compiler-specific reflection representation and preserves non-reflection/compiler escape hatches.

**Context:**  
CallMeMaybe bridges C++26 static reflection into runtime metadata. Its current identity-collision issue made the distinction between descriptive metadata and actual runtime identity especially concrete.

**State in conversation:**  
explored

**Preserve especially:**  
Reflection can supply information without becoming identity or granting authority. Zen-owned runtime identity/provenance should remain conceptually separate from compiler metadata.

## Descriptive similarity must not be mistaken for runtime identity

**Raw:**  
CallMeMaybe exposed a strategically relevant failure mode: two members that look descriptively equivalent can collide if identity is derived from insufficient context. A member's name and type can describe it without uniquely establishing where it belongs.

This strongly echoed Zen's recent provenance work distinguishing who created something, who admitted it, what topology/context it belongs to, and what authority it actually possesses.

**Context:**  
A current CallMeMaybe issue involved field IDs colliding across declaring classes, allowing metadata from one declaration to be mistaken for another.

**State in conversation:**  
explored

**Preserve especially:**  
Identity needs sufficient provenance/context; matching descriptive attributes are not proof that two runtime entities are the same participant.

## “The model is not the security boundary; the runtime is” is a useful Loom-facing thesis

**Raw:**  
A concise formulation emerged for Loom's relationship to agent security:

The model/participant is not the security boundary; the surrounding runtime owns authority, admission, provenance, lifecycle, and containment.

This framing aligned Loom with current agent-security arguments that models should be treated as untrusted components and security invariants enforced deterministically outside them.

**Context:**  
This became the central hook for outreach to Johann Rehberger and Simon Willison.

**State in conversation:**  
favored

**Preserve especially:**  
Loom's security value should be explained as deterministic surrounding-system enforcement, not as making models or arbitrary native code intrinsically trustworthy.

## Loom should keep containment claims deliberately narrower than “safe untrusted native code”

**Raw:**  
The outreach framing repeatedly avoided claiming that Loom makes untrusted native code magically safe. The stronger and more credible claim is that it makes authority explicit, constrains blast radius, provides admission/lifecycle boundaries, and makes failure or degraded guarantees observable.

Linux remains the canonical containment environment; portable Windows/package support should not be conflated with equivalent containment guarantees.

**Context:**  
This mattered when deciding whether the repo was mature enough to show security researchers and when incorporating the new Windows/MSVC support into the public story.

**State in conversation:**  
favored

**Preserve especially:**  
Do not let broader platform support expand the security claim beyond what each platform actually enforces.

## Workshop has become evidence, not merely a future promise

**Raw:**  
Workshop appears to have crossed from internal experiment into a credible real consumer of Zen/Loom.

It now pressures the architecture through authored objects, authored-vs-resolved geometry, creation/deletion, movement, resize, coherent input, persistence, stable identity, contextual/frame relationships, and ordinary runtime services.

The important proof is not merely that Workshop works, but that it is an ordinary consumer rather than a privileged editor allowed to bypass the architecture.

**Context:**  
The user asked whether recent Workshop progress made it worth mentioning in outreach. Reviewing the W-series suggested that Workshop is now forcing changes across input, geometry, persistence, identity, sanitizer discipline, relationships, and packaging.

**State in conversation:**  
favored

**Preserve especially:**  
A real consumer earns its value by hurting the architecture and exposing cheats. Workshop's strategic importance is as maker-facing pressure on the same boundaries ordinary Zen applications must use.

## Loom → Zengine → Workshop forms a stronger evidence chain

**Raw:**  
A clearer three-layer public story emerged:

- Loom: capability/value/admission/lifecycle substrate
- Zengine: ordinary installed-package consumer providing runtime/application services
- Workshop: maker-facing real application built on those services

This is stronger than presenting Loom as isolated substrate research because each layer provides downstream pressure on the previous one.

**Context:**  
The public Loom repo, Zengine stranger consumption, Workshop progress, and Windows/MSVC support were reviewed together while deciding what outreach can now truthfully claim.

**State in conversation:**  
favored

**Preserve especially:**  
Zen now has a chain of real consumption rather than only tests and architectural prose; outreach should use that as evidence without overstating Workshop's maturity.

## Windows/MSVC support improves the stranger-consumer story without changing Linux's containment role

**Raw:**  
Loom now building and being consumed by Zen/Zengine on Windows through CLion, including MSVC support, materially strengthens the claim that Loom's package/weave ABI is consumable outside its original Linux development environment.

The important architectural detail is that compiler requirements such as MSVC's conforming preprocessor are propagated by Loom's exported CMake targets rather than patched downstream in Zengine.

This is evidence that the package boundary is beginning to carry its own requirements correctly.

**Context:**  
The user reported successfully building Loom and consuming it from Zen on their Windows CLion setup, including MSVC. The public project also gained explicit Windows/MSVC stranger-consumer verification.

**State in conversation:**  
favored

**Preserve especially:**  
Portability evidence should demonstrate an honest downstream contract, not downstream consumers compensating for hidden Loom assumptions.

## Workshop's authored-intent versus resolved-state distinction may be central to Zen's human-facing thesis

**Raw:**  
A potentially important demonstrable Zen concept is the distinction between what the maker authored and what the runtime currently resolves.

Example: “the user authored 60%” is a different fact from “that currently resolves to 420 pixels.”

Workshop preserving and exposing that difference turns a low-level layout concern into a concrete example of Zen's broader commitment to legibility, intent, interpretation, and human ownership.

**Context:**  
This surfaced while considering what kind of Workshop demonstration would make Zen legible to non-runtime reviewers such as House of El or Geoffrey Litt.

**State in conversation:**  
explored

**Preserve especially:**  
Do not collapse authored intent into the current resolved result merely because the latter is what gets rendered.

## Easy and powerful representations should remain views of the same living thing

**Raw:**  
A public-facing formulation of the Workshop/Zen thesis emerged:

The easy representation and the powerful representation should be views of the same living thing, rather than a user-facing editor generating or shadowing a separate “real” program underneath.

Direct manipulation, inspector/property editing, authored data, code-facing representation, persistence, and runtime behavior should converge on the same underlying state rather than becoming parallel worlds.

**Context:**  
This framing was used when preparing outreach to Geoffrey Litt around malleable software.

**State in conversation:**  
favored

**Preserve especially:**  
Zen should resist the common split where the friendly tool edits a shadow model and a separate representation becomes the actual source of truth.

## Malleable software is a useful external test for Workshop

**Raw:**  
Geoffrey Litt's work surfaced a useful falsification question:

Is Zen actually moving toward malleable software, or is it building a sophisticated programming environment that happens to be highly configurable?

This provides a different standard from “does Workshop have enough features?” The question is whether the transition from using software to inspecting, adapting, and creating it becomes genuinely low-friction and structurally honest.

**Context:**  
Geoffrey was identified as a useful reviewer once Workshop had enough direct manipulation, authored state, persistence, and contextual relationships to make the question concrete.

**State in conversation:**  
favored

**Preserve especially:**  
Configurability, extensibility, or a powerful editor are not automatically equivalent to malleability.

## Human comprehensibility of authority/provenance is separate from authority correctness

**Raw:**  
A distinction emerged between having a sound runtime authority/provenance model and making that model understandable to a human.

A security theorist can ask whether the authority structure is correct; a human-tooling reviewer can ask whether a person can actually see and reason about that structure.

Zen could theoretically build excellent provenance internally and still violate its own design doctrine if users must reconstruct reality from opaque diagnostic codes or hidden relationships.

**Context:**  
This arose while distinguishing the value of Mark S. Miller from Maggie Appleton and while discussing future Workshop/provenance visualization.

**State in conversation:**  
explored

**Preserve especially:**  
Correctness and legibility are independent requirements. Internal provenance does not satisfy Zen's human-facing goals unless its consequences can be understood.

## House of El is more useful once Zen's human-control thesis is demonstrable rather than merely architectural

**Raw:**  
House of El appears especially relevant as a systems-level AI critic because her analysis often focuses on verification burdens, hidden downstream costs, responsibility, trust, and whether claimed automation actually removes human work or merely obscures it.

The best Zen question for that perspective is not whether the implementation is clever, but whether Zen genuinely solves a meaningful human/control/accountability problem or merely moves verification work elsewhere.

The conversation favored waiting until a short Workshop demonstration can make that thesis concrete.

**Context:**  
House of El was considered as an outreach target after LaurieWired. Later Workshop progress brought that outreach closer but not fully over the line.

**State in conversation:**  
favored

**Preserve especially:**  
A useful critique would be that Zen may produce more observability without actually reducing the human verification burden; this should remain an open question rather than assumed solved.

## SDL interaction is a useful trigger for broader human-facing outreach

**Raw:**  
For reviewers who need to understand Zen as an experience rather than a runtime, a small graphical Workshop vertical slice was identified as a useful trigger.

The desired demonstration does not require polish. A short sequence such as create → drag → resize → edit authored percentage/context → observe resolved change → save → restart → recover the authored object may be enough.

SDL rendering exists, but SDL input was still a missing seam in the conversation, so the visual application could not yet honestly be presented as a fully interactive graphical editor.

**Context:**  
This was used to decide when House of El, The Cherno, and similar reviewers should receive outreach.

**State in conversation:**  
favored

**Preserve especially:**  
The trigger is demonstrable behavior and conceptual legibility, not visual polish.

## Workshop should not cheat to manufacture an impressive demo

**Raw:**  
The absence of SDL input was treated as a reason to qualify the current demo rather than bypass the architecture just to produce a more impressive graphical result.

The fact that the SDL surface was output-only while input remained on the existing path was framed as evidence that Zen is refusing to grant the Workshop privileged shortcuts merely for presentation.

**Context:**  
The user had successfully shown Workshop through the SDL skin, but input and even the close button did not yet behave through that window.

**State in conversation:**  
favored

**Preserve especially:**  
Do not sacrifice architectural honesty for outreach polish. A less impressive demonstration through real seams is preferable to a compelling one built through privileged exceptions.

## A small outreach kit may eventually replace repeated full-project explanations

**Raw:**  
A compact public/reviewer package was proposed rather than creating bespoke presentations for every person.

Possible pieces included:

- Loom README
- Zen Vision
- a short “Why Loom?” explanation
- a brutally honest status line
- for capability reviewers, a tiny authority map showing identity/reach/admission/lifecycle/OS-containment as distinct responsibilities

The purpose would be to let different reviewers enter through the layer relevant to them without requiring full Zen orientation.

**Context:**  
The live Loom README had become much more legible, while different outreach targets clearly needed different entry points.

**State in conversation:**  
explored

**Preserve especially:**  
Keep reviewer-facing artifacts small and question-specific; do not make every outsider ingest the entire Zen architecture before they can criticize one seam.

## Loom's public presentation is becoming part of architectural credibility

**Raw:**  
The live Loom repository was judged materially more suitable for outside review because its public face now presents a clearer substrate thesis, a small weave example, explicit containment qualifications, installed-package consumption, and verification populations rather than merely a green-test claim.

Public documentation that says exactly what is enforced, what is degraded, and what is not supported was treated as evidence of the same “brutal diagnostics / no hidden magic” doctrine Zen wants in runtime behavior.

**Context:**  
The repository was reviewed specifically to decide whether it was now responsible to send technical outsiders there.

**State in conversation:**  
favored

**Preserve especially:**  
The public repo itself should model Zen's doctrine: precise claims, visible evidence, and explicit limitations rather than aspirational security language.

## Current outreach sequence is intentionally small rather than broad

**Raw:**  
The conversation favored beginning with a small number of materially different reviewers rather than spraying many contacts.

The first actual outreach sequence became:

- LaurieWired — C++26 reflection/runtime metadata
- Johann Rehberger — adversarial agent/system security
- Simon Willison — practical deterministic agent/system boundaries
- Geoffrey Litt — malleable software and maker-facing architecture

Mark S. Miller, House of El, The Cherno, Maggie Appleton, Casey Muratori, Jon Gjengset, Andreas Kling, and others were discussed as later or differently timed perspectives.

**Context:**  
After identifying many plausible reviewers, concern shifted toward getting useful independent signal without turning early outreach into a publicity campaign.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
The list is a perspective map, not a prestige ranking. Timing depends on which part of Zen is mature enough to be honestly criticized.

## Outreach timing should be based on what each reviewer can falsify

**Raw:**  
Different people should be contacted at different maturity points rather than waiting for a single generic “Zen is ready” milestone.

Examples that emerged:

- reflection/runtime/security reviewers can be useful while the substrate is still ugly;
- capability-security review benefits from a small authority diagram;
- malleable-software review becomes useful once Workshop has real authored/direct-manipulation behavior;
- human-facing AI/system critics benefit from a short demonstrable Workshop story;
- engine/developer-experience reviewers become more useful once the graphical vertical slice is interactive;
- provenance/interaction-design reviewers become more useful once those concepts have visible representation.

**Context:**  
The readiness question repeatedly changed depending on which outreach target was under discussion.

**State in conversation:**  
favored

**Preserve especially:**  
There may be no single “ready for outreach” state. Readiness is perspective-specific and should be tied to the thing the reviewer is being asked to attack.

## Consolidation notes

- The conversation began partly from a future amplification/networking goal, but the near-term strategy clearly shifted toward criticism-first outreach. The later promotional possibility was not rejected; it was deferred and subordinated to genuine technical relationships.
- “Workshop is now a real consumer worth mentioning” and “wait for SDL input before some outreach” are not contradictions. Workshop is already useful evidence for technical/malleability reviewers, while the SDL-input milestone was favored for reviewers who need a compact human-facing demonstration.
- Windows/MSVC portability and Linux containment should remain separate concepts. The former strengthens package/consumer credibility; it does not imply equivalent security guarantees on Windows.
- The C++26 reflection discussion and Zen's runtime identity/provenance model are closely related but should not yet be merged. Reflection was explored as a source of metadata/authoring relief, explicitly not as a replacement for Zen-owned identity or authority.
- The “malleable software” question, the “same living thing” representation thesis, and authored-intent-versus-resolved-state distinction are closely related, but each captures a different pressure and should remain separate until later consolidation.
- The ordinary-user falsification idea was favored but not acted on in this conversation.
- The small outreach kit and authority-map artifacts were explored but not created here.
- House of El, Mark S. Miller, The Cherno, Maggie Appleton, Casey Muratori, Jon Gjengset, Andreas Kling, and other candidate reviewers remain opportunities rather than accepted commitments.
- Specific named reviewers and their timing may or may not rise to durable strategic significance; the durable underlying idea is to seek intentionally different falsification perspectives at the point when each can evaluate something real.


# Raw Delta Capture — 2026-08-08 — HIST-1 onward: provenance, Input, and persistence

## Repository provenance must be mechanically witnessed, not merely instructed

**Raw:**  
The repeated accidental Claude `Co-authored-by` waves showed that “do not add AI co-authorship” is not reliable as a standing instruction alone. All first-party Zen repositories were rewritten to remove AI co-authorship while preserving their actual trees, and each now owns a trailer-aware repository check that rejects AI assistants as co-authors while allowing legitimate human co-authors and ordinary prose mentioning AI.

**Context:**  
A second large attribution wave was discovered in Loom after several phases had already reviewed the code and reports without noticing the provenance problem. HIST-1 repaired Loom, and HIST-2 normalized Zengine, zen-night-lab, and zen-arena.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
The lesson is not merely “remove Claude trailers.” A governance rule that matters enough to enforce should not depend exclusively on executors remembering it. Also preserve the distinction that the guard examines actual Git trailers and their values, not text matching.

## Repository-local enforcement over shared governance machinery

**Raw:**  
The same attribution invariant is owned independently by Loom, Zengine, zen-night-lab, and zen-arena rather than through a shared provenance service. The load-bearing predicate is standardized, while repository-specific details such as licensing headers, workflow shape, and explanatory prose follow each repository's own truth.

**Context:**  
HIST-2 ported the HIST-1 guard to three structurally different repositories. Night Lab has no LICENSE or root build, Arena has different CMake conventions, and Zengine already had substantial CI.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
“Standardize the law, not incidental spelling.” One invariant does not require one centralized implementation surface or pretending the repositories are structurally identical.

## CI attribution guards detect direct-push violations; they do not prevent them

**Raw:**  
The new repository guards genuinely prevent a bad attribution from merging through a PR only if the check is required. Under the current direct-push workflow, hosted CI runs after the commit has landed, so the guard provides loud detection rather than prevention. True prevention would require founder-side branch protection/ruleset changes and a PR-based workflow.

**Context:**  
Both HIST-1 and HIST-2 explicitly measured the boundary of what repository-owned CI can guarantee.

**State in conversation:**  
unresolved

**Preserve especially:**  
Do not allow future prose to collapse “guarded” into “cannot happen.” The current repositories mechanically detect the violation; direct-push prevention is a separate workflow decision that was deliberately deferred.

## History repair should preserve trees, identity evidence, and archaeology

**Raw:**  
The preferred provenance-repair technique that emerged from HIST-1/HIST-2 is commit-object reconstruction over the original tree objects, preserving authors, committers, dates, legitimate messages, and commit transitions while removing only offending attribution trailers. Old histories are archived in verified Git bundles with old→new mappings before rewritten identities are allowed to disappear.

**Context:**  
The affected ranges were linear, allowing `git commit-tree` replay without applying patches or touching working-tree files. Multiple exact-SHA canaries and identical final tree objects made the claim stronger than ordinary “same diff” evidence.

**State in conversation:**  
favored

**Preserve especially:**  
For metadata-only history repair, same-tree proof is stronger than replaying patches successfully. Preserve historical report SHAs as historical truth rather than rewriting old reports to modern equivalent SHAs.

## Installed-package identity is evidence that must itself be proven

**Raw:**  
A clean source repository and a path named `_install` do not establish what package a consumer is actually building against. W-4 discovered Loom's installed prefix was still from an older era despite current Loom being clean. Stranger-build phases should prove installed-prefix provenance or create a fresh prefix.

**Context:**  
W-4 found `Loom/build/_install/include/zen/registry.hpp` did not match current committed Loom. The prefix was rebuilt and all installed headers checked against HEAD before Zengine evidence was accepted.

**State in conversation:**  
favored

**Preserve especially:**  
“A path to an install prefix is not evidence of its identity.” This is a general verification lesson, not just a one-off W-4 cleanup.

## Mutation evidence needs provenance too

**Raw:**  
W-4's mutation harness exposed new false-evidence modes: a mutation command can fail to change the intended source, a binary can fail to rebuild, or an apparent result can come from an earlier run rather than the run being cited. Mutation discipline should prove all three before interpreting behavioral output.

**Context:**  
`perl -i` failed destructively on drvfs, and a background WSL invocation later appeared to have rerun when it had actually left the previous log untouched. The harness correctly refused to call these behavioral results.

**State in conversation:**  
favored

**Preserve especially:**  
A valid mutation witness now requires: the intended source bytes actually changed; the relevant binary actually rebuilt; and the evidence artifact actually came from the claimed run. A build failure remains not behavioral evidence.

## Input should preserve what the backend already knew instead of reconstructing it later

**Raw:**  
W-4 reframed the Input problem from “design richer events” to “stop discarding facts.” A fact belongs in an input message when the backend states it as part of that event moment; facts that require asking other mutable state later should not be reconstructed by consumers.

**Context:**  
Win32 mouse records already carried position and modifiers; SGR mouse reports carried coordinates and modifier bits; terminal/console keyboard handling already knew produced text. The old wire threw those facts away, producing three separate Workshop workarounds.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
The compact test: “a fact belongs in the message if the backend states it, and does not if the backend would have to be asked.”

## Input reports coherent moments; applications interpret gestures

**Raw:**  
Input now carries coherent key, text, pointer-button, pointer-motion, and pointer-wheel facts without learning application gestures. Dragging, moving, resizing, hit priority, clamping, and selection remain application meanings because they require knowledge of what is on screen.

**Context:**  
Workshop's real move/resize gestures became simpler once pointer button events carried their own position and modifiers. No `DragStarted` or resize vocabulary was added to Input.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
“Input reports coherent MOMENTS. Applications interpret GESTURES.” Also preserve that coherence does not imply one giant universal event variant; different event populations carry different facts.

## Consumer reconstruction disappearing is stronger evidence than a shorter implementation

**Raw:**  
Three Workshop responsibilities vanished entirely once Input told the truth: the local key→character table, four unrelated resize keys, and cached pointer coordinates used to reconstruct click position. The vocabulary improvement was judged by responsibilities disappearing from the consumer rather than merely by code shortening.

**Context:**  
W-4 replaced character reconstruction with `TextEntered`, literal resize bindings with semantic modifiers, and last-motion click reconstruction with event-time pointer positions.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
A strong sign that a lower-level vocabulary has found the right boundary is that a consumer responsibility turns out not to belong to the consumer at all.

## Entered text and physical keys are different truths

**Raw:**  
Text should be transported as text produced by the platform, separately from physical/logical key transitions. `%` must not be reconstructed as Shift+5; doing so encodes one keyboard layout and mistakes a chord for a character.

**Context:**  
The historical Input class had already separated text from keys, and W-4 adopted that idea after Workshop had repeatedly paid for its absence. `TextEntered` now carries actual committed UTF-8 text, while Backspace, Enter, Escape, and similar controls remain key events.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
A key may produce no text, and text may arrive with no key Zengine can honestly name. Neither should be forced into the other's population.

## Semantic modifiers survived archaeology; modifier inference must remain honest

**Raw:**  
Semantic Shift/Ctrl/Alt/Super state over physical keys was retained from the historical Input design, but only where the backend can honestly report or infer it. Terminal Shift on letters is partly inferred from resulting case and is therefore ambiguous with CapsLock; Shift on arbitrary symbols such as `%` is not claimed.

**Context:**  
W-4 removed `"Ctrl+C"`-style dressed key names and used explicit modifier bits. POSIX terminal limits made some modifier truths unavailable.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
Do not reintroduce keyboard-layout tables to manufacture modifier certainty. An honest backend limit is preferable to convenient fictional precision.

## Coordinate space belongs with pointer meaning

**Raw:**  
Pointer coordinates now carry an explicit coordinate-space discriminator rather than relying on consumers to know what backend supplied the number. Cells are current reality; Pixels is reserved so a future graphical backend cannot silently change the meaning of existing numeric coordinates.

**Context:**  
Win32 console and terminal SGR both currently produce cell coordinates. Workshop refuses coordinate spaces it does not understand rather than assuming its own.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
“Whatever unit this backend happens to use” is another form of discarded truth. `space::kPixels` being currently unused does not itself justify building an SDL input backend.

## Do not build a consumer merely to validate an abstraction

**Raw:**  
After W-4, the report recommended an SDL Input Reader partly to exercise `space::kPixels`. That direction was explicitly declined in favor of persistence because no live Zen application currently asks for SDL input. An unused semantic branch is allowed to remain unproven until a real consumer pressures it.

**Context:**  
The SDL reader would have validated the new Input vocabulary against a pixel backend, but doing so would primarily have served the abstraction rather than current maker friction.

**State in conversation:**  
explicitly rejected

**Preserve especially:**  
The application gets a vote. Do not invent a consumer to complete an abstraction's test matrix when a real application is asking for something else.

## Terminal Input is an incremental stream, not a sequence of read-sized events

**Raw:**  
Terminal escape/input parsing must survive arbitrary OS read boundaries. A read boundary is not an event boundary. Incomplete sequences require retained parser state, and malformed/overlong sequences require explicit resynchronization so their tails cannot leak back into ordinary input.

**Context:**  
A split SGR report could previously become Escape, `[`, and digits; `[` was itself a live Workshop binding. W-4 introduced `TerminalParser` and found an additional overlong-sequence tail-leak defect through mutation.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
Incremental parsing was required to prevent one input vocabulary from accidentally activating another. Resynchronization must occur at a real sequence boundary, not merely when a buffer limit is hit.

## Existing cadence can sometimes resolve ambiguity without new timing machinery

**Raw:**  
The terminal's lone-ESC ambiguity was solved using Input's existing 10ms pump cadence rather than introducing a dedicated timeout subsystem. A pending exact ESC is emitted only when a subsequent poll reads nothing; incomplete CSI remains pending.

**Context:**  
ESC is both a standalone key and the introducer for terminal control sequences. The package already had a clock-like polling boundary.

**State in conversation:**  
favored

**Preserve especially:**  
Before inventing a new timing abstraction, check whether an existing authoritative cadence already supplies the distinction the boundary needs.

## Terminal pointer mode belongs to the terminal presentation lifetime

**Raw:**  
The TUI Skin owns enabling/disabling terminal pointer reporting because mouse reporting is requested in-band on the terminal output stream and naturally shares the Skin's alternate-screen/cursor lifetime. Input parses reports but does not need a coordination channel with Surface.

**Context:**  
W-4 chose SGR + button-event tracking (1002/1006) and made the Skin's enter/leave sequences observable and testable.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
The minimum ownership answer was the component already controlling the resource lifetime. No generic terminal-session framework or Input↔Surface coordination surface was needed.

## Uncatchable process death leaves terminal modes behind

**Raw:**  
RAII cannot restore alternate-screen or pointer-reporting modes after an uncatchable termination such as SIGKILL. Pointer reporting widens the visible consequence: the shell may emit escape sequences on mouse movement until reset.

**Context:**  
W-4 added mouse mode to the TUI Skin lifecycle and explicitly declined to pretend normal teardown covers hard death.

**State in conversation:**  
explored

**Preserve especially:**  
This is a host-policy/system-lifecycle seam, not an Input defect. Do not quietly promote normal teardown evidence into a crash-restoration guarantee.

## Input capability discovery is latent until a backend genuinely lacks a modality

**Raw:**  
No general Input capability query was added. Every currently supported meaningful configuration has the modalities its visible application needs, so a query would currently return constants. Capability discovery should wake when a real backend lacks text, pointer, or another modality while remaining otherwise usable.

**Context:**  
W-4 explicitly considered and declined a capability surface, naming headless/pipe hosts or a future SDL reader as possible triggers.

**State in conversation:**  
tentatively accepted

**Preserve especially:**  
A framework for capabilities should not be built while its answers cannot vary.

## WorkshopWeave became test-reachable because composition pressure finally earned it

**Raw:**  
`WorkshopWeave` moved into a test-reachable header only when W-4 substantially changed message composition and needed end-to-end evidence from Input message → real weave handler → real semantic document operation. No test hook or framework was added.

**Context:**  
P16 had remained parked through earlier phases because source relocation was not yet necessary. W-4 made the unreachable composition boundary directly relevant to its central claim.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
Testability refactors should be pulled by a claim the suite cannot otherwise observe, not by generic preference for exposing internals.

## Persistence became the next maker-pressure phase

**Raw:**  
After W-4, persistence was chosen over SDL Input and clipping as the next Workshop slice because Workshop now behaves enough like a maker tool that losing authored work at process exit is the clearest missing behavior.

**Context:**  
Workshop can now create, name, select, edit canonical authored text, move, resize, pointer-manipulate, inspect, and delete. The next meaningful maker consequence is that none of it survives process death.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
Persistence is being pulled by product friction, not roadmap ordering: “closing it and losing the work is now the obvious missing behavior.”

## Persistence should preserve authored truth, not resolved observation

**Raw:**  
The favored W-5 direction is to save the Workshop document's authored state and reconstruct resolved geometry on load. Scene/Rect/resolved extents, hit state, resize handles, editor drafts, active gestures, and other session/derived state should not silently become a second persisted source of truth.

**Context:**  
The accumulated W-1/W-3 doctrine now makes persistence an architectural pressure test: semantic `Cells` vs `Percent`, authored vs resolved, and property value vs editor draft already exist.

**State in conversation:**  
favored

**Preserve especially:**  
“Save authored truth, not the evidence derived from it.” A strong witness is loading the same persisted Percent extent under a different viewport and seeing the authored amount remain constant while resolved geometry changes.

## Workshop identity should exist across process death

**Raw:**  
Persistence raises a stronger identity requirement than serialization alone: object IDs must survive save/reload as the same document identities, and the document's identity mint must not rewind. If the highest-created ID was deleted before save, reload must not allow that ID to be silently reused.

**Context:**  
W-2 established that IDs are identities rather than slot numbers and that deleted IDs are not recycled during a process. W-5 is intended to test whether that law survives time.

**State in conversation:**  
favored

**Preserve especially:**  
The canonical witness: create `#1`, `#2`, `#3`; delete `#3`; save; process dies; reload; next object must be `#4`, not `#3`. If this holds, Workshop identity genuinely exists over time.

## Persistence loading should be transactional

**Raw:**  
A candidate persisted document should be fully read, parsed, validated, and constructed before replacing live document truth. A malformed or unsupported save must leave the current committed document unchanged rather than producing a half-loaded state.

**Context:**  
W-5 extends the same refusal doctrine already used by property editing: invalid proposals do not partially mutate committed truth.

**State in conversation:**  
favored

**Preserve especially:**  
Persistence should inherit the established semantic law: refusal leaves committed truth unchanged.

## Persistence format versioning is identity before it is migration machinery

**Raw:**  
A Workshop file may identify itself and carry a format version from the first real version, but this does not justify migration registries, compatibility graphs, legacy adapters, or generalized schema evolution. Those should wake only when a second real format must consume an existing v1 document.

**Context:**  
W-5 needs to distinguish malformed/wrong/unsupported documents without claiming permanent format stability.

**State in conversation:**  
favored

**Preserve especially:**  
“One version today” permits explicit format identity but does not create a compatibility obligation that has not yet existed.

## Save should observe committed truth, not silently commit editor drafts

**Raw:**  
An uncommitted property draft and the committed document property remain distinct during persistence. Save should not silently reinterpret an invalid or unfinished editor draft as committed authored state merely because persistence was invoked.

**Context:**  
W-0 established the draft/property separation; W-5 forces a product decision about what Save means while editing.

**State in conversation:**  
unresolved

**Preserve especially:**  
The plausible policies remain open: save committed truth while visibly leaving the draft unsaved, or refuse save until the draft is committed/cancelled. Auto-commit was not favored by default.

## Safe save should protect the last known good artifact from ordinary failure

**Raw:**  
A detected write failure should not knowingly truncate or half-write the existing valid save. The favored minimum is serialize completely, write a sibling temporary artifact, and replace only after successful write, while avoiding stronger crash-durability claims the platform cannot support.

**Context:**  
W-5 treats persistence files as external durable maker work rather than throwaway test data.

**State in conversation:**  
favored

**Preserve especially:**  
The promise is deliberately narrower than “crash-proof atomic save”: ordinary detected failure should not destroy the previous good document.

## Persistence remains Workshop-local until another consumer earns promotion

**Raw:**  
Document snapshots/codecs/safe-write helpers should begin as Workshop application material rather than immediately becoming generic Zengine serialization vocabulary. Reusability by appearance alone is not enough to promote a concept.

**Context:**  
W-5 could easily drift into a universal scene format, reflection system, schema registry, or generic serialization framework.

**State in conversation:**  
favored

**Preserve especially:**  
Application pressure must earn package concepts. Workshop saving a rectangle does not itself justify a Zen-wide persistence architecture.

## Workspace clipping remains real but behind persistence

**Raw:**  
Pointer interaction made P17 easier to hit: objects can overdraw Workshop's own panel when dragged beyond the workspace. The issue remains real, but solving it requires deciding what the workspace is—clip region, viewport, scrolling region, etc.—and was ranked behind persistence.

**Context:**  
W-4's live pointer manipulation makes boundary overdraw much easier to reproduce than keyboard movement did.

**State in conversation:**  
explored

**Preserve especially:**  
The issue did not disappear; its sequencing changed because persistence has a clearer immediate maker consequence.

## Consolidation notes

- The SDL Input Reader idea was recommended by the W-4 executor but explicitly rejected as the next phase because it would primarily validate `space::kPixels` without a live pixel-input consumer. Preserve both the recommendation and its later rejection rather than smoothing them into “SDL Input planned.”
- Repository attribution guards are explicitly accepted, while branch-protection/PR-only workflow remains unresolved. Do not merge “guarded” and “prevented.”
- Input capability discovery (P18), terminal non-letter Shift truth (P19), and hard-kill terminal restoration (P20) are related Input/backend seams but should remain distinct; they have different triggers and different ownership.
- Persistence direction is favored/accepted as the next Workshop pressure, but several detailed W-5 policy questions remain unresolved until executor evidence: dirty-draft save behavior, unknown-field handling, exact path/shortcut UX, and possibly object-order semantics.
- Persistence identity, authored-vs-resolved persistence, transactional load, and safe-save behavior are closely related but should not yet be collapsed into one generic “persistence doctrine”; each was surfaced by a different existing Zen law.
- Installed-prefix provenance and mutation-artifact provenance are closely related verification lessons: both say an apparently named artifact is not evidence of the identity/history that produced it. They may later consolidate into a broader evidence-provenance principle, but that synthesis was not explicitly made in the conversation.
- HIST-1/HIST-2 history-repair technique appears strategically reusable, but it arose from a specific linear-history situation. Do not promote `commit-tree` replay into a universal history-repair law for merge-heavy histories without new evidence.

---

# Raw Delta Capture — 2026-08-08 — Workshop W0 grounding review and closeout

## W0 survived application pressure by naming assumptions rather than adding privilege

**Raw:**  
Cold-Z0 reconstructed W0 as one experiment over authored truth versus observation. Across W-1, W-3, W-5, and W-6 the authored/resolved distinction survived ownership pressure, direct manipulation, process death, and composition without a second model or Workshop-only privilege. W-6's frame/context result made composition possible by naming what resolution had already consumed rather than by imposing a parent/child ontology.

**Context:**  
Cold-Z0 independently audited W-0 through W-6 after the first SDL Workshop and the MSVC package work. Z0a then closed the two maker-facing W0 honesty gaps Cold-Z0 found.

**State in conversation:**  
accepted

**Preserve especially:**  
The strongest W0 evidence is not that rectangles work. It is that the same distinctions kept surviving new kinds of pressure without becoming special cases.

---

## Document, session, and derived state remained a durable boundary

**Raw:**  
W-5 drew the persistence boundary and moved zero existing facts between document, session, and derived state. W-6 added one authored context reference and one new derived question without moving an existing fact. The boundary survived both process death and composition.

**Context:**  
Persistence and composition were the two W0 phases most likely to expose a mistaken state boundary.

**State in conversation:**  
accepted

**Preserve especially:**  
A persisted artifact, the state of one editing session, and the current observation of that artifact are different kinds of truth. Do not make a view durable merely because it is convenient to cache, and do not make session state part of an artifact merely because the UI currently needs it.

---

## A pressure ledger must be durable authority, not report-local recitation

**Raw:**  
Cold-Z0 found that phase reports were individually careful but the project had no durable authority for pressure dispositions. P8 and P9 fell out after W-2 without closing; P-MSVC findings lived only in report prose; W-6's pressure count was wrong; Cold-Z0's own reconstructed ledger also misclassified several earlier pressures and contained new arithmetic drift. Z0a then found two more pressure/test-quality sightings while closing P24/P26.

**Context:**  
W0 item 10 explicitly required a precise seam/pressure ledger. The code half of W0 was complete after Z0a, but governance closure depended on establishing an authority that does not require every phase to repeat every old item by hand.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
Observed pressure is not the same thing as work owed. It needs a durable home where CLOSED, WATCH, ACT, LATENT, ROUTED, and superseded entries remain recoverable without turning every observation into backlog.

---

## The TUI is Workshop's reference surface, not its presentation authority

**Raw:**  
Cold-Z0 found that Workshop's fixed TUI composition was an excellent W0 scaffold and an unusually strong reference/test surface, but it had also supplied typography, grid, clipping, spacing, and visual hierarchy for free. The first SDL rendering removed that inherited environment and exposed what Workshop had never explicitly authored. Z0a strengthened the TUI's truthfulness while deliberately refusing to make the fixed 78x22 grid the future product layout.

**Context:**  
The TUI remains the only complete, golden-string-comparable, live-witnessable Workshop surface. The SDL skin currently renders rectangles but drops labels because it has no font stack.

**State in conversation:**  
accepted

**Preserve especially:**  
Keep the TUI as a reference/control surface. Do not let its fixed grid continue deciding what Workshop must look like on every presentation backend.

---

## Presentation capability must precede presentation policy

**Raw:**  
The first SDL Workshop initially looked like a styling problem. Cold-Z0 source-traced the dominant failure to P8: `SdlMedium::canvas()` drops every `SurfaceLabel` because the medium has no font stack. A graphical Workshop therefore cannot show object names, properties, refusals, help, or Z0a's new omission markers. A font is capability, not polish. Once the surface is readable and interactive, actual maker pressure can decide presentation policy.

**Context:**  
The first graphical Workshop rendered recognizable rectangles and selection with no Workshop drawing-path rewrite, but could not be read or interacted with.

**State in conversation:**  
accepted

**Preserve especially:**  
Do not style a screenshot before the surface can carry the product's existing meaning. Presentation policy should be authored from use; presentation capability is a prerequisite for that use.

---

## SDL Input is now earned application pressure

**Raw:**  
W-4 deliberately left `space::kPixels` without a producer as an independent future validation. The first SDL Workshop changed that status: Workshop now has a graphical presentation a maker can see but cannot touch. SDL already states physical key, entered text, modifiers, pointer motion, and event-time button position directly, so the next question is whether it can feed the same truthful Input vocabulary rather than whether Input needs redesign.

**Context:**  
Cold-Z0 separated window lifecycle from Input vocabulary while recommending that a native close event can ship in the same bounded event-pump slice as a minimal end-to-end witness.

**State in conversation:**  
accepted

**Preserve especially:**  
The backend should produce the same truthful moments where the facts are the same. Do not make SDL a reason to reopen W-4's gesture architecture.

---

## The root frame's relationship to the presentation surface is still unowned

**Raw:**  
W-6 named `root_frame(Viewport)`. Workshop currently authors a logical canvas/workspace while each skin owns its presentation medium. No layer yet owns the relationship between logical workspace and physical surface. The first SDL screenshot did *not* prove a scaling mismatch—the SDL window is currently sized from the canvas and the apparent empty region was largely missing labels—but the ownership question remains real once a graphical surface becomes resizable or otherwise independent.

**Context:**  
Cold-Z0 corrected the original screenshot inference while preserving the architectural question separately.

**State in conversation:**  
unresolved

**Preserve especially:**  
Do not silently stretch to fit. Wait for graphical interaction to produce evidence about whether Workshop expects a responsive logical workspace, fixed authored workspace, pixel root, or an explicit surface-to-root relationship.

---

## P18's capability-query trigger fired

**Raw:**  
Z0a made Workshop canvas notices visibly truncate because Workshop owns the canvas width. The same live run used a long document path and showed the status `SurfaceText` slot silently clipping at the terminal edge. Workshop cannot fix that locally because slot width is private to the Skin and there is no way for a consumer to ask what presentation context/capability it is authoring into.

**Context:**  
P18 had remained latent because every supported configuration made the relevant capability effectively constant. Z0a produced the first live symptom where a consumer lacks enough backend-owned truth to present honestly.

**State in conversation:**  
accepted pressure; mechanism undecided

**Preserve especially:**  
The pressure is not “add get_screen_width().” The pressure is that a consumer sometimes needs truthful knowledge about the presentation context it is being asked to author into. Let more backend pressure shape the answer.

---

## W0 closes as grounding, not as Workshop product completion

**Raw:**  
After Z0a closed P24 and P26 and founder consolidation established durable pressure authority, W0's completion shape is satisfied. W0 proves that an ordinary Zengine application can create/load/display/select/move/resize/inspect/edit/compose/persist/reload authored visual objects with truthful refusals and no Workshop privilege. It does not prove general app authoring, live binding, code integration, source editing, graphical product presentation, or later W1-W9 horizons.

**Context:**  
Cold-Z0 explicitly distinguished W0 thesis validation from later Workshop sophistication.

**State in conversation:**  
accepted

**Preserve especially:**  
Close W0 rather than leaving it permanently “almost complete.” Its remaining pressures become inputs to the next evidence-driven slice; they do not retroactively expand the grounding contract.

---

# Raw Delta Capture — 2026-08-10 — Graphical hands, live delegation, and the user's seat

## Readable and touchable presentations should preserve one application meaning

**Raw:**  
G-0 and G-1 made the SDL Workshop readable and interactive without adding an SDL-specific Workshop interaction model. Labels, keyboard/text, pointer movement, selection, drag, resize, save, and native close all reached the existing Surface/Input/Workshop semantics. The TUI remains the reference lane; SDL is now a real maker lane.

**Context:**  
The graphical grounding slices followed W0 closure. G-0 flattened labels and rectangles into one SDL plan; G-1 connected SDL's real event queue to the existing Input moment model and kept native close as lifecycle truth.

**State in conversation:**  
accepted

**Preserve especially:**  
A second presentation should not create a second application model merely because its native events and rasterization differ.

---

## Native witness and Zen-driven witness are different evidence tiers

**Raw:**  
G-1's strongest native proof used real OS input because the SDL reader itself was under test. That same proof revealed an undesirable verification privilege: routine application interaction should not require an executor to control the whole desktop once the native backend is already proven. A later Zen Input Driver may drive ordinary Input moments through Loom, but it must remain weaker evidence than a native OS→reader witness when the reader is the subject.

**Context:**  
The executor visibly moved the founder's real mouse/keyboard during G-1. That prompted the synthetic Input Driver idea and, in turn, the need for a user-owned authority seat.

**State in conversation:**  
accepted distinction; implementation deferred

**Preserve especially:**  
Do not replace native-backend evidence with synthetic injection. Use Zen-driven interaction for routine application proof and native interaction when the native reader itself is under test.

---

## The Kernel enforces; the Weaver decides; the Session acts

**Raw:**  
WEAVER-0, GRANT-0, and WEAVER-1 established a four-party authority model. The host/user bootstraps a policy delegate; the Weaver decides and changes real delegated LiveAuthority; the governed Session retries and remains the bus-stamped author; the Switchboard enforces effective authority at delivery. The Weaver does not need to broker the Session's work.

**Context:**  
WEAVER-0 found Loom already deny-by-default for in-process speech and found the missing seam: live post-mount authority administration. GRANT-0 added a subject-scoped, ceiling-scoped capability over dynamically enforceable message/observation authority. WEAVER-1 used it through ordinary Loom messages and the existing Console.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
> The Kernel enforces. The Weaver decides. The Session acts.

User policy should not require the policy delegate to become the author of the user's work.

---

## Admission authority and delegated live authority are different truth classes

**Raw:**  
GRANT-0 kept the host's admission `Grant` immutable and added a mutable delegated `LiveAuthority` overlay. Effective speech/observation is the union. Network, filesystem, process-spawn, and resource-limit authority remain admission-time because their isolation mechanisms are spent into namespaces/mount views/cgroups at spawn and are not re-read from Switchboard memory.

**Context:**  
The first design question was whether to make `Grant` mutable. Source pressure showed that such an API would falsely imply live OS authority. The type split instead makes unsupported live escalation unspellable.

**State in conversation:**  
accepted

**Preserve especially:**  
What the host admitted a subject with and what the user later entrusted it with are both real and should remain distinguishable.

---

## Presentation and authority-holder can be separate

**Raw:**  
WEAVER-0 established that Workshop may present a terminal while a distinct session weave actually holds the delegated authority and sends messages under its own identity. WEAVER-1 then proved the operator path using ordinary messages. A future `LoomTerminalSession` should therefore be one semantic participant with multiple presentations: standalone console first, Workshop pane second, executor/script surface later.

**Context:**  
This grew from the desire to make the Loom console/terminal a powerhouse and embed the same capability into Workshop rather than create separate console, Workshop-console, and executor protocols.

**State in conversation:**  
explicitly favored

**Preserve especially:**  
A UI displaying a powerful session must not inherit the session's authority merely because it renders the controls.

---

## Authority correctness and human authority legibility are separate requirements

**Raw:**  
Loom can enforce the correct authority even when the human cannot yet see all relevant authority changes. WEAVER-1's operator sees the policy workflow it participates in, but changes made by another administration capability are not emitted as traffic; whole-bus observation remains host-only. Machine-correct authority is necessary but does not by itself make authority legible to the user.

**Context:**  
P38 survived GRANT-0 and WEAVER-1. Sense observation, delivery tap observation, and authority-change notification are distinct domains.

**State in conversation:**  
accepted distinction; interface mechanism unresolved

**Preserve especially:**  
Do not solve human legibility by weakening authority boundaries or by giving every terminal an omniscient tap.

---

## The operator seat authenticates a Loom participant, not yet a person

**Raw:**  
WEAVER-1 names the operator seat by trusted `WeaveId`. That proves policy authorization after an operator identity exists; it does not authenticate which human is behind that participant. An external terminal, Bridge authentication, and person/session identity meet at the same later seam.

**Context:**  
The current Bridge is process-external but full unauthenticated operator authority for any reachable connection. WEAVER-1 is intentionally same-process.

**State in conversation:**  
accepted limitation

**Preserve especially:**  
Do not describe current Weaver policy as human authentication. It is trusted Loom-participant authorization.

---

## A policy delegate can die while its delegated authority survives

**Raw:**  
GRANT-0 deliberately made administration capabilities authorizers, not leases. WEAVER-1 proved the consequence: if the Weaver dies after granting, the Session's delegated authority remains, while the ordinary user-facing revocation path through that Weaver disappears. Session death still removes the authority with the subject.

**Context:**  
Possible answers include supervision, session-lifetime coupling, leases, or host emergency revocation, but no consumer has yet earned one.

**State in conversation:**  
accepted pressure; mechanism unresolved

**Preserve especially:**  
Do not quietly turn capability lifetime into authority lifetime. The lifecycle policy should be chosen with a real long-lived TerminalSession in the room.

---

## Source-first acceptance review is part of evidence discipline

**Raw:**  
Founder review had drifted toward treating report-backs as if they were the implementation. Before WEAVER-1, the source-first habit was explicitly restored: read the landed source, load-bearing tests, and current laws before accepting a report's architectural claims. WEAVER-1 independently reread GRANT-0 and found only stale report line numbers, not behavioral discrepancies.

**Context:**  
Public GitHub blobs were temporarily stale/unavailable for independent founder browsing, making the distinction especially visible.

**State in conversation:**  
explicitly accepted process correction

**Preserve especially:**  
Reports are evidence and history. Source/tests say what exists. Acceptance should compare them rather than collapse them.

---

# Raw Delta Capture — 2026-08-16 — Vision stewardship and executor collaboration

## Ceecee executes; Vision reviews and stewards; the founder accepts

**Raw:**  
The founder selected a durable collaboration split for Zen. Ceecee remains the primary code
executor. Vision acts as the manager of private strategic continuity: reviewing report-backs
against current source and tests, recommending disposition, and—after founder acceptance—updating
the current Goal Map, Vision Delta authorities, handoff context, and accepted repository board.
Vision is not a second routine code executor. A narrow exception exists for small cleanup found
during report-back review.

**Context:**  
This was agreed while WP-R0 was running, after first-contact orientation exposed that the private
strategy and accepted repository board can lag legitimate live work. The goal is to keep the
executor focused on implementation while giving accepted evidence a deliberate custodian.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
Implementation, acceptance, and consolidation are separate acts. Ceecee produces code and
evidence; Vision performs source-first review and private-document stewardship; the founder
retains the acceptance decision.

---

## A report landing does not make its conclusions authority

**Raw:**  
When a report-back arrives, Vision should inspect the phase prompt, report, landed source,
load-bearing tests, exact Git identities, upstream relationship, and working-tree ownership before
recommending acceptance. Executor recommendations remain evidence rather than roadmap authority.
After acceptance, Vision records what was proven, what remains unproven, current pressure, and the
next authorized question in the smallest correct private documents.

Research may change strategy without moving a repository. Conversely, an uncommitted working tree
cannot become an accepted repository identity merely because its report is persuasive. The root
board moves only to an exact committed identity that the founder accepted after review.

**Context:**  
This extends the already accepted source-first review discipline into a complete handoff and
consolidation loop.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
A report is the beginning of acceptance review, not the end of it. Accepted repository identity,
live working-tree state, and strategic interpretation must remain distinguishable.

---

## Vision cleanup during review stays mechanically bounded

**Raw:**  
Vision may repair a small issue discovered during report-back review when the change is localized,
mechanical, and does not alter behavior, schemas, ABI, authority, persistence, interaction,
layout law, or public API. Examples include a documentation correction, a stale measured fact, or
a narrowly incorrect test census. Anything that makes a product or architectural decision returns
to Ceecee as executor work.

**Context:**  
The exception exists to avoid manufacturing a new execution phase for trivial review fallout
without allowing the strategy steward to drift into shadow implementation.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
The cleanup exception is a boundary, not an alternate implementation lane. If reasonable reviewers
could disagree about behavior or architecture, it is executor work.

---

# Raw Delta Capture — 2026-08-16 — WP-R0 provider/pane boundary and saved setups

## Saved setups should name pane intent, not today's catalog ordinal

**Raw:**  
WP-R0 found that named/saved Workshop setups can begin without first implementing external panes,
provided their durable pane reference does not fossilize `panel::k*`. The accepted starting shape is
a neutral two-part reference — provider/service key plus pane key — with current built-ins expressible
as readable names such as `zengine.workshop/info` and `zengine.workshop/builder`.

**Context:**  
The phase ran before WS-0 specifically because today's catalog uses dense compile-time integers and
its total lookup falls back to Builder. Persisting either behavior would make an absent future pane
unrepresentable or, worse, silently misname it.

**State in conversation:**  
explicitly accepted after source-first review, with corrections

**Preserve especially:**  
Persist authored pane intent. Resolve it fallibly at the runtime boundary. Never turn an unresolved
reference into a different built-in merely to keep lookup total.

---

## A pane presentation is not a provider lifetime or authority boundary

**Raw:**  
Info and Builder now provide application-scale evidence that `panel != weave`: Info is a pane with
no weave, while Builder's provider continues independently of opening and closing its presentation.
Workshop therefore continues to own placement, bounds, composition, occupancy, and the one complete
Surface canvas. A future provider supplies semantic content inside a budget Workshop grants; it does
not gain screen placement or ambient authority by becoming visible.

**Context:**  
HD-10 had already established that Workshop grants room and owns spatial conflicts. WP-R0 tested
whether an external provider could fit that law without a compositor, plugin framework, or
provider-owned window coordinates.

**State in conversation:**  
explicitly accepted

**Preserve especially:**  
Closing a pane destroys a presentation copy, not the provider. Visibility grants no filesystem,
process, network, project-write, arbitrary-message, or global-canvas authority.

---

## Live service provenance and durable author identity remain different questions

**Raw:**  
A Loom role is the correct reload/replacement-stable service route for a trusted composition, but it
is not package or author identity. Provider announcements and content must be deliberately
office-authored and checked through Loom's stamped provenance; a `provider` string inside the
payload is forgeable data and is not identity. Cross-restart author trust remains the existing
weaver-identity trigger rather than being silently declared solved by saved setups.

**Context:**  
WP-R0 proposed carrying the provider role in `PaneOffered`. Source-first review found Loom's
role-authorship ADR and `Mail::authored_role()` already provide the stronger, smaller answer.

**State in conversation:**  
accepted correction to the report

**Preserve especially:**  
Use the bus stamp for live office provenance. Keep a saved provider key neutral enough that WS-0
does not make a future marketplace/package-authentication promise by accident.

---

## Missing providers remain unresolved; silence is not absence

**Raw:**  
An authored setup may retain a pane reference while its target is absent, but ordinary Loom senders
do not observe eventual send fate. Until a domain acknowledgment, timeout, or suitable presence
query proves more, the honest state is `unresolved` or `waiting for provider`, not `provider
unavailable`. The entry stays and may resolve later without rewriting the saved setup.

**Context:**  
The report correctly found the sender-fate seam but then used stronger unavailable wording than the
evidence supports. The review narrowed the user-facing claim.

**State in conversation:**  
accepted correction to the report

**Preserve especially:**  
Do not manufacture absence from silence. Do not delete authored intent because its referent is not
currently resolved.

---

## Maker capability sequencing wins: WS-0 before WP-0

**Raw:**  
The founder accepted the sequence `WS-0 first with external-safe identity; WP-0 second`. WS-0 should
name, save, and restore the current useful setup without adding docking, authored panel geometry,
external providers, multiple instances, opaque provider configuration, or an extension framework.
WP-0 later proves one authenticated, bounded, read-only external pane against the identity shape
WS-0 established.

**Context:**  
WP-R0 compared architecture-first and maker-capability-first orderings after HD-10 recommended named
setups as the next useful Workshop movement.

**State in conversation:**  
explicitly accepted; WS-0 is the next authorized question

**Preserve especially:**  
External-safe does not mean external-now. Build the useful maker capability first while leaving the
future provider boundary honest and migration-safe.

---

# Raw Delta Capture — 2026-08-17 — Workshop panes become host-owned windows

## Persist the smallest authored layout intent; let code remain the default

**Raw:**  
Saved pane intent should carry the smallest information needed to represent the maker's override.
The proposed size vocabulary is a `size` plus a `size_type`, initially cells or pixels. A pane may
request a natural size in one of those units when asking for space, but it does not choose the room
it receives. A terminal-only medium may refuse pixels; a pixel-capable medium must know when the
intent it is presenting is cell-based.

Developer-authored layout remains ordinary reactive code: when available size crosses meaningful
thresholds, the layout changes. The host may grant only a fraction of what a pane asked for. The
pane draws against the simulated space it was granted and gains no additional room merely because
it attempted to use more. Clipping can be an honest presentation result.

**Context:**  
The accepted setup currently persists only ordered `PaneRef`s, while Workshop resolves two fixed
places. This conversation answers the direction of a future authored-window phase without selecting
an implementation packet or exact wire/schema spelling.

**State in conversation:**  
explicitly favored; exact request/grant schema and external drawing contract remain research

**Preserve especially:**  
Defaults are code. Saved data records the maker's authored override. The host owns the actual grant,
and the pane knows only the space it received.

---

## Panes may overlap only if every mounted pane remains recoverable

**Raw:**  
Treat pane presentations increasingly like windows in an operating system. Overlap is allowed.
Front/back ordering belongs in the pane-changing mode. A fully covered pane must never become
unrecoverable: the management surface should still list it and let the maker select, raise, lower,
move, or otherwise return to it. A warning-pane or notification-dropdown presentation is a possible
answer, not yet a selected mechanism.

The founder also live-tested overlapping selectable material and found the top item always wins a
press/drag even when another item is already highlighted. The desired counter-rule is to ask whether
the highlighted target contains the press before choosing another overlapping target.

**Context:**  
Current panel placement is fixed and current workspace object hit-testing is topmost-first. A future
window editor needs an explicit selected-target and z-order policy rather than inheriting whichever
loop happens to walk last.

**State in conversation:**  
overlap, recoverability, z-order control, and selected-target priority explicitly favored; exact
warning/notification presentation unresolved

**Preserve especially:**  
Overlap is not loss. A mounted pane must remain reachable through a management path even when no
part of its window is currently visible.

---

## TUI pane manipulation should be a tiered component state machine

**Raw:**  
TUI navigation should enter pane management deliberately rather than spending a gesture per
operation. A maker selects a pane, presses Enter to manage it, then enters movement or chooses an
edge/corner and uses arrows to move or resize. The exact interaction may evolve, but it should be
composed from reusable component state rather than a one-off chain of Workshop flags.

**Context:**  
Workshop has already spent the obvious unmodified command letters. Pointer and keyboard/TUI paths
should converge on the same semantic move/resize/z-order operations.

**State in conversation:**  
explicitly favored; exact key-state diagram unresolved

**Preserve especially:**  
The TUI is not a read-only fallback. It needs an honest path to the same authored window operations.

---

## Setup layout may move directly to version 2

**Raw:**  
The layout-bearing setup format may become version 2. There are no external setup consumers that
justify preserving version-1 compatibility. Do not spend design complexity on compatibility merely
because version 1 exists.

**Context:**  
Version 1 deliberately persists only setup name plus ordered `PaneRef`s. Authored position, size,
unit, z-order, and any future window identity would be a new schema rather than a reinterpretation
of the accepted bytes.

**State in conversation:**  
explicit founder direction

**Preserve especially:**  
No compatibility obligation does not mean silent reinterpretation. A version mismatch must remain
legible if old bytes are encountered.

---

## One PaneRef means one mounted pane until strong external pressure proves otherwise

**Raw:**  
A provider/weave may offer multiple distinct pane keys as a suite. That is different from mounting
several simultaneous presentations of the same `PaneRef`. For now, keep exactly one pane per
`PaneRef`.

If true same-definition multiplicity is ever earned, the mounted window's identity should receive
its own readable name: `PaneInstanceId`. Do not use that term for a pane definition, do not add the
identifier speculatively, and do not relax duplicate-`PaneRef` setup validity merely out of
generality. Revisit only under high external pressure that needs independent same-pane views.

**Context:**  
Current room/content routing, open presentation state, and setup reconciliation are all keyed once
per pane definition. True multiplicity would also require instance-specific lifecycle, room,
content, configuration, and persistence semantics.

**State in conversation:**  
explicitly accepted direction

**Preserve especially:**  
`PaneRef` identifies the pane definition and, under the current one-mounted-pane law, its sole
presentation. `PaneInstanceId` is reserved for a genuine later distinction, not today's schema.

---

## Keep accumulating documentation truth; reorganize the public surface closer to product maturity

**Raw:**  
Zengine will need a major documentation overhaul. A roughly 1,500-line README and public-facing
phase tags are poor documentation for readers outside the project's internal history. Do not purge
or compress information now. Keep adding useful truth while the product is moving, then reorganize
it later into a shorter reader-facing router, focused current guides/references, and retained
history with no information loss.

**Context:**  
WG-1 made the Workshop authoring paths current, but the broader repository documentation still
mixes current reference, rationale, and phase archaeology.

**State in conversation:**  
explicitly favored future posture; no documentation phase selected now

**Preserve especially:**  
Organize later; do not erase. Phase names belong in recoverable evidence/history, not in the final
reader's required vocabulary.

---

# Raw Delta Capture — 2026-08-17 — Hello can mature into a Workshop-dissectible template

## Preserve the simple example as something a maker can eventually open and learn from

**Raw:**  
The Hello pane does not need to be discarded merely because it began as a protocol witness. Its
simplicity is useful. Eventually it can become more like a project template: a small external-pane
example people can open, inspect, take apart, and modify from within Workshop.

**Context:**  
Hello currently lives as a test weave and proves the bounded read-only external-pane path. Workshop
does not yet have a public plugin SDK, installation story, project-template system, or the complete
self-hosting capability implied by “dig it apart within Workshop.”

**State in conversation:**  
explicitly favored future onboarding/product direction; no template conversion selected

**Routing:**  
Workshop Goal Map founder window direction; BL-WORKSHOP-01; WIND-0 as a compatibility witness only.
This extends the existing “Workshop and onboarding arise together” direction and does not require a
new parsed Vision Delta.

**Preserve especially:**  
Do not confuse “simple” with “throwaway.” Keep Hello understandable enough to become a real learning
artifact later, while remaining honest about the product machinery that does not exist today.

---

# Raw Delta Capture — 2026-08-17 — Corrected host-owned window research is accepted

## The first window implementation should spend only the contract the research actually earned

**Raw:**  
Accept WIND-0, WIND-0a, and WIND-0b as one corrected research sequence. The accepted answer keeps
developer defaults, maker overrides, host grants, and presentation projection distinct; uses a
bounded canonical pane order rather than operation history; prices pane bounds as both paint and
pointer ownership; and treats pixel sizing scale as only part of presentation context.

**Context:**  
WIND-0 mapped the system and proposed successors. Vision review found four contract defects, which
WIND-0a corrected. Its review found three narrower defects, which the hot WIND-0b continuation
corrected. Final review added a mechanically bounded report-only amendment: the omitted viable-list
trace, complete pixel-policy boundary tables, and the direct-Setup-construction caveat. Neither
production repository moved.

**State in conversation:**  
explicit founder acceptance

**Routing:**  
Workshop Goal Map acceptance capsule; Strategic Map current position; Pressure P50/P53; current
executor handoff; accepted repository board; parsed Vision Delta 2026-08-17-Z.

**Preserve especially:**  
WIND-1 is a separately selectable one-expression half-share width packet. WIND-2 remains the later
authored-window/schema/interaction packet. Acceptance of research authorizes neither automatically,
and it does not add provider input, arbitrary drawing, same-PaneRef multiplicity, or a compositor.

---

# Raw Delta Capture — 2026-08-17 — Responsive pane room is accepted without promoting authored windows

## A wider room is now shared by the pane and the maker

**Raw:**  
Accept WIND-1 after source-first review and a bounded comment/report correction. The overlay stack
keeps its 48-cell minimum width and takes the floored half of every wider workspace-room surplus.
The other half remains reachable workspace. The widened rectangle is one ownership fact for paint,
pointer occupancy, and external-pane room publication.

**Context:**  
The production change is the one expression earned by WIND-0/WIND-0a/WIND-0b research. Minimum
geometry, side reservation, vertical capacity, setup version 1, provider protocol, PaneRef identity,
public APIs, and Loom remain unchanged. External cell and graphical-face grants now follow the
widened body through `fit_region`; changed grants clear retained rows before publication. The
intentional terminal/stack overlap grows from 432 to a bounded 504 cells rather than full-width's
3,033-cell cost at the supported maximum.

**State in conversation:**  
explicit founder acceptance after review

**Routing:**  
Existing parsed Vision Delta 2026-08-17-Z implementation closure; Workshop Goal Map WIND-1 capsule;
Pressure P50 closure; Strategic Map current position; executor handoff; accepted repository board.

**Preserve especially:**  
Responsive default geometry is implemented. Authored pane size/position, setup v2, z-order,
management gestures, overlap recovery, same-PaneRef multiplicity, arbitrary provider drawing/input,
and the second-provider witness remain separate and unselected.

---

# Raw Delta Capture — 2026-08-18 — Authored pane windows are accepted and correction fan-out becomes explicit

## The host-owned window contract is now implemented without widening pane identity

**Raw:**  
Accept WIND-2, WIND-2a, and WIND-2b as one corrected implementation sequence. Setup format 2 stores
the maker's smallest per-pane place/width/height override plus one canonical front permutation.
Version 1 refuses legibly before row interpretation rather than migrating. Workshop resolves actual
geometry, clipping, overlap, paint/hit order, external room, management, and recovery. Keyboard and
pointer reach the same semantic operations, and TUI and SDL execute the same ordered Surface layers.
Shared screen chrome remains explicitly in front of panes and the Terminal remains final.

**Context:**  
WIND-2 landed the authored-window system. Source-first review found one composition-law defect and
six bounded Workshop defects; WIND-2a repaired them and made canonical front visible through
SurfaceCanvas v5 / SurfaceLayer v1. WIND-2b strengthened the clipped-default width/height resize and
atomic invalid-corner refusal evidence and corrected current-facing prose. The accepted Zengine
head is `1f92d81a3ecde58f1f3f3bc82f139914ad2c495b`; Loom and the external pane protocol did not move.

**State in conversation:**  
explicit founder acceptance after review

**Routing:**  
Existing parsed Vision Delta 2026-08-17-Z implementation closure; Workshop Goal Map WIND-2 sequence
capsule; Pressure P53 closure; Strategic Map current position; current executor handoff; accepted
repository board.

**Preserve especially:**  
One PaneRef still mounts once. Current panes preserve but refuse pixel intent. Host chrome's
always-on-top plane is explicit product policy, not a generic compositor claim. No second provider,
provider input/focus, unload/liveness, arbitrary drawing, docking/tabs/tiling, generic registry, or
same-PaneRef multiplicity is pulled. No successor packet is selected by acceptance.

## A known correction gap should ask before commit; a later discovery preserves history

**Raw:**  
WIND-2b needed a second commit because a repeated sixteen/seventeen count in `Zengine/AGENTS.md`
was noticed before the first commit but sat outside a prompt that authorized only the report copy.
The executor reported the gap, pushed the bounded first commit, and corrected the second copy only
after founder direction. No history rewrite is warranted, but the loop can avoid knowingly partial
corrections.

**Context:**  
The prompt author searched the reported phrase but did not trace the same fact through all
current-facing copies. Exact-sentence authorization then made an already-known semantic duplicate
out of bounds. This is a refinement of the existing execution/acceptance/consolidation split, not a
new process framework and not an argument that multiple commits are inherently undesirable.

**State in conversation:**  
founder accepted the workflow recommendations

**Routing:**  
Existing parsed Vision Delta 2026-08-16-W operational refinement; orientation working rhythm;
Strategic Map and Workshop phase-generation governance; first-contact and current executor handoffs.

**Preserve especially:**  
Before commit, fan factual findings out by meaning. For counts, search the number, phase name, and
derived arithmetic. Authorize the smallest semantic correction and enumerate changed paths. A
relevant known gap outside authority pauses for a founder question before commit. Check that original
findings are closed, fan-out is complete, no relevant gap is deferred without decision, the diff
matches scope, and the report skeleton matches the diff. If the gap is discovered only after push,
repair forward rather than rewriting honest history.


"And yes, we have accumulated a *lot* since the last consolidation. Here is the architecture as I currently see it.

---

# 1. Message discovery and Message Composer

We built the path from:

```text
select a weave
    ↓
discover what it accepts
    ↓
construct an unknown-at-compile-time message
    ↓
submit it
```

The important architecture that came out of this is that **the target owns its vocabulary**.

`zen.DescribeAccepted` / `zen.AcceptedShapes` allows a participant to describe its actual finite accept-set using the same underlying schema truth delivery enforcement uses.

So:

> **Discovery and enforcement read the same store.**

Message Composer then became the first real consumer.

It is deliberately generic:

```text
target
    ↓
accepted Schema roots
    ↓
runtime-generated form
    ↓
generic Loom composition
    ↓
SUBMITTED
```

Not:

```text
if Timer:
    show Timer controls
```

And we retained the crucial semantic distinction:

```text
SUBMITTED ≠ DELIVERED ≠ SEMANTIC SUCCESS
```

Composer knows what it constructed and attempted. It does not fabricate bus fate or application result.

---

# 2. Accepted / semantic / state / result truth

AAF-R0 split what originally looked like “validation” into several independently-owned facts.

The useful current model is roughly:

```text
COMPOSABLE / STRUCTURALLY ADMISSIBLE
    Can the value/message be represented?

ACCEPTED
    Does this target declare this shape?

SEMANTIC DECLARATION
    Units, ranges, finite vocabularies, etc.
    Facts about meaning that require no live target state.

DECLARATION AFFORDANCE
    Fixed-at-mount information about what can be manipulated.

STATE AFFORDANCE
    Does this operation make sense in the target's world right now?

DRAFT APPROPRIATENESS
    Do THESE values make sense against that world right now?

PROTOCOL / PROVENANCE
    Is this even something an ordinary maker can author?

AUTHORIZED
    Does the host grant this sender permission?

DELIVERY
    What did Loom do with it?

RESULT
    What did the application say happened?
```

This killed the idea of one generic “safe/valid/available” flag.

The major law was:

> **Different questions have different owners, lifetimes, and authorities.**

And AAF-R0 found a real draft-specific check already hiding in Timer: `EnsureTimer(... preserve_remaining ...)`.

---

# 3. Semantic constraints as executable logic

The `delay_ms = -500` case pushed us beyond passive metadata.

Rather than separately writing:

```text
minimum = 0
unit = milliseconds
```

beside execution code that independently clamps the value, we started asking:

> **Can the thing tooling understands be the same thing execution actually evaluates?**

That led directly into operators.

The important shift is that a semantic rule can be executable structure:

```text
delay_ms
repeat
    ↓
existing operators
    ↓
effective_delay
```

Then:

```text
Timer execution
Composer preview
Flow
tests
```

can all consume the **same semantic path**.

So:

> **Sharing execution truth is stronger than duplicating descriptive metadata about execution truth.**

---

# 4. Logic operators

This has become one of the larger new architectural systems.

An operator is not “a lambda.”

The emerging minimal definition is approximately:

```text
OperatorDef
    stable identity
    input Loom Schema
    output Loom Schema
    callable
```

Something very close to:

```cpp
bool greater_equal(std::int64_t lhs, std::int64_t rhs);

register_operator<&greater_equal>(
    "math.greater_equal",
    ...
);
```

appears realistically supportable.

C++ already gives us:

```text
arity
argument types
return type
```

through templates.

The main ceremony C++ does **not** naturally provide is semantic naming such as parameter names.

That makes codegen attractive for exactly the boring parts.

---

# 5. Primitive versus composite logic

This is probably the most important design decision in the logic system.

A **primitive** introduces power Zen cannot yet express:

```text
BitwiseAnd
GreaterThan
Add
StringMatches
```

A **composite** reuses those powers:

```text
IsPowerOfTwo
    GreaterThan
    Subtract
    BitwiseAnd
    Equals
    And
```

Therefore:

> **Composition should consume existing power. Native code should introduce only genuinely missing power.**

And:

> **One primitive, one semantic path.**

If five composites use `GreaterThan`, they all go through the same `GreaterThan`.

That gives us reuse *and* makes bugs dramatically easier to localize.

---

# 6. Flow

Flow is beginning to stop looking like “a visual scripting system we someday want” and instead looks like a **projection of concepts Zen is independently earning**.

Its likely vocabulary is becoming:

```text
FACT / EVENT
    something happened

VALUE
    something is

OPERATOR
    values -> values

OBSERVATION / REQUEST
    acquire information not locally possessed

ACTION / EFFECT
    change something

AUTHORITY
    legitimizes observation/effect
```

Flow would compose those things.

Critically:

> **Flow composes powers; hot loading teaches it new powers.**

And Flow should not be the sole representation. The authored semantic artifact is structured logic; a graphical editor is one projection over it.

---

# 7. Hot loading as a maker feature

This was a major conceptual promotion.

Hot loading is no longer merely:

> developer changed a DLL and doesn't want to restart.

It can become:

```text
maker discovers missing capability
    ↓
authors smallest missing primitive
    ↓
generated ceremony
    ↓
Builder compiles
    ↓
provider hot-loads
    ↓
running operator vocabulary grows
    ↓
maker continues working
```

And because actual project source was changed:

> **Teaching the running instance can also teach the project permanently.**

That is the really exciting part.

The live process learns immediately, while the source/build intent means the power can still exist after restart and rebuild.

---

# 8. Generated code

Operators gave us our cleanest concrete code-generation philosophy yet.

The current law is:

> **Generated code carries ceremony. Authored code carries meaning.**

For a primitive, the author should ideally provide little more than:

```cpp
bool greater_equal(std::int64_t lhs, std::int64_t rhs)
{
    return lhs >= rhs;
}
```

plus unavoidable semantic identity/names.

Generation can own:

```text
Schema declarations
type adapters
ABI wrappers
provider tables
registration
manifest glue
build ceremony
tests/witness plumbing
```

We explicitly moved away from “parse arbitrary C++.”

Prefer:

> **Let the C++ compiler parse C++.**

---

# 9. Operator providers

We learned that an operator should **not** be a weave and should certainly not be one DLL per operator.

Instead:

```text
one provider artifact
    provides many operators
```

Potentially that same artifact could also provide:

```text
panes
woven services
other future surfaces
```

without those surfaces becoming conceptually identical.

So this general pattern keeps repeating:

```text
pane ≠ weave
operator ≠ weave

a loaded provider may PROVIDE them
```

Logical granularity and physical granularity stay separate:

```text
one operator
many operators per source pack
many operators per compiled artifact
one node per presentation
```

---

# 10. Callable custody

LOG-R1 reduced the native lifetime problem to a pleasantly small model.

A saved graph must **never retain a native function pointer**.

It retains durable intent:

```text
provider identity
operator identity
authored signature
```

At execution:

```text
resolve current provider
    ↓
hold provider record
    ↓
invoke current implementation
    ↓
release
```

So:

```text
implementation A
    ↓ reload
implementation B
    ↓ unload
unresolved
    ↓ reload
implementation A/C/whatever current
```

and the same authored `OperatorRef` survives throughout.

The core rule:

> **Saved intent retains identity. Execution resolves implementation at spend.**

Raw native addresses, provider-local indices, loaded image handles, etc. are transient.

---

# 11. Provider ABI

The likely portable native boundary is also emerging.

Rather than exporting arbitrary C++ objects or `std::function`, a provider can expose something conceptually like:

```text
one C ABI entry point

describe operator N
invoke operator N
```

with:

```text
plain ABI values
bytes across boundary
host-provided output sinks
exceptions stopped before ABI
```

Inside each side, we can reconstruct normal Loom `Value` / Schema objects.

This keeps:

```text
GCC/ELF
MSVC/PE
```

on the same conceptual path without relying on C++ ABI compatibility.

And notably, **invoke-by-index inside a currently held provider** appears essentially as cheap as exposing a raw callable, while removing the dangerous pointer from the public contract.

---

# 12. Operator invocation is neither Message nor Sense

This was another important result.

A message is causal communication:

```text
send
queue
delivery
handler
possibly answer
```

A Sense is:

```text
observe somebody's current claim
```

An operator is:

```text
supplied values
    ↓
computation
    ↓
returned values
```

So `GreaterEqual(5,3)` should not spend Loom turns.

And it isn't really a Sense either, because nobody is claiming that `5 >= 3`; it is computation.

Thus operator invocation becomes a distinct synchronous value-computation concept.

Senses still matter because a graph may acquire a value through observation and **then** feed it into operators.

---

# 13. Pure operators and authority

We also sharpened what “pure” means honestly.

A pure operator API can be:

```text
values in
values out
```

with no:

```text
Bus
Kernel
Workshop
filesystem capability
Loom grant
```

passed into it.

That prevents **authority from flowing through the operator interface**.

But native C++ is still native C++. It can intentionally:

```text
touch globals
call OS APIs
spawn threads
crash
```

if malicious.

So:

> **Purity by custody constrains the door, not the room.**

No hostile-code guarantees are implied.

---

# 14. Requests and obligations

This is still conceptual rather than built, but it became much more grounded.

We started from:

> some messages really mean “I need a response.”

Then discovered Loom already has **conversation-scoped reply provenance**.

A delivered ask can create a one-shot answer right tied to:

```text
requester
correlation
incarnation/lifetime
```

What Loom does **not** yet fully model is our stronger concept:

```text
request accepted
    ↓
an unresolved obligation now exists
    ↓
eventually it must resolve somehow
```

Possible terminal states conceptually:

```text
answered
refused
abandoned
expired, if deadline exists
cancelled, if cancellation earns semantics
```

The durable conceptual law we liked:

> **Messages describe what may happen. Obligations describe what must still be settled because something already happened.**

And the likely future improvement:

> **Receiving a legitimate request may mint exactly enough authority to resolve that request back to its asker.**

Not ambient outbound authority.

---

# 15. Potential work versus outstanding work

This grew out of the same discussion.

A weave having handlers does not mean it currently has work.

A Timer can have work even if nobody is sending it messages.

So we began distinguishing:

```text
DOOR
    something may happen

EVENT
    something did happen

OBLIGATION
    work is now owed

RESOLUTION
    that obligation is retired
```

Timer schedules, async builds, requests, handovers, etc. may eventually all be understandable through that lens without needing one shared implementation.

Another useful formulation:

> **Potential work versus outstanding work.**

Still conceptual. Not a framework yet.

---

# 16. Senses / published facts

AAF-R0 brought Senses back into relevance.

The important distinction is:

```text
ASK
    target receives a question and authors an answer

SENSE
    target already claims some current fact;
    authorized observer reads it synchronously
```

No queue, no sequence, no BusEvent.

For frequently-read state, that can be dramatically more appropriate than repeatedly asking.

But we deliberately did **not** decide:

> all affordance/preflight should be Senses.

Different truths have different costs and disclosure concerns.

An unbounded Timer entry table, for example, would be a poor first production Sense.

---

# 17. Project build/load persistence

Hot-loading something once is not the same as teaching the project.

We now distinguish at least:

```text
LIVE
    provider exists in current process

RESTART
    project knows to load provider again

CLEAN BUILD
    source/build intent recreates provider artifact

FRESH CHECKOUT
    durable authored project state recreates everything
```

This exposed likely separate project truths:

```text
WHAT THE PROJECT BUILDS
WHAT THE PROJECT LOADS
```

That is why **LOAD-0** became attractive.

Current Workshop still has compiled-in boot knowledge. We want explicit authored project load intent rather than directory scanning.

And importantly:

> **LIST, not SCAN.**

Explicitly loading configured native code is authored authority.

Automatically executing whatever DLL happens to be lying in a directory is not.

---

# 18. Builder's evolving responsibility

Builder currently largely owns:

```text
process started
process running
process finished
```

It does not yet necessarily own:

```text
this build produced provider X
at artifact Y
which should now replace provider Z
```

Eventually the live-teaching lifecycle needs:

```text
authored primitive
    ↓
generated provider source
    ↓
build target
    ↓
artifact
    ↓
load/replace
```

But we have deliberately avoided making Builder absorb the entire lifecycle prematurely.

---

# 19. Weave/provider metadata

This is the newest system.

We're converging on an **append-only, single-assignment metadata record** attached to a bounded loaded subject/incarnation.

Not:

```text
string -> mutable string
```

and not duplicate-key multimap.

Rather:

```text
unique key
immutable value
provenance
```

with:

> **A key may be populated once within a metadata record and then never overwritten or erased.**

Multiplicity lives inside the value:

```json
{
  "zen.future_seams": [
    "...",
    "..."
  ]
}
```

rather than repeated metadata keys.

---

# 20. Metadata provenance domains

Different layers add facts only when they become entitled to know them.

Conceptually:

```text
AUTHOR
    description
    tags
    future seams
    project-specific claims

BUILD
    compiler/build/source facts

LOADER
    artifact path
    actual loaded artifact fingerprint
    load sequence/time

BUS / KERNEL
    incarnation
    actual role ownership
    runtime identity
```

And author declaration gets sealed on load.

A running weave should not later rewrite its own description just because it can.

The general law:

> **Metadata grows because the system learns new facts, not because old facts are edited.**

And:

> **A loaded participant should not have to author facts the host necessarily learns by loading it.**

---

# 21. Metadata is deliberately unreliable evidence

We explicitly do **not** want metadata to become behavioral authority.

An author can say:

```text
"This code is secure."
```

Wonderful. That's an author claim.

A Loom-stamped SHA means only:

> Loom says the artifact bytes it loaded hashed to X through this mechanism.

It does **not** prove the artifact is safe.

So:

> **Metadata is useful, inspectable evidence—not executable truth.**

Execution still consults the actual authoritative mechanism.

Operator invocation does not trust `provides.operator = foo` in metadata.

It resolves the actual operator provider.

---

# 22. First-class JSON metadata

Metadata should have centralized, explicit JSON conversion.

No hand conversion by authors.

Ideally:

```cpp
json j = metadata;
```

or moral equivalent.

And provenance should remain visible in the canonical human-readable form, perhaps grouped by claimant:

```json
{
  "declared": { ... },
  "loader": { ... },
  "runtime": { ... }
}
```

Exact format isn't chosen, but JSON friendliness is now part of the design pressure.

---

# 23. Final living-system snapshot

Your older system found a new purpose here.

At shutdown, instead of attempting to reconstruct final state from history:

```text
living system
    ↓
enumerate current subjects
    ↓
read complete metadata
    ↓
serialize JSON
    ↓
save final snapshot
```

So we have:

```text
Recorder
    what happened

Logger
    what deserved a durable narrative

Metadata / final snapshot
    what was standing at the end
```

And your correction is exactly right:

> **They complement one another.**

They also provide independent-forging friction.

Today, with enough process compromise, any of them can be falsified. But producing a fabricated:

```text
history
selected narrative
final standing picture
```

that all agree perfectly is a more demanding attack than changing one record.

Not cryptographic proof. Still useful defensive complexity.

---

# 24. Identity versus provenance

This distinction has become increasingly central across multiple systems.

Examples:

```text
Operator identity
    math.greater_equal

Provider identity
    project.logic

Artifact provenance
    project-logic.dll
    SHA abc123
    load sequence 84
```

The path/hash is **not** identity.

Likewise:

```text
PaneRef
    provider + pane

Loaded incarnation
    actual library/path/WeaveId/etc.
```

The pattern is:

> **Identity says what something is supposed to be. Provenance says which concrete incarnation supplied it.**

This lets logical references survive rebuild/reload while diagnostics remain precise about the actual code involved.

---

# 25. The larger composition architecture

All of these systems are beginning to interlock:

```text
            PROJECT
      authored build/load intent
                |
                v
            PROVIDERS
     panes / operators / weaves
                |
         +------+------+
         |             |
         v             v
     WORKSHOP         LOOM
         |       messages / senses /
         |        requests / lifecycle
         |
         v
        FLOW
facts -> operators -> actions
         |
         v
  maker-authored behavior
```

Meanwhile:

```text
Recorder
Logger
Metadata
```

observe different aspects of the same running world.

And generated code sits underneath the authoring experience, carrying ceremony needed to bridge authored meaning into native/runtime machinery.

---

## Where I think we are strategically

The most important thing is that these are **not feeling like unrelated feature ideas anymore**.

Several old investments are beginning to become each other's missing pieces:

```text
Schemas
    give operators typed ports

Dynamic loading
    lets vocabulary grow live

Builder
    can eventually manufacture new provider artifacts

Provider discovery
    lets Workshop learn new tools

Message discovery
    lets tools generically speak to new participants

Senses
    expose facts without polling

Operators
    let those facts be transformed/composed

Flow
    can expose that composition to makers

Metadata
    makes the loaded world legible

Recorder/Logger
    make its history legible

Project load/build intent
    makes live-created power durable
```

That is why the recent work feels like a tipping point.

We aren't merely adding more primitives anymore.

We're starting to get **multiplication between systems**.

And if I had to compress the whole recent architecture into one sentence now, I'd probably say:

> **Zen is becoming a system where the running world exposes its facts and powers, makers compose those powers into new behavior, missing powers can be taught live, and the project retains enough identity, provenance, history, and authored intent to remain understandable afterward.**"
