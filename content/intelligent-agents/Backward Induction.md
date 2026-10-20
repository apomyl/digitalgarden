---
publish: true
created: 2026-10-20T12:21:23.427Z
modified: 2026-10-20T12:56:15.679Z
tags:
  - intelligentagents
  - school
  - game-theory
---

> [!definition]
> Algorithm for finding [[Subgame Perfect Equilibrium]] in games by starting at the reward and maximising at each step.
>
> For backward induction to find a [[Subgame Perfect Equilibrium|SPE]] in a [[Repeated Normal-Form Games]] or [[Extensive-Form Games]] we require a finite game of perfect information.

1. Represent game as a finite, perfect information [[Extensive-Form Games|EFG]]
2. Start at leaves
3. At each decision node, maximise payoff for current player
4. Propagate subgame payoff values upwards

> [!tldr] [[Cooperation]] failure in [[Repeated Normal-Form Games]]
> If you play [[Prisoner's Dilemma]] multiple rounds and both players know the exact final round $T$ then through Backward Induction both players will Defect on every single round since players are picking whatever is best for them in that one round only.
>
> In order to make cooperation rational, there can be no known final round - we need an indefinite end.

#### References
