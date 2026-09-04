Absolutely. I think the roadmap has become much clearer over the last few phases because several formerly tangled questions have separated into distinct layers.

The biggest change is this: **Workshop is no longer mainly trying to become a better hard-coded IDE. It is becoming an environment that can increasingly inspect, author, arrange, and eventually wire itself.** WUX-R14 confirmed that the missing thing is real: pane interiors are mostly imperative/transient today, and no durable representation currently means “what is inside this pane.” 

Here is how I would currently map everything ahead of us.

1. **Finish stabilizing the Workshop we already have — immediate/near-term.**
   - **Loaded scrolling.** QR-18 made scrolling local to each pane that already owns traversal state, but Loaded still emits `... N more` without having a list origin. That is the one explicit remaining violation of our emerging law: *if you disclose hidden ordered content, you owe traversal of it.* 
   - **Rename the current WUX-13 tool to `Pane Manager`.** Its actual responsibilities are pane inventory, participation, identity/provider, outer X/Y/width/height, state and front order. That name leaves `Pane Editor` available for editing `MyPane` itself.
   - **Make Pane Manager the normal pane-management surface.** Likely add a direct participation control on each row—checkbox/toggle semantics rather than forcing `o`.
   - **Reuse the Info/properties surface for value editing.** Long term, selecting a pane in Pane Manager should let the right-side inspector present its X/Y/width/height/etc. rather than every future semantic editor growing its own duplicate property UI.
   - **Give Pane Manager the recovery contract:** `p` summons it if absent and selects/addresses it; `R` while it is addressed restores its usable default place and size. If the current pane-count ceiling could block admission, reserve one recovery seat rather than making the whole pane special.
   - **Then retire the fixed `PANEL` picker.** Its original architectural justification was reacquisition. Once `p → R` is presentation-independent and arrangement traversal remains available, I no longer see a compelling spatial recovery case requiring it.
   - **Keep QR-18's conservative Escape rule.** Escape clears ordinary selection only where Workshop can know Escape is unclaimed; text-taking/external panes retain it because the provider seam has no `consumed` reply. 
   - **Finish terminology cleanup:** maker-facing `panel` → `pane`. Internal `PanelKind`, `paint_panels`, etc. can wait for a mechanical cleanup; they do not currently change semantics. WUX-R14 explicitly separates these historical symbol names from the real durable `PaneRef` concept. 
   - **Hotkey/attention chrome cleanup:** Hotkeys sizing is done; remaining pressures include making the permanent hotkey band optional/removing it, moving its one discovery hint elsewhere, and giving warnings/errors an honest transient/history surface instead of allowing them to overwrite standing status.
   - **Dirty-editor quit decisions:** silent refusal should eventually become an explicit Save / Discard / Cancel decision surface.
   - **Read-only text behavior:** labels, paths, diagnostics, etc. should become selectable/copyable, with double-click word selection and a way to inspect text that cannot fit.
   - **Pane-local status positioning:** the “gray explanatory text pinned at bottom” pressure remains, but I would solve it through authored interior layout rather than introducing a hard-coded `footer` species.

2. **Establish the first genuinely maker-authored pane — next major architectural milestone.**
   - WUX-R14's strongest result is that a pane's reusable authored interior simply does not exist as data today. Built-ins compose C++; providers emit transient rows; Surface sees resolved presentation, not reusable meaning. 
   - The smallest useful experiment remains excellent: **one maker-created pane containing one text region**, authored on the fine lattice relative to the pane's interior, saved as project truth, loaded again, and presented honestly on SDL and TUI.
   - Its durable artifact should be separate from Setup and Session:
     - pane artifact = what the maker made;
     - Setup = where an instance participates on one desk;
     - Session = which desks were open/how the machine was left.
     WUX-R14 strongly supports a distinct project-level pane artifact. 
   - Fine geometry should remain medium-independent. SDL can resolve exact pixels; TUI honestly projects the same intent to cells. Surface already proved it can carry independently positioned fine text regions without a vocabulary change. 
   - **Important correction to WUX-R14:** this data-authored pane is the first pane implementation we can create inside Workshop. It must **not** become the definition of what every editable pane is allowed to be.
   - In other words:
     > **PaneDefinition is one implementation path, not the ceiling of Pane.**

