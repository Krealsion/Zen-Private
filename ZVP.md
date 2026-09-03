# Zen Verification Proportionality — Vision Handoff

**Branch conclusion after QR-15 runtime observation**

Purpose: carry one process-level correction back to the primary Zen: Vision thread without importing the branch transcript.

## Decision

**Verification should scale with the blast radius of the claim, not with the maturity of the repository.**

Zen has accumulated strong proof techniques—cross-platform lanes, sanitizers, mutation testing, package witnesses, live TUI/SDL witnesses—but we have begun applying too many of them uniformly to every phase. The result is that tiny repairs increasingly pay release-scale verification cost.

**Immediate policy change:** small QRs should normally prove the repaired property on the smallest affected surface. Heavy confidence sweeps remain valuable, but belong at architectural phases, milestone/arc closure, or explicit confidence passes—not automatically on every formatting or local interaction repair.

## What exposed the problem

QR-15 was intended to be tiny: remove presentation quotes from layout names and change the active marker from a left-only form to a symmetric tight form such as:

    Home >Code< Art

Despite that narrow production claim, the prompt still requested Linux/GCC, ASan+UBSan, Windows/MSVC, focused tests, driven TUI and SDL witnesses, and a broad set of mutations.

The executor run took roughly **40 minutes**.

That duration is not evidence that the repair itself was complex. It is evidence that our verification floor has grown into a fixed tax large enough to dominate tiny implementation work.

## Diagnosis

- **Release-candidate verification became the default.** Proof methods that repeatedly paid for themselves were gradually promoted from “use when relevant” into “run every phase.”

- **The Workshop test surface has meaningful fixed cost.** QR-13 demonstrated this physically: the panes suite became large enough for one MinGW Debug translation unit to overflow the COFF section-name string table. Even after splitting it, shared test support remains expensive to instantiate.

- **Mutation testing drifted toward ritual.** Mutations are excellent when they identify the seam enforcing a new law or prove a repaired defect. A large mutation matrix is not automatically justified by a tiny presentation change.

- **Live witnesses were treated too uniformly.** A real product witness is often essential, but both TUI and SDL are not always needed when the touched presentation path or claim does not materially differ across media.

- **Sanitizers and platform lanes were detached from risk.** ASan/UBSan is disproportionately valuable for memory, lifetime, ownership, and undefined-behavior risk; it is much less informative for a local string-formatting repair. Cross-platform verification should likewise follow platform-sensitive seams.

- **Repository maturity was making small edits slower.** That is backwards. A mature, well-factored test suite should make localized edits cheaper to trust because the relevant proof surface is sharper.

## Proposed verification weights

### 1. Local Repair / QR

Default for bounded defect fixes, presentation corrections, local interaction repairs, and other changes whose source-traced seam is small.

- Build the affected target or smallest dependency closure.
- Run focused relevant tests, not standing repository-wide populations by default.
- Use one relevant live witness when the claim is maker-visible or integration-sensitive.
- Use one or two sharp falsifiers/mutations that put the repaired defect or property back.
- Do not automatically owe sanitizers, every platform lane, package witnesses, both media, or a broad mutation matrix.

### 2. Production Phase

Default for new capability, changed ownership, new durable behavior, protocol interaction, or a feature spanning several existing seams.

- Affected suites plus the ordinary primary lane.
- Relevant live witnesses for the media or gestures whose claims changed.
- Targeted mutations/falsifiers for the new laws and fragile ownership seams.
- Add sanitizer or platform lanes when the touched seam creates memory/lifetime/UB or portability risk.
- Add package/install witnesses when public or installed surfaces moved.

### 3. Milestone / Arc Closure / Release Confidence

This is the proper home for the expensive accumulated confidence machinery.

- All standing compiler/platform lanes.
- Sanitizer population.
- Installed-package/public-surface witnesses.
- Broader mutation families where useful.
- Cross-medium driven witnesses.
- Longer integration and regression sweeps.

A **30–60 minute confidence sweep is acceptable here**.

The mistake is attaching that same cost to a two-character presentation repair.

## How to choose proof, not merely how much

The important question is not just:

> How much verification does this phase deserve?

It is:

> What kind of failure could make this claim false?

Verification should answer that question directly.

A local formatting repair should primarily prove formatting and inversion.

A lifetime/ownership change should spend sanitizers.

A public API change should spend the installed-package witness.

A medium-sensitive interaction should spend the affected medium.

A portability change should spend the relevant platform lanes.

A new architectural law should earn stronger falsifiers and mutations.

The proof mechanism should follow the failure mode.

## Escalation rule

**Start narrow, then escalate from evidence.**

A QR does not receive weak verification; it receives proportional verification.

Broaden the proof surface when any of the following occurs:

- Source tracing reveals the repair crosses the initially expected owner/seam.
- A focused test or witness fails outside the expected defect.
- The repair changes a public, durable, cross-process, or cross-platform contract.
- A sharp falsifier survives, suggesting the claimed enforcing seam is wrong or incomplete.
- The executor must introduce materially broader machinery than the prompt expected.

Escalation should be recorded as a **finding**, not hidden inside an automatic full-lane run.

## Prompt-writing doctrine change

For small QRs, replace standing verification boilerplate with language like:

> **Verification is proportional to this repair. Run the smallest affected build/test surface and a live witness that exercises the repaired behavior. Do not run standing full-repository lanes, broad mutation matrices, package witnesses, sanitizers, or unrelated media merely for ceremony. Escalate only if source changes cross the measured seam, a focused proof fails, or current repository law identifies a directly relevant standing obligation.**

For production phases, state the **specific risks** that justify each heavier lane rather than copying the entire verification inventory.

For arc closure / confidence phases, say explicitly that this is the broad sweep where the standing confidence machinery is intentionally paid.

## What this does not mean

- It does not weaken Zen’s honesty doctrine or allow unproved completion claims.
- It does not remove existing tests or standing lanes.
- It does not forbid full verification after a QR when the repair touches a risky seam.
- It does not turn executor discretion into “skip tests if they look annoying.” The prompt should identify the expected proof floor and the conditions that require escalation.
- It does not make speed the primary value. It prevents irrelevant proof cost from obscuring the cost of the thing actually being changed.

## Recommended follow-up in primary Vision

- Adopt the three-weight verification model as prompt-authoring policy immediately.
- Do not retroactively rewrite historical phase standards; this is a forward process correction.
- Use the next genuinely small QR as the first deliberate proportional-verification trial and compare wall-clock cost with recent QRs.
- Keep periodic heavy confidence passes—after a meaningful arc, before release/stability claims, or when broad architectural work accumulates.
- If even focused QRs remain slow, investigate the fixed cost of Workshop test support separately. QR-13 already showed that shared panes test machinery is large enough to be a real build-system pressure sensor.

## Branch evidence / context

The conclusion was reached while reviewing the WUX layout-tab arc and its repairs:

- **WUX-9-RB.md** — multiple Workshop layouts; heavy verification appropriate to a genuinely architectural feature.
- **QR-13-RB.md** — MinGW panes Debug build overflow; revealed substantial fixed cost in the Workshop panes test machinery.
- **QR-14-RB.md** — top-of-screen tab-band repair; one-file production delta still carried broad verification.
- **QR-15 prompt/run observation** — extremely narrow presentation repair took roughly 40 minutes, exposing verification process debt.

## Bottom line

Zen should keep its unusually strong proof culture, but spend proof where the claim can actually fail.

**The goal is not fewer guarantees; it is sharper guarantees at the right scale.**
