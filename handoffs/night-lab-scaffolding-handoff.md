# Handoff: Transition to Zen Night Lab — Pane/Setup Scaffolding, Interaction Choreography, and Pairing-Intent UI Drafts

From the founder (Krealsion), 2026-10-15. Written by Vision for the session finishing the Round 2
merge train (`#220` to `#249`), which transitions into holding **Zen Night Lab (`BL-LAB-01`)**.

## 1. The New Development Process (One Vision + Three Executor Paths)

Once the Round 2 merge train (`#220` to `#249`) lands and `main` is green, Zen operates with **one
Vision thread** and **three execution paths**:

1. **Path 1 — Primary Development Executor (under Vision)**:
   - Driven directly by prompts in `Zen/prompts/` written and reviewed by Vision.
   - Executes the bottom-up structural spine on `Loom` and `Zengine`:
     - **Phase 1**: Composable Weave Facets (`With<Facets...>`, `P-WORK-72`, `P-WORK-73`) and One
       Action Path (`backlog.md` §1b, Theme 3).
     - **Phase 2**: Hub split (`backlog.md` §1b, Theme 2: Terminal door first, reload-safe state
       across the 9 weaves in `ownership.md`, and moving the window/arrangement job whole into
       `graphics/`).
     - **Phase 3**: The 11 core `graphics/` elements, helper functions, and migrating/collapsing
       Workshop's 12 panes onto `graphics/` windows (`BL-WORK-37` Stages 2 to 5).
     - **Phase 4 & 5**: Explicit per-row grants (`P-WORK-68`), wakeable Timer/input latency
       (`P-WORK-70`, `BL-WORK-43`), Settings Stages 2 & 3 (`BL-WORK-36`), UX batch, Release
       (`BL-ADOPT-06`), and the First Complete Maker Story.
2. **Path 2 — Zen Night Lab (`BL-LAB-01`, Your Thread)**:
   - Works **top-down** ahead of Phase 2 and Phase 3: designing and prototyping how panes, setups,
     interactions, and human-agent pairing intents should actually look and play out on the target
     architecture.
   - Your outputs feed Vision's Phase 1B, Phase 2, and Phase 3 prompts so that when Path 1 builds
     the 11 core elements and rewrites Workshop's panes onto `graphics/`, it builds directly to
     your proven scaffolds and interaction drafts rather than guessing UI and intent shapes on the
     fly.
3. **Path 3 — Isolated Local-Model Issue Lane (`BL-LANE-01`, `UnknownWorkers`, Later)**:
   - Runs strictly off public repositories inside an isolated wall under the `UnknownWorkers`
     GitHub account, taking self-contained `ready` issues fenced by `## Folders` blocks once Path 1
     has split the hub and shrunk the panes.

---

## 2. Your Baseline After the Merge Train

Before starting Night Lab work:
1. Finish landing Round 2 of the `#220` to `#249` merge train so `Zengine` `main` is green with the
   updated population floors.
2. Read the diagnostic outputs from Phase 0:
   - `Zen/reportbacks/manuals-first-RB.md`
   - `Zen/reportbacks/manuals-first/ownership.md`
   - `Zen/reportbacks/manuals-first/messages.md`
   - `Zen/reportbacks/participant-census-RB.md`
   - `Zen/private/backlog.md` (§1a and §1b, Themes 1 to 13)
   - `Zen/private/ux-batch.md`
   - `Zen/private/handoffs/phase-1-handoff.md`

---

## 3. Your Primary Deliverable: The Scaffolding, Interaction, and Pairing-Intent Package

