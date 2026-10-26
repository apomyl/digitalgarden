---
publish: true
created: 2026-10-23T11:10:15.295Z
modified: 2026-10-25T15:45:50.038Z
tags:
  - deeplearning
  - school
  - machinelearning
---

> [!definition]
> Methods used to adjust network parameters (weights and biases) to minimise [[Cost Functions|loss function]], based on gradients calculated through [[Backpropagation Algorithm]].

> [!garden] First Order Techniques
> Optimisation techniques that consider the first derivate, the slope (which direction) of the [[Cost Functions|Loss Space]].
>
> This includes:
>
> - [[Gradient Descent|Stochastic Gradient Descent]]
> - [[Classical Momentum]]
> - [[Nesterov Accelerated Gradient]]
> - [[AdaGrad]]
> - [[RMSProp]]
> - [[Adaptive Moment Estimation]]

> [!garden] Second Order Techniques
> Optimisation techniques that consider the second derivate, the curvature (how quickly slope bends) of the [[Cost Functions|Loss Space]].
>
> We use the [[Hessian Matrix]] to represent the second derivates.
>
> This includes:
>
> - [[Newton's Method]]
> - [[Hessian-Free Method]]

> [!bug] Challenges
> **Geometry & Terrain**
>
> - [[Saddle Points]]
> - [[Ill-Conditioned Curvature]]
>
> **Learning Rate**
>
> - Sensitivity
>   - too low = slow learning, too high = overshooting
> - Uniform Updates across Parameters
>   - "If our data is sparse and our features have very different frequencies, we might not want to update all of them to the same extent, but perform a larger update for rarely occurring features."
>   - rare signals getting drowned out by common ones

#### References

- [[An overview of gradient descent optimization algorithms]]
