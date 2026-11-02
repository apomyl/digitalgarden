---
publish: true
aliases:
  - Hyperparameter
created: 2026-10-10T10:23:29.146Z
modified: 2026-10-29T15:07:00.844Z
tags:
  - machinelearning
  - school
  - deeplearning
---

> [!definition]
> A fixed parameter of a machine learning model (usually manually chosen by the designer). We can tune these to optimise training/testing loss and computational resources.
>
> Includes things such as:
>
> - learning rate
> - no. of hidden layers
> - no. of neurons, learning rate
> - mini-batch size (for [[Gradient Descent|Stochastic Gradient Descent]])
> - [[Regularisation Parameter]] $\alpha$
> - pruning parameter $\lambda$ (for [[Decision Trees]] and [[Support Vector Machines (SVMs)]])
> - etc

Methods:

- [[Random Search for Hyperparameters]]
- [[Grid Search for Hyperparameters]]
- [[Cross-validation]]
- [[Weight Freezing]]

> [!tldr] Hyperparameters
>
> - Learning Rate - most important, choosing a good initial learning rate and tuning the decay - [[AdaGrad]]/[[Adaptive Moment Estimation|Adam]]
> - Batch Size - there is an optimal that isn't the max, powers of 2 are common to fit exactly in memory
> - Initial Weights
>   - start from scratch - random weights (uniform or normal distribution)
>   - fine-tuning - initialising from pre-trained weights (previous model)

#### References

- [[Hyperparameter Tuning Lab]]
