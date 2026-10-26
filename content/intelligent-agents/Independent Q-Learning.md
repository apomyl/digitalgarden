---
publish: true
created: 2026-10-26T17:43:44.398Z
modified: 2026-10-26T17:54:54.622Z
tags:
  - intelligentagents
  - school
---

> [!definition]
> Independent approach to [[Q-learning]] for [[Multi-agent Reinforcement Learning|MARL]], each agent $i$ maintains an independent table $Q_{i}(s,a_{i})$, ignoring what other agents choose, treating them as part of the environment.

> [!tldr]
> Ran independently for each agent $i$:
> $Q_i(s_t, a_{i,t}) \leftarrow Q_i(s_t, a_{i,t}) + \alpha \left[ r_{i,t} + \gamma \max_{a'_i \in A_i} Q_i(s_{t+1}, a'_i) - Q_i(s_t, a_{i,t}) \right]$

- ✓ Scales Well
  - each agent only explores its own $\vert{}A_i\vert{} = k$ actions
  - total values stored across $n$ agents is $n \cdot \vert{}S\vert{} \cdot k$ (linear in $n$), rather than $\vert{}S\vert{} \cdot k^n$
- ✓ Fully Distributed
- ✗ Suffers from [[Non-Stationarity]]
  - the Markov property is broken from Agent $i$'s perspective. The transition probability $\Pr(s' \mid s, a_i)$ and reward $\mathcal{R}_i(s, a_i)$ keep shifting as other agents learn
- ✗ High Variance / Cyclic Dynamics
  - agents can get stuck in infinite loops chasing each other's changing policies without ever converging to an equilibrium
- ✗ No [[Multi-Agent Credit Assignment]]
  - a lazy agent can get reinforced by the good deeds of another agent

#### References
