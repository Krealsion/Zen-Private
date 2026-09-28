# ModCraft — From One Plant to a World of Games

**The seed idea: make something fascinating that people can understand, change, and share. Let the larger world grow from what they discover.**

The working relationship is **Loom → Zengine → ModCraft**: substrate, reusable capabilities and authoring tools, then a game that gives those capabilities a playful purpose. This describes the direction, not a claim that all of it already exists.

## Start with one plant

A seed carries genetics: inputs to an algorithm that produces development, variation, and recognizable form. Golden-ratio-inspired arrangements are an appealing starting ingredient. A small neural model, explicit developmental rules, or a hybrid could provide the generative behavior; the implementation is not yet settled.

The first activities are enough: **copy a seed, copy it with mutations, plant it, water it with an all-powerful spell, and accelerate its growth to 1000× time.**

The pleasure is watching it grow, discovering an unexpected form, and trying another variation. Neither realistic ecology nor balanced resource scarcity needs to precede that pleasure.

Copying a seed preserves inherited possibilities. Copying an experiment preserves a particular developmental state and its conditions. Keeping a parent beside a variation makes comparison natural without destroying the original.

A fascinating plant might later become an ingredient, a material, a crop, or the subject of breeding experiments. Crafting, cooking, and alchemy can emerge from that interest. **They are possibilities to discover, not prerequisites to implement.**

## The interface is made of spells

There is no permanently privileged game interface with magic placed inside it. **The interface—and even the 3D camera—is spellcrafted.**

The first plant/genetics UI should demonstrate this. It is an authored presentation over accessible information, not a plant-specific inspector buried inside the engine.

One viewing spell might present the beautiful organism. Another reveals its branching structure. Another exposes genetic values or highlights what changed during the latest growth burst. Different people can create different ways of attending to the same thing.

> “Here is how I see my garden. Try it.”

That can mean sharing a usable interface, not merely a screenshot. Someone can make a more understandable genetics display, an accessible control arrangement, or a specialized cultivation view without replacing the plant’s underlying model.

The first useful view can be a small authored arrangement. A complete universal interface editor is not a prerequisite; exactly how the initial viewing spell is bootstrapped remains a design question.

## Spells make useful operations repeatable

Spells are closer to **reusable, parameterized code macros or compositions** than a fixed list of combat abilities.

They can obtain a reference, extract a value, transform it, change permitted state, present a result, or communicate with another participant.

For example: select a plant, extract its branching parameter, modify it through a mutation spell, apply it to a copied seed, and compare the offspring with its parent. That sequence can itself become a reusable working with selected inputs exposed.

The goal is to avoid reconstructing the same plumbing every time. Selecting the specimen should carry its identity into the next action. Declared inputs should help produce understandable controls.

Using a finished spell, adjusting its parameters, composing existing operations, and writing a new operation are all valid levels of participation. **Everyone has magic; not everyone must write every spell they use.**

## Open the plant, then open its computation

The guiding interaction is:

> **Start with the interesting leaf and work backward to what produced it.**

Selection should lead toward the part’s identity, state, genetic inputs, developmental history, and responsible operations. The environment should make “What happened here?” and “What changes when I alter this?” easy to investigate.

The proposed Blueprint-like inspector is a **scope-centered projection of source-available C++**. Existing compiler ASTs should help identify scopes and semantic relationships correctly.

A collapsed region preserves its meaningful boundary: inputs, outputs, calls in and out, referenced state, and effects. Opening it reveals nested computations. Messages, operators, schemas, roles, managers, and documented contracts provide additional links where evidence supports them.

Not every statement needs a box. Unresolved calls and opaque code should remain visibly unresolved or opaque.

Three kinds of truth must stay distinct: **what the source describes, what the running instance currently contains, and what a recorded execution actually did.** Edited source is not automatically the source of the loaded artifact. Opening an inspector must not silently execute the thing being inspected.

Read-only source projection, editing owned compositions, and editing arbitrary C++ through nodes are separate ambitions. The first can be useful without promising the third.

## Mana connects magic to actual work

Players supply mana through computation. Hosts can contribute capacity, and resources can contribute useful preparation, references, materials, or conditions.

A crystal containing the ID for water is a prepared component of a working. Its value can come from making a spell circle more economical—not merely from adding another numerical battery.

