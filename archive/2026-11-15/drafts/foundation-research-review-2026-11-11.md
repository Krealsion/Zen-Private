# The foundation research, two reports: Vision's review (2026-11-11)

Ceecee's research ([report](../../reportbacks/loom-foundation-research-RB.md), fourteen
decisions) and the auditor's run of the same prompt ([report](../../reportbacks/loom-foundation-auditor-RB.md),
eleven), both read at Loom `9fa4896a` and Zengine `a28bd068`. Checked here against those trees.

## The headline

The union goes first, in both. Ceecee's finding stands and corrects the expectation: the union
removes no handler from the hub. The hub grew in doors (31 accepted shapes and 7,639 lines on
2026-09-15; 93 in its own list and 3 more from its two facets, which Ceecee counts as 98, and
12,574 lines at `a28bd068`), and doors
leave when the facts it relays move to their owners, when calls replace the hooks, and when the
floor replaces the quit watching. The union is what lets every later round publish its shapes
once.

## Both agree

- **The union**: a named shape with a kind of its own, nested or at a door, written as a
  `std::variant` and one line naming its cases; an enumeration is a union of empty cases.
- **Admitted values never change**: Loom#18, then a nested value made in place and never adopted
  (closes P-LOOM-23), and a visit budget for shared values; not a flat rewrite of `Value`. The
  auditor's positional slots wait for a measurement.
- **Blobs**: named by content (SHA-256 and size), held once by the host, handed and never forged,
  bounded a weave; a history names them and does not hold them; not a frame buffer.
- **Deadlines**: the reactor wakes a trusted role at the time it claimed; idle goes from a beat a
  second (`kBeatCapMs` 1000) to none. Loom ends no ask at a time (Ceecee's 9).
- **Strict through the release**; the release checklist already deletes today's migration code.
- **The ABI grows**: sizes on its tables, one more exact break, appends after it.
- **The order**: the union first with the seam beside it, then the floor; deadlines at any time.
- **A weave past 24 doors is suspected of being two.**

## Where they differ, and Vision's lean

1. **Creation** (Ceecee 8, auditor D6). Ceecee: nothing; the first turn. Auditor: one gated value
   at `create`, declared by the weave, delivered with the load. Lean: the value, data and never
   doors (Ceecee's own list of mistakes allows it): a Loom primitive in place of each host's
   first-turn message, recorded with the load, refused through `create`'s existing sink before
   admission. In the growth break.
2. **Calls** (7, D5). Ceecee: a function of the argument and the provider's claims. Auditor: of
   the argument alone. Lean: the argument alone, provided by a role's holder (Ceecee's naming,
   so replacement still holds). The four C ABIs are argument-only already; a caller that needs a
   provider's state reads its claim and passes it in. Widening later is easy; narrowing is not.
3. **The open set** (4, D1). Ceecee: a union cannot list shapes named at run time, so Loom's body
   codec goes public (two functions), and a kind for any shape stays pressure. Auditor: the union
   deletes `graphics/implied.hpp` whole. First lean: Ceecee's. Then, asked: the union for a node's
   operands (a closed set) and whole envelopes for an element's changes (the open set). Corrected
   on the founder's question: a kind for any registered shape, in the union's round. The gate
   checks a nested value at the send, a weave nests only what it may send, history and tools see
   it, and Loom has its own consumer, `zen.Bequest`'s items (the takeover's letter); an "untyped
   Any" is what the auditor refused, and bytes are the untyped form. Fence: a field takes any
   shape only where the set is open.
4. **The measure** (13, D11). Ceecee: a pinned census, red when the tree differs either way, the
   hub's row marked to fall, in the documentation lanes. Auditor: file and class line ratchets and
   a runtime cap of 24 doors in Loom's `register_weave`. Lean: the census, with the auditor's
   class-lines ratchet beside it (the hub hid in 22 files); no runtime cap: a substrate refusing a
   stranger's weave over its door count is a style rule made a law.
5. **Joint publication** (14, D10), about a thousand lines of `Switchboard` with one consumer
   (the opening). Ceecee: keep it, ask after the floor. Auditor: extract now, delete before the
   release if the opening can use one claim. Lean: ask after the floor and delete if the opening
   does without it; a move into its own file shrinks nothing.
6. **Evolution after the release** (11, D8). Ceecee: doors open to declared extensions before
   the first pane lives in another repository. Auditor: a small authored migration helper for
   files. Neither is needed before the release. Timing: Workshop's own repository before the
   release would pull Ceecee's choice earlier.
7. **The ABI's numbers** (6, D9). Ceecee: v12 for Loom#17 as decided, 13 the growth break.
   Auditor: #17 folded into one v12 break. Lean: the founder's v12 for #17 stands; 13 is the growth
   break; after it every change still moves the number (never avoid a version bump), without
   breaking an older image.

## Checked, and what did not hold

- **Held**: `HostContext`'s 19 hooks (`workshop/weave.hpp` 91); the hub's 12,574 lines and its
  September numbers; 329 includes of `workshop/` from other folders outside `tests/` (the pane
  contract's rounds are already cutting them); the beat cap; `kMaxArgsBytes` 64 KiB, so 127 by
  127, not Vision's 128; Loom's in-memory gate asking identity by the 64-bit id
  (`src/gate.cpp` 172, 208); the artifact page reading and hashing the whole file each page.
- **Ceecee**: `HostContext::interaction_now` is not dead. The rigs wire it as their clock
  (`tests/workshop_support.hpp` 1026, 3448) and the hub reads it, falling back to the steady clock
  (`workshop/weave_run.cpp` 25). Its "deletion for the issue lane" is not filed.
- **The auditor**: 107 accepted and 50 emitted do not match the hub's declaration (93 in its own
  list and 3 from its facets, 61 emitted; Ceecee's 98 is near, its 61 exact); "80+ hub overloads" deleted by the union is
  not supported; "`HostContext` to 0" leaves out its seven members of live state (`quit`,
  `host_fact`, `managed_pane`, `showings`, `undelivered_quits`, `standing_conditions`,
  `conditions_generation`); the content-id fix belongs to the private round (option A, decided),
  not the union's public round.
- **The private round's list** is both lists together: Ceecee's Zengine sites (evidence E9) and
  the auditor's `flow/generate.hpp` and Loom's own in-memory gate, whose field check after the id
  narrows it, and which option A covers.

## Next, on the founder's decisions

Loom's U and S, then F1; Zengine's ZR (the realization owner a participant) needs no Loom round,
but it takes `app/`'s includes of Workshop's headers, which wait on the stranger research's seven
decisions.
