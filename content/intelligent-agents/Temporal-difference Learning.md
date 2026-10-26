---
publish: true
aliases:
  - TD learning
created: 2026-10-21T17:05:28.321Z
modified: 2026-10-26T16:19:30.326Z
tags:
  - intelligentagents
  - machinelearning
  - school
---

> [!definition]
> [[Reinforcement Learning]] technique where you update value estimates $Q$ directly from sampled transitions $\mathcal{X}$, without needing to know $\mathcal{T}$ or $\mathcal{R}$ ([[Markov Decision Process]])
> $Q(s,a) \leftarrow Q(s,a)+\alpha[\mathcal{X}-Q(s,a)]$
>
> - $\mathcal{X}$ - the target: an estimate of the true value
> - $\alpha$ - learning rate
> - online - policy improves while agent is still interacting with the environment
> - bootstrapped - uses current estimate of next state-action value as part of the target
>
> _(Prediction = evaluating actions and state)_

> [!tldr] [[On-Policy vs Off-Policy]]
> Applying TD learning with different control problem settings
>
> - [[SARSA]] - on-policy TD control
> - [[Q-learning]] - off-policy TD control
>
> _(Control = process of updating values to find optimal policy)_

![[media/Temporal-difference Learning-1792605438496.webp]]

#### References
