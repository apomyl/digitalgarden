---
publish: true
created: 2026-10-21T19:18:49.710Z
modified: 2026-10-26T17:40:24.702Z
tags:
  - intelligentagents
  - machinelearning
  - school
---

> [!definition]
> Solution to problems in [[Multi-agent Reinforcement Learning|MARL]] by having one agent control all agents.
>
> Learn a single central [[Policy|policy]] $\pi_{c}$ that observes the state and selects a [[Joint Action and Policy|joint action]] $(a_{1}\dots,a_{n})$
>
> - requires tuning reward vector $(r_{1},\dots,r_{n})$ into a single scalar $r$
> - does not scale - joint action space grows exponentially
> - unsuitable when agents must act on local information only

#### References
