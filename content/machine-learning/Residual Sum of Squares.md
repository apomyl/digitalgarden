---
publish: true
aliases:
  - RSS
created: 2026-09-23T10:29:13.529Z
modified: 2026-09-25T11:53:20.494Z
tags:
  - maths
  - school
  - machinelearning
---

> [!definition] RSS
> A statistical measure of the sum of squared residuals (the difference between an estimation and the true value) used to "score" estimation models.

$R(a_0, a_1) = \sum_{n=1}^N \Big(y_n - (a_0 + a_1 x_n)\Big)^2$

Parameter vector $\theta = (a_0, a_1)$
For any $\theta$ which defines a **linear function**:
$\frac{∂R}{∂θ} = −2X^T (y − Xθ)$
(side note: $X\theta$ is equivalent to $y=a_0 +a_1x$, in order to do this $\mathbf{X} = \begin{bmatrix} 1 & x_1 \\ 1 & x_2 \\ \vdots & \vdots \\ 1 & x_N \end{bmatrix}$)

If you plot the total error $R$ against all possible combinations of parameters it forms a smooth 3d bowl.
![[Images/Residual Sum of Squares-1790159992263.webp|199]]
We use the derivative to find the minimum error where parameters are optimal:
$\frac{∂R}{∂θ} = 0$
The optimal parameters $\hat\theta$ can be expressed by the equation:
$\hat\theta = (X^TX)^{-1}X^Ty$
This is the [[Least Squares]] solution.

![[Images/Residual Sum of Squares-1790160757991.webp|449]]

#### References

- https://en.wikipedia.org/wiki/Residual\_sum\_of\_squares
- https://uob-coms30035.github.io/lectures/lect04/lect04.pdf
