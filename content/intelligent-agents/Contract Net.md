---
publish: true
created: 2026-10-19T10:16:05.250Z
modified: 2026-10-19T10:44:19.036Z
tags:
  - intelligentagents
  - school
---

> [!definition]
> A [[Coordination in Agent Systems|coordination]]/[[Task Allocation|allocation]] protocol where a "manager" announces tasks and "contractors" bid.
>
> Greedy, one task at a time algorithm.
>
> Typical steps: announce -> bid -> award -> execute -> report

> [!question] What's a bid?
> A bid isn't a single numerical value but instead it's informational. When an agent is bidding they send (local) information such as:
>
> - hardware specifications
> - estimated completion time / deadlines
> - resource costs and risk estimations
> - reliability or probability of success
>
> The "manager" then evaluates them with some _scoring rule_ considering some weighted combination of the information provided and perhaps some social context such as [[Trust and Reputation]].

Example:
![[media/Contract Net-1792405277099.webp]]

> [!error] Drawbacks
>
> - assumes agents can estimate their own cost/capability
> - needs a rule for comparing bids
> - may fail when tasks are interdependent
> - can produce local choices that are poor globally
> - if agents are strategic, truthful bidding is not always guaranteed

#### References
