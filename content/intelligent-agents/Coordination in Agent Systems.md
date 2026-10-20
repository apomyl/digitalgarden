---
publish: true
aliases:
  - coordination
created: 2026-10-18T17:30:21.729Z
modified: 2026-10-20T09:15:44.283Z
tags:
  - intelligentagents
  - school
---

> [!definition]
> [[Joint action]] under distributed information and control in [[Multi-Agent Systems]]. Concerned with the joint outcome not just interactions.
>
> Key Goals:
>
> - prevent conflicts
> - manage resources
> - handle dependencies
> - reduce redundancy
>
> Key Challenges:
>
> - [[Task Allocation|allocation]] - who does which task?
> - scheduling ([[Multi-Agent Path Finding|path coordination]]) - when should things happen?
> - resource coordination - who gets scarce resources?
> - joint activity - how do agents act as a team?

> [!question] Difference between coordination and communication?
> [[Communication in Agent Systems|Communication]] focuses on interactions, what was said between agents, expectations, etc.
>
> Coordination focuses on if actions are mutually compatible, is duplicate work being done, are resources managed efficiently, etc.

We can use [[Organisations in MAS]] as a coordination structure

- Organisations reduce coordination burden by shaping who can do what, who knows what, and who decides

[[Distributed Constraint Optimisation (DCOP)]] - framework solving global optimisation with no central coordinator (how we structure the problem to solve it)

> [!bug] Metrics for Evaluating coordination
>
> Choosing the best coordination mechanism depends on how you evaluate it.
>
> Outcome metrics
>
> - social welfare $\sum_i u_i$
> - makespan $\max_j C_j$
> - task completion rate
> - fairness or envy
> - safety violations
> - robustness under failure
>
> Process metrics
>
> - number of messages
> - computation per agent
> - delay to reach agreement
> - privacy loss
> - explainability of allocation
> - accountability evidence

#### References
