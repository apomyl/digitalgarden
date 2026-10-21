---
publish: true
aliases:
  - Normal-Form Game
created: 2026-10-20T10:12:57.734Z
modified: 2026-10-21T13:37:30.707Z
tags:
  - intelligentagents
  - school
  - game-theory
---

> [!definition]
> A [[Repeated Normal-Form Games|Normal-Form Game]] played over multiple rounds.

> [!question] What changes for repeated?
> Extended normal-form game to include sequential interaction by playing the same game over multiple rounds.
>
> Agents now have access to a shared history from previous rounds that can be used to determine [[Policy|policy]], [[Reward Functions|payoff]], etc.
>
> We can't simply use a normal payoff matrix because:
>
> - matrix space explodes exponentially
> - allows for empty threats
>
> Solution: [[Backward Induction]]

In infinitely repeated games, almost any feasible outcome can be sustained as an [[Nash Equilibrium|equilibrium]] if the players are [[Patience|patient]] enough.

This is known as the [[Folk Theorem]].

This is good as it means we have [[Non-cooperative Systems|self-interested agents]] who cooperate while self-policing.
However, due to repetition, too many behaviours become rational [[Nash Equilibrium|equilibria]], even negative ones as seen below.

> [!tldr] [[Cooperation in Agent Systems|Cooperation]] failure in Repeated Normal-Form Games
> If you play [[Prisoner's Dilemma]] (or any [[Non-cooperative Systems|non-cooperative game]]) multiple rounds and both players know the exact final round $T$ then through [[Backward Induction]] both players will Defect on every single round since players are picking whatever is best for them in that one round only.
>
> In order to make cooperation rational, there can be no known final round - we need an indefinite end.

#### References
