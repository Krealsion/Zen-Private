# Service succession with work left running

**Research and recommendation — 2026-09-11.** Follows the founder's proposal to redirect new
work while a Zengine manager supervises the old weave until it can retire. This explores one
of the [authored continuity choices](../goals/workshop.md#authored-continuity-and-repair);
it selects no production implementation or new Loom API.

**Disposition: preserved seam; further implementation and experiments parked.** The founder
considers the feasibility evidence sufficient for the main road to continue. No current
requirement depends on overlapping service generations. The
[Goal Map](../goals/workshop.md#roadmap-disposition-of-service-retirement) owns the current
priority and wake condition; this note retains the mechanisms and limits for a future consumer.

## Direction when a consumer needs it

Prefer a **Zengine-owned service policy using existing Loom mechanisms first**. Keep
the incumbent's instance, identity and required authority alive; change where newly admitted
work goes; retire the old instance only under a domain-defined completion or abandonment policy.
The manager takes responsibility for that process. Kernel and Switchboard retain their actual
artifact and instance custody.

Prefer the existing application owner of new work as the place to make this decision. For
presentation, that is the proposed presentation manager: it already decides which output
provider receives a picture. It can retain an old binding for outstanding work while selecting
a new binding for later work. A separate universal retirement service is not needed to prove
this first case. Keep the responsibility identifiable so another manager can own it later.

There are two useful implementations to distinguish:

| Approach | Fits when | What it does not supply |
|---|---|---|
| Move the public role with `commit_candidate`, keeping the former holder alive | A compatible service receives new jobs through that role, while existing jobs finish through answers or concrete instance addresses | Separation of other ingress, readiness/activation guarantees, or knowledge that work is finished |
| Keep an application-facing owner and bind each operation to a concrete worker | Existing and new work share message shapes, require follow-ups, or already have an application manager | Transparent forwarding of arbitrary identities, or knowledge of work outside its protocol |
| Use prepared admission and authored handoff | The domain requires a final boundary, state transfer and the incumbent's withdrawal from ordinary service | Continued ordinary service by the admitted successor's sealed predecessor |

For a future presentation consumer that needs overlapping service, start with the second
approach. Use a role-only switch where the simpler contract actually fits; do not widen prepared admission to cover every continuity
policy. A concrete capability gap in the first loaded experiment would justify revisiting Loom.

## What the current substrate permits

The low-level role-only commit already leaves both participants alive. Its mutation clears the
candidate's seal, clears the incumbent's role, and moves the role to the candidate. It neither
destroys nor reloads the incumbent. Kernel exposes a name-based wrapper over that same operation.
[Switchboard implementation](../../Loom/src/switchboard/switchboard.cpp), lines 1965–1991;
[Kernel wrapper](../../Loom/src/kernel/kernel.cpp), lines 1122–1136.

This differs from prepared admission, which seals the predecessor for retirement and admits
the successor with activation in one dispatch. The lower-level call does not inherit its
authenticated preparation, exact participant revalidation or transaction outcome machinery.
Its public contract is narrower. [API distinction](../../Loom/include/zen/switchboard/switchboard.hpp),
lines 883–913; [prepared admission](../../Loom/docs/reference/prepared-replacement.md#admission).

| Traffic or fact | After a role-only move |
|---|---|
| A new role-addressed request | Reaches the successor |
| A role-addressed request queued before the move, still undelivered | Also reaches the successor: resolution happens at delivery |
| An already delivered request's deferred answer | The incumbent can still answer as itself, subject to its grant and both participants remaining current |
| An authenticated answer to the incumbent's earlier outgoing request | Returns to that incumbent, even after it loses the role |
| A direct message to the old WeaveId | Still reaches the incumbent, including a new job sent that way |
| A publication accepted by both unsealed weaves | Can reach both; losing a role does not unsubscribe a weave |
| A follow-up or self-message sent to the former role | Goes to the successor, even if its author intended to continue old work |
| A new statement deliberately authored as the moved office | The old holder cannot author it |
| A statement authored as that office before the move | Keeps its historical office stamp, subject to ordinary delivery checks |

Sources: [routing and seal checks](../../Loom/src/switchboard/switchboard.cpp), lines 1613–1668;
[publication and office authorship](../../Loom/src/switchboard/switchboard.cpp), lines 1278–1407;
[answers](../../Loom/src/switchboard/switchboard.cpp), lines 905–927 and 1098–1141.
The probe below exercises the central continuation claims and several counterexamples.

Thus “stops receiving messages” must mean **stops admitting new work through the governed
entrances**. Old work may need replies, ticks, downstream results and other continuations.
An unaware incumbent is possible when its ordinary work protocol already makes those routes
and completion conditions available. It is not a property we can infer for every weave.

## Authority is several decisions

| Concern | Direction |
|---|---|
| Client reach to the public role | May remain unchanged across a holder change. An exact-id grant is a different permission and does not follow the role. |
| Incumbent's ability to finish | Retain the necessary send/observe authority on the old identity. Moving a role neither transfers nor revokes it. |
| Successor's ability to work | Give the successor its own host-approved authority. It inherits no grant merely by taking the role. |
| Outstanding answer rights | Leave them with the exact participants that earned them. Keeping the original instance can preserve them; copying them to a new worker cannot. |
| Permission to change grants or unload artifacts | Belongs to explicitly authorized host wiring or administrators, not to a manager by virtue of its name. |
| Files, graphics resources and native effects | Follow their owners' resource contracts. Message authority changes do not transfer these resources. |

Loom's effective message authority is baseline union delegated authority. The baseline is
immutable. A host-minted `GrantAuthority` can replace the delegated part for one subject within
its ceiling; it cannot subtract baseline permission or apply itself to the successor's id.
Authorization occurs at delivery, including for a queued answer. Revoking the permission to
finish can therefore turn a valid retained answer right into an undeliverable response.
[Capabilities](../../Loom/docs/reference/capabilities.md#live-delegation-grant-0);
[answer grant requirement](../../Loom/include/zen/switchboard/bus.hpp), lines 88–92.

Two present integration limits matter before promising a loaded manager:

- The ordinary Kernel load and `load_candidate` convenience path give permissive baseline
  sends. Revoking delegated permission cannot narrow those existing grants. An explicit-grant
  `Kernel::load` exists; a Zengine host adapter can compose it with sealing as appropriate,
  without a new loading primitive. Candidate native construction is still not a side-effect
  sandbox. [Load implementation](../../Loom/src/kernel/kernel.cpp), lines 1018–1120.
- Native participating weaves can use a supplied `GrantAuthority`. ABI v7's `ZenHostApi` has
  no delegation or role-commit slots, and its library-side bus supplies no delegation override.
  A loaded manager needs a scoped host-side conversation for those acts if it uses them.
  Define that bridge around authorized subjects and decisions rather than granting arbitrary
  Kernel reach. [ABI table](../../Loom/include/zen/kernel/abi.h), lines 218–310;
  [library-side bus](../../Loom/include/zen/kernel/export.hpp), `HostApiBus`;
  [default delegation refusal](../../Loom/include/zen/switchboard/bus.hpp), lines 287–301.

This is application wiring work, not evidence that Loom must change. The current Kernel control
door already supplies load/unload but not this retirement policy; Workshop's realization owner
and `PlanBooter` demonstrate a host owner with a message-facing bridge. Keep lifecycle facts at
their existing owners. [Control](../../Loom/include/zen/kernel/control.hpp), lines 187–260;
[realization](../../Zengine/agents/realization.md), lines 81–90.

## The manager's meaningful boundary

For each supported operation, retain the initiating intent, concrete owning generation and
the domain's current progress or completion fact. Select the active generation only for newly
admitted work; retain the old assignment for related messages. That record can stay small and
domain-specific. It need not become a universal obligations framework.

For a presentation example:

```text
new picture request       -> currently selected output binding B
completion for A's work   -> operation that still names A
late condition report A   -> A's observed condition, not B's active condition
retirement of A           -> A's concrete artifact instance, never the current public role
```

The manager's own record of B being selected is separate from a report that B produced output.
Provider A may continue useful work without remaining authoritative over the selected picture.
If A and B write directly to the same native window, changing logical routing alone cannot
prevent their physical output conflicting. Coexistence, interruption or exclusive-resource
transfer must be demonstrated for that medium.

Ordinary forwarding also changes who is speaking. A router that receives a request and sends
another request is a participant in two conversations; workers see the router. It must not
pretend to preserve the original caller's authenticated identity by copying a payload field.
Use a deliberate manager/worker relationship, or arrange for clients to address the selected
instance under appropriate authority. No universal transparent proxy is assumed.
[Host-only identity injection](../../Loom/include/zen/switchboard/switchboard.hpp), lines 543–551;
[ordinary relay response](../../Loom/include/zen/weave/relay.hpp), lines 123–135.

Retirement is established by a domain closure condition: the governed admission path is closed
to new work, its required operations and effects have completed, and resource release is permitted.
An empty queue, no recent message or an empty local AskBook cannot establish all of that. The
worker can remain unaware of retirement if ordinary completion facts suffice. Otherwise the
application needs an authored query, cooperative quiescence, an explicit discard policy or
honest indefinite waiting. Inability to establish completion is not evidence of completion.

Bound the number of retiring generations and retained operations. At capacity, refuse another
transition or offer an explicit policy decision. A timer expiring must not silently redefine
unfinished work as finished. A failed manager also needs a route for another authorized owner
to reconstruct the actual participants and outstanding obligations it can establish; installed
authority survives the administrator's death.

When removal is appropriate, identify the retired **instance**, with a unique loaded name and
revalidated identity. `UnloadRole(public_role)` after cutover selects the successor. Merely
retaining the old name without preventing its reuse is insufficient for delayed cleanup.
[Kernel unload](../../Loom/include/zen/kernel/kernel.hpp), lines 266–305;
[authority administrator lifetime](../../Loom/tests/test_grant.cpp), near line 892.

## Keeping old code is not freezing its whole world

This matters especially for the spell example. Zengine's composite operators resolve through
the current catalog when invoked. Keeping the old weave instance and image alive does not
make its next operator call use the old provider. A live overlay can change what an existing
composition spends without rewriting its graph. [Operator resolution](../../Zengine/docs/reference/operator-providers.md#resolution-happens-at-spend);
[loaded consumers](../../Zengine/docs/reference/operator-host.md), lines 157–161.

An author can reasonably want either live dependency updates or a stable set of implementations
for an effect's lifetime. State which one is promised. A stable dependency set needs an authored
resolution/versioning arrangement and its own lifetime evidence; the current retirement proposal
does not supply one or overturn the current resolve-at-spend law.

The paused native `maker/` succession path is a useful precedent for a Zengine-owned ceremony,
but implements a different policy: cooperative Quiesce, authored conversion, prepared admission,
then explicit host removal. It uses native interpreter objects, not Kernel-loaded workers, and
does not prove unaware-incumbent draining. [Maker succession](../../Zengine/maker/succession.hpp),
lines 268–286; [its law](../../Zengine/agents/maker/succession.md), lines 82–108.

## Evidence and its limits

Inspected identities: Loom `eee04550dfbae61638ff84f1c9da1c32ad90f9b0` (source tree matching
accepted `f20f32df01e36ae672cef8013ea4499b76e3954c`); Zengine
`9cbf5a5ac8d4751472dc891371401d93a25e03cc`; private START
`2a4be2146e3d2a3866f7f81613bd8a9ffde13897`, clean. No remote refresh is claimed.

The isolated [probe source](C:/Users/Joshua/Documents/Codex/2026-09-08/https-github-com-krealsion-loom-https/work/service-retirement-research/probe.cpp)
was freshly compiled under WSL Ubuntu 22.04, GCC 11.4.0, Debug, using the existing unmodified
Editor-integration Loom installation. Six relevant current source/header hashes matched the
reused source, and installed headers matched where applicable; that identity record is beside
the probe. This was a focused native-participant experiment, not an official verification lane.

Final configure, build and probe each exited 0; **17 checks passed**. They included:

- old incoming deferred answer and outgoing dependency answer surviving role-only movement,
  with their authenticated-answer provenance checked at the recipients;
- an undelivered pre-cutover role request reaching the successor, while the old instance stays
  alive and unsealed;
- direct/broadcast traffic still reaching the incumbent and loss of its ability to author as
  the moved office;
- delegated authority enabling work, revocation blocking already-queued traffic, and baseline
  authority surviving delegated revocation;
- an empty queue while the old weave still has unfinished work.

The [final output](C:/Users/Joshua/Documents/Codex/2026-09-08/https-github-com-krealsion-loom-https/work/service-retirement-research/probe.log)
and command exit files are retained with the source and runner. No actual output-provider
coexistence, loaded-manager bridge, dependency pinning, manager recovery, OS containment or
performance claim was tested. The experiment validates building blocks, not an implemented
service retirement system. Existing [Kernel tests](../../Loom/tests/test_kernel.cpp), lines
4246–4269, separately assert both loaded artifacts remain Live after a low-level commit;
they were source-traced, not rerun here.

Five of five review areas completed: traffic/continuation, authority, instance/resource custody,
current Zengine ownership/dependencies, and fit/ceremony. A bounded independent source review
checked routing and the existing maker succession path. No Loom or Zengine source was changed.

## Possible investigation after the seam wakes

This experiment is parked; it is not the next development task. Revisit it when a concrete
consumer needs successor service before the incumbent finishes, or a change threatens to
close that possibility.

Extend a selected presentation experiment with two real loaded output-like workers and one
owner of new work. A has a delayed operation; B becomes selected for later work; A then completes under
its original identity. Show all three facts independently: **B selected, A still working,
A retired when permitted**. Keep the actual host actions behind the proposed scoped bridge,
including explicit grants and cleanup by concrete instance.

Exercise one candidate refusal, one old continuation delivered after selection, stale cleanup
aimed at the wrong generation, an authority change that would block completion, and an old
worker that never reports completion. Include a direct/broadcast bypass as a deliberate limit,
not as something the manager silently claims to prevent. Then test the actual Skin resource
boundary before promising that two real media can coexist. Define the output-selection claim
and completion predicate for this witness; do not solve all continuity policies at once.

This extends the same maker experience already proposed: revisit a pending transition, inspect
what is known and missing, and perform one authored intervention. It does not resolve Editor's
separate cross-owner document/presentation commitment or authorize resuming PR #23.

Related backlog/pressure: BL-WORK-01 and BL-WORK-02 favor keeping ordinary authoring simple;
BL-WORK-03's Editor obligations remain open. P-WORK-14 remains the concrete need for readable
retained evidence. P-LOOM-03 is now relevant to the retirement design because a supervisor can
die while its installed authority and workers remain; include recovery/revocation ownership
when scoping implementation. BL-ARCH-01's include debt is not triggered by public-source edits,
and this study keeps new mechanism proposals outside mandatory law under BL-ARCH-02.
