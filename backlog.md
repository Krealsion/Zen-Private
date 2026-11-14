# Zen backlog

**What it holds:** the work Zen has decided it owes and has not finished, in the order it runs.  
**Updated:** 2026-10-27, rewritten short. The old file is kept whole as
[history/closed_work.md](history/closed_work.md): every closed arc, and the full story of each
item below up to that day.  
**Beside it:** [pressure.md](pressure.md), pressure that may become work;
[ideas-2026-10-27.md](ideas-2026-10-27.md) and [ux-batch.md](ux-batch.md), asks not yet filed.

## How this file works

- An item is here only once Zen has decided the work is owed. Possibilities, seams and pressure
  stay in pressure.md until then. Nothing here is authorized work until a prompt says so.
- Each item says what it is, where it stands, what starts it, and where its prompt, report or
  issue is. No history: a round's story is its report, and a closed item's goes to
  closed_work.md.
- Bounded work goes to a GitHub issue, filed by Vision's prompt under `UnknownWorkers` with the
  labels set in the founder's name; a filed item keeps one line in section 6. A security defect
  is never a public issue: it goes into a draft private security advisory.
- An issue's pull request merges first, and an open phase branch rebases onto it.
- A prompt not yet run waits in `prompts/unrun/` (constitution section d).
- Issue and pull request numbers written before 2026-11-01 are the `-history` repositories'; an
  open issue was carried to a new number ([map](relicense/issues-map.tsv)).

## 1. Now: the wave

Four lanes run at once on three build slots: two work slots at 8 jobs, one final slot at 4
(constitution section f). WSL has 48 GB.

- **The baseline** (the founder, 2026-11-08): after the two researches (several roles, owned shape
  names), complete what is known through the Workshop split, stopping only for obviously correct
  detours; concerns are marked here and readdressed at the end. The issue lane runs: Raid, a Cursor
  cloud agent under `UnknownWorkers` from its fork (the founder, 2026-11-09), its first four
  Zengine#125, #126, #127 and #129 reviewed 2026-11-09 and ready. Cursor's footers and its hidden
  marker were taken off their bodies before the merges, which copy the description into `main`'s
  message. #126 is re-authored as `563f6986`, the
  reviewed tree; #127's MSVC red has Raid's fix, `18df54d6` (U7 asks `status` until the run
  settles), green; #125's run predates #124, so it is closed and reopened for a fresh run before
  its merge, and its picture is retaken in the next picture round. The attribution guard's issue
  is #128 ([draft](../issues/attribution-check-ai-identities.md)), Raid's #129 its fix; Loom's
  copy of the predicate follows in an issue of its own. Merged 2026-11-09 in Vision's order, each a merge
  commit: #129 (`0998847d`), #126 (`fcf49556`), #127 (`4ccf743d`); #125 closed and reopened, its
  fresh run started with no approval (`UnknownWorkers` now a contributor), then merged
  (`b55aca8c`), `main` green on every merge; Raid's batch
  ([issues](../issues/raid-batch-2026-11-09.md)) next.
  Concerns for the end: `PaneRefusalRequested` (#126) lets any seated pane have Workshop say a
  sentence as its own refusal notice, and `act` hears it as one; for the Builder the words are
  Workshop's own verdict, but the notice should say whose refusal it is. The audit of 2026-11-09,
  sorted into seven groups ([its page](drafts/audit-2026-11-09.md)): its small fixes are the lane's
  issues ([batch](../issues/raid-batch-2026-11-09.md)), its two security findings Ceecee's private
  round ([prompt](../prompts/private-security-pair.md),
  [report](../reportbacks/private-security-pair-RB.md), reviewed 2026-11-09): two draft
  advisories, the session key's fix made, the schema id's weakness assessed. Decided (the founder,
  2026-11-09): a key the host cannot make owner-only is refused, FAT and exFAT among them, so
  session folders live on NTFS; the schema id's option A, structure compared wherever the id
  decides agreement, before release; the key's advisory published once its fork holds the
  refusal, the schema's once its fork holds A. The continuation
  ([prompt](../prompts/unrun/private-security-pair-continued.md), hot) lands both before Loom's
  next rounds; the lane's `loom-host` catch issue waits for the key's advisory. Its one-way doors
  and its structure the end's.
  #129's three follow-ups: a re-run reads the description its run started with, so the refusal's
  "edit the title or the description" wants "then push, or close and reopen"; its self-test pins
  Cursor's hidden marker as passing, the founder's call whether it is a credit (stripped before
  these merges, so refusing it later fails no commit on `main`); its self-test footer carries the
  real agent link from #125, where a made-up one does the same. Approval: GitHub checks a pull
  request's author and the event's actor; #125's and #129's runs, from opening, name
  `UnknownWorkers`, and #126's and #127's, from Raid's fix pushes, `cursor[bot]`, so a fix push may
  still wait for approval after `UnknownWorkers` has a merged pull request.
- **Loom's foundation** (the founder, 2026-11-10): a cold audit of Loom and Zengine
  ([its text and Vision's check](drafts/audit-2026-11-10-foundation.md)) found Zengine building
  around gaps only Loom can close: no union kind, no data plane, nothing synchronous and nothing
  at a weave's creation, no deadlines. Its claims held in the source, some overstated (Sense
  already reads a claim synchronously) and some already moving. The founder's goal: things
  shrink, no god-file growing back; he expects the union to open the path. Researched
  ([prompt](../prompts/loom-foundation-research.md), warm) with the replacement research's floor,
  takeover and L2 folded in, twice: Ceecee's ([report](../reportbacks/loom-foundation-research-RB.md),
  fourteen decisions) and the auditor's run of it
  ([report](../reportbacks/loom-foundation-auditor-RB.md), eleven), reviewed 2026-11-11
  ([Vision's review](drafts/foundation-research-review-2026-11-11.md)). They agree on the union,
  values that never change once admitted, blobs, deadlines, an ABI that grows and the order (the
  union with the seam, then the floor); seven choices differed, each with Vision's lean. Decided
  (the founder, 2026-11-11): a weave is handed one gated value at creation, data and never doors,
  with its load; a call is a function of its argument alone, provided by a role's holder; the
  measure is the census of doors a weave, exact both ways, a class-lines ratchet beside it, and no
  cap in Loom; joint publication is asked again after the floor and deleted if the opening does
  without it; Loom#17 keeps v12, 13 is the last exact break, and every change after it still
  moves the number while older images load. Evolution after the release is a research of its own
  that tries both (doors open to declared extensions; an authored migration helper), tools
  welcome. The open set (choice 3), decided after Vision's corrected lean: a kind for any
  registered shape, in the union's round, the gate checking a nested value at the send and a weave
  nesting only what it may send; `implied.hpp` goes in that round's Zengine half (a node's operands
  by the union, an element's changes by the kind). The founder's rule with it: "we are not waiting
  for it to hurt anymore", so the research's items hooked to a trigger (a buffer two weaves see, a
  shape that contains itself, the pipe's request frame, a link that carries blobs, capabilities as
  tokens) are ordered by the plan, none waiting. `HostContext::interaction_now` is
  the rigs' clock, not dead as Ceecee's report says; the founder wants it test-only, so it leaves
  with the deadlines round's Zengine half, the hub reading no clock. The union removes no handler
  from the hub: its doors leave with the facts' owners, calls and the floor. F1 follows the
  union's round and the seam's, both ready to prompt; the open pull requests stand. Workshop moves to its own
  repository after Loom's gaps close. `app/` leaving `workshop/`'s headers is Zengine's ZR (the
  realization owner a participant), free since the stranger research's seven decisions were taken
  (the founder, 2026-11-11), and prompted for 2026-11-13.
- **The files every session reads, kept true** (the founder, 2026-11-12; a side lane,
  [prompt](../prompts/unrun/instruction-drift.md), warm): another tool's audit of the routers
  (`Zen/Claude outputs/prompt-audit-2026-11-12.md` and its diff) found four stale names and a
  machine timing, each holding on Zengine `main` by Vision's check, and no dated prompting. The
  lane widens it to the constitution, the memory store, the kit's README and the much-read pages,
  fixes what is stale (the constitution and the memory store proposed, not edited), and lands a
  documentation-lane check that every backticked name resolves; at its end the audit's two files
  go, and `local/batch-137-138` is force-deleted if the primary is free.
- **The lanes of 2026-11-13, evening** (Vision's prompts, on the founder's word that day). Merged
  first (the founder, 2026-11-13): Loom#26 and #29 (Loom `main` `003cff6`), Zengine#161, #160 and
  #162 (`c9ac655a`). Decided with them: the review's leans; for the game-time research's decision
  7, after a detour (Vision's field stamped by Loom, withdrawn: Loom does not write a sender's
  fields), the founder's form: the turn's time attached to every delivery whatever its source, an
  optional fact a handler reads or ignores (`mail.turn_ms()`), which is the research's TT as
  leaned; the turn's time is the steady clock's, the date the calendar's, read together when the
  wait ends, and nothing schedules on a date. Loom, one session: the
  wait's leftovers ([prompt](../prompts/loom-wait-leftovers.md), warm, the chain's first),
  then the control door and the Weave Manager keeping the answers they owe
  ([prompt](../prompts/loom-own-respondents.md), hot; before ZF), then TT, added to the chain
  after it began ([prompt](../prompts/loom-turn-time.md), hot). Zengine, one session:
  `main`'s reds ([prompt](../prompts/zengine-main-reds.md), warm: the MinGW-w64 flake, the
  night package's publish step, the four slow sanitizer entries), #163 onto `main` with
  `PlanWhere`'s state an enumeration
  ([prompt](../prompts/zengine-realization-participant-rebase.md), hot), then the union's
  last four items ([prompt](../prompts/zengine-union-spent-continued.md), hot). Beside them,
  Neovim on the wait's time, G3 ([prompt](../prompts/zengine-neovim-wait-time.md), warm).
  The lane ([batch](../issues/raid-batch-2026-11-13b.md)): one Loom issue, the four lists of the
  documentation checks missing `census` and a check's entry after its path read by `doc_names`.
  Reviewed (Vision, 2026-11-13, night): every pull request green on its head, and the text checks
  passing on trial merges of Loom's three and Zengine's five. Loom#30 (`0c89189`,
  [report](../reportbacks/loom-wait-leftovers-RB.md)), then #32 (`cae56cc`, ABI 16,
  [report](../reportbacks/loom-turn-time-RB.md)), then #31 (`ac9fe50`,
  [report](../reportbacks/loom-own-respondents-RB.md)), its one conflict, `docs/CONTEXT.md`'s
  router row, resolved in GitHub's editor (#31's row kept, #32's after it: the tree the trial
  merges built). Zengine#165, #166, #167 and #168
  ([report](../reportbacks/zengine-main-reds-RB.md)), then #164, G3
  ([report](../reportbacks/zengine-neovim-wait-time-RB.md)), merge clean together. Asked, with
  Vision's leans: Loom's run record on Windows, refused while a reader holds `run.json` and retried
  only at the run's next change (J4's red; #167 only names it) -- the manager retrying a stale
  record on its own, option (a), in a Loom round with the run manager's stamps split (a handler's
  from its delivery's date, TT's follow-up); a night publishing an older commit after a workflow
  change -- waiting, as #166 does, with no stored token holding `workflows`; #30's one `watch_own`
  set, all or nothing -- several own sets, each held or refused alone. ZTT, the Neovim bound's
  extra wake among its uses, follows #32's merge.
  Merged (the founder, 2026-11-13, night): Loom#30 (`16b7f68`) and #32 (`d824033`); #31's conflict
  resolved in GitHub's editor (`6b8d614`, its tree the trial merges'), its run going. Zengine#165,
  #166, #167, #168 and #164 (`main` `894309fb`). #163 reviewed the same night
  ([report](../reportbacks/zengine-realization-participant-rebase-RB.md)): rebased onto
  `c9ac655a`, its first two commits as reviewed (the census's `lines` block resolved, the second
  unchanged), the third the review's ask: `PlanWhere::state` the enumeration `PlanState`
  (`loading`, `waiting`, `complete`, `refused`), the four word constants gone, a guest still told
  the word (`spelling`). Green at `f34ffad1`; merged onto `894309fb` it is clean, the nine text
  checks pass, and no case count moves in a pieced part. Ready. Asked, with Vision's lean: Loom's
  public spelling of an enumerator and its reverse (`loom::spelling`), which Loom's `ask_ended.hpp`
  and Zengine's `PlanState` each write by hand -- in Loom's next round, Zengine's copy then gone.
- **The overnight lanes of 2026-11-13** (Vision's prompts, on the founder's yes that day; three
  sessions side by side, every stage its own pull request from `main`, each Green the standard
  delivery). Lane 1, Loom: Loom#26 rebased onto `main`
  ([prompt](../prompts/unrun/loom-names-check-rebase.md), warm), then the floor in process, F1
  ([prompt](../prompts/unrun/loom-floor.md), hot: `mail.ask` and `ask_role`, refused for a weave
  that does not accept `zen.AskEnded`; that notice a union of the four stages, each ending of the
  research's 2.4 told where it is made; `kMaxDeferredPerWeave` under a raised Loom-wide bound; the
  helpers ending; ABI 15 appended, 14's image loading; the bus's census rows falling, the ask's
  record a unit the bus consults), then the wait's leftovers
  ([prompt](../prompts/unrun/loom-wait-leftovers.md), hot: `WaitSet`/`Waited` v1 gone; a
  `BridgeClient` wait set, so `loom-host` rests with links mounted and `kLinkLookMs` and
  `kServeLinkLookMs` go). F1 builds the replacement research's leans on its decisions 1 to 4 and
  16, which the founder ordered but did not take one by one. Lane 2, Zengine: the union spent,
  now from `main` ([prompt](../prompts/unrun/zengine-union-spent.md), warm: the class-lines rows a
  ratchet first, the act tool spelling a lone Shift, the Timer's three gaps), then the realization
  owner a participant, ZR ([prompt](../prompts/unrun/zengine-realization-participant.md), hot: the
  booter and the executor one weave in a folder of its own, its readings claimed, `HostContext` 18
  to 14, the app's four `line` rows gone, a trial merge with the union's branch). A third session:
  game time and the frame clock, a research ([prompt](../prompts/unrun/game-time-research.md),
  warm; P-WORK-85).
  Reviewed 2026-11-13, each holding and green on every job
  ([reports](../reportbacks/loom-floor-RB.md) and beside it): Loom#26 rebased, both checks kept
  (13 of 13); Loom#29, the floor at ABI 15 (13 of 13): `zen.AskEnded` a union of four stage
  enumerations, every ending of 2.4 told where it is made, `kMaxDeferredPerWeave` 64 under 1024,
  the kept answers a unit (`switchboard/asks.hpp`), the bus's rows falling (4107 to 4105 lines, 154
  to 153 members), one door appended (15 to 16), 14's image loading; #26 and #29 merge clean, six
  text checks green on both. Zengine#162, the union's first five items (10 of 10): the class rows a
  ratchet, the guards gone and each `Kind::Message` comparison decided, `Moment` a union of input's
  six shapes (`InjectInput` and `AttributedInput` 2), the act tool spelling a lone and a double
  Shift, the census reading hand-built shapes, the Timer's three gaps; items 4 to 7 not done (the
  session's whole-diff read before the push skipped, Vision's read of the hunks found nothing).
  Zengine#163, ZR (17 of 17): `realization::Owner` one weave in `realization/`, installed and
  exported, claiming `PlanWhere` and `ChoicesHeld`; `HostContext` 18 to 14, the app's four `line`
  rows and twelve more gone; it conflicts with #162 in the census's `lines` block only (resolved
  by its trial; nine text checks green on all four Zengine pull requests together). Vision's ask
  before #163 merges: `PlanWhere::state` (four words) an enumeration, the open-set decision's
  closed set, with the rebase onto #162. Raid's #160 (3 succeeded, the rest skipped as a text
  change) and #161 (10 of 10) meet their issues; #161 takes packaging.md one step and the three
  unbudgeted pages rows (operators 7, realization 8, panes 19). The game-time research
  ([report](../reportbacks/game-time-research-RB.md)): real time stays the wait's, a date its
  second reading, a world's time a Zengine world clock serving the Timer's shapes; the frame clock
  the window's own claim, a frame's time its due time; rounds TT (Loom, the turn's time and date as
  delivery facts), G1 world time, G2 the frame clock (V5's first stage, after ZU's rest), G3
  Neovim on the wait's time, ZTT. Asked, with Vision's leans: the floor's two (Loom's control door
  and Weave Manager keep their answers, in a round before ZF: yes; the run-time refusal for a
  `WeaveBase` asker stands: yes); the union's items 4 to 7 a round of their own (yes); #26's two
  (`census` added to the lists of the lane's checks, and the routing table's parenthesized name
  read as an entry: one Loom issue); the research's twelve (all as leaned; TT the founder's own
  call, since every delivery would carry the turn's time). Found beside them: Zengine `main`'s
  MinGW-w64 job failed on two push runs (#151's `344b42d`, #156's `ff4722d0`) and passed on the
  scheduled run of `ff4722d0`, an intermittent case not yet named (its log is behind sign-in); the
  night package of 2026-11-13 (`b8fa0e3`) failed at its publish step; four sanitizer entries are
  past VM-LANE-27's 600 s (`workshop_panes_hand_2` up to 946 s, `hand_4` 732, `panes_info_8` 659,
  `workshop_desk` 607) and the sanitizer build peaks at 14.4 GB. The wait's leftovers wait for the
  founder's restart, warm.