3. **Build the real `Pane Editor` around live semantic subjects.**
   - This is the editor you originally meant.
   - The subject is **`MyPane`**, not merely an instance's outer rectangle and not necessarily a pane created from our serialized region vocabulary.
   - Normal mode: use the pane normally.
   - Editing mode: select that pane as the editor subject and toggle semantic overlays showing whatever the implementation can honestly expose:
     - text regions;
     - drawing/background regions;
     - interaction regions;
     - layout/frame regions;
     - eventually bindings/state/endpoints.
   - Selecting a region should expose its properties in the common inspector.
   - The durable principle should be:
     > **The editor edits semantic facts a pane exposes; it does not define the maximum semantics a pane may possess.**
   - A fully data-authored pane may expose everything.
   - A code-backed pane may initially expose only a resolved body/text capture.
   - A reactive Powers-like pane may eventually expose much richer dynamic structure—but only when its implementation/protocol can honestly describe that structure.
   - WUX-R14 already gives us the honest fallback for imperative panes: show a **read-only capture**, not fake decompilation. 
   - The old gray workspace remains valuable here. Its **subject is obsolete**, but its interaction grammar—objects/list, selected properties, direct manipulation, authored vs resolved, create/delete, safe persistence—is lineage worth quarrying. Eventually it may become the 1:1 authoring canvas for a selected pane interior. 

4. **Give pane interiors real spatial authorship.**
   - Multiple semantic regions.
   - Region identities that survive editing.
   - Fine X/Y/width/height.
   - Share-of-interior / relative extent.
   - Direct drag and resize inside Pane Editor.
   - Region order/overlap.
   - A visible distinction between **authored intent** and **resolved presentation** exactly as we already use for pane placement.
   - Eventually anchors/frame relationships, but **not yet**. WUX-R14 confirmed the old `Context` is a frame reference, not the anchor system we have imagined, and the first pane floors do not require anchors. 
   - Later candidates:
     - anchors;
     - sibling-relative placement;
     - parent/container relationships where actually useful;
     - fill/remaining-space;
     - responsive sizing.
   - These should be earned individually instead of becoming a general constraint solver because “layout engines have constraints.”

5. **Finish making SDL a graphical face rather than a prettier TUI.**
   - **Scalable typography.** Today SDL falls back to bitmap/cell glyphs when the one fixed face doesn't fit. We want SDL to choose a smaller graphical face before inheriting a TUI-shaped fallback.
   - Durable semantics must never store “this happened to fit 3 rows at 13pt.” Font metric stays a face fact.
   - **Semantic controls must survive to the Skin.** Right now `[ Create ]` becomes characters before Surface knows that a Button-like thing exists; WUX-R14 measured 80px of glyphs answering a ~328px hit target. 
   - This is where we have finally earned the **Button question**:
     - semantic action/control shared;
     - TUI can spell it `[ Create ]`;
     - SDL can render a rectangle, chamfered enclosure, hover, pressed state, etc.
   - Same future work probably earns actual checkbox semantics for Pane Manager's visibility controls.
   - Drawing/color regions will eventually need similarly inspectable bounds.
   - Selected/read-only text should remain normal text rather than terminal-shaped rows where the graphical face can do better.

6. **Build behavior/wiring only when presentation has something real to wire.**
   - I agree with your latest instinct: a maker-authored pane cannot become meaningfully interactive without either **Flow** or another semantic wiring representation.
   - We should not fake this with a finite `CustomizablePane` configuration language.
   - The target backend model we discussed remains:
     - schema/interface creator;
     - pane/weave-local state;
     - local Sources;
     - local Operators;
     - `on` bindings;
     - explicit inputs/outputs/events;
     - bindings between panes;
     - authority-bearing weave behavior.
   - “Functions” should probably remain **scoped Operators**, not another computation species:
     - zero maker inputs → Source;
     - maker inputs → Operator;
     - scope determines private/local/published visibility.
   - An `on` is not an Operator. It means:
     > when this declared event happens, spend this behavior/composition.
   - Pane-local immediate presentation behavior should remain distinct from weave participation/authority.
   - Cross-pane wiring should use explicit interfaces, not arbitrary reach-through into another pane's private state.
   - A wire moves information/trigger semantics; it **does not confer authority**.
   - Flow, when it arrives, should be an authored representation of the same Sources/Operators/bindings already understood by Zen—not a second evaluator/runtime.
   - Provider-fed regions/slots are another later seam: a data-authored presentation eventually needs a way to consume code/provider-owned values by declared role without granting the definition executable authority.
   - This is also where reactive code-backed panes become much more introspectable: instead of reverse-engineering their C++ paint code, their semantic computation already exists as exposed Sources/Operators/state/bindings.

