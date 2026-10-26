---
publish: true
aliases:
  - Widrow-Hoff learning rule
  - Adaline rule
created: 2026-09-24T09:38:39.966Z
modified: 2026-10-25T13:54:19.809Z
tags:
  - school
  - deeplearning
---

> [!definition] Delta Rule
> How to update weights based on the "blame" assigned to each input.
>
> $\Delta \mathbf{w} = -\eta \nabla J(\mathrm{X}; \mathbf{w})$

> [!tldr] Break down of equation
> For a single weight $w_k$:
> $\Delta w_k = -\eta \, x_k \left( \mathbf{w}^\mathrm{T} \mathbf{x} - f^*(\mathbf{x}) \right)$
> $\Delta \mathbf{w} = -\eta \, \mathbf{x} \underbrace{\left( \mathbf{w}^\mathrm{T} \mathbf{x} - f^*(\mathbf{x}) \right)}_{\delta \text{ is the error derivative}}$
> $\Delta \mathbf{w} = -\eta \, \mathbf{x} \, \delta$
>
> - $\delta = \mathbf{w}^T \mathbf{x} - f^*(\mathbf{x}) = (\text{Your Prediction} - \text{The True Target})$
>   - the error derivative for [[Mean Squared Error|MSE]]
> - $-\eta$ - learning rate
>   - negative so you move in opposite direction of error
> - $\mathbf{x}$ - the blame assigned to each input

> [!question] How does it relate to [[Gradient Descent]]
> It is GD at its simplest, applied to a single linear unit using a [[Mean Squared Error|MSE]] [[Cost Functions|cost function]].

#### References

- [[Error Derivatives and Gradient]]
