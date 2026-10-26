---
publish: true
aliases:
  - Stochastic Gradient Descent
created: 2026-09-22T16:30:08.680Z
modified: 2026-10-25T13:56:44.511Z
tags:
  - school
  - deeplearning
  - machinelearning
---

> [!garden] Gradient Descent
> A method used to find the minimum of [[Cost Functions]] (objective function) by moving towards the direction of "steepest descent" – where the slope/gradient is descending fastest. Adjust weights using [[Delta Rule]]
>
> ![[media/Gradient Descent-1790188104072.webp|634x404]]

> [!definition] Determistic Gradient Descent
> Computes the gradient of the cost function w.r.t. to the parameters θ for the entire training dataset:
>
> $\theta=\theta-\eta \cdot \nabla_{\theta}J(\theta)$
>
> _(provides best solution but too computationally expensive)_

> [!definition] Online Gradient Descent (Pure Stochastic)
> Calculate error of single input ($x^{(i)}, y^{(i)}$) at a time:
> $\theta=\theta-\eta \cdot \nabla_{\theta}J(\theta;x^{(i)}; y^{(i)})$
>
> _(cost function of single sample may not be representative, will be messy and struggle to find a minimum)_

> [!definition] Mini-Batch Gradient Descent (Stochastic Gradient Descent)
> Mini-batch gradient descent finally takes the best of both worlds and performs an update for every mini-batch of $n$ training examples:\
> $θ = θ − η · ∇_θJ (θ; x^{(i:i+n)}; y^{(i:i+n)})$

This is what happens when a model is "learning": it is continuously minimising the cost function to optimise the parameters, weights and biases.

![[media/Gradient Descent-1790188627420.webp]]

> [!eg] [[Linear Regression]] using (Deterministic) [[Gradient Descent]]
>
> ```python
> # Gradient Descent Solution
>
> import numpy as np
>
> N = 200
>
> # Generate our dataset, random sample of linear equation with noise
> x = np.sort(np.random.sample((N,1)))*10
> y = (6 * x) + 7 + np.random.normal(0, 0.5, (N, 1))
>
> # Initialise variables
> W = 15
> b = 3
> lr = 0.01
>
> # Gradient descent
> for i in range(2000):
>    y_pred = W * x + b
>   
>    residuals = y_pred - y
>   
>    dW = (-2 / N) * np.sum((y - y_pred) * x)
>    db = (-2 / N) * np.sum((y - y_pred))
>   
>    W = W - lr * dW
>    b = b - lr * db
>
> print(f"W: {W}")
> print(f"b: {b}")
> ```

#### References

- https://www.youtube.com/watch?v=IHZwWFHWa-w
- SGD PyTorch - https://docs.pytorch.org/docs/2.14/generated/torch.optim.SGD.html
- https://www.geeksforgeeks.org/machine-learning/gradient-descent-in-linear-regression/
- [[An overview of gradient descent optimization algorithms]]
