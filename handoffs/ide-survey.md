# What other tools do that Zen could take (Vision, 2026-10-21)

For the alpha: layouts worth taking and small features that make the first five minutes feel good,
each mapped to the Zen owner that would hold it. Read from each project's own pages; licenses
checked where code might be copied. Zen is MPL-2.0: code from an MIT, Apache-2.0 or MPL-2.0
project can come in with its notice; GPL code cannot, so Blender and most of Zed give ideas only.

## Licenses

| project | license | its code in Zen |
|---|---|---|
| VS Code (Code - OSS) | MIT | yes, with its notice |
| Godot (the editor) | MIT | yes, with its notice |
| Dear ImGui (docking) | MIT | yes, with its notice |
| Helix | MPL-2.0 | yes, Zen's own license |
| Node-RED | Apache-2.0 | yes, with its notice |
| Lapce | Apache-2.0 | yes, with its notice |
| Zed | GPL-3.0-or-later; parts marked Apache-2.0 | ideas, and the marked parts |
| Blender | GPL (not checked here) | ideas only |

In practice the layouts and features below are ideas, rebuilt as weaves: none of these projects is
C++ on a message bus, Dear ImGui aside.

## Layouts worth taking

- **Named layouts in a menu.** Godot saves the arrangement by name (Editor > Editor Layouts > Save)
  and loads it from the same menu, kept in `editor_layouts.cfg`. Zen has this as the Layouts row;
  its owner comes with the desk split (D1).
- **A dock made floating, and back.** Godot's "Make Floating" moves a dock into a window of its own;
  closing that window returns it. This is the story's step 5 in miniature, and its bonus: a pane
  into a window of its own and back as a pane. Take the gesture and the words.
- **Areas split and joined by dragging** (Blender's areas, Dear ImGui's docking): Zen's arrange
  mode places panes by pixel; dragging a pane onto another's edge to split, or its title to tab
  them, is UX-06's ("The weaver arranges the whole window"). After the alpha.

## Small features, in order for the alpha

1. **A command palette.** One key; type to find any action, pane, setup or file, and run it. VS
   Code's Command Palette, Blender's operator search, Helix's pickers. Zen has none
   (`workshop/docs/hotkeys.md`: "there is no command palette"), yet every pane already declares its
   actions, so the list exists. Owner: a palette pane, a weave beside the menu presenter, asking
   Workshop for what is declared. One phase. The largest single gain in finding things, and it
   covers the demos too ("start demo presets").
2. **A first-run quick setup.** Blender's first launch asks four things: the keymap (Blender,
   Blender 2.7x or Industry Compatible), which mouse button selects, what the spacebar does, and the
   theme. The founder's wizard is the same shape: a control scheme, a Vim checkbox, a way to the
   setups. Owner: a first-run pane in the shipped setup, its choices written through Workshop's own
   keymap and settings writes. One phase, without theme presets (cut).
3. **A walkthrough as a checklist.** VS Code's walkthroughs: a few steps, each an action named by a
   verb, ticked as done; not many, and only one walkthrough. For the story: make a view, wire its
   button into Flow, show Flow's answer, give it a window of its own. Zen's own way to point at each
   step exists: a guest in the `tutor` role draws guide marks and reads the desk (WL-GUIDE), but it
   needs a Loom session as the demos do. The plain way: the first-run pane lists the steps.
4. **Zoom a pane.** One key fills the desk with the focused pane and back (VS Code's Zen Mode,
   Blender's maximized area). Owner: Workshop's arrangement, which owns the room. Small.
5. **Drop a wire on empty space to add a node.** Blender's node editor: release a link over empty
   space and a search of the nodes compatible with it opens; the chosen node is made there, wired,
   and moves with the hand. Flow already narrows its search to a selected port's type; this is the
   drag gesture onto it. Owner: the Flow pane. Small.

## Seen, and Zen has it already

- Key hints at the bottom of the desk (Blender's status bar, Helix's popups): Workshop's bottom rows
  name the keys in force.
- A journal of what a graph did (Node-RED's debug sidebar): Flow's events page.
- Views of a value chosen for it (Glamorous Toolkit's inspector views): described views shown in
  Info and Inventory (`view/docs/view-builder.md`, "Views here, in Info and in Inventory").

## Sources

- Blender's first launch: docs.blender.org/manual/en/2.80/_sources/getting_started/configuration/defaults.rst.txt
- VS Code walkthroughs: code.visualstudio.com/api/ux-guidelines/walkthroughs; Code - OSS's MIT
  statement in its README
- Godot layouts and floating docks: docs.godotengine.org/uk/4.4/_sources/tutorials/editor/customizing_editor.rst.txt;
  its license: godotengine.org/license
- Blender's link drag search: developer.blender.org/rB11be151d58ec0ca955f019b0eed738e3245110b8
- Helix: pkgs.alpinelinux.org/package/v3.19/community/x86/helix
- Node-RED: nodered.org/about/license; its editor's parts: winccoa.com's Node-RED editor page
- Dear ImGui docking: cppget.org/libimgui-docking
- Lapce: gpo.zugaina.org/app-editors/lapce
- Zed: its README (cdn.jsdelivr.net/gh/zed-industries/zed@main/README.md)
- Glamorous Toolkit: book.gtoolkit.com, "What is Glamorous Toolkit?"
