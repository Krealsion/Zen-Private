# Easier interaction authoring — accepted foundation

**Status:** accepted; Loom #14 and Zengine #53 merged on 2026-09-23, with every PR CI job green.\
**Purpose:** reduce the work and opportunities for error in adding an authorized interaction,
while preserving the ownership that makes tools composable.\
**Roadmap owner:** [Workshop goal map](../goals/workshop.md#near-term-order-and-purpose).

## What this foundation supplies

- Loom's opt-in `weave/role_request.hpp` records one ordinary typed role send and matches
  authenticated answers or exact dispatch refusals. The participant supplies its correlation;
  the application validates meaning and decides when to forget the request.
- Terminal capture and the Inventory client used by Inventory/Info consume that mechanism.
  Gesture identity, operation stages, conditional saves and result meaning remain Zengine policy.
- `workshop/grant.cpp` owns the native host's explicit send policy once, shared with fixtures.
  Independent withheld-grant evidence guards against shared policy mistakes.
- Workshop can explicitly retain refusals and render its log without booting the application.
  The supported history/log route can connect a denied immediate reply to its requesting handler.
- The existing public tool-authoring guide starts with maintained Tally and an exercised
  installed-package build, then explains request handling and failure diagnosis.

These are accepted capabilities, not a universal operation framework. There are no automatic
permission grants, retries, timeouts, rollback, remote cancellation or new ABI promises. A missing
reply can leave its caller pending. Dispatch ancestry is not a universal identity for deferred work.

## Remaining boundaries

The broad Workshop fixture header still has costly build fan-out. Moving grant policy to a
compiled owner helps that edit specifically; it does not establish a general build speedup.
P-BUILD-08 owns the remaining pressure. Apply targeted separation when the next story touches
that header, rather than selecting a build-system rewrite in advance.

BL-WORK-01 and BL-ADOPT-01 remain goal-coupled: an exercised warm authoring path does not establish
independent human onboarding. BL-WORK-02's simple example remains useful. BL-ARCH-01 stays parked;
this helper introduced no upward package dependency. BL-ARCH-02 continues as a subtractive duty.

## Next use and evidence

Return to a maker story that benefits from this foundation. The current recommendation and
alternatives live in the [inventory plan](inventory-command-presets-plan.md#next-maker-stories);
they are proposals for founder selection, not additional implementation authorized by this page.

The [implementation report](../../reportbacks/zen-interaction-authoring-RB.md),
[evidence](../../reportbacks/zen-interaction-authoring-evidence.md) and
[exploration](../../reportbacks/zen-interaction-authoring-exploration.md) retain the work and
measurements. The [merge consolidation](../../reportbacks/zen-interaction-authoring-merge-consolidation.md)
closes their historical CI dependency. The [execution packet](../../prompts/zen-interaction-authoring.md)
retains the original scope; current usage belongs in the product documentation.
