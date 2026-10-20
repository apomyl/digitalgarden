---
publish: true
aliases:
  - SPE
created: 2026-10-20T12:12:46.047Z
modified: 2026-10-20T12:51:48.287Z
tags:
  - intelligentagents
  - game-theory
  - school
---

> [!definition]
> A strategy profile where you induce [[Nash Equilibrium]] in every subgame
>
> - every player's choices make rational sense at every possible stage of the game
>
> A Nash Equilibrium that eliminates _empty threats_ and _hollow promises_

Can find it through [[Backward Induction]]

###### Example of empty threat:

![[media/Intelligent Agents Lecture 2026-10-13-_-_-1-1792498574523.webp|292]]
For this game tree, a normal payoff matrix would produce 2 NE:

- (Enter, Accommodate)
- (Stay Out, Fight)

If $I$ chooses fight then $E$ will pick Stay Out since 0 > -1, however if $E$ does Enter, $I$'s best move is Accommodate, so this is an empty threat.

_$I$ threatens to fight if $E$ enters, but if agents make the best choice at each step then when $E$ does enter $I$ will accommodate to get a better result_

$E$ knows that so it will never pick Stay Out, and that way $I$ is hurt by it's own rationality

#### References
