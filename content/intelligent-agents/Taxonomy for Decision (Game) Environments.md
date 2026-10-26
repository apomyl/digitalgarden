---
publish: true
created: 2026-10-20T10:03:40.418Z
modified: 2026-10-26T15:45:17.019Z
tags:
  - intelligentagents
  - school
  - game-theory
---

> [!garden] Summary
> Breaking down the dimensions for different environments and how we can classify different situations as different "[[Game Theory in Agent Systems|game]]" types.

> [!definition] Environment Dimensions
>
> - Accessible vs Inaccessible (Fully vs Partially observed)
> - [[Probabilistic vs Deterministic|Deterministic vs Stochastic]]
> - Episodic vs Sequential
> - Static vs Dynamic
> - Discrete vs Continuous
> - Single vs Multi-Agent

> [!tldr] Types
>
> - [[Normal-Form Games]] - n agents, 1 state e.g. rock-paper-scissors
>   - [[Repeated Normal-Form Games]] - over multiple rounds
> - [[Markov Decision Process]] - 1 agent, m states e.g. maze navigation
> - [[Stochastic Games]] - n agents, m states (fully observed) e.g. chess
> - [[Partially Observable Stochastic Games]] - n agents, m states (partially observed) e.g. poker (or LoL)
> - Sequential games - [[Backward Induction]] to find [[Subgame Perfect Equilibrium|SPE]]
> - [[Extensive-Form Games]] - sequential game with tree node states

![[media/Intelligent Agents Lecture 2026-10-13-1791889948324.webp|700]]

## Game Theory Taxonomy

| Model                | Agents | States | Observability             | Temporal Structure    | Classic Example             |
| :------------------- | :----: | :----: | :------------------------ | :-------------------- | :-------------------------- |
| Normal-Form Game     |  $n$   |  $1$   | Accessible / Inaccessible | Episodic (one-shot)   | Rock-Paper-Scissors         |
| Repeated Normal-Form |  $n$   |  $1$   | Accessible / Inaccessible | Sequential (repeated) | Iterated Prisoner's Dilemma |
| MDP                  |  $1$   |  $m$   | Accessible                | Sequential            | Maze navigation             |
| POMDP                |  $1$   |  $m$   | Inaccessible              | Sequential            | Maze with blind spots       |
| Stochastic Game      |  $n$   |  $m$   | Accessible                | Sequential            | Chess, Backgammon           |
| POSG                 |  $n$   |  $m$   | Inaccessible              | Sequential            | Poker, LoL                  |

#### References
