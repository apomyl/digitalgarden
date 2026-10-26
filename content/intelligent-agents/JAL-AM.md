---
publish: true
created: 2026-10-21T19:22:26.016Z
modified: 2026-10-26T19:38:53.065Z
tags:
  - intelligentagents
  - machinelearning
  - school
---

> [!definition] Joint-Action Learning (JAL)
> Each agent $i$ learns its own values over [[Joint Action and Policy|joint actions]], $Q_{i}(s,a_{i},a_{-i})$, where $a_{-i}$ = the other agents' actions
>
> This raises a new problem: we cannot just take $\max_{a_{i}}Q_{i}$, the best $a_i$ depends on what the other agents do.

> [!definition] Agent Modelling (AM)
> Predict other agents' behaviour from what they did before
>
> - policy reconstruction - learn $\hat{\pi}_{j} \approx \pi_{j}$ from $j$'s observed actions
> - best response to the models - $\pi_{i} \in BR_{i}(\hat{\pi}_{-i})$, where $\hat{\pi}_{-i}$ = the models of all other agents

> [!question] How does it solve our problems from [[Multi-agent Reinforcement Learning|MARL]]
> It helps with [[Non-Stationarity]] by explicitly outlining the existence of other agents, it's only a partial solution as we are estimating the opponent model.
>
> Similarly because the other agents are accounted for, it learns what rewards are based on its own contributions, however the [[Joint Action and Policy|Joint Action]] space is too large so the sample isn't all inclusive and perfect.

![[media/JAL-AM-1792610885598.webp]]

> [!tldr] The JAL-AM Algorithm (3 Steps)
>
> 1. **Joint-Action Values:**
>
> Learn values $Q_i(s, a_i, a_{-i})$ for every joint action.
>
> 2. **Agent Modelling (Policy Reconstruction):**
>
> Estimate each opponent $j$'s policy $\hat{\pi}_j(a_j \mid s)$ by tracking empirical action frequencies in state $s$:
>
> $\hat{\pi}_j(a_j \mid s) = \frac{C_j(s, a_j)}{\sum_{a'_j} C_j(s, a'_j)} = \frac{\# \text{ times agent } j \text{ played } a_j \text{ in } s}{\# \text{ total visits to state } s}$
>
> 3. **Best Response (Action Selection):**
>
> Score each candidate action $a_i$ by its expected joint Q-value under the opponent models:
>
> $\mathbb{E}[Q_i(s, a_i)] = \sum_{a_{-i}} \left( \prod_{j \neq i} \hat{\pi}_j(a_j \mid s) \right) Q_i(s, a_i, a_{-i})$
>
> Select the highest-scoring action greedily (or explore $\epsilon$-greedily):
>
> $a_i^* = \arg\max_{a_i \in A_i} \mathbb{E}[Q_i(s, a_i)]$

#### References
