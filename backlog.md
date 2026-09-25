# Zen Standing Backlog

**Status:** PRIVATE LIVE AUTHORITY  
**Refreshed:** 2026-09-25\
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
truthful explanation of the real concept. Keep the one tool-authoring path legible: a pane provider
is a weave communicating across the pane protocol. Files, Builder, Attention, Info, Terminal and
Editor have completed the selected extraction arc; the Goal Map names the remaining host-owned
surfaces (VD-19). Grow the human contributor front door from tested public explanations rather
than from private phase vocabulary.

**Wake:** every Workshop phase with repeated human-facing friction; mandatory before actively
inviting outside contributors.

**Evidence:** Workshop Goal Map, WG/DOC external-reader work, current public guides.

**Delivered foundation:** merged interaction authoring repairs the existing loaded-pane guide around
Tally, request handling and missing-reply diagnosis. Warm installed-package exercise is useful evidence,
not second-maintainer validation. The goal-coupled obligation remains open. The tower-defense example
(accepted Zengine #60) adds a public 0-to-game route whose every step is a documented ELH tool
and whose replay was proven from an empty directory; it is a maker's route, not onboarding proof.

### BL-WORK-02 — Keep the simple external pane useful as a learning artifact

**State:** PARKED / PRESERVATION  
**Owed:** Do not let the small Hello/provider witness become incomprehensible or disappear before an
ordinary maker can inspect how a pane arrives. If Workshop gains a real project-template or
installed-pane story, convert the witness into a dissectible example rather than inventing a second
tutorial implementation.

**Wake:** installed external-pane distribution, project templates, or a Workshop-native “open this
tool's source” path.

**Boundary:** this does not itself authorize a plugin SDK or an installation system.

### BL-WORK-03 — Split the Info value view before it grows again

**State:** PARKED / MAINTAINABILITY  
**Owed:** `info-pane/value_view.hpp` is one class of about 1,340 lines holding the draft, the
owner-operation record and its adoption rules, the watch custody, sampling, field pickup, and the
picture with its controls. The corrections kept it whole because a split was not needed to make the
repairs clear. Extract the picture/controls composition and the watch custody (`Watch`, `ending_`,
start, stop, cycle and the lease answers) into their own image-local headers, keeping every record
per view and the one act entry point. Behaviour and law stay as they are.

**Wake:** the next change that adds an operation, a pending-request kind or a control to that file,
or the file passing 1,500 lines.

**Source:** [corrections report](../reportbacks/zengine-independent-info-workbench-corrections-RB.md).

## 3. Bounded defects and quick repairs

### BL-VERIFY-01 — Reconcile Builder field clicks locally

**State:** PARKED / LOCAL FOLLOW-UP; explicitly not a blocker to merging Zengine PR #43.
**Owed:** Resolve the retained Builder role-field evidence: the terminal capture shows
`abcdKef...` while its report claimed `abcKdef...`; the native capture shows `Kabcdef...`
after Home, which cannot distinguish a missed click from a caret-placement defect. Retain the
actual coordinate space, x/y, expected insertion point and before/after value on a local rerun.
Repair product behavior only if the diagnosis establishes a defect.

The native `witness/gui/host/step.ps1` must retain its sent command and fail on an unsettled or
failed probe, missing fresh capture, child failure or mismatched expectation. Exercise a negative
control through that driver. The existing Files checks and maker journey remain usable; no full
workflow replay or new input architecture is owed here.

**Wake:** the next local Builder role-field check or reuse of this native witness driver.

**Source:** founder's 2026-09-21 decision to merge with local evidence follow-up;
[verification review](../reportbacks/zengine-files-builder-mouse-verification-review/review.md).

### BL-DEF-01 — Sandbox view-root cleanup after refusal

**State:** PARKED  
**Owed:** One empty `/tmp/zen-sb-*` view root may survive a sandbox refusal after root creation.
Remove it without weakening the refusal path or the evidence that containment was not established.

**Wake:** long-running sandbox-host pressure, visible accumulation, or the next isolation cleanup.

**Evidence:** `COLD-2-REPORT.md` C-6.

### BL-DEF-05 — Files action identity changes meaning across modes

**State:** CLOSED — founder confirmed PR #29 merged after the accepted documentation housekeeping.
Browsing, chooser selection and authoring submission now have separate operation meanings.
The [housekeeping report](../reportbacks/zengine-files-action-identity-doc-housekeeping-RB.md)
and Git retain the evidence; do not reopen this repair from the older pending status.
General queued-picture provenance remains a distinct pressure.

## 4. Adoption and release

### BL-ADOPT-01 — Human contributor front door

**State:** GOAL-COUPLED  
**Owed:** Turn the truthful but thin contributor entry into a practical human route: persistent
installed Loom/Zengine prefixes, IDE discovery (`CMAKE_PREFIX_PATH`/package dirs), canonical lanes,
repository ownership, and links to the product concepts Workshop has proven. Reuse public guides;
do not make humans read the executor constitution.

**Wake:** before actively soliciting outside contributors or claiming second-maintainer onboarding.

**Delivered foundation:** Loom #14 / Zengine #53 supply an exercised loaded-pane authoring
route and explicit diagnostic commands. Persistent setup, IDE discovery and independent human
onboarding remain broader work; this bounded repair does not close the item.

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

**Measured foundation:** accepted interaction authoring measures local implementation and shared-fixture
header invalidation on one Windows/MinGW Debug configuration. Native grant edits now have a compiled
owner; the large shared fixture remains a measured pressure, not a claimed general speedup.
The phase evidence owns exact counts/times and the limits of mtime-only probes.

## 5. Architectural debt that waits for pressure

### BL-ARCH-01 — Cross-layer public include debt

**State:** PARKED (reassessed 2026-09-12 at the ABI v8 landing; not made material)  
**Owed:** A few portable/public surfaces depend on headers whose current contents happen to remain
platform-neutral. Repair ownership only when a package/platform break or public-header evolution
makes the debt material.

**Measured disposition (loom-joint-publication-landing):** the touched public boundary was traced
header by header. Every new type lives in the layer that owns its concept -- the operation and
its authority beside the Sense types in `switchboard/sense.hpp`, the hook's answer beside the weave
contract, the notices beside `DispatchRefused` in `weave/`, the two statuses and slots in the C
`abi.h` -- and every new include points downward or sideways (switchboard → core; weave → switchboard;
kernel → switchboard, as before). The three-way answer has one truth on each side of the C seam,
joined by two mapping functions (`do_claim_published` library-side, `HostAdapter::claim_published`
host-side), and the package witness and the MinGW/MSVC lanes passed on the installed headers. No
upward include, no platform-conditional content entered a portable header; the debt is unchanged
and left parked with this argument in the report.

**Wake:** relevant package failure, platform break, or touched ownership boundary.

### BL-ARCH-02 — Current-law carrying cost must remain bounded

**State:** WATCH / SUBTRACTIVE DUTY  
**Owed:** Keep mandatory and routed current law organized by subject and rewritten in place. If a
routed file becomes a phase-indexed chronicle or repeated concepts require phase archaeology,
consolidate it without deleting the enforceable law or proof history.

**Wake:** a cold reader cannot find the owner without phase names, or a routed current-law file's
growth materially slows every task touching that surface.

### BL-ARCH-03 — The comment arc's remaining phases

**State:** OWED, sequenced by the founder (phase one, `workshop/`, landed for review 2026-09-24)  
**Owed:** Read the rest of the tree against the source comment standard
(`docs/contributing/repository-conventions.md`, "Source comment conventions") and widen
`source_comments`' `ZEN_COMMENT_ROOTS` behind each phase: the other Zengine packages (3.24 MB,
1.42 MB of it comments), `tests/` (6.43 MB, 2.03 MB comments, 340 star notes), then Loom under
its own conventions -- each by its own prompt, each with `tools/comment-pass/`'s edit tool,
census, map, applier and proof.

**Wake:** the founder's prompt for the next phase. **Source:**
`reportbacks/zengine-workshop-comment-compression-RB.md`.

## 6. Explicitly not backlog

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
