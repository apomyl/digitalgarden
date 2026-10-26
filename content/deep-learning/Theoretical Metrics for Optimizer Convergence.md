---
publish: true
created: 2026-10-25T12:37:29.245Z
modified: 2026-10-25T12:52:51.775Z
tags:
  - deeplearning
---

> [!definition]
> There are two frameworks we could use to comparte [[Optimisation Techniques]]' convergence, how fast they reach the minimum.

> [!garden] Terrain Difficulty $R$
> Given the _condition number_ of the curvature at the minimum $R$ and momentum $\mu$:
> $R=\frac{\text{Steepness of canyon walls}}{\text{Steepness of canyon floors}}$
> $\mu=\frac{(\sqrt{ R }-1)}{(\sqrt{ R }+1)}$
> _(if R=1, it's a perfectly round bowl, if R=100, walls are 100$\times$) steeper_

> [!garden] Time $T$
> Set a time T and compare the remaining error, so for an algorithm with $O(1/T)$ it means that the remaining error is $\leq \frac{1}{T}$.

| **Optimization Method**                         | **Error after TTT steps (General Smooth Convex)** | **Iterations needed to reach error ϵ\epsilonϵ (Canyon / Strongly Convex)** |
| ----------------------------------------------- | ------------------------------------------------- | -------------------------------------------------------------------------- |
| [[Gradient Descent\|Standard Gradient Descent]] | $O\left(\frac{1}{T}\right)$                       | $O\left(R \ln \frac{1}{\epsilon}\right)$                                   |
| [[Classical Momentum]]                          | $O\left(\frac{1}{T}\right)$                       | $O\left(\sqrt{R} \ln \frac{1}{\epsilon}\right)$                            |
| [[Nesterov Accelerated Gradient]]               | $O\left(\frac{1}{T^2}\right)$                     | $O\left(\sqrt{R} \ln \frac{1}{\epsilon}\right)$                            |

#### References

- [[On the importance of initialization and momentum in deep learning]]
