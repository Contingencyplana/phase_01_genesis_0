# Narrative Infrastructure Before 1000 Scenes

## What should happen before 1000 scenes

Well before then, `phase_01_genesis_0` should gain lightweight narrative infrastructure such as:

- `story/areas/`
- `story/sites/`
- `story/locations/`
- `story/scenes/`
- `story/characters/`
- `story/arcs/`
- `story/registries/scene_index.md`
- `story/registries/character_index.md`
- `story/registries/mystery_threads.md`

And on the tooling side:

- scene link validator
- orphan-scene detector
- duplicate-line detector
- location consistency checker
- maybe later a simple story database or generated atlas

That means by the time you have hundreds of scenes, neither you nor I should be trying to “just remember.”

## About Agent and Future Tooling

Yes — Agent will take more and more of the grunt work off your hands:

- locating scenes by anchor text
- inserting or revising cross-references
- updating scene targets
- generating small new scene clusters
- maintaining registries
- running validators
- reporting diffs cleanly

And yes, future tooling will likely make this easier still. But you do not need to wait for that. The current workflow is already good enough to scale much further than where you are now.

## My Recommendation

Proceed on the assumption that:

> memory is not the system  
> files + structure + automation are the system

That is the safe way to build `phase_01_genesis_0`.

So yes: rely heavily on structured files, registries, automation, Agent for repo-visible grunt work, and ChatGPT for orchestration, drafting, review, and interpretation. That is the right way to build this workspace.
