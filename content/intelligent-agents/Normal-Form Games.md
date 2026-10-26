---
publish: true
created: 2026-10-21T11:48:24.722Z
modified: 2026-10-26T15:34:16.866Z
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
> Normal-Form games can be solved using [[Game Theory in Agent Systems|Game Theoretic Principles]] like [[Policy|strict dominance, best response]] and [[Nash Equilibrium]].
>
> We can formulate the problem as a payoff matrix.

> [!bug] One-Shot vs Repeated
> We assume games are played once, with nothing else to consider other than this one round.
> For multiple rounds, modelling agents becomes more complex: [[Repeated Normal-Form Games]]

Example: [[Prisoner's Dilemma]]

#### References
