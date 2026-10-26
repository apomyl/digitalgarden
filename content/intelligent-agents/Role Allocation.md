---
publish: true
created: 2026-10-26T17:13:52.714Z
modified: 2026-10-26T17:17:37.754Z
tags:
  - intelligentagents
  - school
---

> [!definition]
> We use roles as defined in [[Organisations in MAS]] as an improvement to [[Task Allocation]].

> [!question] Why Roles?
>
> - Restricts behavior to make agents predictable and shrinks the joint action space.
> - Roles persist over time (tasks are temporary).
> - Roles define permissions (which messages/resources an agent can access)
> - Roles carry [[Norms in Agent Systems|Norms]]/obligations

> [!tldr] Formal Role Allocation Model
> Assign agents $i \in N$ to roles $r \in R$ with cost $c_{ir}$ and indicator $y_{ir} \in \{0, 1\}$:
> $\min_y \sum_{i,r} c_{ir} y_{ir}$
> Subject to:
>
> - $\sum_i y_{ir} \ge 1 \quad \forall r \in R$ (Every role must have $\ge 1$ agent)
> - $\sum_r y_{ir} \le 1 \quad \forall i \in N$ (Each agent fills at most $1$ role)
>
> _(for $n$ agents and $n$ roles, there are $n!$ possible one-to-one assignments)_

#### References
