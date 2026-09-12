# Zen Standing Backlog

**Status:** PRIVATE LIVE AUTHORITY  
**Refreshed:** 2026-09-12  
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

**State:** STEP 3 IMPLEMENTED (2026-09-12) — PR #23 updated at `26c44b4e1d159adf5c1a8e9fefdf1d660cad8255`, awaiting founder review; not accepted.

**Current disposition:** the managed opening is integrated on PR #23 (`panes/editor-weave`,
two commits over `9cbf5a5`: the reviewed experimental slice `76be71f` imported verbatim, then the
integration) against the accepted installed Loom `a08499f4e445b578b2c4ffcaac6265aa7094b88f`
(ABI v8). The native opening manager, the real loaded Editor and Workshop as the presentation
owner publish the document and the presentation jointly; the old Editor-address relay keeps the
requester's right; Files and the Builder consume exact-attempt refusals and handle an enqueue that
queued nothing at once; every newer terminal outcome retires the manager's retained repair record
(pinned red on the imported slice first); the host loop attributes a native showing failure from
Loom's record at the pump seam and lets everything else propagate; a replaced manager's retained
authority is refused and the host re-mints. Law: `Zengine/agents/workshop/opening.md`
(WL-OPEN-01..09) and the decision record beside it. Verified on the official WSL lane, under
ASan+UBSan, by the package witness, on MinGW-w64, by four red-then-green mutations and by live
terminal and window witnesses; CI at that head is read job by job in the report.
Report: [zengine-managed-open-integration](../reportbacks/zengine-managed-open-integration-RB.md).

**Still owed:** founder review and acceptance of PR #23; nothing self-accepts. The
[Goal Map](goals/workshop.md#pane-extraction-current-status-and-next-work) owns the outcome; the
[roadmap](drafts/editor-pr23-roadmap.md) explains the sequence that led here.

**Wake satisfied:** the dependency is merged, Step 3 is implemented and evidenced. Closure still
requires founder acceptance of the production result.

**Evidence:** [Step 3 report](../reportbacks/zengine-managed-open-integration-RB.md),
[corrected runnable slice](../reportbacks/editor-managed-open-slice-corrections-2-RB.md),
[Loom landing](../reportbacks/loom-joint-publication-landing-RB.md),
[authority corrections](../reportbacks/loom-joint-publication-authority-corrections-RB.md),
[merged PR #6](https://github.com/Krealsion/Loom/pull/6). Earlier investigations and correction
rounds remain in those reports and Git rather than in this current disposition.

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

**State:** IMPLEMENTED IN STEP 3 (2026-09-12), awaiting PR #23's acceptance  
**Owed:** nothing further once PR #23 is accepted. The stale `zen-ui-sdl` comment and the dead
`set(ZEN_SDL …)` are gone from the dev-mode branch of `Zengine/CMakeLists.txt` (PR #23 at
`26c44b4e1d159adf5c1a8e9fefdf1d660cad8255`); `ZEN_LOOM_DEV`, the Loom test/example suppression,
the Windows kernel selection and Zengine's own SDL3 skin are untouched. Checked by source grep
(no `ZEN_SDL` or `zen-ui-sdl` remains) and by the stranger configure of every lane.

**Wake:** closes with PR #23's acceptance.

**Evidence:** LSDL-0 §9; [Step 3 report](../reportbacks/zengine-managed-open-integration-RB.md).

## 4. Adoption and release

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
