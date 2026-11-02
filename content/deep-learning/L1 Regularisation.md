---
publish: true
created: 2026-10-28T16:30:32.614Z
modified: 2026-10-28T16:34:30.130Z
tags:
  - deeplearning
  - school
---

> [!definition] L1 Regularisation
> [[Regularisation Techniques|Regularisation technique]] that shrinks weights toward zero at each training step to prevent [[Underfitting vs Overfitting|Overfitting]], driving unimportant weights to **exactly zero** (sparsity).
>
> Adds $\lambda \|\mathbf{w}\|_1$ to [[Cost Functions]]
>
> - $\|\mathbf{w}\|_1 = \sum |w_i|$
>   - ([[Manhattan Distance]] / sum of absolute values)
>   - derivative is $\text{sign}(\mathbf{w})$, shrinking weights by a constant amount (no $\frac{1}{2}$ needed)

[[Regularisation Parameter]] - $\lambda$ and $\alpha$ both used, important [[Hyperparameter Tuning|hyperparameter]]

#### References