7. **Separate pane implementation from pane occurrence.**
   - I now consider this a genuine future architectural pressure.
   - Today `PaneRef` effectively identifies one tool/occurrence.
   - But multiple instances are plausible:
     - two Files panes at different locations;
     - several storage boxes;
     - schema-specific containers;
     - two views into the same data;
     - multiple instances backed by elements of a vector owned by an `InventoryWeave`.
   - Eventually we probably need a distinction equivalent to:
     > **what kind/implementation of pane is this?**
     >
     > **which occurrence on this desk is this?**
   - I would not name or implement that split yet, but we should avoid making new durable representations assume permanent 1:1 cardinality.
   - Similarly, **one open pane definition in the editor** can be a perfectly good first-floor lifecycle without implying **only one durable maker pane identity can exist**.

8. **Continue the desk/spatial UX arc after pane authoring gets footing.**
   - **P-WORK-08 latent geometry:** removing a pane currently destroys its authored setup row, so reopening returns it to developer defaults. Now that geometry is explicitly inspectable, this loss is more obviously wrong. Likely direction:
     > presentation/participation may suppress spatial intent; only authored editing should erase it.
   - **Locks.**
   - **Snapping.**
   - **Collision avoidance using locks.**
   - That ordering still makes sense:
     > lock → snap → collision avoidance.
   - Locks become more interesting now because Workshop chrome itself is editable.
   - **Two-row/multi-row Layouts pane.** WUX-12 made its height authorable; its internal tab painter still needs wrapping if we want increased height to actually yield another tab row.
   - **Responsive/default pane sizing** and “fill available room” remain open.
   - **Workspace-as-pane** remains a later question, not required for the current self-authoring road.
   - The old authored `pixels` sizing mode remains awkward and may need cleanup once pane-internal fine geometry becomes the normal vocabulary.

9. **Reduce the remaining immutable shell deliberately.**
   - Layouts has already crossed from shell furniture into an ordinary pane.
   - Pane Manager may replace PANEL as normal management and eventually eliminate it from the shell.
   - Hotkey presentation can become less privileged.
   - Attention/notifications can eventually become authored presentation once we preserve an unlosable utterance/recovery path.
   - Bottom-band/notice conversion is still constrained by the requirement that Workshop must always be able to tell the maker why something failed.
   - Transient things should **remain modes**, not become panes just for ideological purity:
     - context menu;
     - arrangement rings;
     - terminal mode;
     - transient picker-like recovery if one still exists.
   - The durable law remains:
     > persistent visible surfaces bear the burden of proving why they cannot be ordinary authored participants; transients remain honest modes; the shell is what is left after those decisions.

10. **Decide the fate of the original document/Info prototype.**
    - `WorkshopDoc` / `workshop.json` is genuinely a separate cell-lattice document system, not secretly a pane definition.
    - It nevertheless contains much of the interaction grammar that inspired the future Pane Editor.
    - Once real pane regions can do what its objects currently demonstrate, we should decide whether:
      - the document product is still useful and gets renamed/preserved as `Document`; or
      - it was scaffolding and can retire.
    - No need to migrate that format merely to build pane authoring. WUX-R14 explicitly recommends against bending `ui::Element` into the new pane representation because it has the wrong lattice, wrong frame, and large migration cost. 
    - If retired, old files should still be treated honestly—never silently overwritten or pretended to mean something new.

11. **Carry the already-established Powers/Source work toward Flow when the consumer appears.**
    - Sources and Operators already share the Powers concept.
    - Composite classification is derived rather than author-declared.
    - Sampling stays explicit.
    - Dragging Powers into Flow remains parked until Flow exists.
    - `SourceRef` exists as the concrete-current reference concept; `SourceIntent` remains interesting but unearned.
    - The second generic Value-presenter consumer is still the point where a shared presenter abstraction becomes worth extracting.
    - Provider presentation helpers may also be approaching extraction pressure: QR-18 found Powers/Compose now duplicate both list-window and wheel-step patterns. The report calls that the third/fourth reason for a shared helper. 

