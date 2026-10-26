---
publish: true
created: 2026-10-25T14:52:57.331Z
modified: 2026-10-25T19:43:29.113Z
tags:
  - deeplearning
  - school
---

> [!definition]
> An algorithm for [[Gradient Descent|gradient-based]] [[Optimisation Techniques|optimisation]], that aims to be more adaptive. This means we adapt our updates to each individual parameter to perform larger or smaller updates depending on their importance.
>
> AdaGrad modifies the learning rate by dividing it by the history of past gradients, larger gradients = smaller learning rate:
>
> $\theta_{t+1,i} = \theta_{t,i} - \frac{\eta}{\sqrt{G_{t,ii} + \epsilon}} \cdot g_{t,i}$
>
> - $G_{t,ii}$ - history, sum of gradients
>   - squared to prevent negatives from cancelling out
>   - square rooted to constrain growth
> - $\epsilon$ - tiny buffer to ensure not dividing by 0 ever

> [!tldr] Vector form using element-wise multiplication
> $\theta_{t+1} = \theta_t - \frac{\eta}{\sqrt{G_t + \epsilon}} \odot g_t$

> [!bug] Problem
> Due to the nature of the history being a raw sum, as the number of gradients increases, the sum can become large enough that the learning rate approaches 0. This issue is addresses with [[RMSProp]], using a running average of gradients instead of a complete history.

#### References
