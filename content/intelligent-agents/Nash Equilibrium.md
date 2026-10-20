---
publish: true
created: 2026-10-20T10:37:56.316Z
modified: 2026-10-20T12:12:23.976Z
tags:
  - intelligentagents
  - school
  - game-theory
---

> [!definition]
> A [[Policy]] configuration where each player in the game chooses the best strategy possible, given the choices of the other players, no player can improve their outcome by unilaterally (by themselves) changing their strategy.
>
> A game state where agents do the same move every time, with no incentive for any to change action.

Joint policy $\pi$ is a Nash Equilibrium if every agent's policy is a best response to the others:
$\forall i, \pi'_i : U_i(\pi'_i, \pi_{-i}) \le U_i(\pi)$

> [!success] When is NE useful?
>
> - predicting outcomes
> - self-enforcing agreements
> - as a target for learning agents
> - it always exists for finite games

> [!failure] What are it's shortcomings?
>
> - sub-optimal - doesn't maximise total reward
> - non-unique - there can be many different NE for a game
>
> Example: Common-Pool Resource problem (The Tragedy of the Commons)
>
> - fishers share one fishing ground; each chooses to Restrain or Overfish
> - an NE exists where everyone does Overfish as it is a dominant action (more reward for the individual)
> - if everyone overfishes, the stock collapses, everyone would be better off if they restrained in the long run

> [!question] How do we measure which Nash Equilibrium performs better?
> In the same way we evaluate any policy - with [[Pareto Optimality]]
>
> We want the pareto-optimal equilibrium where no agent can improve their outcome.
> e.g. In [[Prisoner's Dilemma]] the equilibrium (Defect, Defect) is _pareto-dominated_ by (Cooperate, Cooperate)

> [!question] How can we improve NE?
> NE assumes agents act independently, if we use a shared signal, we can get better results. This is a [[Correlated Equilbirium]].
>
> Every NE is a CE but not conversely: CE can reach rewards no NE can.
>
> For [[Extensive-Form Games]] we use [[Subgame Perfect Equilibrium]] - inducing NE in every subgame

#### References
