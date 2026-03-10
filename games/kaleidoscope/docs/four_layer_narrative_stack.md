# Four Layer Narrative Stack

This document defines the structural hierarchy used by the Kaleidoscope narrative engine.

The goal is to allow the world to scale to thousands of scenes while remaining organized.

---

## Layer 1 — Story Arcs

Story arcs represent major regions or themes of the world.

Examples:

0100_harbor  
0200_library  
0300_forest  

Arcs answer the question:

"What part of the world are we exploring?"

---

## Layer 2 — Story Subarcs

Subarcs represent smaller narrative threads inside an arc.

Examples:

Harbor Market  
Library Interior  
Forest Trail  

Subarcs answer:

"What situation are we interacting with?"

---

## Layer 3 — Scene Clusters

Scene clusters group several closely related interactions.

Example:

0201 Inside Library
 ├─0204 Visionary Journal
 ├─0205 Maps
 └─0206 Shelves

Clusters usually contain 3–5 scenes.

Clusters answer:

"What can the player examine here?"

---

## Layer 4 — Individual Scenes

Scenes are the atomic narrative units of the game.

Each scene is stored as a markdown file:

scene_XXXX.md

Scenes answer:

"What is happening right now?"

---

## Design Goal

This hierarchy allows Kaleidoscope worlds to scale to thousands of scenes while maintaining clarity and navigability.
