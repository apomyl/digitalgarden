---
publish: true
created: 2026-10-28T17:08:07.151Z
modified: 2026-10-28T17:49:12.958Z
tags:
  - deeplearning
  - scientific-papers
---

> [!garden] Summary

#### Notes

Regularisation technique to prevent overfitting and improve generalisation, thin network randomly by dropping neurons every epoch. This forces the network to generalise by combining and taking the average of multiple different architectures.

![[media/Dropout A Simple Way to Prevent Neural Networks from Overfitting-1793207858597.webp]]

Simplest format, neurons dropped with probability $p$

During testing all neurons are present and weights are multiplied by $p$

> [!quote]
> "Applying dropout to a neural network amounts to sampling a “thinned” network from it. The thinned network consists of all the units that survived dropout (Figure 1b). A neural net with n units, can be seen as a collection of $2^n$ possible thinned neural networks. These networks all share weights so that the total number of parameters is still $O(n^2)$, or less. For each presentation of each training case, a new thinned network is sampled and trained. So training a neural network with dropout can be seen as training a collection of $2^n$ thinned networks with extensive [[Convolutional Neural Networks|Weight sharing]], where each thinned network gets trained very rarely, if at all."

skipped

- technical implementation
- test results + comparison
- used for other architectures not just feed-forward

#### References
