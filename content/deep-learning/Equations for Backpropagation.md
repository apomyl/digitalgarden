---
publish: true
created: 2026-09-28T16:15:59.569Z
modified: 2026-09-29T09:03:14.661Z
tags:
  - school
  - machinelearning
  - deeplearning
---

#### The Forward Pass

Work forwards with input to make a prediction output.

###### Activation / Weighted Sum

$a_j = \sum_i w_{ji}z_i$

- **$a_j$**: weighted sum (activation) for the current unit $j$
- **$w_{ji}$**: weight parameter on the connection from the previous unit $i$ to our current unit $j$
- **$z_i$**: input data coming from unit $i$
- **$\sum_i$**: sum
- _Purpose:_ Combines all input parameters into one value

###### Transformation / Activation function

$z_j = h(a_j)$

- **$z_j$**: final transformed output of unit $j$
- **$h(\cdot)$**: nonlinear [[Activation Functions|activation function]]
- _Purpose:_ applies nonlinear curve to raw sum, allowing network to model complex patterns instead of just linear ones

#### Calculate total error and error signal of each unit

Calculate total error then work backwards to assign blame to individual units.

$\delta_j \equiv \frac{\partial E_n}{\partial a_j}$

- **$\delta_j$**: "error signal", "blame score" for unit $j$
  - Use a [[Partial Derivatives|partial derivative]] to calculate how much impact $j$ has on the total error
- **$E_n$**: total error on a specific data point $n$ calculated by [[Cost Functions]]
- _Purpose:_ defines how much will the error be affected from changing unit $j$.

#### Backwards [[Chain Rule]] to get the $\delta_j$ of hidden middle layers

To find the $\delta_j$ of a hidden unit we need to look at the units it sends it's information forward to since it doesn't touch the output directly.

$\delta_j = \sum_k \frac{\partial E_n}{\partial a_k} \frac{\partial a_k}{\partial a_j}$

- **$k$**: units in next layer forward that receive data from unit $j$
- **$\frac{\partial E_n}{\partial a_k}$**: error signal of those future units (which is simply $\delta_k$)
- **$\frac{\partial a_k}{\partial a_j}$**: how much a change in unit $j$ affects weighted sum of next unit $k$
- _Purpose_: using [[Chain Rule|chain rule]] principles to "pass blame" backwards, so error of unit $j$ is the sum of the error of all the units it connects to $k$, scaled by how strongly $j$ influences $k$

#### [[Backpropagation Algorithm|Backpropagation]] Equation

How do we actually solve $\frac{\partial a_k}{\partial a_j}$?
Because $a_k = \sum_j w_{kj}z_j$ then it becomes $\frac{\partial }{\partial a_j}w_{kj}z_j$, summation disappears because we only care about $a_j$ and all other unit activations go away.
Because $z_j = h(a_j)$, $\frac{\partial z_j}{\partial a_j} = h'(a_j)$ then it becomes $\frac{\partial a_k}{\partial a_j} = w_{kj} h'(a_j)$

Substitute that into $\delta_j$ equation above to get: $\sum_k \delta_k (w_{kj} h'(a_j))$
We can take $h'(a_j)$ out of the summation, since it doesn't change depending on k, to get the final formula:

$\delta_j = h'(a_j) \sum_k w_{kj}\delta_k$

#### References

- [[Bishop - Machine Learning]]
