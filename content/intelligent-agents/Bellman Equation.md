---
publish: true
created: 2026-10-21T16:33:11.006Z
modified: 2026-10-21T17:04:37.661Z
tags:
  - intelligentagents
  - machinelearning
  - school
---

> [!definition]
> Value now = reward now + discounted value next
>
> Equation expressing the value of a state recursively as the immediate [[Reward Functions|reward]] received plus the [[Patience|discounted]] expected value of the next state in [[Reinforcement learning]].

> [!tldr] Equations
> $V^\pi(s) = \mathbb{E}_\pi \big[ r_t + \gamma V^\pi(s_{t+1}) \mid s_t = s \big]$
> $Q^\pi(s, a) = \mathbb{E}_\pi \big[ r_t + \gamma Q^\pi(s_{t+1}, a_{t+1}) \mid s_t = s, a_t = a \big]$
>
> - Model known ($\mathcal{T, R}$): compute the expectation exactly
> - Model unkown: replace the expectation with samples ($s,a,r,s'$) from experience
>   - in techniques like [[Temporal-difference Learning]], [[SARSA]], [[Q-learning]]

#### References

- https://en.wikipedia.org/wiki/Bellman\_equation

> [!quote] Description
> "A technique in dynamic programming which breaks an optimization problem into a sequence of simpler subproblems, as Bellman's "principle of optimality" prescribes. It is a necessary condition for optimality. The "value" of a decision problem at a certain point in time is written in terms of the payoff from some initial choices and the "value" of the remaining decision problem that results from those initial choices."
