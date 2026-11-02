---
publish: true
created: 2026-10-29T19:10:55.208Z
modified: 2026-10-29T19:14:09.080Z
tags:
  - deeplearning
  - school
---

> [!definition]
> Newton's method uses second derivatives (the **Hessian matrix** $\mathbf{H}$) to account for curvature:
>
> $\mathbf{W}_{t+1} = \mathbf{W}_t - \mathbf{H}(J(\mathbf{W}_t))^{-1} \nabla J(\mathbf{W}_t)$
>
> where $H_{ij} = \frac{\partial^2 J}{\partial w_i \partial w_j}$

Bad because Hessian matrix too big - see [[Hessian-Free Method]]
Attracted to [[Saddle Points]]

#### References