12. **Keep migration as a first-class evolution mechanism.**
    - MIG-0 has now proven itself across several real schema changes, including WUX-12's unusually interesting “same fields, different meaning” v5→v6 migration.
    - Keep current owners current-only; yesterday belongs in conversion providers.
    - Standalone Setup still has historical-reading pressure when it eventually gains another vintage.
    - Missing-conversion recovery guidance could improve later.
    - Migration Operators currently appear in Powers; whether those should receive some visibility grouping is still an open presentation question.
    - Never let old bytes authorize loading conversion code.

13. **Keep navigation/project/recipe semantics separated as the product grows.**
    - Files location, marks, project anchor, arrangement, and authority remain distinct.
    - External browsing/navigation should stay legal independently of project membership.
    - Relative recipes remain project-anchored.
    - Recipe catalog ownership and live selection are established.
    - Longer-term “project” may eventually become a richer collection of marked files/folders/recipes, but only if real use pressures beyond the current anchor concept earn it.
    - CMake/build-system discovery remains something that may generate or suggest a recipe rather than silently becoming hidden project magic.

14. **Security/hardening remains a parallel major arc.**
    - The long-term north star is still a **secure living development environment**:
      > Genera-like immediacy and inspectability without ambient authority.
    - Editable presentation must not imply executable authority.
    - Loading pane definitions should be inert data admission.
    - Future `on`/Flow bindings must resolve authority at spend time rather than smuggling grants into presentation files.
    - Provider disappearance should leave unresolved authored intent rather than silently deleting it.
    - Hostile-code / kernel-escape-class safety is still a much larger future hardening goal; Loom's existing deterministic/capability work is groundwork, not a claim that this problem is solved.
    - Plugin/weave unload cleanup, provider lifecycle, and hostile-input ceilings remain ongoing hardening territory.
    - Arbitrary maker-visible limits such as the current pane count should eventually be distinguished from **resource/admission safety limits** such as maximum durable/wire sizes.

15. **Keep a few known engineering debts visible without letting them hijack the product roadmap.**
    - Windows parallel `timer` test defect remains known; serial MSVC lanes are still used where appropriate.
    - Filesystem sensitivity under `/mnt/g` versus ext4 is known.
    - Tiny panes can lose selected-border ink because no border physically fits.
    - SDL whole-cell popup chrome reservation still produces some slack despite a one-pixel actual boundary.
    - A short viewport with a content-sized popup can lose its contextual Y anchor when the content cannot fit.
    - Provider Escape remains intentionally unknowable without a `consumed` protocol, and we currently have no reason to widen that seam merely for deselection.
    - These are real pressures, but none blocks the core authoring trajectory.

16. **Milestones/audits I would use to punctuate the road.**
    - **Shell stabilization milestone:** Pane Manager + `p/R` recovery + PANEL retirement + remaining scrolling cleanup.
    - **First authored-pane milestone:** create/save/load a real pane from Workshop without C++.
    - **Real Pane Editor milestone:** inspect/edit exposed semantic regions of `MyPane`, including at least one code-backed pane honestly and one maker-authored pane mutably.
    - **Graphical-control milestone:** semantic Button/control reaches Surface and SDL renders it graphically while TUI keeps an honest text representation.
    - **Wiring milestone:** a maker can define an event/interface and wire it to a local Source/Operator or weave behavior without typing C++ glue.
    - **Self-application milestone:** Workshop's own substantial panes are editable/wireable through those same mechanisms rather than bespoke code paths.
    - **Cold Audit after one of those major closures.** That's where I'd really like to throw Fable 5.1—or whatever the best cold executor is at the time—at the whole living system and ask what we have failed to notice.
    - Continue proportional verification throughout: local repairs get local proof; production phases get affected lanes/witnesses; arc closures earn the expensive broad confidence sweep.

If I compress all of that into the **main road**, I think it is:

> **Pane Manager stabilization → first pane authored from data → real semantic Pane Editor → graphical semantic controls → Flow/wiring → increasingly self-authored Workshop → locks/snapping/collision and deeper spatial tooling → secure living development environment.**

And the architectural compass underneath it is now unusually coherent:

> **The desk owns where instances participate.  
> The Pane Manager owns how those instances are arranged.  
> The Pane Editor owns what an inspectable pane says about itself.  
> Flow/wiring owns how semantic pieces relate and behave.  
> The weave owns participation and authority.  
> The active face owns how those meanings are honestly presented.**

That feels like the roadmap I would want us to steer by from here.
