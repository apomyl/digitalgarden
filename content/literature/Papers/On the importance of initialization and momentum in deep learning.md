---
publish: true
created: 2026-10-25T11:05:45.125Z
modified: 2026-10-25T13:25:26.912Z
tags:
  - deeplearning
  - scientific-papers
  - school
---

> [!garden] Summary
> Paper explains the importance of classical momentum, its relationship to Nesterov accelerated gradient method and how they can be used to improve optimisation convergence compared to standard gradient descent.
>
> Later part, (unread due to unit scope) compares to hessian-free method and explains the importance of initialisation and different techniques.

#### Notes

Solving [[Ill-Conditioned Curvature]] - steep slopes with smooth canyon floor means that optimiser jumps between the canyon walls and overshoots the floor

first order technique to match second order [[Hessian-Free Method]]

- [[Optimisation Techniques]]

[[Nesterov Accelerated Gradient]] is an accelerated version of [[Classical Momentum]]

> [!quote]
> The momentum method (Polyak, 1964), which we refer to as classical momentum (CM), is a technique for accelerating gradient descent that accumulates a velocity vector in directions of persistent reduction in the objective across iterations. Given an objective function $f(\theta)$ to be minimized, classical momentum is given by:
>
> $v_{t+1} = \mu v_t - \varepsilon \nabla f(\theta_t) \quad (1)$
>
> $\theta_{t+1} = \theta_t + v_{t+1} \quad (2)$
>
> where $\varepsilon > 0$ is the learning rate, $\mu \in [0, 1]$ is the momentum coefficient, and $\nabla f(\theta_t)$ is the gradient at $\theta_t$.

- objective = model loss
- persistent reduction = direction that keeps leading downhill step after step
- velocity vector = algorithms accumulated speed and direction

i.e. if terrain slopes down in the same direction multiple times, optimiser adds them together and speeds up
if it keeps jumping back and forth, the opposing pushes cancel out, keeping the optimiser steady

people dismissed momentum because its benefits disappear in stochastic/noisy approaches near the end of training but for deep neural networks the early 'transient' stages dominate training so it doesn't matter?

researchers viewed training from the model of optimising the end trying to get the slope down to 0 and momentum didn't help in that, and because they were using quite shallow simple models the early benefits weren't obvious

[[Nesterov Accelerated Gradient]] is a type of momentum where you calculate the slope based on where your momentum will take you instead of where you currently are

#### References
