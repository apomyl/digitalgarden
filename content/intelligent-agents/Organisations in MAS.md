---
publish: true
created: 2026-10-19T11:04:51.892Z
modified: 2026-10-26T17:13:51.044Z
tags:
  - intelligentagents
  - school
---

> [!definition]
> Computational structure for [[Coordination in Agent Systems|coordination]] that assigns or constrains roles, authorities, dependencies, information flows, protocols, and [[Accountability in Agent Systems|accountability]] relations among agents.
>
> - Role - what functions exist?
> - Authority - who can decide?
> - Information - who observes what?

**Organisational topologies** and **coordination styles**
\- Hierarchy - decisions flow through leaders
\- Market - agents bid for tasks or resources e.g. [[Contract Net]]
\- Team - peer coordination towards single shared objective
\- Blackboard - agents read and write a shared state
\- Federation - semi-autonomous groups (two-tier hybrid of autonomous groups with a designated facilitator who coordinates with other groups)

![[media/Organisations in MAS-1792408374793.webp]]

> [!bug] [[Communication in Agent Systems|Communication]] cost vs robustness
> We can use different organisational topologies for how nodes are connected, each comes with different trade-offs, we are trying to balance no. of messages and robustness.
>
> Takeaway: Cheaper communication increases vulnerability

| Topology        | Directed Messages / Round | Scaling  | Robustness | Main Trade-off                                                        |
| :-------------- | :-----------------------: | :------: | :--------- | :-------------------------------------------------------------------- |
| Fully Connected |        $n(n - 1)$         | $O(n^2)$ | Highest    | Fast spread & no bottleneck, but very expensive at scale              |
| Hub-and-Spoke   |        $2(n - 1)$         |  $O(n)$  | Lowest     | Cheapest, but central hub is a single point of failure                |
| Ring            |           $2n$            |  $O(n)$  | Medium     | Cheap & decentralized, but information travels slowly around the loop |

> [!question] How does a [[Sociotechnical Systems|sociotechnical system]] fit into this?
> A sociotechnical system is a higher level structure than organisations, any of these organisation topologies can be part of an STS as an Org.

> [!tldr] We can improve [[Task Allocation]] using [[Role Allocation]]
> Roles are useful in making [[Task Allocation]] easier, roles:
>
> - restricts behaviour - simplifies coordination by giving agents predictable/known actions
> - makes the [[Joint Action and Policy|joint action]] space smaller

#### References
