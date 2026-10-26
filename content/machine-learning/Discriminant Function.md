---
publish: true
aliases:
  - Linear Discriminant
  - Linear Discriminant Analysis
created: 2026-09-23T13:51:42.136Z
modified: 2026-10-10T10:31:35.313Z
tags:
  - ai
  - maths
  - school
  - machinelearning
---

> [!definition] Discriminant Function
> A formula to assign a data point to a class.

> [!definition] Linear Discriminant Function
> Has a linear combination of input features
> e.g.
> $y(x) = w_0 + \textbf{w}^Tx$
>
> - $x$ is the input vector
> - $w_0$ is a scalar, called _bias_
> - $\textbf{w}$ is our vector of parameters, called _weights_
>
> For K = 2, an input $x$ is assigned to class $C_1$ if $y(x) \geq 0$ and class $C_2$ otherwise.
> We assume the data from each class has a multivariate [[Gaussian Distribution]] whose mean is class-specific but where the covariance matrix for each class is the same.
> Use [[Maximum Likelihood Estimation|MLE]] to find parameters for each of these Gaussians and finally use [[Bayes' Theorem]] to assign classes.

#### References

- https://www.geeksforgeeks.org/machine-learning/ml-linear-discriminant-analysis/
