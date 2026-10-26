---
publish: true
created: 2026-10-25T11:44:33.212Z
modified: 2026-10-25T14:50:45.528Z
tags:
  - deeplearning
  - school
---

> [!definition]
> A technique for speeding up [[Gradient Descent]] by accumulating a _velocity vector_ in directions of _persistent reduction_ in our [[Cost Functions|Loss function]] over iterations.
>
> i.e. Add up steps to accelerate and move faster when making repeat steps in the same direction e.g. on a low slope, steps are small, but with momentum they add up and steps become bigger.
>
> > Given an objective function $f(\theta)$ to be minimised, classical momentum is given by:
> > $v_{t+1} = \mu v_t - \varepsilon \nabla f(\theta_t) \quad (1)$
> > $\theta_{t+1} = \theta_t + v_{t+1} \quad (2)$
> > where $\varepsilon > 0$ is the learning rate, $\mu \in [0, 1]$ is the momentum coefficient, and $\nabla f(\theta_t)$ is the gradient at $\theta_t$

> [!question] How does it help with [[Ill-Conditioned Curvature]]
> With cases where we have narrow canyons and our optimiser jumps from canyon wall to wall, overshooting the floor, momentum will add the opposite velocities and they will cancel each other out. Stabilising the optimiser.

> [!success] How much better does it perform than standard [[Gradient Descent]]?
> Given the _condition number_ of the curvature at the minimum $R$ and momentum $\mu$:
> $R=\frac{\text{Steepness of canyon walls}}{\text{Steepness of canyon floors}}$
> $\mu=\frac{(\sqrt{ R }-1)}{(\sqrt{ R }+1)}$
> _(if R=1, it's a perfectly round bowl, if R=100, walls are 100$\times$) steeper_
>
> Then CM reaches the minimum in $\sqrt{ R }$ times fewer steps than standard gradient descent.
>
> This is only for difficult terrain, they perform the same for standard terrain.
>
> [[Theoretical Metrics for Optimizer Convergence]]
>
> ![[media/Classical Momentum-1792939836725.webp]]

This can be sped up for all terrain with [[Nesterov Accelerated Gradient]]

#### References

- [[On the importance of initialization and momentum in deep learning]]
