# Editor participation in typed drag and drop

**Selected:** founder discussion, 2026-09-24.\
**Owner:** [Workshop goal map](../goals/workshop.md#near-term-order-and-purpose).\
**Packet:** [Editor typed transfers](../../prompts/zengine-editor-typed-transfers.md).\
**Execution:** parallel to the ELH tower-defense creation story; isolated Git worktrees, builds,
runtime, ELH session and records. Neither depends on the other's unmerged changes.

## Purpose

Let conventional coding participate fully in Workshop's reusable material: bring commands/text
into the active editor, capture selected text into Inventory, and retain file locations that
reopen without a Files navigation trip. Flow is the larger drag-and-drop consumer, but it is
not required for any of these actions. Use real coding interactions to learn what should be
easy in Flow, while preserving coding as a useful and enjoyable approach in its own right.

## Selected outcomes

- Insert saved text and a real command/message into standard Editor or Neovim as editable text,
  without execution, save or build. Use a documented truthful representation with schema/data
  preserved; do not invent a destination or fill absent arguments. Pointer targeting and
  selection replacement must be legible, revision-bound and undoable. Neovim must receive data
  rather than interpreting it as commands.
- Extract only an already established nonempty selection: right-click > Extract or primary drag
  beginning inside the existing highlight. Drags starting elsewhere continue selection, without
  exporting on crossing the edge. Export an owned typed copy of actual buffer text, including
  unsaved edits, with separate source metadata; do not cut/move the original. The same owner
  action has a keyboard route. Captured text survives source closure and toolbox restore.
  Neovim selection modes and the standard editor's narrower byte law need truthful
  behavior or clear refusal, never silent loss.
- Save a typed file locator, distinct from file contents and a generic stored command. Dropping
  it on the active editor requests managed open/reveal, preserving dirty work and current-owner
  authority. It survives process restart as a locator, not a live identity; missing sources,
  worktree changes and stale ranges remain explicit. Optional caret/range retention must not
  target a later document. Automatic relocation and rename tracking are not selected.

The founder also authorizes optional C++ generation as a separate action, offered only in
recognized C++ documents. Verify real type/API/header requirements, show proposed includes and
dependencies, and compile a complete supported example. Unknown context stays explicit rather
than becoming guessed runnable code. Generating text performs no send/save/build; optional
generation must not block the core transfer story.

Reuse the existing opaque carrier, Inventory item/metadata pair, operation approvals and managed
opening. The document owner decides mutation; Workshop need not decode editor data. Actor
authority, pending-request identities and pictured geometry survive cross-pane use coherently.
Flow receives reusable meanings, not a mandatory editor dependency or special language.

## Execution and proof

Branch from fetched current remote main in a new product worktree. Explicit dependency prefixes
and task-local runtime/data/session paths prevent interference with Ceecee's running creation
experiment. This task uses ordinary development tools and its own fresh runtimes; the ELH-only
and live-reload experiment restrictions belong to the tower-defense packet. Use a separate Zen
records worktree for reports, read the canonical nested private repository explicitly, and leave
shared private-document proposals for Vision to integrate.

The story connects unsaved selected text, named Inventory storage, editing/undo, a stored command,
file bookmarks and fresh-process restoration, across both editors. Prove SDL drag and TUI pickup,
exact owner data, useful refusal, no execution/save on insertion, and stale-event/switch/open
boundaries. Keep an `editor-materials` toolbox, useful setup and a short state-reactive ELH demo.
Measure ceremony where practical and report implications for Flow and source editing separately.

Relevant pressure: BL-WORK-01 (usable instructions), P-WORK-04 (editor use), P-WORK-25 (pictured
target identity), and BL-WORK-03/P-WORK-28 only when extending the large Info/Inventory owners.
Do not turn this into unrelated editor polish, offer retirement, generic migration, universal
conversion or a general refactor. Product law/guide updates accompany actual behavior changes.

## Later idea: Terminal command scripts

The founder coined `.zenscript` as a possible script of commands run as if sent through Terminal,
similar in purpose to a shell script. It does not exist and is explicitly excluded from this
editor phase. Keep it as a roadmap candidate for repeating real command sequences. Any future
packet must choose ordering/completion, failure/cancellation, addressing and current authority
semantics using the real Terminal/message owners; the extension itself is not an architecture.
