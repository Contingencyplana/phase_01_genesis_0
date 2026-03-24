# Phase 1 — Genesis

## Purpose

This workspace contains the early foundation of the Kaleidoscope ecosystem.

Phase 1 — Genesis is where the first playable substrate is being built: the initial world, the first narrative systems, the first platform connections, and the first workflows that allow the project to grow without collapsing into confusion.

The goal is to establish enough structure to:

- create games
- publish games
- play games
- experiment with interactive storytelling
- grow a small playable world through iterative development

This workspace is not the finished ecosystem. It is the first durable layer beneath it.

---

## Core Systems

Three core systems form the foundation of this workspace.

### Kaleidoscope

Kaleidoscope is the creation system.

It is the place where interactive worlds, narrative structures, and experimental game forms are built.

At the current stage, the first major playable system being developed inside Kaleidoscope is the **Interactive Novel**.

### Alpha Dreaming

Alpha Dreaming is the publishing bridge.

It is responsible for packaging, upload, and publication workflows that connect creation to play.

Alpha Dreaming serves as the developer-facing link between building a game and making it available inside a play environment.

### Morningate Games / TestBed Layer

The play environment is currently represented through the platform layer, including the Morningate Games structure and the early publishing/testing pathway.

This layer is intended to support:

- rapid playtesting
- lightweight access to experimental games
- a growing library of playable builds

The play layer should remain simple enough that experimentation can happen quickly.

---

## Current Development Focus

The first major playable system being built inside Kaleidoscope is an **Interactive Novel**.

This system currently focuses on:

- a narrative world built through interconnected scenes
- interactive exploration through branching choices
- a gradually expanding archipelago structure
- lightweight narrative registries that reduce reliance on memory
- a workflow that balances building, playtesting, and automation

This Interactive Novel represents **Stage 1 — Interactive Fiction** in the Kaleidoscope evolutionary path.

---

## Workspace Structure

```text
phase_01_genesis_0/

docs/                          → architecture, design, and workflow documentation
engines/
    kaleidoscope_engine/       → shared engine layer under gradual development
experiments/                   → experimental work and prototypes
games/
    kaleidoscope/              → current primary Kaleidoscope game workspace
    prototypes/                → additional early game experiments
    trichess_and_tricheckers/  → related game experiments
platform/
    alpha_dreaming/            → publishing bridge
    morningate_games/          → play / launcher / library layer
```

Within `games/kaleidoscope/`, the current story work is centered on the Interactive Novel and its growing world structure.

---

## Development Philosophy

Phase 1 should remain small enough to stay playable, understandable, and survivable.

The aim is not to overbuild the full ecosystem in advance. The aim is to grow it through a sequence of small, testable, working layers.

Current priorities include:

* building a real playable world rather than only planning one
* keeping the workflow sustainable
* adding just enough narrative infrastructure to preserve continuity
* using automation and registries to reduce drudgery
* expanding only when the current layer feels stable

The emphasis is on **experimentation, simplicity, iterative growth, and work/play balance**.

---

## Guiding Principle

Build a little.
Play a little.
Stabilize a little.
Expand a little.

Phase 1 — Genesis exists to create the first playable and survivable foundation from which the wider Kaleidoscope ecosystem can grow.
