---
publish: true
aliases:
  - DCOP
created: 2026-10-19T11:22:09.789Z
modified: 2026-10-20T09:39:59.701Z
tags:
  - intelligentagents
  - school
---

> [!definition]
> A problem in which a group of agents must [[Task Allocation|distributedly]] choose values for a set of variables such that the cost of a set of constraints over the variables is minimised
>
> Decomposes a global optimisation problem into local variables, constraints, and utilities that agents solve through message passing
>
> variables $x_i \in D_i, \qquad$ constraints/utilities $f_k(\mathbf{x}_k)$
>
> $\max_{x_1, \dots, x_n} \sum_k f_k(\mathbf{x}_k)$

> [!question] Why?
> Allows us to compute the globally optimal solution through only peer-to-peer coordination.
>
> Provides an alternative to greedy solutions like [[Contract Net]] that break under interdependence.

This is only the framework/description of the problem, it can be solved using any of these algorithms:

- ADOPT
- [[DPOP Algorithm]]
- Max-Sum
- privacy-preserving DCOP
- dynamic DCOP

#### References

- https://en.wikipedia.org/wiki/Distributed\_constraint\_optimization
