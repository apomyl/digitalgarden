---
publish: true
created: 2026-10-23T11:39:44.032Z
modified: 2026-10-24T13:56:24.460Z
tags:
  - deeplearning
  - school
---

> [!definition]
> A [[Cost Functions|cost function]] for the purpose of turning outputs into probabilities, to do this we need outputs to be within 0 and 1 and sum to 1.
>
> $\text{softmax}(z_i) = \frac{e^{z_i}}{\sum_{j=1}^{K} e^{z_j}}$

![[media/Soft-Max-1792850152582.webp|319]]
Use exponential to give higher values more weight in the probability distribution.

#### References

- https://www.youtube.com/watch?v=oJU6-qW6xZU