- **The next two lanes** (Vision's prompts, 2026-11-12, on the founder's yes that day; two
  sessions side by side). Lane 1, Loom: the seam that grows
  ([prompt](../prompts/unrun/loom-seam-grows.md), warm: ABI 13, the last exact break; each table
  and a delivery's facts saying their size, the addressed role (L3) the delivery's first new fact,
  the manifest's version read before `create()`, an image from 13 on loading on every later host,
  12's image kept and refused; Loom's census of 8.3 beside it), then the creation value on its
  branch ([prompt](../prompts/unrun/loom-creation-value.md), hot: one gated value at a weave's
  making, data and never doors, from a boot row, a load request, the console and a native mount;
  the first append, 14, the seam's kept 13 image shown loading). Lane 2, Zengine: the Timer over a
  deadline from `main` ([prompt](../prompts/unrun/zengine-timer-over-deadline.md), warm: the
  census's door, hook and class rows first; `Drive`, `TimerRest`, `timer::Rest`, `kBeatCapMs`,
  `HeldBeat` and the virtual step gone; the Timer hearing `zen.DispatchRefused`; `interaction_now`
  out of `HostContext` and no clock read in a handler; the suites on a `ManualClock`, P-BUILD-23),
  then the union spent on its branch ([prompt](../prompts/unrun/zengine-union-spent.md), hot: the
  guards and the `Kind::Message` comparisons; input's moments and a drawing's operands as unions,
  `implied.hpp` deleted; the open sets on the any kind; the hub's window events one door where one
  concept; the spelled kinds counted; the shapes built by hand in the shapes census). The union
  round stacks on the Timer's, not from `main` as first said, since it lowers the census rows the
  Timer's lands and both touch the window's and input's files. For the merges: each lane's hosted
  runs read the other repository's `main`, so whichever merges second runs again, a Loom pull
  request closed and reopened (P-BUILD-24); Loom#20 rebases once more if the seam touches
  `host_main.cpp`. Queued behind them, ordered and none waiting: `WaitSet`/`Waited` v1 dropped
  from Loom once lane 2's Timer merges; a plan row that says its host waits on its role
  (`loom-host` trusts none), in round P; a loaded weave handed an open field of a shape it never
  declared (the union round's hook), an appended delivery fact after the seam; game time and the
  frame clock (P-WORK-85); the spelled kinds the union round leaves; then ZR, the pane contract's
  round 4, the line's round 2 and the private content-id round.
  The seam's stage done (Loom#27, its report in `unreviewed/`), green but its Zengine stranger.
  The Timer's stage stopped for room, not a problem (its report, 2026-11-12): the product built and
  pushed on `timer/over-a-deadline` `86b4297`, the census's door, hook and class rows with it, four
  suites still on the beat. Decided (the founder, 2026-11-12): its choice 3 stands, the hub a
  source of the host's wait handed its time, one door (93 to 94) in place of `interaction_now`'s
  hook (19 to 18), the rise said in the pull request; the census's check as built. A fresh session
  finishes it ([prompt](../prompts/unrun/zengine-timer-over-deadline-continued.md), warm), the page
  under its budget first ([prompt](../prompts/unrun/packaging-page-under-budget.md), read by it):
  Zengine `main` is red since #150, `agents/packaging.md` at 16,712 of 16,384 bytes once #148's
  and #150's additions met, which holds Loom#27's stranger and #152. Vision's miss: #150's trial
  merge was read as text, its checks not run on it. For later: the guest door's first claim is made
  by its host (choice 5), since Loom never activates a weave its host registers -- a Loom seam.
  Reviewed 2026-11-13, the continuation holding
  ([report](../reportbacks/zengine-timer-over-deadline-continued-RB.md)): #155 (the page at 16,341
  bytes) green, merging first; the Timer's branch `22bd532` builds whole, its official lane 97 of
  100, the product 742 lines in and 963 out, the guest door's lost re-claim found and fixed. Two
  reds stand -- `workshop_neovim`'s case that made the pane speak by refusing its beat, and
  `guest_journey`, a guest's input session unanswered with the door woken no more after the plan
  loads -- and no pull request: it was held for green lanes, as the prompt's Green read, where the
  standard delivery opens it after the local proof. Vision's trial of every open Zengine pull
  request with the text checks run on the result: #155 then #152 is red in `doc_names`
  (`tests/doc_names.txt`'s `run.cmd` and `run.sh` rows, needed by no page once #155 cuts their
  sentence), so #152 drops them as it rebases; with that, #155, #152, #153, #154 and the Timer's
  branch pass all nine (the packaging page's exported-targets line resolved, 16,166 bytes). Asked:
  the letter's pause; Vision's lean, the letter measured from a time handed at the ceremony where a
  wait holds the Timer, from its last wake only where none does.
  Decided (the founder, 2026-11-13): that lean, option 3. #155 merged (`b8fa0e3a`); Loom#27 merges
  once its stranger is green. A third session finishes the stage
  ([prompt](../prompts/unrun/zengine-timer-over-deadline-continued-2.md), warm): #152's two rows
  first, the two reds, the letter's pause, then the pull request by the standard delivery; a fix the
  guest's wake needs in Loom is a Loom pull request of its own, merging first. The union stage waits
  for a session of its own after the Timer's pull request.
  The lane's three reviewed 2026-11-13, each holding: Zengine#154 (#146's mutant, its hunk the code's
  present text, caught and restored green), #153 (#147's cut on every machine, two marks and a
  seven-row room; red one row early, green restored; the population floor 207, announced in its
  proposed idea), Loom#20 (rebased onto `3d0f684`, #23's loop unchanged inside its try, both builds
  the same version, the fault build not installed, the title's period gone). Every red on them is
  Zengine `main`'s of #150 (#20's stranger resolved Zengine five minutes after #150 merged). Vision's
  trials: each merges cleanly with every open pull request, the text checks green on the result
  (Zengine with #152 and the Timer's branch; Loom with #27 and #28). For the merges: #153 and #154
  closed and reopened for runs on `b8fa0e3a`; #20's stranger re-run, or closed and reopened if #27
  merges first. For Raid's next batch: a commit subject names no issue number (#153's ends "(#147)",
  which `main`'s history reads as a pull request's).
  Merged 2026-11-13: Zengine#153 and #154, Loom#20 (`9e2d822`). Reviewed the same day, holding:
  Loom#27, the seam ([report](../reportbacks/loom-seam-grows-RB.md)): `ZenWeaveAbi` opens with
  `abi_version`, `size`, `host_size` and `manifest_version`; `ZenHostApi` and `ZenSenseBy` start with
  `size`; `handle` takes one `ZenDelivery`, the addressed role its first new fact, written by the bus
  at dispatch; one reading of a descriptor (`zen/kernel/descriptor.hpp`) for the kernel, the box and
  the isolated child, refusing before any slot what is older than `ZEN_ABI_OLDEST` (13), newer than
  the host, short of `handle`, larger in its host table, or of another manifest; 12's header kept
  with its hash and its image refused, 13's kept for the next append; Loom's census (switchboard
  lines and `Switchboard` members falling, `ZenHostApi`'s doors exact). Zengine#152 and Loom#26
  green; the trials: Zengine `main` with #152 passes all nine text checks; Loom #27 and #26 meet in
  `tests/text_checks.cmake` (each adds one check and its file to the two lists; both kept, all six
  checks pass with #28 on top), so #26 rebases after #27 in the next Loom session; #156 meets #152 on
  the packaging page's exported-targets line, resolved at its review.
  Loom#27 merged (`76f0e37`). Loom#28, the creation value, reviewed 2026-11-13, holding
  ([report](../reportbacks/loom-creation-value-RB.md)): `ZEN_MADE_WITH(Setup)` and a constructor
  taking `const Setup&`; ABI 14 appends two slots, `describe_creation` (the shape, no instance
  needed, since the manifest is read from one) and `create_with`; one judgement,
  `loom::judge_creation`, against the image's own declared shapes, for load, reload, candidate,
  the isolated child and `loom::mount_made<W>`; the value from a boot row's `creation`, `start
  --with`, `LoadLibrary` v4 and `zen.LoadWeave` v3, carried as the value's JSON form in text until
  round P carries it as itself (the bus's registry holds no artifact's shape before its load); a
  reload keeps its value, a prepared candidate names its own, `zen.SwapWeave` makes with none (it
  leaves with T2); the seam's 13 image loads and works here, a 14 image refused by a 13 host by
  version. `local/batch-137-138` deleted at its end, at last. Retargeted to `main`; its one run
  predates Zengine's fix, so it is closed and reopened before it merges. #26 is now in conflict
  with `main`, as foreseen.
  The instruction-drift report reviewed 2026-11-13 ([report](../reportbacks/instruction-drift-RB.md));
  Zengine#152 merged (`8a822fed`). Decided (the founder, 2026-11-13), its 1 to 7 as Vision leaned:
  the constitution's three stale sentences applied (`9ae64582`, with the orientation's opening
  guard now "build what it calls for whole, whether or not anything needs it yet; say what a piece
  is for before building it"); the memory store's three sentences
  (`reportbacks/instruction-drift/memory-proposed.diff`) for Ceecee's next session, the machine
  fact they move written into `private/relicense/README.md`; the 16 pass-tools folders without an
  entry listed keep-or-go by the next Ceecee session for the founder's yes; the decision records'
  dead names kept as history; "`component/` knows no medium" into Zengine's law, and suites named
  in plain sentences read by the names check, both Raid issues. Asked back on 8 (the packaging
  page's three targets): the founder's idea, a page that cannot be shortened without losing
  information or clarity takes a raised budget in 20% steps, asked for in the report, the raised
  pages the release's list of what to bring down.
  Decided (the founder, 2026-11-13), as Vision shaped it: shorten first; a page whose cut would lose
  information or clarity takes its kind's default plus 20% a step, each step asked for in the
  report and approved by the merge; one table, each row exact (the fewest steps that hold its
  page); the three unbudgeted pages get rows; the table is the release's list. The lane's batch
  ([issues](../issues/raid-batch-2026-11-13.md)): the steps, with the packaging page's three
  targets as their first use; `component/` knows no medium as a law; suites a sentence names read
  by the names check; and a commit subject names no issue number.
  Final merge check 2026-11-13: Zengine#156, the Timer over a deadline, holding
  ([report](../reportbacks/zengine-timer-over-deadline-continued-2-RB.md)): green on every job and
  on Package at `4216757` over `main` `8a822fe`, the nine text checks green on the merge; the
  guest's "missing wake" was a journey leaning on the beat's timing (the door answered at once, the
  Input row not yet loaded), so the journey asks where the plan is first, as WL-GUEST-12 offers; the
  letter written at the next wait, after what is due then fired, at once where no wait holds the
  Timer; a Workshop nothing can reach now ends (the Package judges' starts pass a guests file).
  Asked, Vision's lean taken to the floor's and takeover's rounds (F1, T3), which design a weave's
  owed answers across a reload: a reload while a letter waits drops its asks (one wait wide), and
  a reload measures from the last wake since no ceremony hands the time first. Loom#28 green on a
  fresh run over `76f0e37`. Loom#26 still in conflict: its rebase
  ([prompt](../prompts/unrun/loom-names-check-rebase.md), warm). Queued: the union stage's prompt
  from `main` once #156 merges, its census rows there, and the class-lines rows marked to fall (the
  decided ratchet; the census holds them exact but unmarked, so the hub's 1825 to 1841 passed);
  `zengine.guests.md` saying a guest asks where the plan is first; the act tool spelling a lone
  Shift; the kit's loop building the libraries a suite loads by path, and `kit.sh end` reading a
  phase's continuations. Both merged (the founder, 2026-11-13): Zengine `main` `ff4722d0`, Loom
  `main` `04c24ea`. Every item queued here is in the night's prompts (the lanes of 2026-11-13,
  above) but `kit.sh end`'s, which waits for the kit's next round.
- **The overnight lanes of 2026-11-12** (Vision's prompts, two sessions side by side, beside
  Workshop's line round 1, which runs in Zengine): lane 1, the union
  ([prompt](../prompts/unrun/loom-union.md), warm: `Kind::Union`, the kind for any registered
  shape, nested values made and never adopted, the gate's budget; the manifest's version, not the
  ABI's), then Loom's own hand-made unions onto it on its branch
  ([prompt](../prompts/unrun/loom-own-unions.md), hot; its end force-deletes `local/batch-137-138`
  on the founder's word). Lane 2: deadlines in the reactor ([prompt](../prompts/unrun/loom-deadlines.md),
  warm), the one-host research ([prompt](../prompts/unrun/one-host-research.md), hot), the
  schema-evolution research trying both answers ([prompt](../prompts/unrun/schema-evolution-research.md),
  hot), then #145's follow-up, the install's downloads cached by the snapshot's date and its time
  limit in words of its own ([prompt](../prompts/unrun/package-download-cache.md), hot; the
  founder, 2026-11-11). The seam round waits for Loom#17; the Zengine halves (the union spent, the
  Timer over a deadline with `interaction_now` gone) follow their Loom rounds' merges.
  Reviewed 2026-11-12, every stage holding ([reports](../reportbacks/loom-union-RB.md) and beside
  it): Zengine#148 (the line's census, both ways, every row falling, and twelve closings; forward
  includes 49 to 30, reverse 47 to 42; Workshop configures whole as a stranger, stopping at closing
  15) merged; Loom#23 (deadlines; `WaitSet`/`Waited` 2, v1 read and answered in kind) merged;
  Zengine#149 and #151 merged; Loom#24 (the union, the kind for any registered shape, nested
  values made in their cell, P-LOOM-23 closed) on its stranger's re-run, then Loom#25 (Loom's own
  `Crossed`, history record and UI node as unions) retargeted to `main` and run again; Zengine#150
  (the download cache) still running. Decided with them (the founder, 2026-11-12): #148's
  tutorials installed by Zengine already exported, read by Workshop's launcher as installed data;
  the census with no base says so and passes. The researches' leans all taken (the founder,
  2026-11-12): one host -- Loom's plan format, `loom.host.Plan`, Workshop's retired outright with
  the repository's plans converted once (O1); a load's capabilities, kind and ceiling in the row,
  approved by the person, minted per weave as opaque handles, a reload asking again (O2);
  participant authority beneath the maker's ceiling, ending with it (O3); nothing built into the
  host for speed, and no `mode` reserved (O4); the person decides what runs, a loaded weave only
  proposes (O5); a publication's refusal told to its author, bounded (O6); rounds V (after the
  seam), A, M, R, P in Loom, ZH1 to ZH5 in Zengine. Schema evolution -- both, open doors for
  additions and the walker for the rest, the wall for state (E1); open doors for observations too
  (E2); an addition written as an extension, a default no optional (E3); the walker in Loom, its
  own files on it from the start (E4); the extension check now, advisory until open doors, red
  after (E5). Queued: `agents/packaging.md`'s stranger half to Workshop's side in the line's next
  round (16,350 of 16,384 bytes); a link's socket in the reactor's wait and v1 of the wait set
  dropped once Zengine's Timer moves to 2; Loom's `TypeToken`, `LogRecord` and `Outcome` as unions
  and a census of `name_of` spellings, ordered by the plan; a census of the Loom shapes Zengine's
  tools read by hand; `local/batch-137-138` still to force-delete (the union chain's end read
  `PHASE` without `PHASE.ended`; the kit's `hold` would have said the primary was free). The lane
  ([batch](../issues/raid-batch-2026-11-12.md)): Loom#17 built as reviewed and green, merging after
  #24; #20 holding but conflicting again with #23 in `host_main.cpp`, its title's period to go;
  Zengine#146 and #147 opened by the lane, waiting for `ready`. No contributor beyond the two:
  every commit of #17 and #20 is UnknownWorkers', `cursor[bot]` only the pusher. Zengine#150 reviewed
  2026-11-12, holding: Vision's premise in its prompt was false -- apt takes a cached `.deb` whose
  size matches without checking its hash (shown with a changed byte handed to dpkg) -- so each
  cached file is checked against the index the update just fetched and removed when its SHA-256
  is not the index's; two dry runs downloaded nothing and installed in 10 s, the build set the
  night's byte for byte; the cache filled across a day's outage of the dated archive, every attempt
  ending in the archive's words. Loom#25's continuation holds (a race in the journey, on `main` too;
  green at `e9987731`).
- **The overnight chain of 2026-11-11** (Vision's prompts, one session, warm then hot), reviewed
  2026-11-11, every stage holding ([reports](../reportbacks/lane-issues-137-138-RB.md), and
  rounds 2, 3 and the kit's beside it): Zengine#142 (#137, Loom#18's Zengine half, `75827dfc`) and
  #141 (#138, the Files places case reads the cut, `c93fdff6`), each green; the pane contract's
  round 2, Zengine#143 (`pane/` and the register PANE-SEAM, `4b03f76b`), and round 3, #144 (the
  world seams out of the pane protocol, `e099fb59`), CI green; the kit holding one phase in the
  primary (`9ac89c41`). #142's "green against Loom#18's head" was unattainable (#18 branched before
  Loom#12) and was shown over `main` with #18 merged. Package's Linux build went red on #143 and
  #144 at its first step: the dated archive's service answered 503 for three indexes, apt went on
  without them and left two suites out whole, and the build set failed as unmet dependencies (the
  night of 03:43 built with the same step); round 2 read it as moved live packages, wrongly.
  Vision's order: #141, #142; Loom#18 closed and reopened for a fresh merge ref (clean onto
  `main`), merged when green; the chain of two
  ([stage 1](../prompts/unrun/package-dated-archive-down.md), warm: the step refuses in words when
  the archive does not answer whole; [stage 2](../prompts/unrun/contract-rounds-onto-main.md), hot:
  #143 regenerated onto `main`, #141's `omitted_text` respelled by the pass, #144 on it); then
  #143 and #144, with Package's Linux judge green, since they change what installs. #143 merged
  after #141 without the rebase would leave `main` unbuildable: the text merge is clean. Done
  2026-11-11: #141 and #142 merged, Loom#18 merged (Loom `main` `827121b`); the chain of two
  reviewed, each holding: Zengine#145 (`14212239`, the step refuses by name after four tries, the
  build set unchanged, green), #143 (`f91f182b`, regenerated onto `main` with the one respelled
  line, checked against Vision's trial merge) and #144 (`12e1bc5a`, replayed identical), every lane
  and hosted run green, Package's Linux judge among them. Asked: the install's own downloads (24
  min on a slow day, inside the job's hour) by a cache keyed by the snapshot date and a time limit
  with words of its own; `local/batch-137-138` force-deleted (`git branch -d` refuses a local merge
  whose work is on `main`). For the kit: a replay script beside each mass-edit pass (round 3's pass
  has no README). The lane's
  batch ([issues](../issues/raid-batch-2026-11-11.md)): the stale mutant `search-ignores-the-role`,
  and a case cutting Files' places on every machine. The lane's own: Loom#20's fix pushed
  (`a2dfc21e`, on L1, wanting #22 under it), Loom#17's proposed idea posted and not yet built (a
  `refusal` on `Ticket` and `RolePublication`, answers out of the bound); both reviewed
  2026-11-11 and in the batch, the lane continuing rather than starting over: #20's three fixes
  answer the review, left only a rebase (`CMakeLists.txt` against #22, the version's definitions
  inside `loom_add_host_executable` for both builds); #17's idea holds with a publication refused
  whole at the bound and `README.md`'s marker at 12, after a rebase onto `main`. #17 merges before
  the foundation's seam round takes 13. The founder's word (2026-11-11): `local/batch-137-138`
  force-deleted at the next Ceecee session's end, carried in its prompt. For the kit's next round: `kit.sh hold` (who holds
  the primary, since when); a stranger check against a Loom pull request as it would merge; a
  warning for a doctest filter holding a comma (hit twice); the README saying `issue-say.sh idea`
  adds its own heading; the two rounds' pass walkers lifted into the kit at the third move;
  `kit.sh end` reading a phase's continuations, whose reports have stems of their own (the Timer's
  third report, 2026-11-13); the primary's Loom prefixes rebuilt when Loom's `main` moves (three
  sessions of 2026-11-13 built their own, the primary's predating the union); `witness.sh` and
  `primary.sh second` working with `KIT_LOOM_WIN_PREFIX` set, `witness.sh start --plan` and
  `witness.sh compare`; `tip-wsl.sh` refusing a copy built against another Loom; `loom-wsl.sh`
  running one case under the delegated scope, and a box build; `timed.sh` finding a kit helper by
  name. A chain's prompt ends each stage's hold before the next names itself. From the reports of
  2026-11-13, night: `kit.sh pieces` (`time_cases.py`, `cut_pieces.py`, `ci_costs.py`), a helper
  repeating an entry that keeps a red's folder, a stack sampler, edit helpers writing LF,
  `merge-trial.sh` for a chain's last stage, `mutate.sh` taking `KIT_MUTATE=loom` with
  `loom-win.sh` under it, one idle counter for the three, `case-wsl.sh --time`.
  The Workshop-as-a-stranger research's seven decisions were taken (the founder, 2026-11-11), so
  `app/` leaving `workshop/` is ZR's.
- **The overnight chain of 2026-11-10** (Vision's prompts, one session, warm then hot; reports in
  `unreviewed/`): the kit's session roots on NTFS and ext4, done (the constitution's section c
  amended, the founder, 2026-11-10: a session's roots live where permissions are kept); several roles L1, Loom#12; its Zengine half Z1,
  Zengine#132; the GUI window's name, Zengine#133, with Loom#13 for the router's words; the pane
  contract's round 1, Zengine#134. L1 reviewed 2026-11-10 and decided (the founder): a release
  ends the role's claims (SENSE-05), as built, since nobody holds the role after it, while a
  replacement keeps the incumbent's stale (SENSE-03); and nothing is left waiting -- every ask
  whose answer can no longer come is told to its asker, with why, so it can retry or wrap up,
  planned explicitly as the first round of the research **replacement without a seam**
  ([prompt](../prompts/replacement-without-a-seam-research.md), warm), the founder's goal a
  total takeover with no work downtime (one shape: the retired weave kept as its successor's
  child to finish what cannot move, such as a build). That research runs before L2, so L2 and the
  split are built once; who is told when a holder leaves (its askers, its subscribers, the weave
  itself) is its own. Reviewed 2026-11-10
  ([report](../reportbacks/replacement-without-a-seam-research-RB.md), pages in
  `reportbacks/replacement-without-a-seam-research/`), its source claims checked by Vision: an
  ask is the asker's (`mail.ask`, refused for a weave that does not accept `zen.AskEnded`), and
  Loom follows it to its answer or to `zen.AskEnded` with its stage and reason; owed long work
  is a kept answer under a bound per weave; a replaced weave is retired to its successor, which
  owns it, told `zen.Leaving` after the switch, its queued speech delivered and its owed answers
  finished, handed over (`zen.AnswerOwed`, role-addressed asks only) or let go, its letter exact
  without a hold; L2 a plan of rows, one candidate accepted, the Manager's swap on the switch;
  the hold its own round. Rounds: Loom F1 (the floor, in process), then F2 and T1 (retirement),
  T2 (L2 and the swap), T3 (the handover, a reload's carry), T4 (the hold, if asked), T5 (the
  split); Zengine ZF after F1, the build runner first. Sixteen decisions asked, each with a lean;
  Vision's two changes: the old swap and `zen.ClaimBequest` gone at once, not after a release
  (decision 13), and no `kept` word reserved until a weave needs it (decision 14). The ABI:
  Loom#17 takes v12 (the founder, 2026-11-02, never avoid a version bump), so the floor and the
  addressed role are v13 and the takeover v14; Loom's new notices are not counted by #17's
  bound, as a dispatch refusal's is not. Z1, #133 with Loom#13, and #134 reviewed 2026-11-10: each holds, #133 and #134
  green on every job. For Z2 (round 5): `LoadedSelected` keeps one `role` field, which carries
  `r1+r2` once a weave holds two, so it wants a `roles` field before Workshop takes its second
  name. Left of office-to-role: the code's multi-word names, which want a census of identifiers
  first (the end's). The founder's rule (2026-11-10): a shape change is never ruled out, with no users
  now its cheapest; and the code does not hold an old name for a file that can change. So #133
  drops `zengine.window.sdl`'s forward read and the demo medium `sdl`, and #132 gives
  `LoadedSelected` its `roles` ([prompt](../prompts/overnight-review-fixes.md), warm). Both fixes
  reviewed 2026-11-10 and holding ([#132's](../reportbacks/several-roles-z1-RB.md#after-review),
  [#133's](../reportbacks/office-to-role-followup-RB.md#after-review) sections): `LoadedSelected`
  v2 carries `roles`, a list, and Compose asks a weave at its first role, the decision Z2's first
  weave of two roles asks; the old window role is read nowhere, and a setup naming `sdl` is
  refused in words. The Files places case (`test_workshop_panes_files.cpp`, `main`'s) assumes
  every place shows, so it is red on a Windows machine with more drives than the pane lists: an
  issue for the lane. The
  lane's three reviewed 2026-11-10, each holding: Loom#15 (the session case owned by its user
  before the read), Zengine#135 (the marker refused, the refusal saying how to clear it, a made-up
  footer link) and Loom#16 (Zengine's predicate, copied); both repositories' trains trial-merged
  clean and the new check passed over each whole history. Merge order: Loom#15 and Loom#16 once
  their first runs are approved, Loom#13, Zengine#135, #134, then #133 after its fix, then Loom#12
  and #132 (after its fix) back to back. The first five merged 2026-11-10; the order now is the
  lane's batch's, below.
- **The lane's batch, reviewed 2026-11-10** ([issues](../issues/raid-batch-2026-11-09.md)). Merged
  first, each a merge commit: Loom#15, whose squash (`5241003d`) carried a co-author line, its tip
  rewritten as `4fa693bc` with the founder (a contributor's pull request merges with a merge
  commit); Loom#13 (`84b5ed0`); Loom#16 (`ca5c641`); Zengine#135 (`99faf89`) and #134
  (`919e466`). Loom `main` at `ca5c641` passed all three Windows jobs, #15's proof on the Server
  runner, and its Zengine stranger ran past its 45 minutes, as #19's and #20's did: it took 27 to
  38 before, and Zengine grows, so its limit goes to 90 (Zengine's longest lanes have 90) in a
  one-line pull request before the next fresh runs. The five from the batch, one commit each (#19
  three) under `UnknownWorkers`, no trailers, ran merged onto `d8d2b82`, before #15, so every Loom
  Windows job is red there, and each Loom one is closed and reopened for a fresh run, which also
  meets #16's check of the title and the description. Zengine#136 (Elounda kept under its author's
  OFL, Basic removed; the font's bytes and its license matched to upstream `fbe57c50` by Vision)
  holds, green. Loom#19 (Clang 18 builds Loom; under Clang the weave contract reads a configure
  probe with `nm`; a Clang lane) holds, and merges first of Loom's so the later fresh runs meet the
  lane; built here with Clang 18.1.3 over `main` with #17 to #20 and L1, its one error was L1's
  against #20 (below), and the switchboard, kernel and `host_console` suites passed once patched.
  Loom#18 (`shared_ptr<const Value>`) holds; its Zengine half, the nine lines it names (the same on
  `main`, none added by an open pull request), can build against both Looms, so it merges first, as
  the lane's issue, then #18's fresh run. Loom#17 (1024 waiting per sender) takes a revision: at the
  bound a role-authored send returns what `weave.hpp` and `bus.hpp` call "does not hold the role",
  `ZEN_ERR_ROLE_AUTHORSHIP_DENIED` across the ABI, and a loaded weave's answer `ZEN_ERR_REFUSED`,
  "no answer to spend", while its right is kept (ANS-06). Vision's lean: answers are not counted,
  each spending a right made by an ask already bounded, and every send door says the bound in its
  own word, a new status and ABI v12 (L3 then 13); asked. Loom#20 (`main` catches what leaves the
  pump, says it, removes the session files, exits 1) takes a revision: its `fault` command, a
  native participant that throws, ships in `loom-host` only for its case (Vision's lean: a test
  build of the host from the same source, as the probe's two variants), and the guide's exit codes
  and the session page's "removed when the host ends cleanly" stayed stale outside its folders;
  #20 and L1 collide at `report_native_failure`'s `role_of`, a clean text merge that does not
  build, so whichever merges second takes `roles_of`. Merged after the review: Zengine#136
  (`65f9b57`); Loom#21, the stranger's 90 minutes (`37835c2`, whose stranger on `main` took 48);
  Loom#19 after a fresh run (`dc06bdd`); Zengine#133 (`3f7b5d1`), before its setup format's
  version could move, so version 2 is a follow-up pull request
  ([prompt](../prompts/setup-format-v2.md), warm). Then Loom#12, L1 (`0faba92`), and Zengine#132,
  Z1 (`4865cf8`), back to back, both `main`s green after. Two Ceecee lanes reviewed
  2026-11-10, each holding and green: one-release-number (Loom#22, Zengine#139; its dry run's
  package says 0.2.8 in all six places) and the setup format's version 2 (Zengine#140,
  [section](../reportbacks/office-to-role-followup-RB-setup-format-v2.md)). Both lanes took
  the primary at once (the kit's one `PHASE` file), each moving to a second copy: the kit
  should refuse a second phase while one holds the primary, and `kit.sh end` and constitution
  section c disagree on when a session's second copy goes, both for the kit's next round.
  Vision's order now: Loom#22, then Zengine#139 (a night is red until Loom names a series);
  #140 at any time; the Zengine half, then Loom#18; Loom#17 and #20 revised, #20 rebased on
  L1 and #22, which it conflicts with in `host_main.cpp`. Concerns for the end: the lane posts
  none of the issue comments `taking-an-issue.md` asks for, a crossing of the folders among them
  (#19's and #136's were needed, and their bodies say why); #18's quoted red cannot come from its
  final case, whose `static_assert` stops the old code compiling; #136's catalog counts four text
  documents where there are five; a sender's own pointer to what it sent (P-LOOM-23).
- **The clock's rounds** (the founder, 2026-11-06): beats-with-work merged (#115, `2dcc3a38`). The
  reactor reviewed 2026-11-07 ([report](../reportbacks/reactor-RB.md)): Loom#5 green on every job
  and merging first, then Zengine#116, whose hosted build stops at Loom's new header until #5 is on
  `main`, so a re-run after it is #116's proof. An idle Workshop turns about once a second, a guest
  linked or not, and a key waits under a millisecond on Windows, about one on Linux. Next, once both
  merge: the frame clock's prompt, its beat 16 ms, a change outside a look presented at once, a
  frame's time read through the clock its host wires, with research on game time beside it
  (P-WORK-85; the founder, 2026-11-07); threads kept possible (P-LOOM-19). Loom#5 merged; #116's
  MSVC fault and the package's missing header fixed (`bc46eaa5`, `5a5a61af`), green on every
  job and its Package run, reviewed 2026-11-07: ready. The
  research: [report](../reportbacks/clock-reactor-research-RB.md). The build warning, #114, merged.
  The view cost ([report](../reportbacks/view-cost-research-RB.md)): Inventory re-declares every
  view at each change, Workshop repaints per declaration and solves the desk per pane; R1 (Inventory
  declares only changes) now; asked: R7's shape (Vision's lean: Loom's after-turn hook) and R8.
- **The visual foundation's V4 and the held pictures** (the founder, 2026-11-07): V3, #118, merged
  as `4dba5cb2` ([report](../reportbacks/visual-foundation-v3-RB.md), closes Zengine#1). V4 is #117
  ([report](../reportbacks/visual-foundation-v4-RB.md), reviewed 2026-11-07): ready on `main`, every
  required job green, the advisory MSVC red on Flow's double press (P-WORK-86). The held pictures
  are #119 ([report](../reportbacks/visual-foundation-pictures-RB.md), reviewed 2026-11-07): 23
  pictures and two pages' words; rebased onto `main` after #120, its patch the same, green on every
  job and ready (its after-review section, reviewed 2026-11-08).
  Order (the founder, 2026-11-07, green on `main`): the double click first, #120
  ([report](../reportbacks/double-click-RB.md), reviewed 2026-11-08, ready, green on every job),
  then the pictures rebased onto it. V4's moves alone are #121
  ([report](../reportbacks/persist-moves-RB.md), reviewed 2026-11-08, ready: `persist/` and the key
  spelling, byte for byte V4's). V4 is held (the founder, 2026-11-08): theming is redesigned as
  design tokens -- the look alone, Workshop's; settings mechanical; keys the keymap's; the terminal
  a look of its own; a repaint or a re-measure by event -- a design page agreed before #117 is
  reshaped ([the theme slice](drafts/context-map-themes.md); the calls: [goals](goals/theming.md)).
  The design ([report](../reportbacks/theming-design-RB.md), reviewed 2026-11-08), taken by the
  founder the same day for V4's next attempt, with Vision's amendments: one owner per palette name
  (four offerers on `main`, the app and the snake too); a pane's own value may default to an exact
  colour; no new change shapes, a size or font change being a new `AreaRoom`. His own calls with it:
  a theme is the host's; the terminal's look its own file, a theme being a name with a window file,
  a terminal file or both, the terminal's defaults today's colours; a theme for the other medium a
  normal link in the chain, converted in its place and warned of in the theme manager; the theme
  manager showing a sample wearing a theme fed to it ([goals](goals/theming.md)). V4's next attempt
  is Zengine#124 ([prompt](../prompts/theming-v4.md), [report](../reportbacks/theming-v4-RB.md),
  reviewed 2026-11-09): every call built, green on every job, ready; #117 the founder's to close
  once it merges. Its follow-ups: the theme manager pane (sample view, editing by group, the links'
  warnings), its own round; a theme case through a real window in the desk suite (the grant bug
  passed it); the kit's picture prefix reinstalled each round, and its end mark wrong on
  `kit-pictures`.
- **The context map and shared vocabulary** ([report](../reportbacks/context-map-RB.md), pages in
  `reportbacks/context-map/`, reviewed 2026-11-08; redrawn by `pass-tools/context-map/`): Workshop
  is the hub and its folder holds other parts' languages (the pane protocol, twelve features'
  seams); fourteen words with two meanings or two owners; eight decisions asked, the founder's.
  Vision's review found two facts off at `main`: the theme words carried from V4's branch (`main`
  still says `workshop.skin`), and `zengine.workshop` copied as a constant in some thirteen parts,
  not five (the tool reads headers' `k...Role` and misses `.cpp` constants). Its numbers want the
  tool's patterns fixed before a decision rests on them. The founder's answers (2026-11-08): office
  becomes role everywhere, in one cut, version bumps accepted; one home per role name; "operator"
  leaves Loom, the console is the weaver's console; Zengine's display mode is the TUI; multi-word
  names where senses meet; a manual names its senders by role, checked. All applied by one round
  ([prompt](../prompts/office-to-role.md)), reviewed 2026-11-08
  ([report](../reportbacks/office-to-role-RB.md)): both hold; #122 and Loom#6 merged, then #123
  rebased onto `main` ([prompt](../prompts/office-to-role-rebase.md); its section in the report,
  reviewed 2026-11-08): green on every job after one fix the package witness caught (the Neovim
  Editor's installed header read an uninstalled one; it keeps a registered copy). Ready: the founder
  merges, then Loom `main`'s stranger job re-runs green. Left: the multi-word names (pages partly,
  code not) and the 13 console pictures, which need the foreground; once both merge, the kit's v1
  grants of `Run` and `RunList` go. The founder's to decide: the drawing operators' word. Decided
  (2026-11-08): `zengine.window.sdl` becomes `zengine.window.gui`, SDL named only in the weave that
  loads it and the pages about that weave; one follow-up round after #123 takes it with the
  multi-word names and the 13 console pictures, the founder's machine free for the foreground at any
  time. Palette waits on the theming design. Open: where the pane protocol and the features' seam
  vocabularies live (decision 2) -- the founder's picture is a tree, Loom, Zengine, Workshop, then
  each pane its own context, a pane in its own repository the standard state. Then his scenario
  (2026-11-08): a pane used without Workshop (Files in a pixel-art editor), and a contract by which
  anyone creates, positions and registers panes; panes Zengine's "acceptable on principle". The
  research ([report](../reportbacks/pane-contract-research-RB.md), pages in
  `reportbacks/pane-contract-research/`, reviewed 2026-11-08): Zengine owns the contract in a
  library folder `pane/`, Workshop one host holding `zengine.pane.host`; four duties, the rest
  refused in words; no new shape; six rounds, the app the second host. Ten decisions, the founder's.
  Vision's review: the settings role wants the host role's reasoning (a contract name, not
  `zengine.layouts`); its theme amendment 4 is superseded by one owner per palette name; its
  amendment 3, the row's theme a host setting, belongs in V4 before it runs. Decided (the founder,
  2026-11-08): the ten, with Vision's two differences: the settings role a contract name,
  `zengine.pane.settings`; the theme amendment 4 declined, 3 taken into the goals. Order: V4 first,
  then the contract's rounds 1 to 4; round 5, the host's name, after Loom research on a weave
  holding several roles (the founder's question, 2026-11-08: a middleman holding the roles of its
  ecosystem). Before a pane in its own repository is the standard: shape names owned by their
  vocabulary (P-LOOM-08, Loom#3, carried from Loom-history#37, open and parked: an opt-in seam, no
  mass rename). Both researched ([several roles](../prompts/several-roles-research.md), [owned
  names](../prompts/owned-shape-names-research.md)). Several roles
  ([report](../reportbacks/several-roles-research-RB.md), pages in
  `reportbacks/several-roles-research/`, reviewed 2026-11-09): a weave answers to a set of names,
  each still with one holder. Decided (the founder, 2026-11-09), the leans with Vision's: the set
  bound at load only, all or none, bounded, and a role released at any time, out loud, as its
  holder leaving it (L1); a replacement takes a plan naming every role of the incumbent's, to the
  candidate or released, an omission refused in words, one candidate (L2); the addressed role (L3,
  ABI v12) held for its first consumer, since round 5's old address is refused by each pane's grant;
  the rule for a second role, one state, one authority, one life, one meaning per shape, Zengine's
  law beside WL-PART-01, Loom stating the mechanism; `roles_of` for `role_of`; round 5 holds
  `zengine.pane.host` beside `zengine.workshop` and `zengine.pane.settings` beside
  `zengine.layouts`, contract lines moved by shape in one round, Workshop's own spellings kept (Z1,
  then Z2, needing L1 alone). L1 can run in Loom beside the contract's rounds 1 to 4. The split, a
  role apiece to several candidates (P-LOOM-21), is designed with L2 in the research below. Owned names
  ([report](../reportbacks/owned-shape-names-research-RB.md), pages, census and spike in
  `reportbacks/owned-shape-names-research/`, reviewed 2026-11-09). Decided (the founder,
  2026-11-09), the leans with Vision's addition: every vocabulary declares once,
  `ZEN_VOCABULARY("<owner>")` or `ZEN_VOCABULARY_BARE()`, and one declaring neither does not
  compile; nothing is renamed now, so no name or content id moves; the owner is the vocabulary's
  own name after its package's spelling, never a role's; published versions stay bare, an owned
  version carrying the number on; older names are read forward by each reader, with no alias at
  Loom's gate; short names only where a person types and nothing is stored; Loom checks an
  owner's spelling, Zengine refuses one on a namespace with no shapes of its own; `code_values`
  the light form, a rule that an owner is a name and not a role's copy; Z1 pins today's bare
  vocabularies, so a new vocabulary takes an owner unless a reviewed pin says otherwise; and
  Loom's spelling of itself is `loom.` (its own bare shapes `BARE` for now, `loom.<area>` once
  owned; the published `zen.` names stay as published). Rounds: Loom L1 (the seam, Loom#3's
  done-when) and Zengine Z1, before the first pane outside this repository and in a gap between
  the contract's rounds; L2, short names, optional; each conversion at its own wake. Roles across the isolation pipe stay
  Loom's known seam; a WASM box speaks as its role (`role_send_to_role`), so boxed tests of role
  holders stand.
- **The overnight chain** (the founder, 2026-11-08), one session, warm then hot: #119 onto `main`
  ([prompt](../prompts/pictures-onto-main.md)); V4's moves alone, `persist/` and the key
  spelling ([prompt](../prompts/persist-moves.md)); the context map and shared vocabulary of
  the whole system ([prompt](../prompts/context-map.md)); the theming design from it, for the
  founder's decisions ([prompt](../prompts/theming-design.md)); why the first weekly mutants
  went red, #99 ([prompt](../prompts/mutants-red.md)). Ran whole; #119 and #121 merged; #122
  ([report](../reportbacks/mutants-red-RB.md), reviewed 2026-11-08): the weekly run's 18 stale
  entries and one #120 stranded, CI green, merge once its dispatched Mutants run is green. Its
  follow-ups: a corpus text check (`run.py --text`) in every pull request's documentation lane, so
  moved code cannot strand an entry for a week; the kit's `ext4.py sync` leaves an emptied folder.
- #120's follow-ups (double-click-RB, reviewed 2026-11-08; its five choices accepted by the
  founder, the count going on among them): an agent's double click rides its link's speed (two
  injects 1/60 s apart), revisited with batching, not by a double-click path of its own -- a batch
  may carry its delays, or land both clicks in one frame (the founder); the mutation runner's
  restore may keep a file's time, leaving a mutated object unrebuilt; the Terminal's word select and
  the Builder's list take a second press with no count (V6); `design.md` 2.5 and 1.8 to say the
  count goes on and is per hand, and V6's versions to carry `PointerTimingAsked`; `zengine-input`
  compiles against Workshop's settings vocabulary, and where input keeps its settings is open (a
  plain JSON file would do, the founder).
- **The kit's phase is one shared file** (`Zen/primary/PHASE`): another lane's `kit.sh phase`
  re-pointed two rounds' helpers mid-session (2026-11-06); both pinned `ZEN_PHASE` by hand. A
  wrong phase makes another's folders read as the session's own to `kit.sh end --clear`. A
  session beside the phase cannot say its start without writing it (status-board-RB, which
  asks for a `kit.sh start`, and a `kit.sh slot --look` that reads without removing dead
  tickets). Its round asked, not yet written.

- **Relicense to AGPL-3.0-only** (the founder, 2026-11-01), before anything else. Done but its
  loose ends: both histories rewritten so no commit says MPL (plain AGPL until a creations
  exception is drafted, no README note), pushed to the new public repositories and green;
  settings, labels and the 103 open issues carried
  ([report](../reportbacks/relicense-agpl-history-RB.md), reviewed 2026-11-01 and 2026-11-02).
  No copy of the old history is left on the machine but the bundles; the six repositories that
  stay carry a pre-push guard; private vulnerability reporting on; `zen-night-lab` and
  `zen-arena` private; #100 merged and the package on (the founder, 2026-11-02). The loose ends
  done (reviewed 2026-11-03): of the carried work 99 dropped and #487's branch kept, the View
  Builder's quarry ([sheet](drafts/loose-changes-2026-11-02.md)); the toolchains in
  `zen-build/toolchains/`; the kit's left-behind check. What it found, cleared, `parked` and
  `later` retired ([report](../reportbacks/left-behind-cleared-RB.md), reviewed 2026-11-03):
  nothing left behind. `v0.2.0` is tagged (`84446fb5`): the MCP server's 0.1.2 package swapped
  for it next. Pushed branches never merged stay in `-history`, carried on request. Still owed:
  the creations exception, drafted with counsel. Asked, not decided: a CLA before outside
  contributions; the trademark.
- **Main lane: Flow made over**, pushed as #559 at the founder's word (2026-10-29,
  [report](../reportbacks/flow-live-requests-RB.md)): batches A to E live in his Workshop, the
  Windows build mended after the first hosted run, three guide pictures taken from recipes (the
  older ones wait on #521). Reviewed 2026-10-29: green at `8ffdacfb`, every job, after the
  sanitizer and MSVC runs found a case reading a copy freed before the read; merges clean onto
  `main`. Flow's next round (the founder, 2026-10-29, after #559): the three old dialogs (Add a
  trigger, Add an emit, Add field) in request 8's words, and a kept field and a trigger's message
  field of one name refused at the edit, which the maker's admission refuses at Run. Later, with
  accordions (BL-WORK-16): the docks narrowed to tags that open on hover with their names and
  connectors.
- **Issue lane**: the UX batch done ([report](../reportbacks/issue-lane-ux-batch-RB.md)): 65
  issues in Zengine (#492 to #566) and Loom #73 (section 6), its eight pull requests merged, the
  weekly mutants run 341 of 341 caught and #476 closed. Then the ELH audit's findings
  ([report](../reportbacks/issue-lane-elh-audit-RB.md), reviewed 2026-10-29): #570, `repo` alone
  in `accounts-machine` so approving `workshop-machine` grants no push, and Loom #77, a spelling
  `loom-session` cannot type refused by the input's name, both green; 21 issues (#569, #571 to
  #589, Loom #76). Then the founder's decisions and the agent tools
  ([report](../reportbacks/issue-lane-decisions-agent-tools-RB.md), reviewed 2026-10-30): eleven
  decisions written on their issues, Loom #73 retraced; #590 the desk tools (#571, #573, #582),
  #591 the input owner's busy words (#579), #592 the workshop tools (#574 to #578, #581, #585,
  #586, #589), each green; #584 and #587 left open with a question each (section 5).
- **Kit lane: the picture tool**, done ([report](../reportbacks/kit-pictures-RB.md)): a picture
  taken from its recipe, an audit of all 128, 26 recipes; twelve retaken in #558, merged. An
  audit of `main` at `14669927` (the accordion lane's, 2026-10-29) finds three already out of
  date: `hotkeys-keymap-folder-window.png` (Start here, after #563), and the Files manual and the
  Pane Manager's row menu the kit round left; the Hotkeys and palette counts do not move with
  #568. After #559, an audit again. The manuals' recipe shows its own hand (Info inspecting the
  Manual's geometry, Notices listing the commits that placed it); a cleaner composition for a
  later kit round. The next two ran and were reviewed (2026-11-04):
  [background launches](../reportbacks/kit-background-launches-RB.md), the kit in Zen
  (`08e23581`) and Zengine #103 (the OS window put behind every window on Windows; green on every
  job, merges clean with #101 and #104, any time): an agent's Workshop opens without the
  foreground and covers nothing, `winhand.ps1` and `conshot.ps1` take the foreground only under
  `KIT_FOREGROUND=1` or `-Foreground`, `front.ps1` brings one forward, and the left-behind check
  counts a report from its first commit. [Private words](../reportbacks/kit-public-words-RB.md)
  (`891cf87a`): `public-words.py` marks a text before it is posted, never refusing. Asked, with
  Vision's leans: the flag named for what it now means (`ZENGINE_SDL_BACKGROUND`, in #103 before
  it merges); next kit round, `behind.ps1` as a guard in the launchers and a `pr-say.sh` route
  that runs the words check on a pull request's text. The windows branch of #103 is compiled by
  no hosted job; the night's Windows package build is its first.
- **Accordion lane: stage 2**, as #568 ([report](../reportbacks/accordion-stage-2-RB.md)): the
  group borrows its owner's list and keeps no copy, so a pane's state is the truth; Info's values
  a tree (WL-INFO-16), with Right, Left and Shift+Left. Rebased onto `main` at `c46f3098` and
  green (its last section, reviewed 2026-10-29): the floors measured (component 59, info 185), an
  open walking a list in any order, witnessed under libstdc++'s debug mode, Info's manual picture
  retaken; merge-ready. Three decisions (section 5).
- **WASM lane: stages 2 and 3** ([report](../reportbacks/wasm-tier-s2-s3-RB.md)): S2 merged as
  Loom #74, `Kernel::containment(name)`, D7's statement in `capabilities.md` as recorded. S3 as
  Loom #75, rebased onto it and green, tests only: the door cases run on boxed twins built from
  the same fixtures (24), and the five bounds met; merged. S4, a Zengine pane boxed in Workshop,
  reported and reviewed 2026-10-30 ([report](../reportbacks/wasm-tier-s4-RB.md)): Loom #78 green,
  12 of 12, merges first; Zengine #594 green but its boxed job, refused at configure until #78 is
  in. #78 merged (`619d102f`); #594's rerun green on every job, the boxed one included, its body
  put right; reviewed 2026-10-30; merged (`8559e428`). S4b, the Builder's second target: the
  founder took it into the Builder (2026-10-30), a recipe making its pane native, boxed or both
  through Workshop ([prompt](../prompts/wasm-tier-s4b-builder.md), warm): reported 2026-10-30
  ([report](../reportbacks/wasm-tier-s4b-RB.md)), its review next.
- **Docs lane: Loom's README as the front door.** The journey page (#79, +1044 lines) closed by the
  founder (2026-10-30): docs get smaller and clearer, never longer. First the eight Loom entries of
  the docs-against-code list in one small pull request, Loom #80, merged (`a2fe7e2`), so the
  rewrite reads no contradiction. Then `Mail::reply` falling back to the stamped sender when no
  reply address was given, ordinary grant-checked speech still (the founder, 2026-10-30;
  [prompt](../prompts/mail-reply-fallback.md)): Loom #81, reported green at `1429803c`, its
  review next. Then Loom's README rewritten
  below the preface: a punchy, honest summary; the ideas, ordered for a reader, each section able to
  stand alone as bullets; install, build, the console, a first weave, loading code, sending a
  message; deep-dive links (loading code, a message's path, the console's commands) folded from
  today's guides. Every command and code block run by a test, each a small main-only program; a cold
  reader following it on a clean machine is the gate, the founder's read last. Vision drafts the
  outline (summary, ideas as takeaways, sections) for his markup before the prompt. After it: the
  self-test cross-referenced, Zengine's README the same way (its entries of the list fixed first),
  then readers outside the project seeding an FAQ of plain questions with direct answers a layman
  can follow.
- **The review waves** (2026-10-29). The first: #485, #491, #489, #486, #484, #490 and #488
  merged, #487 closed. The second, reviewed the same day: #553, #555, #561, #557, #563, #567,
  #550, #565, #558 and Loom #74 merged. The third, reviewed that evening, all green and each
  clean on `main` and with the others: #570, #568 and #559, then Loom #75 and #77 back to back.
- **UI census**, reported ([report](../reportbacks/ui-census-RB.md), `08693d45`) and reviewed
  (2026-10-29): an element set of nine and an order; its nine decisions with the founder
  (section 5).
- **Closed this week**, each in its report: the desk's round 2 (#467, #469, #470, #472); the
  repository's mutants and their follow-up (#471, #473, #475); the View Builder lane (#484, #489,
  #490, #491; #487 not merged, the builder made over after Flow); the text lane (#485, #488);
  accordion stage 1 (#486); the kit's compile gate (12 GB a work slot, each tree its own peaks).

## 2. Next, in order

1. **Flow made over** (BL-WORK-32), its prompt written (2026-10-28, section 1). The clickable
   [mockup](https://claude.ai/artifact/JxK1MLFeeSmQh2GgD3v4jY): When, Do and Then kept as colour
   with more room to Do; the rule read as a sentence; a Next line in place of Run's refusals; a
   nine-stop tour. The founder's calls (2026-10-27): a press may change several things, and
   several messages may change one field; each node listens only to its own message and
   condition, so pressing `+` computes no divide; a gear for settings. Quicksort needs a branch
   form (only the chosen side computed) and list operators. Start here's moves for steps 2 and 3
   wait on it. Zengine #142 holds the older milestone question.
2. **The element set, its text pieces first** (prompted 2026-10-30,
   [prompt](../prompts/element-set-text.md), warm) (the founder, 2026-10-29: "High quality
   components means higher quality composites"), a stage worth the time. The census's set
   (section 3), its drawn faces lifted from Flow's pen once his round ends. First the text: one
   core (the text, places in it, the selection, the word rules, the window over it, the copy);
   the text area over it, read only; the text box over it, adding the caret and the editing, at
   first with every behaviour its 25 users have today, then the whole box pressed and the caret
   blinking. The box seen as a box (the founder, 2026-10-29): a 1 px border in a light grey role
   a theme maps; Loaded's search is the first that needs it. Before the View Builder's makeover,
   which builds on it. The text stage reported 2026-10-30
   ([report](../reportbacks/element-set-text-RB.md)): Zengine #593, green on every job at
   `492e96c9`. The founder (2026-10-30): `[text___]` in cells; every text box always seen as a
   box, empty included; Loaded's search shown from the start; `component/` knowing no medium.
   The faces round (`bd184417`) green on every job, reviewed 2026-10-30, merge-ready:
   `component/` measured in characters, each look a face in `graphics/elements/`, a row carrying
   its box. The founder (2026-10-30): the Terminal's own line plain in cells (`> ls -l`), its
   outline kept in a window. #593 merged (`13cc5674`, squashed); the Terminal's line came as
   #595, one commit on `main` ([prompt](../prompts/element-set-text-terminal-line.md)), its report
   due.
3. **The View Builder made over** (the founder, 2026-10-29), after Flow, as Flow was: the design
   as a whole, not the lane's three notes one by one. What it carries: the kinds a row each below
   Grid (his note of 2026-10-27); the width that responds, which he liked (#487, never merged,
   its branch the makeover's quarry: the kit primary's `carried/batch/lane-view-builder`);
   Discard asking a second press, as New and Open do; the census's element set as its kinds; and
   after it, Workshop's two pictures of the builder taken again (`quit-box.png`,
   `pane-manager-new-view-builder.png`), and its `<action> complete` (WL-NOTE-06), a leftover the
   issue lane left to it. Then a pass over the smaller panes on the new pieces (the founder,
   2026-10-29), in a few phases side by side. The three picture panes' boxes (view host, View
   Builder, Flow) go onto `text_box_face` with this makeover and Flow's next round, not alone
   (the founder, 2026-10-30). The Builder earns a makeover of its own after this one (the
   founder, 2026-10-30).
4. **The operator suite** (BL-WORK-48), which Flow's calculator runs on. Today: five Int
   primitives (`operator/primitives.hpp`). To add:
   - Math: subtract, multiply, divide and remainder (both refusing 0), negate, abs, min; square
     root and logs, which want Float beside Int;
   - comparators: equal, not equal, less or equal, greater, greater or equal;
   - Logic: and, or, not;
   - later: Lists, with the quicksort; Text after.
5. **The UX batch**, filed by the issue lane (above), then **the first complete maker story**
   (theme 13, section 7).

## 3. Decided, not yet ordered

Each starts on the founder's word; "wake" is what must be true first.

- **The visual foundation** (the founder, 2026-10-31,
  [answers](drafts/decision-wave-graphical-answers.txt)), before the makeovers, built for the ideal
  future: the earned rule retired the same day.
  - Colours, a new system: the painter knows no colours, each draw carries its own; a pane colours
    by an exact value, a name from a shared pool named by use (background, text...), or a slot it
    exposes to themes; themes are JSON, loaded without compiling, setting any exposed slot, each
    theme saying whether a slot nothing exposes is skipped or refuses it whole; the same pool holds
    fonts and text sizes. Census 9's emphasis colours fold into it. Names reached as C++ names,
    generated as the quarry's Config Generator did: a name per pool entry and per exposed slot,
    a typo a compile error, the window turning the name into a colour when it paints (the
    founder, 2026-11-02).
  - Looks: Vision's model (when, what, how; operators a closed set the window knows, a weave's own
    only boxed and later), several at once on one node, an operator taking a value struct (a fade's
    end colour). The window-looks record rewritten so: (b) to (d) yes, (e) the act tool holding
    steady for its run. Looks of one trigger on one property chain in the order added (the
    founder, 2026-11-02); of two triggers, the one fired last wins while it holds.
  - Text: weight, size and every character past ASCII drawn in the window; `?` only where a
    terminal can't show one.
  - The element set: button (once `control`), field, list, collapsible, text area, hint
    (2026-11-02; `collapsible` the founder's, 2026-11-03: one fold, a group of them an
    accordion, so the code's `Accordion` and `IndependentAccordions` are renamed to match).
    Search is the list's filter: filters and a sort chained in order, by the list's type and
    parameters. A choice is no element but a rule (the founder, 2026-11-03): a group over
    elements that have an on state, wherever they sit (three radio buttons, each over a form of
    its own), saying how many may be on. A form greyed out until its box is checked, a field
    required or checked, are rules of the same family, his linked-field logic: designed as one
    when the element set reaches forms. Tabs are toggle buttons under a one-of rule, `tab_strip`
    their strip's layout. Groups are a pane's layers, painted
    and hit in tree order; a move puts a node before or after a sibling, a raise flag lifts one
    until lowered without touching the order, never across groups (Vision's call, the founder
    deferring). The old drawn classes retired as faces supersede them, Image and Grid kept
    until superseded; a menu row's key and submenu mark as fields;
    every key a hint names read from the keymap; Info's list rule with the list piece; Workshop's
    panes on a shared piece wherever one fits.
  - Keys: a pane hears a key first, what it doesn't consume going up to Workshop, and a pane may
    opt out of Workshop's defaults; a pane owns its own key (from outside it opens or selects the
    pane, inside it closes it); one action shape carrying its source (a click and its place, a key,
    an agent's). Keymap ids scoped by their owner (2026-11-02). Every pressable thing an action
    and one way in, a button its own declaration, a press declaring what it does (a message, the
    message a draft holds, or the pane's own code), a hotkey only a keymap binding: Vision's
    ideal, taken (the founder, 2026-11-03). A command tile's press runs it. Jump hints with a
    mode each, press and focus first, a hint's letter triggering its action. One way out is
    always Workshop's: a pane may take any key, and a press reaches only the area under it, so
    the setups bar stays one.
  - Docks cover the room, and only authored anchors move panes; a dock keeps a strip its edge's
    whole length, open or shut. Fold and dock are typed fields of a setup's pane row (setup v7,
    session v13; the founder, 2026-11-02).
  - Settings: the double-click speed is input's; themes merge and reset (the research's two);
    locked settings a final layer; a failed key skipped or the theme refused, the theme saying
    which, a wrong type always loud; a reset whole, or applied on top; several keys an action.
  Answered 2026-11-02 and 2026-11-03 ([clarify](drafts/decision-wave-clarify-1.md),
  [clarify 2](drafts/decision-wave-clarify-2.md)). Workshop in its own repository: the right end
  state (Vision's read, taken): the boundary proven in one repository first, a stranger lane,
  then the move, after the visual foundation's first stages; the distance measured
  ([report](../reportbacks/workshop-as-a-stranger-research-RB.md): 111 reverse include lines,
  the seam Zengine's, 23 closings). Its calls (the founder, 2026-11-11): W-1 settled by
  the pane contract (2026-11-08); W-2 the Builder, `external-host/` and the launcher Workshop's,
  the app host and the menu presenter Zengine's; W-3 the Flow host exported whole for now, one
  host the end goal (Loom's `loom-host`, every build-out a plan; a research queued: each
  in-process mount in both Zengine hosts mapped to the Loom feature that frees it, the boot plan
  and the load plan merged, the capabilities a loaded weave holds, the byte seam's cost measured);
  W-4 named trees; W-5 fixtures; W-7 the closings that depend on nothing now, in one round with
  the text check and the Flow host's export, the contract by the pane contract's rounds, the
  suites after it, the key spelling after V7, W-4's two trees before the move, the package, laws,
  checks and links at the move, and the move after the pane contract's rounds, the foundation's
  Zengine rounds through calls, and V7. W-6 the line held from now by a text check in the
  documentation lane, both ways, a census row that only falls, and by Zengine built without
  Workshop's folders before the move. Round 1 prompted
  ([prompt](../prompts/unrun/workshop-line-round-1.md), warm), to run once #141 to #144 are on
  `main`. Designed whole (2026-11-03,
  [design](../reportbacks/visual-foundation-research/design.md),
  [stages](../reportbacks/visual-foundation-research/stages.md),
  [report](../reportbacks/visual-foundation-research-RB.md)): eleven stages in Zengine, V1 the
  pool and palettes first. Both reviewed 2026-11-03, their thirteen calls with the founder
  ([review](drafts/research-review-2026-11-03.md)). The visual foundation's six settled the same
  day, the design amended so (the founder, 2026-11-03), V1 prompted
  ([prompt](../prompts/visual-foundation-v1.md), warm) and V8 beside it in a second lane
  ([prompt](../prompts/visual-foundation-v8.md), warm):
  - **Pictures**: one may change where the change is the point, named with its reason, before
    and after, for his review; byte for byte only for V2's sweep. Every picture added or retaken
    comes from a recipe the kit's picture tool replays. Excised rather than carried: which of the
    four looks ship as themes is proposed with pictures for him to pick; no widening of old
    shapes for strangers (`v0.2.0` is pre-1.0), a bridge for our own drawers ending in V2; the
    conversions of saved setups and sessions kept.
  - **V1**: `Paint` named `Color`, and `color` in every new name. Generated names give
    autocomplete, and a name nobody declared does not build; any name is fine. The generator a
    CMake script, installed, the floor 3.22, a version a lane runs. The skin seam retired, the
    painter one library behind one interface in the window. A colour's terminal word (`cells`)
    optional: without it, the nearest colour the terminal shows; its own ground never matched.
  - **V2**: Flow's 31 hues collapsed to as few slots as is reasonable (about six by Vision's
    count), the rest pool names.
  - **V3**: monospaced first; the platform's fonts, then an embedded last resort that draws the
    character; cases and pictures on the embedded faces; a fallback glyph in its own cells.
    Proportional text a stage of this arc, after V3 and before V9, a pane writing one layout for
    both media.
  - **V4**: a theme's entries for a pane the load plan names wait for it; `refuse` judged when
    the theme is applied, a miss found later skipped and said.
  - **V5**: the beat an office-wide setting, changed through the settings door; a look computed
    from the time since it began, so it lasts its length at any rate. `back` named
    `reverse_on_end`; `repeats` a count, forever a named largest value, not 0. A look never moves
    a hit: the hit drawn at its largest extent, a leaving node taking no press.
  - **V6**: the press lambda stays in its pane, only its message's shape declared; a hotkey asks
    an action by its id, and that action's own press form runs.
  - **V7**: one way-out chord, Ctrl+Q by default, moved only by the weaver; the band shows it
    while a pane holds the keys, and a notice says once where it went if the legend is hidden.
    Inputs, batched ones too, resolved one at a time against the state the last one left, the
    chord never waiting; how keys are routed is Ceecee's.
  - **V8**: shut on the title bar once it is a `Collapsible`, the arrow at the bar's start (the
    left of a horizontal bar, the top of a vertical one); meanwhile on today's title row, no
    second bar; a shut pane keeps its title row with titles hidden.
  - **V9 to V11**: each element stage reviewed for feel, its faces in both media and a pane's
    code using them, before it merges.
  - **Built**: V1 as Zengine #101 and V8 as #102, each green on every required job, reviewed
    2026-11-03 ([V1](../reportbacks/visual-foundation-v1-RB.md),
    [V8](../reportbacks/visual-foundation-v8-RB.md)). #101 merges first, then #102 rebased
    (`tests/shapes.txt`, adjacent lines; [prompt](../prompts/visual-foundation-v8-rebase.md),
    hot). Their texts stay as posted: an edit keeps the old words in GitHub's history.
    Asked, with Vision's leans: the looks (night and day ship, block a tests' fixture, classic
    another word for night; the pool's `own` kept for text and grounds alone, so a terminal shows
    the other colours by nearest ink; into V2); the snake's `1 skin` (kept); the advisory MSVC
    job's hour, settled (the founder, 2026-11-04): ninety minutes before #101 merges, since a job
    stopped at its limit saves no cache and cancels the run, and the night packages only a passed
    one, green all the same; the night made to say so: #104
    ([report](../reportbacks/ci-msvc-hour-RB.md), reviewed 2026-11-04, green on every job), then
    #101 rebased onto `main` and run again
    ([prompt](../prompts/visual-foundation-v1-rebase.md), hot), then #102's rebase.
    #104 merged (2026-11-04). A reviewer of the founder's read the open work (2026-11-04): #66
    closed by #101 and the word `skin` named as known debt in #101's record, both in its rebase;
    v0.2.0's notes ("replaces the package before it") untrue for the first release alone, fixed on
    the release, and `main's tip` kept out of a pull request's Package run: #105
    ([report](../reportbacks/ci-release-notes-RB.md), reviewed 2026-11-04, merged; the notes
    edited). Its cost, the reviewer's: the judge runs in no pull request, so one that breaks it
    passes; the judge exercised on fixed cases in every pull request that changes it
    ([prompt](../prompts/ci-tip-judge-cases.md), warm): #106
    ([report](../reportbacks/ci-tip-judge-cases-RB.md), reviewed 2026-11-05, ready), eight
    cases, one judge; its first live witness the first night after it merges. #100's stale-green
    night already answered by #104's tip job; the shapes conflict and #102's role-picked colours
    (V2's sweep) as known. The peek (waived until
    the title bar's composite); the fifteen held pictures (one recipes pass after V3); one word for
    theme, palette and skin where a weaver sees it (theme, renamed with V4; block's summary
    still says "classic's light").
    #102 rebased onto `main` (2026-11-04): its sanitizer job stopped three times mid-verify by a
    runner shutdown (exit 143), under its 90-minute limit. The job sits at its runner's memory:
    `main` peaks at 15.1 of 16 GB at four jobs, #102 155 MB above it
    ([report](../reportbacks/visual-foundation-v8-rebase-RB.md)); its fix (the founder,
    2026-11-04): each entry measured, the heaviest apart, three at a time only if none stand out,
    the peak said and warned past 12 GB
    ([prompt](../prompts/ci-sanitizer-memory.md), warm): #107
    ([report](../reportbacks/ci-sanitizer-memory-RB.md), reviewed 2026-11-04, merged 2026-11-05,
    `main` green with it), the two
    largest panes suites apart, 6.4 GB on the runner; then #102 rebased
    ([prompt](../prompts/visual-foundation-v8-rebase-2.md), hot;
    [report](../reportbacks/visual-foundation-v8-rebase-2-RB.md), reviewed 2026-11-05, ready: green,
    its sanitizer job at 88 of its 90 minutes after a rerun for a full disk). The looks
    (the founder, 2026-11-04): night and day ship, and block as the terminal look, the one theme
    that changes how a terminal draws (the tests and the snake keep it; a layer over night or day
    with V4's `merge`); classic another name for night; `own` for text and grounds alone. V2
    prompted ([prompt](../prompts/visual-foundation-v2.md), warm): #108
    ([report](../reportbacks/visual-foundation-v2-RB.md), reviewed 2026-11-05), its content ready;
    it follows #102, by its applier from the new start, once the lane's scaling lands
    ([prompt](../prompts/ci-sanitizer-scale-research.md), warm): its sanitizer job passed its
    90 minutes, the runners' doubling, not V2's. The founder's calls on it (2026-11-05): `own`
    named `terminal default`; a pane's ordinary border grey in a terminal; Flow's columns on a
    second background (`background_alt`, the DO column's old `#20252d`); a terminal matched to
    what it can show later, with the terminal research: V2 continued once #102 merges
    ([prompt](../prompts/visual-foundation-v2-continued.md), hot). The snake's pictures
    taken in play by a pilot, the first participant an agent runs to play a program for it,
    playing against the world's own beat and never stepping it, a pause the world honours
    for a picture ([prompt](../prompts/snake-pilot.md), warm), after the research.
    V2 continued: #108 ([report](../reportbacks/visual-foundation-v2-continued-RB.md), reviewed
    2026-11-05, ready: green on every job, its sanitizer job 74 of its 90 minutes); three block
    pictures in a terminal stale for want of recipes, for the held pictures' pass. The pilot:
    #109 ([report](../reportbacks/snake-pilot-RB.md), reviewed 2026-11-05, ready after #108),
    its place by an exercised replacement (WL-PART-01, asked); onto `main` once #108 merges,
    with the snake's pictures in play ([prompt](../prompts/snake-pilot-continued.md), hot).
    #108 merged (2026-11-06). The sanitizer job at scale: #110
    ([report](../reportbacks/ci-sanitizer-scale-RB.md), reviewed 2026-11-06, ready, clean onto
    `main`), in before the pilot's continuation; asked: Inventory's view cost (P-WORK-81) and a
    warning for the builds' memory (P-BUILD-21). The clock's first steps: #111 and #112, their
    report not yet in, #111's run going; both merge clean onto `main` with #110, and #111 meets
    the pilot in the snake's CMake list and the population.
    #110 merged (2026-11-06). The pilot continued: #109
    ([report](../reportbacks/snake-pilot-continued-RB.md), reviewed 2026-11-06, ready on today's
    `main`): the snake's two pictures in play, steady; its test names and rig still say classic
    (V4's word pass). The clock's first steps: #111 and #112
    ([report](../reportbacks/time-first-steps-RB.md), reviewed 2026-11-06), their content ready,
    their runs on `9bc2f646`: onto `main` after #109, with the facet's claim trap fixed
    ([prompt](../prompts/time-first-steps-continued.md), hot). Asked: whether the reactor
    or frame clock (the idle wakes, about 220 a second) is the next round. Not measured: a key in
    a Neovim pane; the switch asked from the Terminal answered and left the standard Editor.
    #109 merged (2026-11-06). The founder took Vision's three leans (2026-11-06): the clock's next
    round, a reactor or a frame clock, researched first
    ([prompt](../prompts/clock-reactor-research.md), warm); the view cost researched as the
    product's, the case unchanged ([prompt](../prompts/view-cost-research.md), warm); and the
    sanitizer builds warned past 14 GB, in a lane beside them
    ([prompt](../prompts/ci-sanitizer-build-memory.md), warm). The clock round's
    continuation reported: #111 and #112 onto `main`, the facet's claim trap in #113
    ([report](../reportbacks/time-first-steps-continued-RB.md), reviewed 2026-11-06, all three
    ready, one tree in any order); the Timer's own claim hook unneeded once #113 is in, one line.

- **State or checkpoint: a research pass** (the founder, 2026-10-29). The Hotkeys pane's open
  sections (`DesktopState::hotkeys_open`, #486) are a checkpoint: the truth is the accordion
  group in the pane's view, copied into the state after each act and read back only when the
  weave activates, so an edit to the field would show nothing and the next act would overwrite
  it. The pass: every weave's state, each field the truth or a copy; each copy made the truth, or
  named for what it is (his `HotkeysStateBackup`). First the eleven states that are `ZEN_EXPOSE`d
  (two in the snake example), where a poke's write is acknowledged; `IntrospectionState` already
  says the rule: "a copy here would be the answer that goes stale". The Hotkeys pane's own fix,
  accepted (the founder, 2026-10-29): its open sections kept in its state as the truth. Beyond the
  pass (the founder, 2026-10-29): components mark the fields they would keep (a text box's words,
  never a hover), and a pane given leave keeps its view's marked fields, by a message set apart
  from snapshot and restore, so no pane keeps a second copy of what it shows. Research at that
  stage; the element set's values (the census) are where the marks would live.
- **What terminals can show: a research phase** (the founder, 2026-10-29, in place of an issue).
  The terminal medium asks a colour of each role (`sgr_for_role`,
  `graphics/window/terminal_io.hpp`) and turns on VT processing in a Windows console, yet the
  accordion's console pictures showed every role in one grey. What each terminal shows, and why
  that console showed none; the medium draws what it honestly can, and no two media promise one
  picture.
- **A message picked by name, declared whole** (near roadmap; the founder, 2026-10-29). Flow's
  New message declares a view's message by name with no fields, and listening for a message is of
  use only with its fields: knowing something happened without its data is hearing an action and
  not being able to answer it. Needs an owner that answers a message's shape by its name.

- **A pane's own top right** (desk round 2's parked item): close and move, a gear, a box around
  each icon, the arrange markers on boxes of their own, "remove from the setup"; about 116 page
  pictures retaken with it. Wake: the kit's picture tool, now built (#558, 2026-10-29). With the
  accordion's desk stages (the founder, 2026-10-28): the title bar is the pane's own accordion
  header, its words and buttons there, a double click shutting or opening the pane; a dock's tag
  is the same bar drawn small, a vertical one its icons stacked and its name a letter a row.
- **One element set for the panes and the View Builder** (Vision's proposal, 2026-10-28, from
  the old `zen-ui-vocabulary.md`, the rebuild scaffold's element census and the code): each
  element a value in `component/` and a face drawn from it, drawn by the panes and offered to
  makers as the View Builder's kinds. The census reported and was reviewed (section 1,
  [report](../reportbacks/ui-census-RB.md)); its nine decisions, the scaffold's call 6 among
  them, wait on the founder (section 5). The text area, from the founder's note (2026-10-29): in
  cells, markers for what is above and below; in a window, free scrolling with a bar of 4 to 8
  pixels on the right; wrapping by width; its text selected and copied. Vision's reading: the
  value keeps the scroll and the selection as places in the text, never rows or pixels, so a
  rewrap keeps both; free scrolling needs the window to cut a line of text by its pixels (today a
  group's clip drops a line whose top is outside it and lets the last spill); the bar's room kept
  whether or not the text overflows, so nothing reflows when it appears, and pressed in a wider
  band than it is drawn; a copy is the text as written, without the wrap's breaks or indents; in a
  terminal the selection is drawn by the pane, since Workshop holds the terminal's mouse. The
  founder's calls (2026-10-29): the bar drawn 8 px wide, 12 px while the pointer rests on it (the
  widening's animation later), its room and its press 16 px, to adjust once used; the markers
  `... 3 more below` and `3 more above...`; the text box built on the text area, with its own
  caret, the whole box pressable (today only its text is) and the caret blinking.
- **The window-run element retired** (the founder, 2026-10-29): `ElementPut`, `ElementChange`,
  the element seam (`graphics/element_abi.h`, `element_export.hpp`, `ZENGINE_EXPORT_ELEMENT`), the
  window's element code and its four shapes, so no window keeps an element's state; the snake's
  board drawn by its world as a picture. About 22 files; two installed headers go, a change to
  the package. Filed as #546 (2026-10-29); `limitations.md`'s line on `graphics/elements/` (#565)
  goes with it.
- **What a window may carry: looks that change with time or the pointer** (the founder,
  2026-10-29, from the blinking caret). A pane's drawing names a behaviour from a closed set the
  window knows (a caret's blink, a part lit while the pointer rests on it, a pressed look while
  held, a change eased from one drawing to the next, perhaps a scroll inside rows drawn past the
  edges), and the window runs it with no message; what the pane must know to answer (a
  selection, a fold, what a press means, where a scroll settled) stays the pane's. The test: if
  the window forgot it now, nothing but a frame of looks is lost. No pane's code in the window,
  which keeps it apart from the retired element seam. Pictures and cases need a steady mode
  (no blink, a change shown at its end). A research, the element set stage's first step. The
  founder (2026-10-29): each animation says its own length, since one may loop for good; and an
  agent's press skips animations: the act tool's own press carries the skip, never a key a
  weaver uses, such as Shift, which will extend a selection (agreed, 2026-10-29).
- **A pane's bar tinted while it holds news the weaver has not seen** (the founder, 2026-10-28),
  shut, covered or only unfocused; the pane's own word says what is news, and looking clears it.
  To weigh against Attention's conditions before a second channel is made.
- **Settings, stages 4 to 6** (BL-WORK-36; stages 1 to 3B merged, #101 and #314 to #326). Stage
  4 is the settings weave applying themes, once its research is read again against the desk's
  owner; it takes the open report rows 47, 48 and 69 to 71. First check whether stage 3B's
  stopgap (locks, pins and baseline in Workshop's settings file) moved with the desk split. The
  design is the founder's eight decisions of 2026-10-18. Wake: met.
- **Every pane a free picture** (BL-WORK-46; steps 1 and 2 merged, #387 and #394). Next: the
  thirteen panes still on rows move one at a time, `PaneRowsFacet` retiring with the last.
- **Control schemes** (BL-WORK-47; the POSIX slice merged, #402). Next: a loader that stacks
  schemes as themes stack, and a chooser in Workshop, the first-run screen's first.
- **Layout modes L3, the views** (L1 #413 and L2 #421 merged). A share's inverse and an anchor's
  offset sit in `workshop/setup.hpp` for it. Wake: met (#340).
- **The story's step 7**: Workshop reconnects to an exported app and takes its weaves back (C1,
  L2 and C2 of the [research](../reportbacks/app-export-research-RB.md)); it needs prompts, not
  research. With it, Loom's small follow-ups: an installed `AuthorityDesk` seat, `authority
  trust` naming a host's baseline, and the bridge's sockets closed on exec (private). Wake: after
  the release.
- **The editor-switch weave** (WL-SWITCH-07): a small weave holding the four switch asks the
  Terminal holds, its remembered choices in the session's header. Wake: met (D1, #415).
- **Places kept across runs**: a pane closed in one run comes back where it was in the next.
  About a day: the session's and the setup file's next versions.
- **Agents and weavers on one desk** (BL-WORK-38). Left: #139, stages 3a and 3b, `host`, `ask`,
  `check` and `probe`, then 4a to 7; the dense reading (a grid rectangle row by row) not yet
  placed. Until the agent desk, an agent's press still moves the keys and the selection.
- **Untrusted code, the WASM tier** (S1 to S4 merged: Loom #72, #74, #75, #78; Zengine #594).
  Left: S4b, the Builder's second target (section 1), then S5, its doors (a clock, standard
  output as messages, a module cache), designed whole. D7's statement is in Loom's
  `capabilities.md` as the research wrote it (#74). An agent without a shell waits on this and on
  tools by reach.
- **The MCP adapter's live check** through the app, and the weaver case on package 0.1.3. Wake: a
  lane left empty.
- **The ELH audit's findings** (a cold agent for the founder, 2026-10-29,
  [report](../reportbacks/elh-audit-report.md)), checked by Vision against the code: the
  `workshop-machine` package's `repo` tool gives git push and pull requests to any session that
  approves Workshop's machine tools; act passing a press its owner refused; `open` leaving a pane
  being placed; Loom's `loom-session` reading an unknown bool spelling as false (`cli.py:247`);
  `inspect-capture`'s test inputs on an agent's tool; scenario scripts a quarter of the catalog;
  no quickstart, and no tool asking for a pane's document. Its claim that Inventory, Info, Demo
  and Compose declare no causes does not hold (30, 7, 2 and 1 rows); resolve answering a missing
  shape as a real one does. Wake: the issue lane's round after its UX batch
  ([prompt](../prompts/issue-lane-elh-audit.md), warm, 2026-10-29).
- **The Perspectives Lab's pages** rebaselined after D1, before any becomes a prompt. Wake: met.
- **Faster builds** (BL-WORK-44; #343 merged): split `tests/workshop_support.hpp`, the largest
  lever (2026-10-27: 36 of the 45 compiles over 2 GB include it, 43 % of a cold build's compiling);
  the sanitizer job back to 60 minutes if the code's health allows (90 now, #356; #419 profiles its
  longest entries); the old CI caches evicted.
- **Fast forward** (BL-WORK-43; S1 and S3 merged): S2 and S4 to S6.
- **The release for Windows and Linux** (BL-ADOPT-06). The nightly package is live (`v0.1.0` on
  2026-10-24, 0.1.3 since, its tally story walked each night). Left: the rest of the release,
  the first tutorials starting from the extracted folder.
  **The release checklist** (the founder, 2026-11-10):
  1. Every version restarts at 1: each shape, each file format, the weave ABI. The release is
     the marker: from the reset on, a library or file says the release that made it, and a
     reader refuses one that says none, so nothing from before passes on a matching number.
  2. All migration code goes: every reader of an older version.
  3. A documentation and comment pass: no past state anywhere, every page and comment saying
     what is.
  4. One release number, 0.3.0 or later, everywhere: the tag, both repositories'
     `project(VERSION)`, the package, `--version` and the pages' copies. Each nightly is a
     release of its own and rolls the last number (the founder, 2026-11-10). Built by
     one-release-number ([report](../reportbacks/one-release-number-RB.md), Loom#22 and
     Zengine#139, reviewed 2026-11-10): the series in one line in each repository
     (`LOOM_SERIES`, `ZENGINE_SERIES`), a package's number from its tag, both programs and
     both CMake packages saying it; at the release only the series moves.
  5. The one-way doors decided first ([the audit](drafts/audit-2026-11-09.md), section 2): the
     ABI's exact-version rule and its fixed tables, the schema id, the licence.
  6. The founder's own setup restarted from nothing; no pre-release build or package kept.
  7. A version fetched is the version found: a project that fetches a tag or its source archive
     (FetchContent, CPM, vcpkg, Conan) and installs it is answered by `find_package(zengine
     0.2.7)`, so a person keeps old versions side by side without a package finder, or their
     later self, mistaking one. The number is in the downloaded files themselves (the founder,
     2026-11-10): git fills a placeholder when GitHub builds the archive (`export-subst`), or
     the nightly attaches a source archive with the number written in. A git checkout of a tag
     reads its tag. Never a commit made by a workflow. Its seam: `LOOM_PACKAGE_VERSION` and
     `ZENGINE_PACKAGE_VERSION`, filled from the tag in place of the nightly.
- **Loom's own release** (BL-ADOPT-07, [prompt](../prompts/loom-release-research.md)): researched
  once Zengine's nightly has published a few clean nights.
- **The documentation overhaul's rest** (BL-ADOPT-05): stage C's tutorials wait for the complete
  stories; stage D comes after the release.
- **The founder's order of 2026-10-03**, after the settings:
  1. what the canvas unlocks (BL-WORK-09): a hover cue, and a tutorial mode walking a pane's
     parts;
  2. accordions and anchors, researched first (BL-WORK-16; anchors to edges and shares landed in
     L1 and L2, the research's prompt written 2026-10-28, section 1);
  3. Files answering a request for a path (BL-WORK-17);
  4. Info as a one-slot inspector (BL-WORK-10);
  5. images (BL-WORK-11);
  6. load metadata, researched first (BL-WORK-26);
  7. a dead weave's last state, inspectable (BL-WORK-27).

  Agents acting by intent (BL-WORK-25) runs beside them.
- **On the founder's word alone**: text in UTF-8 everywhere, researched first (BL-WORK-39); the
  simplest snake played by its own AI, with a C++ to Python owner handoff (BL-WORK-40); the Data
  Conversion Mapper (BL-WORK-41); the Black Box Reader (BL-WORK-42); the demos' last step, a
  right-click that runs one.
- **Maybe later**: a second package set named with `_python`, carrying a Python for those
  without one; the setup words a row lower, with Workshop's own title bar.

## 4. Standing duties and watches

- **Report-backs land in `Zen/unreviewed/`** (the founder, 2026-11-06; constitution section d):
  Vision reviews each, moves it with its evidence and folders into `reportbacks/`, and commits it.
  The status board shows the lanes, what waits for review, the pull requests and the slots
  ([report](../reportbacks/status-board-RB.md), reviewed 2026-11-07). It could show the runs still
  going too -- a pull request's CI, a dispatched Mutants run and its pieces -- so a long run's
  state is seen without asking (the founder, 2026-11-08).
- **Workshop and onboarding grow together** (BL-WORK-01): repeated friction gets a better
  interaction or a true explanation; mandatory before inviting outside contributors.
- **A front door for human contributors** (BL-ADOPT-01): installed prefixes, IDE discovery, the
  lanes; before soliciting contributors.
- **Current law stays cheap to carry** (BL-ARCH-02; #201 merged): the next pass binds each case
  to its cited test file, then the search-and-link pass.
- **The drawing door grows to its full set** (BL-WORK-37; stages 1 to 7 merged): ovals,
  polygons, images, shaders and whole widgets, built for the design rather than as consumers ask
  (the founder, 2026-10-31).
- **The census's remainder** (BL-WORK-45): the mirrors (Attention, Connections, Info's
  properties, Introspection) become data-form views.
- **Night Lab, era 2** (BL-LAB-01): held, top-down; its findings go through the founder to Vision.
- **The local lane** (BL-LANE-01): shelved while the founder weighs where the agents run.

## 5. Waiting on the founder

- The review of 2026-11-13, night: three questions, each with Vision's lean (section 1, the lanes
  of 2026-11-13, evening): Loom's run record on Windows, an older commit published after a
  workflow change, and the host's own wait set all or nothing.
- An adversarial read of Loom, Zengine and Workshop (the founder's Grinch agent, 2026-11-05,
  revised with Vision's corrections): gates inside the visual foundation's rest -- the clock
  (A2) before V5, the interaction contract (A4: gesture streams, a focus chain, dispositions,
  key routing from declarations against the settled pane-first) before V6 and V7, door-level
  authored migration edges (A1) and roles on every element before V9 to V11; async causality
  host-only with an own-origin form for recipients (A5). Cheap now: handler times measured,
  Neovim's reads off the dispatch thread (`call_now` blocks it up to 2 s, 10 s to adopt or
  start), the nap between turns rather than inside the Timer's handler: taken (the founder,
  2026-11-05; [prompt](../prompts/time-first-steps.md), warm), input's wire unchanged.
- The composer's bare values and optional fields (Loom #31's report, 2026-10-08, not asked since):
  a bare value fills the first field in declaration order, optional or not, so `7` for
  `{limit?: Int, n: Int}` fills `limit` and leaves `n` open, and the reply does not say where `7`
  went. Vision's lean: a bare value fills the first required field, an optional one is filled by
  name, and the reply says where each value went.
- `authority pending`: a grammar change, only if he wants one.
- The Demo pane's development recipe: Vision's lean is none.
- Show me opening over Start here, covering its words: Vision's read is to leave it.
- The graphics research's round 2, decisions 2 (a group is a layer: how it lands, in
  [clarify](drafts/decision-wave-clarify-1.md)) and 10 (its eleven seams filed as issues).
- Where the desk's 3a and 3b (BL-WORK-38) and fast forward (BL-WORK-43) fall in the direction.
- The open decisions in one wave (the founder, 2026-10-30), not small batches: every decision
  asked since 2026-10-15 swept against `main` (Zengine `13cc5674`, Loom `a2fe7e2`), with this
  section's, on one [sheet](https://claude.ai/artifact/XQRS3aJeBCbcR9KGDZ4no2) (2026-10-30): 64
  to answer in 12 groups, colours first; 15 small calls Vision takes unless he says otherwise;
  15 not wise to answer yet, each with its reason, at its group's end. His answers save to the
  sheet; Vision reads them back and folds them in here. The sweep's record:
  [drafts/decision-wave-2026-10-30.md](drafts/decision-wave-2026-10-30.md). The items below that
  the sheet carries are answered there. Its first half answered (2026-10-31) in a file of his own,
  kept [verbatim](drafts/decision-wave-graphical-answers.txt) and recorded in section 3; his open
  calls from it, with Vision's answers, in [clarify](drafts/decision-wave-clarify-1.md).
- Where the local lane's agents run (BL-LANE-01).
- The accordion research's eight decisions: Vision takes seven of its recommendations (docks
  taking room, the two row words, the bar's length one setting, the piece in `component/`, Info a
  tree after the first stage, Files' places with the Hotkeys pane first, a pane shut where it
  stands). The founder's shape (2026-10-28): one accordion (a section) apart from its groups, each
  group a small component over it: independent, exclusive, and a pair ("two-sided": two, one always
  open, their space constant); a pane on the desk one accordion, its neighbours following by
  anchors between panes. Settled the same day: an exclusive group may be all shut; a pair is a
  set-size frame of its own, placed like a pane, its first header always at the top and the second
  under it while the first is shut, at the foot while it is open, so it needs no anchors and may
  itself be a section of an outer accordion; docks (the bars) before anchors between panes, a
  vertical bar spelling each tag one letter a row. The founder (2026-10-31): docks cover the
  room, only authored anchors moving panes, and a dock keeps a strip its edge's whole length; the
  row words asked again ([clarify](drafts/decision-wave-clarify-1.md)).
- The census's nine decisions ([report](../reportbacks/ui-census-RB.md)): Vision takes the
  recommendations of 1 to 8, with the hint fed by one facet that hears the keymap, the View
  Builder's parts moved into its makeover; for 9, the drawn faces lifted from Flow's pen once his
  round ends, its emphasis faces as roles a theme maps, not Flow's own colours (2026-10-29). The
  founder (2026-10-29): the window-run element retired whole (section 3); then "I love what we
  have so far", read by Vision as yes to these leans, to confirm. The founder (2026-10-31): 3, 4,
  6 and 7 yes, Image and Grid kept until superseded; 9 folded into the colour system (section 3);
  1 and 5 asked again ([clarify](drafts/decision-wave-clarify-1.md)); 8 with the View Builder.

- #568's first decision ([report](../reportbacks/accordion-stage-2-RB.md)): no door edits
  `DesktopState` or `InfoPaneState` from outside today (Loom's poke writes scalars, its reset
  wants every field exposed), Vision's lean the intended reach for now, the door a later Loom
  stage (on the sheet). Its other two settled as #568 merged.
- The issues' decisions (the founder, 2026-10-29), to be written on each issue and labelled
  `ready` by the next issue lane: #492 every launch key, `Ctrl+p` among them, selects its surface
  when it is open and not selected and closes it when selected; #493 a press outside ends the
  arranging, a one-pane arranging too; #526 the shipped catalog carries every pane's recipe, the
  Demo pane's none; #533 the 34 `using namespace` lines first, the issue kept open to audit the
  530 aliases later; #535 the maintainer's copy of `quarry/` kept in a Zen folder; #572
  `desk/resolve` walks the paths each owner declares a message leads to, hop by hop, branching
  where an owner declares several, stopping at a loop or a bound, and its answer carries no rule
  for filing an issue (the guide does); #580 a refusal said whole as a notice, beside #548; #583
  `zengine.demo` answers a setup's guidance by message, each pane's office its purpose; #588 the
  one-story tools and the demo service in a demos package, the test-only inputs in their own,
  `lane` and `source` where they are; #543 a pane may change its own settings while it runs,
  limits like `keep` among them, Info's rows over another pane's with a settings pane later;
  Loom #73 retraced first (Loom already scopes a grant to a run, to a Weaver's session and for
  good with `authority revoke`; the console grants only for good), session a new grant's
  default, a grant for one run a later scalpel. With their stages: #494, #495, #503, #518, #519,
  #522 to #525, #534. Written on each issue (2026-10-30).
- The decisions round's questions, answered (the founder, 2026-10-30), for the next issue lane to
  write on their issues: #584 an entry's value decoded by Inventory and answered by message; Loom
  #73 `authority allow` lasts the session by default and `authority trust` stays as it is ("trust
  is earned, allowance is a leash to test it on"). #587, a walk carrying a value from an earlier
  step: yes, its whole scope talked through with the founder first.
- Flow's decisions ([report](../reportbacks/flow-live-requests-RB.md)): 3, a view's message
  declared whole, is section 3's near-roadmap item; 5 was agreed (section 1).

## 6. Filed as issues

GitHub holds these; each issue is written as a small prompt any lane can take. Zengine unless
marked.

- **The UX batch** (2026-10-29, [report](../reportbacks/issue-lane-ux-batch-RB.md), whose table
  maps each draft to its issue): #492 to #566 and Loom #73; 39 `ready`, 16 `needs-decision`, 11
  waiting on a lane, another issue or a reproduction.
- **The ELH audit's findings** (2026-10-29, [report](../reportbacks/issue-lane-elh-audit-RB.md)):
  #569 (taken by #570), #571 to #589 and Loom #76 (taken by #77); grouped by tool, 17 `ready`.
- **Needs a decision:** #117 a UTF-8 path cut at a clipped boundary; #118 a required Windows
  lane under non-ASCII folders; Loom #35 a path-encoding contract for `loom-host` sessions on
  Windows.
- **Ready:** #419 profile the Info and Project entries that dominate the sanitizer's verify.
- **Parked:**
  - #119 a release identity and compatibility promise (BL-ADOPT-02);
  - #120 the workload behind the first performance promise (BL-ADOPT-03);
  - #121 the unused authored UI API, and #122 `frame_in` with resolution (BL-DEF-06);
  - #123 the Builder's field-click evidence (BL-VERIFY-01);
  - #124 the simple external pane as a learning example (BL-WORK-02);
  - #126 pane controls reachable when the room is small (BL-WORK-14);
  - #127 the View Builder zooms (BL-WORK-15);
  - #128 to #135 Inventory: an entry found without walking folders, unused views retired, the
    next hotkey context, a folder deleted with its contents, Back and Forward, several entries
    at once, locked entries kept in place, tags (BL-WORK-18 to BL-WORK-21);
  - #136 a saved command run without a hotkey (BL-WORK-22);
  - #137 Terminal command scripts (BL-WORK-23), with Zenscript's research beside it;
  - #138 parallel work detects publication conflicts (BL-WORK-28);
  - #139 a held agent gesture cancelled (BL-WORK-29, a stage of BL-WORK-38);
  - #140 a native operator's source opened from Flow (BL-WORK-30);
  - #141 row views reused in a long list (BL-WORK-31);
  - #142 Flow's next milestone (BL-WORK-32; the makeover is section 2);
  - #143 canvas text fit with a size floor (BL-WORK-34);
  - #144 maker participants' addressed requests and conditional speech (P-WORK-36);
  - Loom #36 cross-layer public include debt (BL-ARCH-01), and Loom #37 a shape's name owned
    explicitly where vocabularies must coexist (P-LOOM-08; now Loom#3, decided 2026-11-09 in
    section 1: its L1 and Zengine's Z1).
- **Later:** #145 GitHub from Workshop (BL-ADOPT-04); #146 several Workshop windows
  (BL-WORK-12); #147 Python scripts as participants (BL-WORK-13, paired with the snake's handoff);
  #148 undo through the owners (BL-WORK-33); #149 an app of its own, edited live (BL-WORK-35).

## 7. Directions that govern

- **Never avoid a version bump** (the founder, 2026-11-02): a shape or a file format moves to a
  new version whenever it changes; the migration path is worth the exercise. At the release
  every version restarts at 1 (the founder, 2026-11-10; the release checklist), so a bump now
  costs nothing that lasts.
- **The goal** (the founder, 2026-10-14): Zen legible, and good to use as a human weaver:
  documentation, then the split, then the UX batch, then complete stories on a well-formed
  architecture.
- **The direction** (2026-10-19): subtract before adding, one owner at a time, decisions before
  prompts. Phase fences are off until Workshop is release-ready.
- **The founder's order**: the UX batch, then the first complete maker story.
- **The principles**: the ability to intuit and learn comes first; systems compose gracefully;
  what is good for human makers is good for agents; source code stays a first-class way to make,
  beside Flow.
- **The roadmap's themes** (each in full in closed_work.md, section 1b):
  1. documentation first: done, its tutorials waiting for the stories;
  2. one owner per job: the later splits take the ownerless seams;
  3. actions, subjects and outcomes described once;
  4. relationships and powers: every loaded row but Inventory is admitted `allow_any`, and
     `SetupApplyRequested` judges no asker;
  5. a subject keeps its identity;
  6. workspaces, perspectives and navigation (UX-08 to UX-11), waiting for the workspace's owner;
  7. two modes for agents; open: what each restricted profile may read;
  8. graphics, components, and data as UI with a presenter;
  9. connected tools: Loaded, Project and Compose researched as one journey;
  10. configuration and personal work, kept apart from shared contributions;
  11. tools, demos and workers: the quarry out of Zengine is fileable now;
  12. execution experiments, later, message cost measured first;
  13. the first complete story, last.
- **Cut from the alpha**: the C++ installer suite, theme presets, plain-language passes beyond
  what the story touches, fast forward's S2 and S4 to S6.
- **Design calls that still govern**:
  - POSIX keys are a compatibility layer patching the defaults, each weave declaring its own;
  - a press is refused only where a new element stands under the hand;
  - a pane too small to be useful is the weaver's choice until it cannot be found or recovered;
  - Notices says only what helps the weaver understand what just happened;
  - a placing ends only at a key or a press;
  - a page's old pictures wait until the page next changes;
  - a floating pane is a whole workspace in a window of its own, and an exported app is code of
    its own;
  - work is done by mouse where it can be, its keys the ideal ones (the Perspectives Lab's rule);
  - a terminal is never made to show every element a window shows: a border, a bar or a look is
    the window's, and the cells' own layout decides how an element reads there (2026-10-30);
  - `component/` knows no medium: a piece is measured there in characters, and its looks, the
    window's and the terminal's, are faces side by side (2026-10-30).

## 8. Loose ends for the next issue sweep

GitHub labels (the founder, 2026-11-03): `parked` goes with no replacement, and `later` with it,
both vague and restrictive; `needs-decision` stays, the honest kind of not ready. Their issues
keep their other labels; better-named labels may come. Prompted in `left-behind-cleared`.

Loom's threading line (the founder, 2026-11-02): `docs/laws/messaging-laws.md` says multi-threaded
dispatch is not built, and nothing may assume it never will, not "a non-feature until a consumer
forces it". The same stance stands twice more: MSG-09 ("neither is planned") and
`docs/reference/known-seams.md` ("Maybe or never").

Filed by the UX batch (2026-10-29, section 6): the guest `ask` row (#536), `fill_laws.sh`
(#537), the `Surface*` shapes (#538), `apply`'s scan (#539), the desk split's cases (#540) and
its close sentence (#541), `three-places.md` (#542), Notices' `keep` (#543), the held drag
(#544), the fixture split (#545), the window-run element (#546), a window's release and text
(#547), a refusal `act` cannot hear (#548), the palette's start line (#549). Taken by its pull
requests: the census's doc gaps (#565), the corpus page (#555). Found settled on `main`: the
census header's `PaintTask`, the notices headers (#430), the build runner's starters, G2's SDK
install, the restore notice (Notices keeps every notice; reasoned).

- Comments and pages still name `judge_content` and `canvas_content_problem`, which exist in
  neither repository, and say one byte a canvas cannot draw refuses a pane's whole picture:
  `builder/builder-pane/pane.cpp`, `introspection/loaded.hpp`, `files/files.cpp` (twice),
  `workshop/pane_text.hpp`'s header, `agents/panes.md`, `agents/decisions/
  a-build-keeps-its-own-words.md`, two cases' comments. #553 mended `drawable`'s alone.
- In the pages' pictures the terminal's Pane Manager covers Info's first column, and the
  smallest window's Notices covers Info (the kit's audit).
- A suite's floor is the fewest cases any configuration compiles (`input`: 62 on Linux, 59 on
  Windows, #591's first run red): `docs/contributing/taking-an-issue.md` says "the measured count"
  without saying on which.
- A loaded weave cannot read its own id (Loom; no owner).
- The desk split's `-s` aborts in nine more assertions, fixed at each case's next change.
- An issue to shorten `neovim_journey`, set aside.
- Doc gaps not located on `main` from these words (2026-10-29): `AGENTS.md`'s floor wording (now
  the sum over four); doctest's `--duration` on WSL's stepped clock.
- The kit: the mutation script could count each mutant's text before building; a probe helper, asked
  twice. From beats-with-work-RB (2026-11-07): `case-wsl.sh` passes a `-tc` filter with a comma,
  which doctest splits; `mutate.sh` runs while a lane builds the same copy; `run-end.sh` ends on one
  network timeout.
- The reactor's follow-ups (reactor-RB, reviewed 2026-11-07): a source the wait lets go in its hold
  (past the 62-handle bound) hears so only after a whole wait, up to the 1 s cap, and an end to the
  wait whenever the hold told anything would close that; the hosts trust their plan's offices once,
  at start, so a setup that brings new offices leaves their sources beating; with every window gone
  from a running Workshop the Input office takes the console back only at its next delivery; a
  source must drop from its claim a handle it can no longer drain, an ended pipe, since the wait's
  guard cannot see one claimed anew; on a classic console a resize of the height alone may send no
  record (`graphics/docs/zengine.window.terminal.md`).
- The installed-package witness ran only where rule 6 asked, and the reactor round judged its
  headers did not reach the package, though a public header it changed included a new one
  (reactor-RB, after review, 2026-11-07): a header a public header includes is the package's too;
  `tip-wsl.sh --package` the cheap way to ask. Owner: the standard delivery (constitution c) or the
  kit's README beside `tip-wsl.sh`.
- V3's leftovers (visual-foundation-v3-RB, reviewed 2026-11-07): ASCII projections outside its 24
  files still draw `?` past ASCII and count bytes (Files' `shown_name` and its path test,
  Introspection's `powers_detail::printable`, Flow's `clean`, Neovim's `ascii_of`,
  `workshop/path_admission.hpp`), each its owner's change; pane code that measures labels and rule
  lines by `size()`; the Terminal's manual sections at their 2,048-byte budgets. Files'
  `files-name-beyond-ascii-window.png` and its alt text say a `?` a byte (`Zo?? ??/`), false since
  `f66429a6` (2026-10-29, a `?` a character), and no recipe takes it: a recipe and a retake once
  Files draws a name as spelled.
- V4's follow-ups (visual-foundation-v4-RB, reviewed 2026-11-07): a merge's look lasts until the
  next launch (its settings and keys are kept), and a palette named by its theme holds one layer,
  so `block` over `day` in one layout and over `night` in another cannot both stand (asked;
  Vision's lean: a layout keeps the stack it wears, the palette named by the stack); a row's
  `workshop.theme` takes the three built-in themes alone, and `app.json` still says `window.skin`
  (both asked); a stale batch is known by its refusal's words (`stale revision`), not a field; an
  apply in flight across a reload is lost unanswered; `settings/slots.hpp` is not installed, so a
  stranger's pane cannot declare slots; the snapshot, promote and provenance doors refuse.
- The pictures' follow-ups (visual-foundation-pictures-RB, reviewed 2026-11-07): the Files manual's
  and the row menu's pages cannot be reached by a walk (WL-DESK-20; no `act` step presses a frame's
  handle); the window twins and 66 other pictures have no recipe; `picture.sh audit` crashes on a
  picture its checkout lacks; a terminal selection draws nothing in the default look (P-WORK-87).
- A suite does not build the weaves it loads: `zengine-tests` names `snake-world-v1` through
  `$<TARGET_FILE:...>`, which adds no build dependency, so building the suite's program alone ran an
  old library against new tests (beats-with-work-RB, 2026-11-07); `tests/CMakeLists.txt` could
  `add_dependencies` each suite on the libraries its definitions name.
- A rows pane draws its caret whether or not it holds the keys, so with every box shown two
  carets stand at once (Loaded's empty box beside the Terminal's line, #593's picture).
- `story_journey`'s U7, a 0.5 s wait in the tower-defense story driver, ran out on a slow
  MinGW-w64 run (#594's first attempt at `8f40dbf`); green on the rerun.
- Docs against code, from the founder's self-test (2026-10-30): 26 places where a page or a
  comment says one thing and the code another, each with its lines, in
  [drafts/docs-vs-code-2026-10-30.md](drafts/docs-vs-code-2026-10-30.md). The weightiest:
  `messaging.md` calls `Mail::reply` a send back to the sender when it goes only to `reply_to`,
  so README's first snippet replies to no one; the poke pages call reading opt-in when every
  field reads by default; Loom's sessions guide says a package's `asks` where the code reads them
  per tool; the demo setups' page leaves out the two `-machine` packages every setup approves;
  four Zengine pages call the Input weave the sole producer of input, which the SDL window is not.
- The doc gaps of 2026-11-13, night: `editor-materials-demo` looks for the Terminal's old input
  row (`external-host/tools/workshop-machine/editor_materials_demo.py`, `capture_command`); the
  game-time research's readings table counts the transfers' naps as product bounds, which were
  Neovim's own timers; VM-LANE-27 names its budget in hosted seconds and its pieces in local ones,
  the ratio (4-5 on the slowest runner class) written nowhere, and the sanitizer build's 14 GB
  warning, past on the panes runner, has no owner; the rig's screen check
  (`tests/rig_windows.cpp:527`) failed once under a faster `Keys::row_of`, not investigated;
  `windows.h`'s `far` and `near` macros broke a MinGW-w64 build (Loom's portability notes); a
  case asserting a time it slept is a flake at Windows' 1 ms timer period, which a check could
  refuse.
- For Raid's next batch (the founder, 2026-11-13): realization's claim `PlanWhere` (#163) renamed
  `PlanStatus`, the house name for where a thing stands (Zengine's `BuildStatus` and `DemoStatus`,
  Loom's `LedgerStatus` and `SenseStatus`); it is the only `*Where` shape. `PlanState` stays its
  one-word phase inside.

## 9. Not backlog

These stay trigger-governed horizons or pressure, not owed work:

- inside the built-in Editor: tabs, Vim emulation, syntax highlighting, a VFS, a file watcher, a
  Flow editor (a differently shaped editor arrives as a pane weave instead, P-WORK-07);
- one pane shown several times, and plugin discovery (a pane's free drawing is BL-WORK-46's);
- live artifact replacement before a concrete owner and continuity case;
- general obligation, consensus, metadata or persistence frameworks;
- multithreaded dispatch;
- Windows native containment, or escape-tier security;
- production hardening of the bridge before hosted or remote use;
- a replacement SDL executor for Loom's portable pixel layout.
