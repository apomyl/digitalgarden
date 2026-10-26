---
publish: true
aliases:
  - Joint Policy
  - Joint Action
created: 2026-10-19T09:49:48.096Z
modified: 2026-10-26T19:57:24.629Z
tags:
  - intelligentagents
  - school
---

> [!definition] Joint Action
> Combination of individual actions chosen simultaneously by [[Multi-Agent Systems|agents]] in a shared environment.

> [!definition] Joint Policy
> A tuple $\pi$ of all agents' individual policy.

> [!tldr] **Scenario: Multiagent Decision at One Step**
> $N = \{1, \dots, n\}$ - agents
> $a = (a_1, \dots, a_n) \in A_1 \times \dots \times A_n$ - joint action space
> $V(s, a)$ - value of chosen joint action given true state
> However each agent may observe only $o_i$ - partial information
>
> In a centralised system: $a^* \in \arg\max_a V(s, a)$
> In a distributed system: $a_i = \pi_i(h_i, m_i)$ (each agent $i$ executes its own _policy_ $\pi$, choosing based on history $h$ and messages $m$)
>
> **Calculating action space**
> If each of $n$ agents has $k$ possible actions, there are $k^n$ joint actions
> $|A_{1} × · · · × A_{n}| = k^n$

> [!tldr] Expected Reward/Return under a joint policy
>
> We combine multiple agents' [[Policy|policies]] into a joint policy $\pi=(\pi_{1},\dots ,\pi_{n})$, then the expected reward is:
> $U_{i}(\pi)=\sum_{a \in A}\left( \prod_{j \in I}\pi_{j}(a_{j}) \right)\mathcal{R}_{i}(a)$
>
> - agent $i$'s average reward over many plays

> [!bug] Coordination over time
> For a joint activity, agents must coordinate not only on initial [[Task Allocation|task allocation]], but also on progress, failure, repair, and termination.
>
> We need to define: [[Joint Intentions]]

#### References
