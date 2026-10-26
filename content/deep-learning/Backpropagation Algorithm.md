---
publish: true
created: 2026-09-24T20:58:48.975Z
modified: 2026-10-22T10:07:11.587Z
tags:
  - school
  - deeplearning
  - machinelearning
---

> [!definition] Backpropagation Algorithm
> Algorithm to efficiently calculate the [[Error Derivatives and Gradient|error gradient]] by propagating the output error backward through the layers of a [[Neural Networks|Neural Network]].
>
> Formula:
> $\delta_j = h'(a_j) \sum_k w_{kj}\delta_k$
>
> Derivation broken down here: [[Equations for Backpropagation]]

> [!question] General Idea
> Combine [[Reverse Auto Differentiation]] (calculating derivatives) with [[Gradient Descent]] (calculating adjustments for weights)

> [!list] Steps for Error Backpropagation
>
> 1. Apply an input vector $\mathbf{x}_n$ to the network and forward propagate through the network using $a_j = \sum_i w_{ji}z_i$ and $z_j = h(a_j)$ to find the activations of all the hidden and output units.
> 2. Evaluate the $\delta_k$ for all the output units using $\delta_k = y_k - t_k$.
> 3. Backpropagate the $\delta$'s using $\delta_j = h'(a_j) \sum_k w_{kj}\delta_k$ to obtain $\delta_j$ for each hidden unit in the network.
> 4. Use $\frac{\partial E_n}{\partial w_{ji}} = \delta_j z_i$ to evaluate the required derivatives.

> [!eg] Algorithm Pseudocode
> ![[Images/Backpropagation Algorithm-1790323604753.webp|292]]
>
> ![[Images/Backpropagation Algorithm-1790323621793.webp|295]]

#### References
