---
publish: true
aliases:
  - Solution concepts
created: 2026-10-20T10:26:47.439Z
modified: 2026-10-26T15:33:39.736Z
tags:
  - intelligentagents
  - school
  - game-theory
---

> [!definition]
> The internal decision rule that guide how [[Agents]] behave.
>
> In [[Game Theory in Agent Systems|Game Theory]], it's what the independent "players" use to determine their strategy, what actions they should choose.
> In [[Reinforcement Learning]], it is a mapping from states to actions: $\pi(a \mid s) = \mathbb{P}(A_t = a \mid S_t = s)$

An example of a policy configuration (a solution concept) is [[Nash Equilibrium]] where agents reach a state of equilibrium where they choose the same actions every time with no incentive to switch.

We can evaluate a joint policy (collective efficiency) with [[Pareto Optimality]]

#### Key solution concepts:

> [!definition] Best Response
> Agent $i$'s best response to the other agents' policies
> $\pi_{-i}=(\pi_{1},\dots,\pi_{i-1},\pi_{i+1},\dots,\pi_{n})$ is
> $\mathrm{BR}_i(\pi_{-i}) = \arg\max_{\pi_i} U_i(\langle \pi_i, \pi_{-i} \rangle)$
> (if you know exactly what other agents will do)

> [!definition] Dominant Actions
> Agents' best option no matter what others do
>
> - strict dominance - action $a_{i}$ strictly dominates $a_{i}'$ if:
>   - $\mathcal{R}_i(a_i, a_{-i}) > \mathcal{R}_i(a'_i, a_{-i}) \quad \text{for every } a_{-i}$
> - e.g. for [[Prisoner's Dilemma]] - defect dominates cooperate for both agents

> [!definition] Pure (Deterministic) and Mixed (Stochastic) policies
> Action choices available to agent
>
> - pure - always the same action
> - mixed - a distribution $\pi_{i}$ $A_{i}$

#### [[Reinforcement Learning]] policies:

> [!definition] Behaviour
> The policy used to generate actions, explore and collect transitions e.g. [[ε-Greedy]]

> [!definition] Target
> The policy whose value function is being evaluated or learned.

[[On-Policy vs Off-Policy]]

- on-policy: target $=$ behaviour
- off-policy: target $\neq$ behaviour

#### References
