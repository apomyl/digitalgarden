---
publish: true
created: 2026-10-21T15:29:23.350Z
modified: 2026-10-26T16:02:21.391Z
tags:
  - intelligentagents
  - machinelearning
  - school
---

> [!definition]
> Altered greedy approach to [[Multi-Armed Bandit]] problem, where you either explore or exploit randomly based on variable $\epsilon$.
>
> - With probability $\epsilon$ - explore (pick random arm)
> - With probability $1-\epsilon$ - exploit (pick highest reward arm)
>
> _Note: when exploring we can still pick the highest reward arm from $|A|$ therefore, the probability distribution is:_
> $\pi(a \mid s) = \begin{cases} 1 - \epsilon + \frac{\epsilon}{\vert{}A\vert{}} & \text{if } a \text{ is greedy (best)} \\ \frac{\epsilon}{\vert{}A\vert{}} & \text{otherwise} \end{cases}$

> [!attention] Regret for $\epsilon$-greedy
> ![[media/ε-Greedy-1792596865642.webp]]

#### References
