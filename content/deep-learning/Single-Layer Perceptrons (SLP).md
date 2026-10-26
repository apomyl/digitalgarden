---
publish: true
aliases:
  - Perceptrons
  - Hidden Units
created: 2026-09-23T16:10:30.932Z
modified: 2026-10-23T10:15:00.501Z
tags:
  - school
  - deeplearning
  - machinelearning
---

> [!definition] Basic Perceptron
> A perceptron is a single computational unit inspired by neurons, used to build neural networks.
>
> 1. It takes multiple inputs and assigns weights.
> 2. It computes a weighted sum.
> 3. It applies a threshold ([[Activation Functions|activation function]] ([[Step Functions]])).
> 4. Outputs either 0 or 1 based on weight sum and threshold.
>
> ![[Images/Single-Layer Perceptrons (SLP)-1790180101530.webp]]
>
> Therefore, the basic perceptron defines a hyperplane $\mathbf{w}^T\mathbf{x}$ in $\mathbf{x}$-state space that [[Linear Separability|linearly separates]] two regions of that space. Corresponding to a two-class linear [[Classification|classification]].

> [!definition] Hidden Units
> Actual neural network units are different as they use a continuous activation function like [[Sigmoid]].
>
> They are "hidden" because they act internally.

##### Basic Perceptron ([[Supervised learning|Supervised]]) Learning Rule

Idea: whenever the system produces a misclassification with current weights, adjust weights by $\Delta$w towards a better performing weight vector.

$\underbrace{\Delta \mathbf{w}}_{\textit{update}} = \begin{cases} \eta \, f^*(x) \, x & \textit{if} \quad \overbrace{f^*(x)}^{\textit{ground truth}} \neq \overbrace{f(x)}^{\textit{actual output}} \\ 0 & \textit{otherwise} \end{cases}$

where $\eta$ is the learning rate.

###### Training Cycle

![[Images/Single-Layer Perceptrons (SLP)-1790181591257.webp|408]]

The **weights** don't have to be something scary, thinking of each neuron as detecting a specific feature or some abstraction of the overall data, then the pixels we care about for that feature would be more heavily weighted than the rest. If we care about detecting an edge then maybe the positive weights will be surrounded by negative weights for the areas we want empty.
e.g. Weights on the left, data on the right
![[Images/Single-Layer Perceptrons (SLP)-1790186574573.webp|344]]
![[Images/Single-Layer Perceptrons (SLP)-1790186690788.webp|349]]

##### Course-specific notational details

Weighted sum $s = \sum_i w_i x_i=\mathbf{w}^T \mathbf{x}$
Activation function $g$
Unit output $y = g(\mathbf{w}^T \mathbf{x}) = f(x)$
$y=f(x) \equiv f(\mathbf{x} ; \mathbf{w})$ where the semicolon separates input from parameters

_Italic font refers to scalars_.
A minor letter in non-italic font refers to a vector.
A capital letter in non-italic font would refer to a matrix or vector set.

**Bias** is a value for when we want to skew results to better match the "real" scenario. Bias is incorporated within our parameter vector.

![[Images/Single-Layer Perceptrons (SLP)-1790180147476.webp]]

#### References

- https://www.geeksforgeeks.org/deep-learning/what-is-perceptron-the-simplest-artificial-neural-network/
- https://www.youtube.com/watch?v=aircAruvnKk\&list=PLZHQObOWTQDNU6R1\_67000Dx\_ZCJB-3pi\&index=1
