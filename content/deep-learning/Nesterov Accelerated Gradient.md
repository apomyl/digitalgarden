---
publish: true
aliases:
  - NAG
created: 2026-10-23T11:16:14.802Z
modified: 2026-10-25T13:14:02.561Z
tags:
  - deeplearning
  - school
---

> [!definition]
> [[Optimisation Techniques|Technique]] similar to [[Classical Momentum]] but instead of calculating the slope at its current position it looks ahead to the position its momentum will carry it and calculates from there to avoid overshooting.
>
> > NAG update may be written as:
> > $v_{t+1} = \mu v_t - \varepsilon \nabla f(\theta_t + \mu v_t) \quad (3)$
> >
> > $\theta_{t+1} = \theta_t + v_{t+1} \quad (4)$
> >
> > where $\varepsilon > 0$ is the learning rate, $\mu \in [0, 1]$ is the momentum coefficient, and $\nabla f(\theta_t + \mu v_t)$ is the gradient evaluated at the lookahead position $\theta_t + \mu v_t$.

![[media/Nesterov Accelerated Gradient-1792934036047.webp]]

> [!question] How does it perform?
> As seen in [[Theoretical Metrics for Optimizer Convergence]] it's maximum remaining error is $O\left( \frac{1}{T^2} \right)$ compared to [[Gradient Descent]] with $O\left( \frac{1}{T} \right)$.

#### References

- [[On the importance of initialization and momentum in deep learning]]
