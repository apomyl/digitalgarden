---
publish: true
aliases:
  - Normal-Form Game
created: 2026-10-20T10:12:57.734Z
modified: 2026-10-20T12:40:44.445Z
tags:
  - intelligentagents
  - school
  - game-theory
---

> [!definition] Normal-form Game  $(I, \{A_i\}_{i \in I}, \{\mathcal{R}_i\}_{i \in I})$
>
> - $I = \{1, \dots, n\}$: a finite set of **agents**
> - $A_i$: agent $i$'s finite set of **actions**
>   - a **joint action** is $a = (a_1, \dots, a_n) \in A = A_1 \times \dots \times A_n$
> - $\mathcal{R}_i : A \to \mathbb{R}$: agent $i$'s **[[Reward Functions|reward function]]** over joint actions
>
> Assumptions:
>
> - single step (one shot) - game is played once, no state, time or next round
> - simultaneous choice
>
> We can solve this by making a payoff matrix with all combinations and picking the highest payoff.

> [!question] What changes for repeated?
> Extended normal-form game to include sequential interaction by playing the same game over multiple rounds.
>
> Agents now have access to a shared history from previous rounds that can be used to determine [[Policy|policy]], rewards, etc.
>
> We can't simply use a normal payoff matrix because:
>
> - matrix space explodes exponentially
> - allows for empty threats
>   Alternative: [[Backward Induction]]

#### References
