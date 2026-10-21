---
publish: true
created: 2026-10-21T17:55:41.478Z
modified: 2026-10-21T17:56:43.977Z
tags:
  - intelligentagents
  - machinelearning
  - school
---

> [!definition]
> [[On-Policy vs Off-Policy|Off-policy]] [[Temporal-difference Learning|TD control]]
>
> Q-learning targets the _optimal_ action-value function directly, using the _max_ operator:
>
> $Q(s_t, a_t) \leftarrow Q(s_t, a_t) + \alpha \left[ r_t + \gamma \max_{a' \in A} Q(s_{t+1}, a') - Q(s_t, a_t) \right]$

#### References
