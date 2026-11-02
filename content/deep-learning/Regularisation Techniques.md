---
publish: true
aliases:
  - Regularisation
created: 2026-09-30T13:23:35.816Z
modified: 2026-10-29T14:27:38.162Z
tags:
  - school
  - machinelearning
  - deeplearning
---

> [!definition] Regularisation
> Techniques to reduce [[Generalisation]] error without hurting training. This page breaks down different approaches

> [!tldr] via Parameter Norm Penalties
> Some approaches are based on introducing a parameter norm penalty $\Omega (\theta)$ to the objective function $J$, with the goal of penalising large weights to prevent [[Underfitting vs Overfitting|Overfitting]]:
> $\tilde{J}(\theta; X, y) = J(θ; X, y) + αΩ(θ)$
> where $\alpha \in [0, \infty)$ is the [[Regularisation Parameter]] that weighs the relative contribution of the norm penalty term.
>
> Different norm methods:
>
> - [[L1 Regularisation]]
> - [[L2 Regularisation|L2 Regularisation]]
>
> _Biases are left of parameter penalty methods because they control only 1 variable and penalising them induces [[Underfitting vs Overfitting|Underfitting]]_

> [!tldr] via Data Pre-processing
> Intervening at the inputs before they enter the network.

he best method for preventing overfitting is to have more data. We can augment our data to increase the size and variance of our dataset.

> - [[Data Augmentation]]
> - [[Input Noise Injection]]

> [!tldr] via Network Architecture
> Intervening in the structure, connections, and unit operations of the model.
>
> - [[Dropout]]
> - [[DropConnect]]
> - [[Convolutional Neural Networks|Parameter sharing]]
> - [[Residual Neural Networks]]

> [!tldr] via the Optimization Procedure
> Intervening in how parameters are updated and when training stops
>
> - [[Early Stopping]]
> - [['Pocket' Algorithm]]
> - [[Model Ensembling]] (Bagging)

> [!tldr] via Loss / Output Targets
> Intervening in the error formulation and target representation
>
> - [[Soft-Max]]
> - [[Cross-Entropy]]

#### References

- Deep Learning Book Chapter 7 - Goodfellow et al.
