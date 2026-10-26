---
publish: true
created: 2026-10-20T12:02:46.673Z
modified: 2026-10-26T15:42:52.640Z
tags:
  - intelligentagents
  - school
  - game-theory
---

> [!definition]
> A [[Taxonomy for Decision (Game) Environments|game specification]] that uses a tree to show the exact sequence of moves and final payoffs, compared to a [[Repeated Normal-Form Games|Normal-Form Game]] that uses a matrix.
>
> Nodes - represent who moves
> Edges - represent possible actions
> Leaves - final rewards
> Strategy - specifies an action at every node where an agent might move

We solve these through [[Backward Induction]], starting from leaves and moving upwards, at each step we assume agent picks its best continuation. This is in order to achieve a [[Subgame Perfect Equilibrium]]. Using a normal payoff matrix would give us multiple sub-optimal [[Nash Equilibrium]].

> [!question] Is [[DPOP Algorithm]] the same as backward induction?
> They are similar in that they work through propagating backwards through a tree, however in backward induction each agent is [[Strategic Agents|Strategic]] and cares only about it's own utility while in DPOP each node calculates the utility of the subtree underneath it.
>
> This would be the equivalent of backward induction for a cooperative game where agents are working together to maximise the global utility/minimise global cost.

#### References
