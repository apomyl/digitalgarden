---
publish: true
aliases:
  - Lagrange Multiplier
created: 2026-10-11T10:36:49.077Z
modified: 2026-10-11T10:56:52.638Z
tags:
  - machinelearning
  - school
---

> [!definition] Dual Parameters
> A method to score how much each training input affects the output.
> The parameters optimised in [[Support Vector Machines (SVMs)]] to enforce constraints such as no data points on the wrong side of the boundary.
>
> - attach penalty factor Lagrange Multiplier ($a_n$) to each constraint

Every training point ($x_n$) is assigned a dual parameter $a_n \geq 0$

- if $a_n=0$ - point is outside margin, ignored by model
- if $a_n > 0$ - point is a support vector, shapes decision boundary

#### References
