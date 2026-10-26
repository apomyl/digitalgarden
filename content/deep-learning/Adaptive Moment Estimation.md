---
publish: true
aliases:
  - Adam
created: 2026-10-25T15:43:19.803Z
modified: 2026-10-26T16:53:34.100Z
tags:
  - deeplearning
  - school
---

> [!definition]
> An [[Optimisation Techniques|optimisation]] method to calculate adaptive learning rates combining [[AdaGrad]] and [[Classical Momentum|momentum]]

> [!tldr] The equations (3 parts)
>
> Set up running average of gradients (for momentum):
> $m_t = \beta_1 m_{t-1} + (1 - \beta_1) g_t$
>
> Running average of squared gradients (for [[RMSProp]]/AdaGrad):
> $v_t = \beta_2 v_{t-1} + (1 - \beta_2) g_t^2$
>
> _where default $\beta_{1}=0.9$ and $\beta_{2}=0.999$_
>
> > [!bug] Initialisation of m and v
> > Because the running averages start initialised at zero, early estimates are pulled unnaturally close to zero e.g. $m_t = 0.9 (0) + 0.1 (20) = 2$, way off from our first reading because the running average is weighted more heavily.
> >
> > Solution: divide by $(1 - \beta^t)$ to correct for bias
> >
> > $\hat{m}_t = \frac{m_t}{1 - \beta_1^t} \qquad \hat{v}_t = \frac{v_t}{1 - \beta_2^t}$
> >
> > _From our previous example, now we'd have $\hat{m_{t}}=\frac{2}{1-0.9}=20$, so we've corrected the average_
>
> Final equation:
> $\theta_{t+1} = \theta_t - \frac{\eta}{\sqrt{\hat{v}_t} + \epsilon} \hat{m}_t$

#### References

- [[An overview of gradient descent optimization algorithms]]
