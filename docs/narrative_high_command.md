# Narrative High Command

## Purpose

Narrative High Command is the lightweight command layer for the Interactive Novel inside `phase_01_genesis_0`.

It exists to reduce narrative drift, preserve continuity, and support growth without forcing the project to rely on human memory alone.

Its role is not to replace the scenes themselves.

Its role is to help the scenes remain legible, coherent, and expandable as the world grows.

---

## Current Role

At the current stage of Phase 1 — Genesis, Narrative High Command serves four practical functions:

- track the playable scene structure
- track current characters and what they know
- track active mystery threads and unresolved narrative pressure
- support clean collaboration between human judgment, AI reasoning, and automated grunt work

This allows the Interactive Novel to expand island by island without requiring constant rereading of the entire story.

---

## Current Components

The current Narrative High Command layer consists of:

- `games/kaleidoscope/story/registries/scene_index.md`
- `games/kaleidoscope/story/registries/character_index.md`
- `games/kaleidoscope/story/registries/mystery_threads.md`

These files function as the first command layer above the playable scenes.

They do not replace the scenes.  
They summarize and coordinate them.

---

## Design Principle

Memory is not the system.

Files + structure + automation are the system.

Narrative High Command exists so that continuity, symbolism, character knowledge, and scene relationships do not depend on repeated acts of recollection.

This is especially important for a project intended to grow gradually through many scenes, many islands, and many future layers of interaction.

---

## Relationship to the Interactive Novel

The Interactive Novel remains the playable heart of the current system.

Narrative High Command exists to support that heart by making the story world easier to:

- build
- navigate
- test
- revise
- extend

The scenes remain primary.  
Narrative High Command remains secondary and supportive.

It is a command layer, not a replacement layer.

---

## Relationship to Automation

Narrative High Command also creates a stable surface for collaboration with automation.

It makes it easier for AI assistants and tools to:

- locate relevant scenes quickly
- update continuity safely
- trace character appearances
- track unresolved threads
- perform bounded edits without guessing blindly

This reduces drudgery and helps preserve quality as the project scales.

---

## Future Growth

Narrative High Command should grow gradually and only when needed.

Possible later additions may include:

- `story/areas/`
- `story/sites/`
- `story/locations/`
- `story/characters/`
- `story/arcs/`
- scene link validators
- orphan-scene detection
- duplicate-line detection
- location consistency checks
- a generated atlas or story database

These are future expansions, not current requirements.

---

## Constraint

Narrative High Command must remain lightweight enough to stay useful.

It should grow only when the current layer of the project genuinely needs more coordination.

It exists to reduce drift and drudgery, not to create bureaucracy.

If a new command layer does not improve either playability or survivability, it should not be added yet.

---

## Current Working Rule

Build a little.  
Play a little.  
Stabilize a little.  
Expand a little.

Narrative High Command should follow the same rule as the rest of Phase 1 — Genesis.

It should evolve as a practical support structure for a growing playable world.