The initial accounting should be simple, beginning with the proposed 1:1 relationship rather than benchmarking players against one another or trying to saturate their devices. The important question is **how efficiently a working turns its inputs and communicated data into a useful result**. A limited number of requests could still produce complicated genetic outcomes or regional geological changes.

Voluntarily contributing spare capacity to maintain plants and other world processes can strengthen someone’s connection to the weave and the support they can provide for powerful workings. The precise accounting and allocation rules remain open.

For accelerated growth, requested speed is not completed progress. Work can consume the local allowance, slow down, or seek additional compute. Completed results arrive in bursts, accompanied by color or magical effects that reveal the new development.

**The magic should make computation perceptible, not conceal its status.** A plant waiting for water is different from a plant whose next step has not yet been calculated.

Compute contacts can appear as remembered mana signatures. Bonds, discovery spells, and messages make those relationships usable. Sources disclose what they offer and refuse; people choose which relationships to maintain.

## The larger game is an interconnected multitude of games

Gardening can be someone’s whole game. So can spellcraft, mining and making, embodied VR combat, or scouting and ruin exploration.

The inspirations describe different pleasures: Stardew-like cultivation, Bitburner-like computational discovery, Minecraft-like making, and martial practice through embodied play. **They should not become shallow support professions for one dominant combat game.**

Systems load where they are needed. A dungeon client does not need the detailed gardening tools or responsibility for calculating distant plant growth. Appropriate hosts can maintain those processes while their consequences remain part of the shared world.

People exchange more than commodities: seeds, spells, interfaces, techniques, discoveries, and useful arrangements. A gardener can benefit from a spellwright’s irrigation without learning spell programming. A scout’s discovery can matter to a maker. Several activities can contribute to the same event without everyone playing the same way.

A village can eventually bring these experiments together. It does not have to exist before the first seed.

## Many alchemies; no compulsory adoption

Someone can make an easy-mode alchemy system, an intricate simulation, or something based on completely different ingredients and transformations. They are not restricted to adjusting difficulty or reskinning an official algorithm.

**The right to make and share a system is not the right to make everyone accept it.**

Players and hosts choose which spells, models, effects, participants, and results belong in their worlds. They may adopt an invention, modify it, restrict it, or decline it. Interoperation is something to establish where useful—not proof that different rules are automatically equivalent.

Single-player experiments, private servers, campaigns, shared regions, and entirely new games are legitimate destinations. They are not inferior departures from one mandatory world.

A private home can welcome unrestricted experimentation while a public arena enforces its chosen fair-play rules. Monsters and players can encounter the same local mana restrictions. Fire in a volcano can be favored without every region needing identical balance.

Digging into underlying mechanisms and exploiting in-world assumptions can become **dark magic**. Hosts can choose strict checking or trust-dependent validation. Those are local policies, not a universal promise—and exploring a fictional system is not blanket permission over another person’s real computer.

## The purpose is people enjoying things together

A few satisfying hours should be a complete way to belong.

A gardener can exchange observations with another gardener. A spellwright can teach someone how a working behaves. An experienced martial artist can teach through a fantasy dojo, with honest boundaries around what the medium can represent.

These relationships may remain entirely in the game or grow into real-world friendships. Both are worthwhile.

The world should reward cooperation without turning absence into failure, generosity into a permanent obligation, or someone’s preferred activity into unpaid support for everyone else’s fun.

## What this asks of Zengine

Not every pane needs to be reusable, and not every botanical rule belongs in the engine. The important foundations are **accessible values, composable operations, separable presentation, explicit effects, and understandable sharing**.

We need both a computationally sufficient composition vocabulary and practical guidance: state–presenter–view, source–transformation–presentation, command–change–observation, bounded work–accepted result, and seed–variation–comparison. The guidance should explain when each arrangement earns its complexity and when an ordinary function is enough.

MOD-R0 suggested a compact plant implementation around exposed state and a growth step, proposed generic state-inspection tooling, and identified missing runtime-to-source connections. Those are research findings, not confirmation that the proposed facilities have since landed. 

The plant should not wait for a universal inspector. The inspector should not wait for a finished game.

**First proof:** grow something surprising, understand one reason it grew that way, preserve or change the working, and let someone else enjoy it.

**Full picture:** a world of games people can understand, reshape, and share—without requiring everyone to play the same game or accept the same rules.
