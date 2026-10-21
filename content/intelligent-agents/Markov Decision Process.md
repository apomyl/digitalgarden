---
publish: true
aliases:
  - MDP
  - Sequential-Decision Problem
created: 2026-10-21T12:08:21.206Z
modified: 2026-10-21T16:08:24.103Z
tags:
  - intelligentagents
  - game-theory
  - school
---

> [!definition]
> A [[Taxonomy for Decision (Game) Environments|game]] that models sequential decision making for a single agent and is defined as a 5-tuple
> $(S\,, \, A\,, \, \mathcal{R} \,, \, \mathcal{T} \,, \,\mu )$
>
> - $S$ - finite set of states (with terminal states $\bar{S} \subset S$)
> - $A$ - finite set of actions
> - $\mathcal{R} : S \times A \times S \to \mathbb{R}$ - [[Reward Functions|reward function]]
> - $\mathcal{T} : S \times A \times S \to [0, 1]$ - state transition function
> - $\mu : S \to [0, 1]$ - initial state distribution
>
> (Note: When infinite horizons are modeled, it is often extended to a 6-tuple with a [[Patience|discount factor]] $\gamma \in [0, 1)$).
>
> Extended for multiple agents in [[Stochastic Games]]

> [!tldr] Assumptions
>
> - Markov property - future depends only on current state and action, not full history
> - Full observability - agent sees the entire state of the environment
> - Stationarity - $\mathcal{T}$ and $\mathcal{R}$ do not change over time
> - Usually unknown - agent typically only knows $\mathcal{S}$ and $\mathcal{A}$, $\mathcal{T}$ and $\mathcal{R}$ must be [[Reinforcement learning|learned]]

#### References
