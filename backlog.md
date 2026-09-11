# Zen Standing Backlog

**Status:** PRIVATE LIVE AUTHORITY  
**Refreshed:** 2026-09-10  
**Role:** work Zen knowingly owes but is deliberately not doing now  
**Pressure:** `private/pressure.md`

An item here is not authorized work and does not imply urgency. Closed items have been removed from
the live file; their evidence remains in reports and Git history.

## 1. Rules

An item belongs here only when Zen has decided work is owed. A possibility, known seam, or observed
pressure stays outside until that decision exists. Every item names its wake condition and source.

## 2. Workshop and onboarding

### BL-WORK-01 — Workshop and onboarding grow together

**State:** GOAL-COUPLED  
**Owed:** Repeated maker friction must either improve the interaction or produce an available,
truthful explanation of the real concept. Keep the one tool-authoring path legible: a pane is a weave
across the pane protocol, and the compiled-in path is debt being retired one pane at a time (VD-19;
Files left in Zengine PR #16). Grow the human contributor front door from tested public explanations
rather than from private phase vocabulary.

**Wake:** every Workshop phase with repeated human-facing friction; mandatory before actively
inviting outside contributors.

**Evidence:** Workshop Goal Map, WG/DOC external-reader work, current public guides.

### BL-WORK-02 — Keep the simple external pane useful as a learning artifact

**State:** PARKED / PRESERVATION  
**Owed:** Do not let the small Hello/provider witness become incomprehensible or disappear before an
ordinary maker can inspect how a pane arrives. If Workshop gains a real project-template or
installed-pane story, convert the witness into a dissectible example rather than inventing a second
tutorial implementation.

**Wake:** installed external-pane distribution, project templates, or a Workshop-native “open this
tool's source” path.

**Boundary:** this does not itself authorize a plugin SDK or an installation system.

### BL-WORK-03 — Resume the Editor extraction after sender fate

**State:** PARKED BY FOUNDER (VD-27)

**Owed:** Resume PR #23 from its preserved branch for bounded integration and acceptance.
The [Goal Map](goals/workshop.md#pane-extraction-current-status-and-next-work) owns the remaining
transaction/input obligations. The PR is unmerged and unaccepted; parked does not mean waived.

**Wake:** the scoped sender-fate phase is ready for consumer integration. Start with a concrete
transaction argument using the capabilities actually delivered; name further missing capability
before implementation rather than assuming dispatch fate supplies conversation settlement.

**Evidence:** founder's 2026-09-10 sequence decision; [research](../reportbacks/sender-fate-research-RB.md).

## 3. Bounded defects and quick repairs

### BL-DEF-01 — Sandbox view-root cleanup after refusal

**State:** PARKED  
**Owed:** One empty `/tmp/zen-sb-*` view root may survive a sandbox refusal after root creation.
Remove it without weakening the refusal path or the evidence that containment was not established.

**Wake:** long-running sandbox-host pressure, visible accumulation, or the next isolation cleanup.

**Evidence:** `COLD-2-REPORT.md` C-6.

### BL-DEF-02 — Object-name byte limit reports the wrong unit

**State:** SMALL QR CANDIDATE  
**Owed:** `Zengine/workshop/document.hpp::check_name` measures `std::string::size()` against 64 but
says `characters`. Change the refusal to `bytes` and pin the exact multibyte boundary. Do not change
the bound or introduce code-point/grapheme/display-width policy.

**Wake:** next document/name-validation touch or an explicitly selected cleanup QR.

### BL-DEF-04 — Remove the dead Loom SDL dev override from Zengine

**State:** SMALL QR CANDIDATE  
**Owed:** Zengine's dev-mode CMake branch still describes Loom's retired `zen-ui-sdl` as a future port
and writes the now-undeclared `ZEN_SDL` cache option. Remove the stale comment and dead `set()`; do
not alter Zengine's own SDL3 skin or the sibling-Loom dev path.

**Wake:** next CMake/dev-mode touch or a compact QR.

**Evidence:** LSDL-0 §9 and current `Zengine/CMakeLists.txt`.

## 4. Verification and process



### BL-VER-02 — Resolve the hosted/advisory Zengine MSVC result

**State:** OWED WHEN LOG ACCESS EXISTS  
**Owed:** Read authenticated hosted logs and reconcile the advisory CI result with the green local
MSVC stranger/full lanes. Repair the mechanism or claim; do not merely broaden a diagnostic regex.

**Wake:** authenticated CI access or before upgrading the Windows support promise.

## 5. ABI, adoption, and release

### BL-ABI-01 — Positional aggregate ABI hazard

**State:** VERIFIED — PENDING FOUNDER ACCEPTANCE

**Disposition:** The source hardening already landed in Loom
`2cf7e0565c810f61375fca4c31f5088b7e3b6c6c`: all descriptor/host constructions name their fields.
ABI v7 fired the promised reassessment. At `eee04550dfbae61638ff84f1c9da1c32ad90f9b0`, the exhaustive callback-type inventory,
real-host cross-wire canary, loaded semantic red/restored-green witness, strict C99/C11/C17
producer and C++20 export checks, official Linux lane and all eight new-head CI jobs passed
their intended verdicts. The new send_to_role/office_publish equality is distinguished by
destination, personal/office provenance and attempt/count meaning; descriptor safeguards remain.

**Acceptance:** Recommend removing this item from the live backlog when the founder accepts
the reassessment; retain its history in reports and Git. No work remains parked on ABI v7.
Future appended fields or changed signatures follow the current ABI evolution checklist.
Standing C-producer/binding infrastructure remains triggered by an actual such producer/binding,
not by this bounded compatibility witness.

**Evidence:** [reassessment report](../reportbacks/abi-v7-wiring-reassessment-RB.md),
[full inventory and mutation proof](../reportbacks/abi-v7-wiring-reassessment-evidence.md),
[original BL-4 record](../reportbacks/BL-4-RB.md), and Loom PR #5 CI run `34557565217`.

### BL-ADOPT-01 — Human contributor front door

**State:** GOAL-COUPLED  
**Owed:** Turn the truthful but thin contributor entry into a practical human route: persistent
installed Loom/Zengine prefixes, IDE discovery (`CMAKE_PREFIX_PATH`/package dirs), canonical lanes,
repository ownership, and links to the product concepts Workshop has proven. Reuse public guides;
do not make humans read the executor constitution.

**Wake:** before actively soliciting outside contributors or claiming second-maintainer onboarding.

### BL-ADOPT-02 — Release identity and compatibility promise

**State:** PARKED  
**Owed:** Establish dependable tags/release identity and a public stability/deprecation posture
before external consumers are asked to depend on a named Zen release rather than pinned `main`
identities.

**Wake:** first public release/support promise or multiple external consumers exposed to churn.

### BL-ADOPT-03 — Performance evidence before performance claims

**State:** PARKED  
**Owed:** Do not manufacture a benchmark suite for maturity theater, but do not make throughput or
latency claims without claim-specific measurements.

**Wake:** first material performance promise, observed bottleneck, or adoption decision that
depends on performance.

## 6. Architectural debt that waits for pressure

### BL-ARCH-01 — Cross-layer public include debt

**State:** PARKED  
**Owed:** A few portable/public surfaces depend on headers whose current contents happen to remain
platform-neutral. Repair ownership only when a package/platform break or public-header evolution
makes the debt material.

**Wake:** relevant package failure, platform break, or touched ownership boundary.

### BL-ARCH-02 — Current-law carrying cost must remain bounded

**State:** WATCH / SUBTRACTIVE DUTY  
**Owed:** Keep mandatory and routed current law organized by subject and rewritten in place. If a
routed file becomes a phase-indexed chronicle or repeated concepts require phase archaeology,
consolidate it without deleting the enforceable law or proof history.

**Wake:** a cold reader cannot find the owner without phase names, or a routed current-law file's
growth materially slows every task touching that surface.

## 7. Explicitly not backlog

The following remain trigger-governed horizons or pressure, not owed cleanup:

- tabs, Vim emulation inside the built-in Editor, syntax highlighting, a VFS, file watcher, or Flow
  editor (a differently-shaped Editor arriving as a pane weave is P-WORK-07's case, not this);
- arbitrary pane drawing, same-PaneRef multiplicity, or plugin discovery;
- live artifact replacement before a concrete owner/continuity case;
- general obligations, group/consensus, metadata, or persistence frameworks;
- multithreaded dispatch;
- Windows native containment or escape-tier security;
- production Bridge hardening before hosted/remote use;
- a replacement SDL executor for Loom's portable pixel layout brain.
