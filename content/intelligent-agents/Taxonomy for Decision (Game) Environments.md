---
publish: true
created: 2026-10-20T10:03:40.418Z
modified: 2026-10-21T15:56:31.841Z
tags:
  - intelligentagents
  - school
  - game-theory
---

> [!definition] Summary
> A hierarchical structure for classifying where a certain "[[Game Theory in Agent Systems|game]]" lies and then choosing the correct approach for modelling and decision-making, useful in [[Reinforcement learning]].
>
> Important factors:
>
> - no. of agents (1 vs n)
> - no. of environmental states (1 vs m)
> - info available to agents (fully vs partially observed)

> [!tldr] Types
>
> - [[Normal-Form Games]] - n agents, 1 state e.g. rock-paper-scissors
>   - [[Repeated Normal-Form Games]] - over multiple rounds
> - [[Markov Decision Process]] - 1 agent, m states e.g. maze navigation
> - [[Stochastic Games]] - n agents, m states (fully observed) e.g. chess
>   - special case using tree to model sequential - [[Extensive-Form Games]]
> - [[Partially Observable Stochastic Games]] - n agents, m states (partially observed) e.g. poker (or LoL)
> - Sequential games - [[Backward Induction]] to find [[Subgame Perfect Equilibrium|SPE]]

![[media/Intelligent Agents Lecture 2026-10-13-1791889948324.webp|700]]

#### References
