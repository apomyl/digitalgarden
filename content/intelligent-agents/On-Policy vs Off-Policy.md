---
publish: true
aliases:
  - on-policy
  - off-policy
created: 2026-10-21T17:35:37.274Z
modified: 2026-10-21T17:57:47.349Z
tags:
  - intelligentagents
  - machinelearning
  - school
---

> [!definition]
> Terms in [[Reinforcement learning]] referring to [[Policy]] of RL agents (e.g. [[ε-Greedy]]).
>
> - Οn-Policy - agent learns value of exact policy it's running – including mistakes and exploration
>   - i.e. if agent explores randomly with 10% chance, it factors that in when evaluating states
>   - e.g. [[SARSA]]
> - Off-Policy - agent learns value of hypothetical optimal greedy policy
>   - i.e. agent always assumes it will perform the perfect move
>   - e.g. [[Q-learning]]

#### References
