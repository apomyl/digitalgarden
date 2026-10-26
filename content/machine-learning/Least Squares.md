---
publish: true
aliases:
  - Ordinary Least Squares
created: 2026-09-23T14:21:28.786Z
modified: 2026-10-03T10:53:58.909Z
tags:
  - maths
  - school
---

> [!definition] Least Squares
> Method to find the line or curve of best fit for a set of data points by minimising the sum of the squared differences (residuals) between actual and predicted values.

###### Method:

1. Choose model form (linear, curve, etc)
2. Calculate residuals
3. Square each residual and sum them up
4. Minimise sum using calculus

> [!definition] Ordinary Least Squares
> One-time calculation to find the line of best fit
> $\hat{\beta} = (X^T X)^{-1} X^T y$
> $\hat{\beta}_1 = \frac{\sum_{i=1}^n (x_i - \bar{x})(y_i - \bar{y})}{\sum_{i=1}^n (x_i - \bar{x})^2}$

#### References

- [[Least Squares Estimation (Linear Regression)]]
- https://www.geeksforgeeks.org/maths/least-square-method/
