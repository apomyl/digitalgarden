---
publish: true
created: 2026-10-21T11:48:24.722Z
modified: 2026-10-21T11:54:39.501Z
tags:
  - intelligentagents
  - game-theory
  - school
---

> [!definition] Normal-form Game  $(I, \{A_i\}_{i \in I}, \{\mathcal{R}_i\}_{i \in I})$
>
> Games where all participants have complete information and act simultaneously.
>
> - $I = \{1, \dots, n\}$: a finite set of **agents**
> - $A_i$: agent $i$'s finite set of **actions**
>   - a **joint action** is $a = (a_1, \dots, a_n) \in A = A_1 \times \dots \times A_n$
> - $\mathcal{R}_i : A \to \mathbb{R}$: agent $i$'s **[[Reward Functions|reward function]]** over joint actions
>
> We can solve this by making a payoff matrix with all combinations and picking the highest payoff.

> [!bug] One-Shot vs Repeated
> We assume games are played once, with nothing else to consider other than this one round.
> For multiple rounds, modelling agents becomes more complex: [[Repeated Normal-Form Games]]

Example: [[Prisoner's Dilemma]]

#### References
