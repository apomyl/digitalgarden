---
publish: true
created: 2026-10-19T10:48:03.210Z
modified: 2026-10-26T13:41:06.681Z
tags:
  - intelligentagents
  - school
---

> [!definition]
> A [[Coordination in Agent Systems|coordination]] problem in [[Multi-Agent Systems]] where agents move physically in a share space.

> [!failure] Conflict Types
>
> - Vertex conflict - two agents occupy the same cell at the same time
> - Edge conflict - two agents swap positions on the same edge at the same time
> - Resource conflict - two agents reserve the same scarce facility

> [!success] Solutions
>
> - Priority - agents access cells/resources based on a priority ranking
>   - can be unfair
>   - fast and easy
> - Reservation - agents reserve cells/time slots (first-come first-served)
>   - provides explicit ownership, easy to audit
>   - can fragment capacity (idle time)
> - [[Joint Action and Policy|Joint planning]] - plan for all agents together
>   - best result at higher cost
>   - hard for private goals

Interesting solution: **Stigmergy** - coordination through the environment

- e.g. ants leaving pheromone trails, software agents updating a share board, etc

#### References
