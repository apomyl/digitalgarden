---
publish: true
created: 2026-10-26T17:43:30.251Z
modified: 2026-10-26T17:50:00.476Z
tags:
  - intelligentagents
  - school
---

> [!definition]
> A [[Central Learning]] approach to [[Q-learning]] to solve issues that arise in [[Multi-agent Reinforcement Learning|MARL]].

> [!tldr]
> Learn a single central [[Policy]] $\pi_{c}$. A central controller observes the global state $s$ and selects a [[Joint Action and Policy|Joint Action]] $a=(a_{1},\dots,a_{n})$
>
> $Q(s_t, \mathbf{a}_t) \leftarrow Q(s_t, \mathbf{a}_t) + \alpha \left[ r_t + \gamma \max_{\mathbf{a}' \in A} Q(s_{t+1}, \mathbf{a}') - Q(s_t, \mathbf{a}_t) \right]$

- $✓$ Solves [[Non-Stationarity]]
- $\checkmark$ Solves [[Multi-Agent Credit Assignment]]
- $×$ Fails to Scale - joint action combinatorics
- $×$ Requires Global Knowledge & Control

#### References
