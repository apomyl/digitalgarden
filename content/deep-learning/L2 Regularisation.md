---
publish: true
aliases:
  - Weight Decay
created: 2026-09-30T13:17:38.227Z
modified: 2026-10-28T16:29:56.947Z
tags:
  - school
  - machinelearning
  - deeplearning
---

> [!definition] Weight Decay
> [[Regularisation Techniques|Regularisation technique]] that shrinks large weights toward zero at each training step to prevent [[Underfitting vs Overfitting|Overfitting]].
>
> Adds $\lambda\textbf{w}^T\textbf{w}$ to [[Cost Functions]]
>
> - $\textbf{w}^T\textbf{w} \equiv ||\textbf{w}||^2_2$
>   - (square of [[Euclidean Norm|2-Norm]])
>   - can be $\frac{1}{2}$ to make differentiation easier

[[Regularisation Parameter]] - $\lambda$ and $\alpha$ both used, important [[Hyperparameter Tuning|hyperparameter]]

#### References
