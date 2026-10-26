---
publish: true
aliases:
  - MARL
created: 2026-10-21T18:03:42.739Z
modified: 2026-10-26T19:24:09.294Z
tags:
  - intelligentagents
  - machinelearning
  - school
---

> [!definition]
> Finding optimal decision [[Policy|policies]] for two or more agents interacting in a shared environment ([[Multi-Agent Systems]])
>
> - Environment - a game model ([[Taxonomy for Decision (Game) Environments|normal-form, stochastic game]])
> - Learning - after training round $z$, a learning algorithm $\mathbb{L}$ uses collected data $\mathcal{D}^z$ to update the joint policy, $\pi^{z+1}=\mathbb{L}(\mathcal{D^z},\pi^z)$
> - Goal - converge to a solution concept e.g. [[Nash Equilibrium]]

This introduces new problems for learning:

- [[Non-Stationarity]] - changing policies affect other agents' payoffs
- [[Nash Equilibrium|Equilibrium]] selection - agents with early random exploration can easily converge on risk-dominant (safer options, not dependent on other agents' actions) equilibrium instead of reward-dominant (optimal, more trust needed) ones
- [[Multi-Agent Credit Assignment]] - whose actions contributed to a received reward?

Three ways to deal with the challenges:

- [[Central Learning]] - one learner controls all agents, choosing a joint action
- Independent Learning - each agent learns alone, treating the others as part of the environment
- [[JAL-AM]] - each agent learns joint-action values and models the others
  First two reduce MARL to single agent [[Reinforcement Learning|RL]], JAL-AM is in between.

| Approach                         | Non-stationarity | Multi-agent Credit Assignment | Scaling to Many Agents |
| -------------------------------- | ---------------- | ----------------------------- | ---------------------- |
| **Central Learning (CQL)**       | $\checkmark$     | $\checkmark$                  | $\times$               |
| **Independent Learning (IQL)**   | $\times$         | $\times$                      | $\checkmark$           |
| **JAL-AM** _(the middle ground)_ | **partly**       | **helps**                     | $\times$               |

We can apply both [[Central Q-Learning|central]] and [[Independent Q-Learning|independent]] learning to [[Q-learning]] and compare to JAL-AM
![[media/Multi-agent Reinforcement Learning-1792610943238.webp]]

#### References
