---
publish: true
created: 2026-10-25T15:31:10.530Z
modified: 2026-10-25T19:33:21.747Z
tags:
  - deeplearning
  - school
---

> [!definition]
> A [[Optimisation Techniques|technique]] to fix the biggest issue of [[AdaGrad]], the fact that as more and more gradients accumulate the denominator gets so large that the learning rate approaches 0.
>
> RMSProp uses a moving average of the most recent gradients instead of keeping an entire history.
>
> $\theta_{t+1} = \theta_t - \frac{\eta}{\sqrt{E[g^2]_t + \epsilon}} g_t$
> $E[g^2]_t = \gamma E[g^2]_{t-1} + (1 - \gamma) g_t^2$
>
> where
>
> - $\gamma$, the decay factor, is usually set to 0.9
> - $g_t^2$ is the squared gradient of the current step
> - $E[g^2]_t$: is the moving average of squared gradients

#### References

- [[An overview of gradient descent optimization algorithms]]
