---
publish: true
created: 2026-10-21T17:55:41.478Z
modified: 2026-10-26T20:28:43.259Z
tags:
  - intelligentagents
  - school
---

> [!definition]
> [[On-Policy vs Off-Policy|Off-policy]] [[Temporal-difference Learning|TD control]]
>
> Q-learning targets the _optimal_ action-value function directly, using the _max_ operator:
>
> $Q(s_t, a_t) \leftarrow Q(s_t, a_t) + \alpha \left[ r_t + \gamma \max_{a' \in A} Q(s_{t+1}, a') - Q(s_t, a_t) \right]$

[[Central Q-Learning]] and [[Independent Q-Learning]]

> [!bug] Where it falls short
> Q-learning maintains a giant lookup table of all $Q(s,a)$ values, for huge state spaces this isn't feasible so we train a neural network to estimate the values in [[Deep Q-Network (DQN)]].
> ![[media/Q-learning-1793031527780.webp]]

#### References
