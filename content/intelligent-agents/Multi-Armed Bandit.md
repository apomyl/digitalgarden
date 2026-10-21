---
publish: true
aliases:
  - Single-Agent Bandits
created: 2026-10-21T14:23:47.743Z
modified: 2026-10-21T15:58:26.073Z
tags:
  - intelligentagents
  - machinelearning
  - school
---

> [!definition]
> A [[Reinforcement learning]] problem set up where an agent has k arms that give a reward with an unknown distribution. Each round, agent picks an arm and gets a reward for that arm only.
>
> Only one agent, one state - form of [[Markov Decision Process]]
>
> A classical stochastic multi-armed bandit (MAB) problem is defined as a tuple:
>
> $\big(\mathcal{A}, \, \{P_a\}_{a \in \mathcal{A}}, \, T\big)$
>
> - $\mathcal{A} = \{1, 2, \dots, K\}$ - finite set of $K$ actions (arms)
>
> - $\{P_k\}_{a \in \mathcal{A}}$ is a collection of unknown probability distributions over $\mathbb{R}$, where each distribution $P_k$ corresponds to arm $k$ and has an expected reward (mean payoff):
>   $\mu_{k} = \mathbb{E}_{R \sim P_k}[R]$
>
> - $T \in \mathbb{N}$ - time horizon (total no. of rounds, can be finite or infinite)

> [!garden] Simplified Idea
> Imagine a gambler at a row of slot machines (arms), who has to decide which machines to play, how many times to play each machine and in which order to play them, and whether to continue with the current machine or try a different machine.

> [!attention] Regret
> Regret is the cost of not knowing $\mu_{k}$ in advance, i.e. how much could you have gained if you knew the optimal action from the start.
>
> $Reg(T)= T \cdot \mu^* - \mathbb{E} \left[ \sum^T_{t=1}r_{t} \right], \,\,\,\,\,\,\,\,\,\, \mu^* = \max_{k}\mu_{k}$
>
> The goal is to minimise regret

> [!tldr] Exploitation vs Exploration
> Balancing these two traits of a learning agent is important.
>
> Exploitation - keep playing the best arm so far
> Explore - try other arms to reduce uncertainty

Approaches to Multi-Armed Bandit problem:

- Greedy approach - always exploit
- [[ε-Greedy]] - balance exploitation and exploration
- UCB
- Thompson Sampling
- no algorithm can do better than $O(logT)$

What if we had multiple bandits? - [[Multi-Agent Bandits]]

#### References
