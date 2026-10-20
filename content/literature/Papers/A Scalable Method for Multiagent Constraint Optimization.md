---
publish: true
created: 2026-10-20T09:16:09.406Z
modified: 2026-10-20T09:43:21.300Z
tags:
  - intelligentagents
  - scientific-papers
  - school
---

> [!garden] Summary
> The paper sets out an algorithm ([[DPOP Algorithm|Distributed Pseudo-tree Optimization Procedure]]) for solving [[Distributed Constraint Optimisation (DCOP)|DCOP]], that is, the optimal combination of agent choices within constraints.
>
> They prove the algorithm requires a linear number of messages and the size of messages is dependent on the _induced width_ $w$ (exponential - $d^w$) of the pseudotree.

#### Notes

![[media/A Scalable Method for Multiagent Constraint Optimization-1792488223388.webp|376]]

- branches are (relatively) independent
- back-edges (dashed lines) that are not part of the spanning tree represent pseudo relationships

> [!tldr] Algorithm
>
> 1. Use [[Depth-First Search]] to create a pseudo-tree from an arbitrary topology.
> 2. Starting from leaf nodes, propagate UTIL message upwards.
>
> - each node calculates "how much utility each of its values gives for the whole subtree rooted at itself"
> - essentially creating a table of all possible choices (based on it's own, parent's and children's choices)
>
> 3. When the root is reached, it can make the optimal choice based on the highest total utility values. It then passes a VALUE message downwards informing children of what choice it made.
>
> - All subsequent nodes use this value and consult their own UTIL tables to see what their optimal choice is based on the parent value and then pass a VALUE message downwards themselves

For nodes with pseudo-parents, they need to take that dependency into account when calculating UTIL so instead of just a message $\langle x_{c}, x_{p} \rangle$ it forms a 2-D hypercube message with two of those: one for it's parent and one for it's pseudo-parent.

Information is local since each node is only concerned with itself, children and parents.

Performs significantly better (in no. of messages) to ADOPT

#### References
