---
publish: true
created: 2026-10-19T09:44:23.934Z
modified: 2026-10-26T17:28:52.129Z
tags:
  - intelligentagents
  - school
---

> [!definition]
> [[Coordination in Agent Systems|Coordination]] problem in [[Multi-Agent Systems|MAS]] of deciding which agent completes which task.

> [!question] Centralised vs Distributed Allocation
>
> Centralised - collect all values (rewards, costs, distances, risk, etc) compute centrally and announce assignments. Good approach when:
>
> - information is reliable
> - agents are cooperative
> - communication is cheap
> - a trusted coordinator exists
>
> Distributed - individual agents choose tasks (or make bids) based on local information. Good approach when:
>
> - information is local/private
> - tasks arrive online
> - central control is infeasible
> - resilience matters

> [!tldr] Assignment Model: Optimisation form
> TL;DR - maximise value across all agent/task combinations given restraints of no two agents on same task and no one agent can exceed their capacity for tasks
>
> Agents $i \in N$, tasks $j \in T$, binary decision $x_{ij} \in \{0, 1\}$.
>
> $\max_x \sum_{i \in N} \sum_{j \in T} v_{ij} x_{ij}$
>
> subject to
>
> $\sum_i x_{ij} \le 1 \quad \forall j \in T, \qquad \sum_j x_{ij} \le c_i \quad \forall i \in N.$

> [!bug] When tasks are not independent (Complementarity)
> Standard auctions ([[Contract Net]]) assume tasks have independent values, this means they fail when tasks work in synergy.
>
> Why does it break it? An agent could get a task that is dependent on another and that other task is failed, meaning it is stuck with a useless task it can't fulfill
>
> - Independent-Value Model (Contract Net assumption):
>   $V(S) = \sum_{j \in S} v_j$
>   _(total value is simply the sum of individual task values)_
>
> - Complementarity:
>   $V(\{map, deliver\}) > V(\{map\}) + V(\{deliver\})$
>   _(the whole is strictly greater than the sum of its parts)_

Solutions:

- [[Contract Net]] - auction system
- [[Coordination Graphs]]

#### References
