---
publish: true
aliases:
  - Payoff Functions
created: 2026-10-20T10:22:41.780Z
modified: 2026-10-21T16:11:38.828Z
tags:
  - intelligentagents
  - school
---

> [!definition]
> Similar to [[Cost Functions]], they are a metric to calculate a "reward" based on multiple factors.
>
> Used in [[Reinforcement learning]] to reward good actions. Use in [[Game Theory in Agent Systems]] to incentivise certain actions.

You can use these functions to classify systems based on their payoff:

| Class         | Condition                                                | Meaning                                          |
| ------------- | -------------------------------------------------------- | ------------------------------------------------ |
| Zero-sum      | $\sum_{i \in I} \mathcal{R}_i(a) = 0 \text{ for all } a$ | competition - one agent's gain is another's loss |
| Common-reward | $\mathcal{R}_i = \mathcal{R}_j \text{ for all } i, j$    | coordination - every agent receives same reward  |
| General-sum   | no restriction                                           | both competition and coordination                |

###### Expected Reward/Return

Expected reward/return under a joint policy $\pi=(\pi_{1},\dots ,\pi_{n}):$
$U_{i}(\pi)=\sum_{a \in A}\left( \prod_{j \in I}\pi_{j}(a_{j}) \right)\mathcal{R}_{i}(a)$

- agent $i$'s average reward over many plays

Expected [[Patience|discounted]] reward/return used in [[Reinforcement learning]]
$u_{t}=\sum_{k=0}^{\infty} \gamma^kr_{t+k} $

> [!question] How can we calculate rewards for [[Taxonomy for Decision (Game) Environments|multi-round games]]?
> We can scale future rewards with [[Patience]] and calculate the value of future actions when considering what to do now.

#### References
