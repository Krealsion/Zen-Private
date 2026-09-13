# Zen Standing Backlog

**Status:** PRIVATE LIVE AUTHORITY  
**Refreshed:** 2026-09-13\
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

### BL-WORK-02 — Keep the simple external pane useful as a learning artifact

**State:** PARKED / PRESERVATION  
**Owed:** Do not let the small Hello/provider witness become incomprehensible or disappear before an
ordinary maker can inspect how a pane arrives. If Workshop gains a real project-template or
installed-pane story, convert the witness into a dissectible example rather than inventing a second
tutorial implementation.

**Wake:** installed external-pane distribution, project templates, or a Workshop-native “open this
tool's source” path.

**Boundary:** this does not itself authorize a plugin SDK or an installation system.

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

### BL-DOC-01 — Finish the pane/focus documentation cleanup after PR #25

**State:** BOUNDED DOCS CLEANUP / DEFERRED (2026-09-13); not a blocker for accepted PR #25

**Owed:** Correct these identified reader-facing inaccuracies without changing product policy:

- Remove stale total-shape claims: the B1 "Five shapes, and there is no sixth" heading in
  `Zengine/docs/guides/make-a-workshop-tool.md`, and the "eleven shapes" summaries in
  `docs/README.md`, `docs/architecture/README.md` and `docs/workshop/panes.md`. Prefer a description
  and route to `workshop/pane_vocabulary.hpp` over another copied total; reconcile nearby counts
  in directly edited owner prose as needed.
- In `Zengine/agents/decisions/the-keys-go-where-last-pressed.md` and
  `agents/workshop/focus.md`, qualify the claim that holder turnover refuses a queued press.
  A compatible successor may receive it; an incompatible successor can refuse it, without retry.
  Align the decision record's "two places" summary with the title/band distinction: the mark
  identifies the resolved return pane, while the band reports where ordinary keys currently go.
- In `Zengine/agents/panes.md`, remove the obsolete claim that forwarding a press changes no
  Workshop picture and causes no repaint. Workshop does not interpret provider rows, but a focus
  press can restore a title, change the granted room and repaint its own presentation.

**Wake:** the next focused pane/focus documentation pass, or an edit to one of these affected
paragraphs. A local correction may narrow this entry; it need not trigger a broad documentation arc.
Run the relevant documentation/link/register checks and keep policy and runtime behavior unchanged.

**Evidence:** [PR #25 report](../reportbacks/zengine-files-focus-implementation-RB.md), Decisions
asked and Documentation/gaps; Vision's review of `9c4242c` on 2026-09-13 and the source homes above.
The founder explicitly requested this backlog entry after confirming the merge.

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
