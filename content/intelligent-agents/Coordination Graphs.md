---
publish: true
created: 2026-10-26T16:53:37.102Z
modified: 2026-10-27T09:52:39.000Z
tags:
  - intelligentagents
  - school
---

> [!definition]
> A method for [[Coordination in Agent Systems|coordination]] using graphs:
>
> - nodes - an agent
> - edges - connect agents whose choices are dependent

> [!question] What do we use them for?
> If we have a [[Reinforcement Learning|global value function]] $V(a)$ for [[Task Allocation]], if we want to find the best combination for 50 agents with 2 states, our value function will have $2^{50}$ values.
>
> We decompose the monolithic value function $V(a)$ by combining individual value and value for actions between linked agents:
> $V(a) = \underbrace{\sum_i u_i(a_i)}_{\text{Individual preferences}} + \underbrace{\sum_{(i,j)\in E} u_{ij}(a_i, a_j)}_{\text{Pairwise interactions}}$

![[media/Coordination Graphs-1793034142604.webp]]

#### References
