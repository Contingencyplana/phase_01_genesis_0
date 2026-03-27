# Kaleidoscope — Workflows

This document describes the operational workflows of the Kaleidoscope ecosystem.

Kaleidoscope supports two primary workflows:

1. **Initial Workflow (Bootstrapping Phase)**
2. **Mature Workflow (Normal Operation)**

The Initial Workflow describes how the first infrastructure is created during Phase 1 — Genesis.

The Mature Workflow describes the intended long-term loop through which developers create games, publish them, and place them into a lightweight play environment for testing and iteration.

---

## Purpose of This Document

This file describes how the major systems of Kaleidoscope relate to one another in operational terms.

It does not attempt to describe every internal implementation detail.

Its purpose is to clarify the main flow by which:

- games are created
- games are packaged and published
- games are made playable
- feedback supports further iteration

---

## The Three Core Workflow Roles

At a high level, the workflow depends on three core roles:

### Kaleidoscope

Kaleidoscope is the **creation system**.

It is the place where interactive worlds, narrative structures, experimental game forms, and early playable systems are built.

In Phase 1 — Genesis, the first major playable system being built inside Kaleidoscope is the **Interactive Novel**.

### Alpha Dreaming

Alpha Dreaming is the **publishing bridge**.

It is responsible for packaging, upload, and publication workflows that connect game creation to game availability.

### TestBed Layer

The TestBed layer is the **play environment**.

In the current Phase 1 structure, this is represented through the platform layer, including the early **Morningate Games** structure and the broader testing / launcher / library pathway.

Its role is to keep playtesting simple enough that experimentation can happen quickly.

---

## Initial Workflow (Bootstrapping Phase)

At the beginning of the project, Kaleidoscope is used to help construct the first durable systems of the ecosystem.

In this early phase, Kaleidoscope functions as both:

- a **game maker**
- a **game-room / play-environment maker**

Using these capabilities, Kaleidoscope helps establish the first two major supporting systems:

- the **TestBed layer**
- **Alpha Dreaming**

Conceptually:

```text
Kaleidoscope
    ↓ helps build
TestBed layer
(game room / launcher / library pathway)

Kaleidoscope
    ↓ helps build
Alpha Dreaming
(upload / packaging / publishing tool)
```

Once Alpha Dreaming exists in usable form, it can be used to publish games into the TestBed layer.

```text
Kaleidoscope
    ↓ creates games
Alpha Dreaming
    ↓ publishes
TestBed layer
    ↓ hosts
initial Kaleidoscope games
```

Early hosted games may include:

- Kaleidoscope
- Alpha Dreaming
- Trichess
- Tricheckers
- early experimental prototypes

The goal of the Initial Workflow is to establish enough infrastructure for ongoing experimentation, playtesting, and gradual ecosystem growth.

## Mature Workflow (Normal Operation)

Once the ecosystem becomes more stable, developers and players interact through a more regular development loop.

```text
Developer creates game in Kaleidoscope
    ↓
Packages and uploads via Alpha Dreaming
    ↓
Game appears in the TestBed layer
    ↓
Players play and test the game
    ↓
Feedback informs further iteration
```

This loop enables:

- rapid experimentation
- lightweight playtesting
- continuous improvement
- growing confidence in the build / publish / play pathway

Developers iterate on their games in Kaleidoscope and publish updates through Alpha Dreaming.

Players explore those games through the TestBed layer and help reveal what is working, what is confusing, and what should be improved next.

## Developer Workflow

The developer workflow focuses on creating, testing, and improving games.

Typical steps include:

1. Create or modify a game using Kaleidoscope.
2. Prepare the game for distribution through Alpha Dreaming.
3. Upload or publish the game into the TestBed layer.
4. Observe playtesting results and player feedback.
5. Improve the game and repeat the process.

This workflow should remain simple enough that experimentation is not smothered by process overhead.

## Player Workflow

Players interact with the ecosystem through the TestBed layer.

Typical steps include:

1. Enter the TestBed layer.
2. Browse available experimental games.
3. Select a game to play.
4. Play and explore the game.
5. Return to the TestBed layer to try other games or later revisions.

The TestBed layer should remain simple and lightweight so that players can quickly launch experimental games without unnecessary friction.

## Continuous Evolution

As the ecosystem grows, the workflow becomes increasingly self-reinforcing.

```text
Developers create games
    ↓
Players test games
    ↓
Feedback improves games
    ↓
Improved tools strengthen Kaleidoscope
    ↓
Better tools support new games
```

This cycle supports the long-term evolution of the platform.

Over time, the workflow is intended to become not just productive, but recursive:

- better tools support better games
- better games attract more testing and insight
- better testing improves both the games and the tools
- the ecosystem gradually strengthens itself through repeated use

## Relationship to Phase 1 — Genesis

In Phase 1 — Genesis, the workflow should remain modest, practical, and survivable.

The goal is not to simulate the final mature ecosystem all at once.

The goal is to establish a first durable loop that allows the project to:

- build a little
- play a little
- stabilize a little
- expand a little

This means the workflow should favor:

- simplicity
- testability
- low-friction iteration
- lightweight publishing
- fast return from creation to play

## Summary

The Kaleidoscope ecosystem operates through two primary workflows.

### Initial Workflow

Kaleidoscope helps establish the early TestBed layer and Alpha Dreaming.

Alpha Dreaming then supports the publication of initial games into the play environment.

### Mature Workflow

Developers create games in Kaleidoscope.

Games are packaged and published through Alpha Dreaming.

Players access and test those games through the TestBed layer.

Together these workflows support an evolving ecosystem of experimental games, playable systems, and iterative growth.
