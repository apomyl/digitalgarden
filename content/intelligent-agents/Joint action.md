---
publish: true
created: 2026-10-19T09:49:48.096Z
modified: 2026-10-19T10:02:02.875Z
tags:
  - intelligentagents
  - school
---

> [!definition]
> Combination of individual actions chosen simultaneously by [[Multi-Agent Systems|agents]] in a shared environment.
>
> **Scenario: Multiagent Decision at One Step**
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

#### References
