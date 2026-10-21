---
publish: true
created: 2026-10-21T19:22:26.016Z
modified: 2026-10-21T19:28:11.635Z
tags:
  - intelligentagents
  - machinelearning
  - school
---

> [!definition] Joint-Action Learning (JAL)
> Each agent $i$ learns its own values over [[Joint action|joint actions]], $Q_{i}(s,a_{i},a_{-i})$, where $a_{-i}$ = the other agents' actions
>
> This raises a new problem: we cannot just take $\max_{a_{i}}Q_{i}$, the best $a_i$ depends on what the other agents do.

> [!definition] Agent Modelling (AM)
> Predict other agents' behaviour from what they did before
>
> - policy reconstruction - learn $\hat{\pi}_{j} \approx \pi_{j}$ from $j$'s observed actions
> - best response to the models - $\pi_{i} \in BR_{i}(\hat{\pi}_{-i})$, where $\hat{\pi}_{-i}$ = the models of all other agents

![[media/JAL-AM-1792610885598.webp]]

#### References
