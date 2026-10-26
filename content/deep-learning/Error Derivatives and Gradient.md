---
publish: true
created: 2026-09-24T20:16:35.672Z
modified: 2026-09-28T08:47:47.321Z
tags:
  - school
  - deeplearning
  - machinelearning
---

> [!definition] Error Derivatives
> Measure of the rate at which the [[Cost Functions|loss function]] changes with respect to a specific parameter, dictating how to adjust weights to minimise error.
>
> Partial derivative of the error in respect to one weight, indicates how that one weight affects the total error.
>
> $\frac{\partial L}{\partial w_{ij}}$

> [!definition] Error Gradient
> Full vector of all the error containing all individual error derivatives.
> It points in the direction of the steepest overall increase in the error function.
>
> $\nabla L = \begin{bmatrix} \frac{\partial L}{\partial w_1} \\ \frac{\partial L}{\partial w_2} \\ \vdots \\ \frac{\partial L}{\partial w_n} \end{bmatrix}$

> [!eg]
> $\frac{\partial E}{\partial w_{ji}} = \sum_{n=1}^N \frac{\partial E_n}{\partial w_{ji}}$
> Consider an arbitrary unit (node) $j$. Bias will be 1.
> The unit compares a value $z_j$ by first computing $a_j$, a weighted sum of its inputs, and then passing $a_j$ through some non-linear [[Activation Functions|activation function]] $h$.
> $a_j = \sum_i w_{ji} z_i$
> $z_j = h(a_j)$
> Since $E_n$ (the error for the $n\text{th}$ datapoint) only depends on weight $w_{ji}$ via $a_j$ we can use the chain rule to write:
>
> $\frac{\partial E_n}{\partial w_{ji}} = \frac{\partial E_n}{\partial a_j} \frac{\partial a_j}{\partial w_{ji}}$
> Since $a_j = \sum_i w_{ji} z_i$, $\frac{\partial a_j}{\partial w_{ji}}$ is easy to compute:
>
> $\frac{\partial a_j}{\partial w_{ji}} = z_i$
>
> As for $\frac{\partial E_n}{\partial a_j}$ let's just introduce some notation for now: $\delta_j \equiv \frac{\partial E_n}{\partial a_j}$
>
> $\frac{\partial E_n}{\partial w_{ji}} = \delta_j z_i$
>
> We compute the $\delta_j \equiv \frac{\partial E_n}{\partial a_j}$ _backwards_, starting with the output units.
> or example, if the error (for a single datapoint) is $E_n = \frac{1}{2} \sum_k (y_k - t_k)^2$ where $y_k = h(a_k)$ then:
>
> $\delta_k \equiv \frac{\partial E_n}{\partial a_k} = \frac{\partial E_n}{\partial y_k} \frac{\partial y_k}{\partial a_k} = (y_k - t_k) \, h'(a_k)$
>
> For the hidden units we use (a multivariable version of) the chain rule:
>
> $\delta_j \equiv \frac{\partial E_n}{\partial a_j} = \sum_k \frac{\partial E_n}{\partial a_k} \frac{\partial a_k}{\partial a_j}$
>
> "where the sum runs over all units $k$ to which unit $j$ sends connections" (Bishop). "we are making use of the fact that variations in $a_j$ give rise to variations in the error function only through variations in the variables $a_k$." (Bishop).
>
> $\delta_j \equiv \frac{\partial E_n}{\partial a_j} = \sum_k \frac{\partial E_n}{\partial a_k} \frac{\partial a_k}{\partial a_j}$
>
> can be reformulated to give the [[Backpropagation Algorithm|backpropagation formula]]:
>
> $\delta_j = h'(a_j) \sum_k w_{kj} \delta_k$

#### References
