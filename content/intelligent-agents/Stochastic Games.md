---
publish: true
created: 2026-10-21T12:03:51.670Z
modified: 2026-10-26T13:41:06.699Z
tags:
  - intelligentagents
  - game-theory
  - school
---

> [!definition]
> A **stochastic game** introduces the notion of **states** and is defined as a 6-tuple
> $(I\,, \, S \,,\, \{A_i\}_{i \in I} \,, \,\{\mathcal{R}_i\}_{i \in I} \,, \, \mathcal{T} \,,  \,\mu )$
>
> - $I$ - finite set of agents
> - $S$ - finite set of states (with terminal states $\bar{S} \subset S$)
> - For each agent $i \in I$:
>   - $A_i$ - finite set of actions
>   - $\mathcal{R}_i : S \times A \times S \to \mathbb{R}$ - [[Reward Functions|reward function]]
>   - $A = A_1 \times \dots \times A_n$ - set of [[Joint Action and Policy|joint actions]]
> - $\mathcal{T} : S \times A \times S \to [0, 1]$ - state transition function
> - $\mu : S \to [0, 1]$ - initial state distribution

Example:
![[media/Stochastic Games-1792589934626.webp|400]]

- each state can be viewed as a [[Normal-Form Games|normal-form game]]
- this is a general-sum game - [[Reward Functions]]

#### References
