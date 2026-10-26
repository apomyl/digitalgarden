---
publish: true
aliases:
  - MDP
  - Sequential-Decision Problem
created: 2026-10-21T12:08:21.206Z
modified: 2026-10-26T15:57:47.506Z
tags:
  - intelligentagents
  - game-theory
  - school
---

> [!definition]
> A [[Taxonomy for Decision (Game) Environments|game]] that models sequential decision making for a single agent and is defined as a 5-tuple
> $(S\,, \, A\,, \, \mathcal{T} \,, \, \mathcal{R} \,, \,\mu )$
>
> - $S$ - finite set of states (with terminal states $\bar{S} \subset S$)
> - $A$ - finite set of actions
> - $\mathcal{T} : S \times A \times S \to [0, 1]$ - state transition function
> - $\mathcal{R} : S \times A \times S \to \mathbb{R}$ - [[Reward Functions|reward function]]
> - $\mu : S \to [0, 1]$ - initial state distribution
>
> Note:
>
> - Episodic MDPs: Have terminal states $\bar{S} \subset S$. The discount factor $\gamma \in [0, 1]$ is often included to encourage fast completion ([[Patience|patience]]/urgency).
> - Infinite-Horizon MDPs: No terminal states. A discount factor $\gamma \in (0, 1)$ is strictly (can't be 0 or 1, only approach them) required so that the infinite sum of rewards converges ($\sum \gamma^t R < \infty$) (if gamma is 1 then reward will be infinite).
>
> Extended for multiple agents in [[Stochastic Games]]

> [!tldr] Assumptions
>
> - Markov property - future depends only on current state and action, not full history
> - Full observability - agent sees the entire state of the environment
> - Stationarity - $\mathcal{T}$ and $\mathcal{R}$ do not change over time
> - Usually unknown - agent typically only knows $\mathcal{S}$ and $\mathcal{A}$, $\mathcal{T}$ and $\mathcal{R}$ must be [[Reinforcement Learning|learned]]

#### References
