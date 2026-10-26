---
publish: true
aliases:
  - Loss functions
created: 2026-09-23T16:40:38.912Z
modified: 2026-10-23T11:18:47.735Z
tags:
  - school
  - deeplearning
---

> [!definition] Cost (Loss) Function
> Measure of the difference between actual and predicted values used to understand how well a model is performing.
> e.g. [[Least Squares]] is a cost function that uses [[Mean Squared Error]]

> [!eg] [[Probabilistic vs Deterministic|Probabilistic]] error
> The error for a probability is the [[Negative Log Likelihood]]

**Idea:** Given a set $\mathbf{X}$ of input vectors $\mathbf{x}$ of one or more variables and a parameterisation $\mathbf{w}$, a Cost Function is a map $J$ onto a real number representing a cost or loss associated with the input configurations.\
(Negatively related to 'goodness of fit'.)

**Expected Loss:**
$J(\mathrm{X}; \mathrm{w}) = \mathbb{E}_{(\mathrm{x}, f^*(\mathrm{x})) \sim p} L(f(\mathrm{x}; \mathrm{w}), f^*(\mathrm{x}))$

**Empirical Risk:**
$J(\mathrm{X}; \mathrm{w}) = \frac{1}{|\mathrm{X}|} \sum_{\mathrm{x} \in \mathrm{X}} L(f(\mathrm{x}; \mathrm{w}), f^*(\mathrm{x}))$

Expected loss is the "true" distribution based on all possible inputs and outputs, this can't be done in practice.
Empirical risk is based on a sample (observed dataset).

![[Images/Cost Functions-1790182294929.webp|376]]

We can minimise the cost function with [[Optimisation Techniques]]

> [!tldr] Examples
>
> - [[Mean Squared Error]]
> - [[Soft-Max]]
> - [[Cross-Entropy]]

#### References

- https://www.geeksforgeeks.org/machine-learning/what-is-the-cost-function-in-linear-regression/
