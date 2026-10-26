---
publish: true
created: 2026-10-26T16:09:27.535Z
modified: 2026-10-26T16:51:57.136Z
tags:
  - intelligentagents
  - school
---

> [!definition]
> Combines [[Digital Garden/maps-of-content/Deep Learning|Deep Neural Networks]] with [[Q-learning]] to approximate the optimal action-value function $Q(s,a)$.
>
> We feed the current state $s$ into our network $\theta$ to get estimates for all actions $Q_{\theta}(s,a_{1}), Q_{\theta}(s,a_{2}),\dots$

> [!tldr] Training Loop
> ![[media/Deep Q-Network (DQN)-1793031728756.webp]]
>
> 1. Use [[ε-Greedy]] to choose action from current outputs of network $Q_{\theta}$
> 2. After taking an action $a$ store the tuple $(s,a,r,s')$ into Replay Buffer $\mathcal{D}$
> 3. Sample a uniform random mini-batch from $\mathcal{D}$ to train on
>
> - breaks the strong temporal correlation of consecutive states
>
> 4. Learn via the target network - move $Q_{\theta}(s,a)$ towards $r+\gamma \max_{a'}Q_{\theta^-}(s',a')$
>
> - reward + estimate from target network used to guide learning
> - $\theta^-$ is the target network
> - every $C$ steps copy $\theta^- \leftarrow \theta$
> - we use this target so that network doesn't chase its own tail, and its better than random guesses for the estimates
> - $\text{Target} = \begin{cases} r & \text{if } s' \text{ is terminal} \\ r + \gamma \max_{a'} Q_{\theta^-}(s', a') & \text{otherwise} \end{cases}$

#### References
