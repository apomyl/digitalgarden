---
publish: true
created: 2026-10-21T17:54:24.984Z
modified: 2026-10-21T17:55:29.939Z
tags:
  - intelligentagents
  - machinelearning
  - school
---

> [!definition]
> [[On-Policy vs Off-Policy|On-policy]] [[Temporal-difference Learning|TD control]]
>
> Using the experience tuple $(s_t, a_t, r_t, s_{t+1}, a_{t+1})$:
>
> $Q(s_t, a_t) \leftarrow Q(s_t, a_t) + \alpha \big[ r_t + \gamma Q(s_{t+1}, a_{t+1}) - Q(s_t, a_t) \big]$

#### References
