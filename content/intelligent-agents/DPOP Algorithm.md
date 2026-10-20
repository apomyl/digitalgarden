---
publish: true
created: 2026-10-20T09:39:36.181Z
modified: 2026-10-20T09:42:49.443Z
tags:
  - intelligentagents
  - school
---

> [!definition] Algorithm
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

![[media/DPOP Algorithm-1792489296285.webp|412]]

#### References

- [[A Scalable Method for Multiagent Constraint Optimization]]