While Path 1 executes Phase 1 (`FacetWeave` + Unified Action Path), your mission is to produce a
cohesive architectural and UX draft package (in `Zen/rebuild-scaffold/` or Night Lab's workspace)
covering three interlocked artifacts:

### A. Pane & Setup Scaffolding
Using the ownership map (`ownership.md`) and participant census (`participant-census-RB.md`),
draft the target structure of Workshop's panes and setups on the post-split architecture:
- **Pane Decomposition & Facet Map**:
  For each Workshop pane (Files, Builder, Editor, Terminal, Inventory, Info, Flow, View Builder,
  Attention, Introspection [Loaded/Project/Powers], Compose, Connections, Desktop/Manual/Hotkeys):
  - What is its **true authoritative domain state** (in Loom `State`, surviving `zen.ReloadWeave`)?
  - Which composable facets (`DrawingFacet`, `ManualFacet`, `ActionFacet`, `SettingsFacet`) does it
    attach?
  - Which panes are actually **data-form mirror views** (Attention, Connections, Introspection,
    Info's properties view) that collapse into thin bindings over standard `graphics/` elements once
    `BL-WORK-37` lands?
- **Setup & Workspace Scaffolding**:
  How a workspace arranges tools and material, and how task-oriented perspectives (Coding, Building
  & Debugging, Flow & View Authoring, Inspection & Stewardship) seat panes and per-layout settings
  (`BL-WORK-36`) without `WorkshopWeave` acting as a central relay.

### B. Step-by-Step Interaction Choreography
Detail how real maker journeys play out message-by-message and gesture-by-gesture across the new
boundaries:
- **Window-Owned Input & Action Routing**:
  How clicks, keys, pointer motion, drag, wheel, hover, and carry/drop travel through the
  `graphics/` window weave (`zengine.window.*`) straight to the area's owner via the unified
  `*Requested` action path—with zero `WorkshopWeave` middleman hops.
- **Cross-Pane & Cross-Workspace Flows**:
  Walk through the concrete steps, message chains (following the naming law: `*Requested`,
  `*Answered` / `*Refused`, past-tense deed, noun observation), subject continuity (`backlog.md`
  §1b, Theme 5), and failure/refusal recovery for:
  1. Opening, editing, building, and reloading a weave in place (`Files` -> `Editor` -> `Builder`
     -> live reload).
  2. Inspecting a participant, editing a typed setting (`Info` <-> owner), saving a command or
     reference into `Inventory`, and carrying it to another workspace (Theme 13's complete maker
     story).
  3. Connected tools (`Loaded`, `Project`, `Compose`) operated by mouse alone (`backlog.md` §1b,
     Theme 9).

### C. Robust UI Draft with Pairing Intents (`BL-WORK-25`, `BL-WORK-38`, `BL-WORK-37`)
Every screen in Workshop serves two hands on one desk: the human maker and the bounded agent. For
each scaffolded pane and setup, specify both sides of the coin:
1. **The Human UI Draft**:
   - Whole-pixel geometry, clean visual hierarchy, low cognitive load for an average user first,
     hover cues, accordion/anchor behavior (`BL-WORK-16`), and which of the **11 core `graphics/`
     elements** (`BL-WORK-37`: text, text box, button/control, recycler list, grid/table, tree,
     accordion, SVG/icon, image, etc.) the pane uses so panes stop drawing bespoke primitives by
     hand.
2. **The Agent Pairing Intents (Two Modes, Theme 7)**:
   - **Human-Interface / Tutor Mode (`BL-WORK-38`)**: What the agent reads on the character grid
     (`DeskRead` / `PaneView`), how every interactive control and subject region is addressed
     (`<office>/<pane>:<id>` / `control:<id>`), and how the Tutor walks a human through the UI via
     `GuideRequested{pane, control, words}`.
   - **Semantic Intent Mode (`BL-WORK-25`)**: The high-density intent messages where an agent (or
     saved Inventory command / Compose draft) states a complete goal in one typed `*Requested`
     message—and receives one attributed `*Answered` or `*Refused` outcome—instead of issuing
     twenty low-level UI clicks or keystrokes.

---

## 4. Boundary Rules Between Night Lab (Path 2) and Primary Dev (Path 1)

- **Do not open competing code PRs against `Zengine` or `Loom` while Path 1 is cutting the spine**:
  keep `main` clean for Path 1's staged PRs.
- **Write concrete, inspectable artifacts**: put your scaffolds, interaction sequences, UI mockups,
  and pairing-intent schemas into `Zen/rebuild-scaffold/` (or `zen-night-lab` once the WSL wall in
  `night-lab-handoff.md` is live).
- **Feed findings through the founder to Vision**: as each piece of the scaffold and UI/intent draft
  is ready, present it to the founder. Once approved, Vision will fold those exact element contracts,
  action tables, and intent shapes directly into Path 1's Phase 1B, Phase 2, and Phase 3 prompts.
