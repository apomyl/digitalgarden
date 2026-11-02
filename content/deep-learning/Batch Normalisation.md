---
publish: true
created: 2026-10-29T14:48:29.478Z
modified: 2026-10-29T19:04:50.152Z
tags:
  - deeplearning
  - school
---

> [!definition]
> Using [[Feature Scaling|normalisation]] to reduce [[Internal Covariate Shift]] in order to improve model performance.

> [!tldr] Equation
> For each dimension/channel $i$ across a mini-batch $\mathcal{B}$:
> $\hat{x}_i = \frac{x_i - \bar{x}_i}{\sigma_i + \epsilon}$
>
> - mini-batch mean $\bar{x}_i$: $\frac{1}{m}\sum^m_{j=1}x_{i,j}$
> - mini-batch standard deviation $\sigma_{i}$: $\sqrt{ \frac{1}{m}\sum^m_{j=1}(x_{i,j}-\bar{x}_{i})^2 }$
> - tiny constant to prevent division by 0 $\epsilon$
>
> Forcing mean $0$ and variance $1$ arbitrarily restricts what the layer can represent (for example, it would force inputs into the linear regime of a sigmoid).
>
> $\gamma$ (scale) and $\beta$ (shift) allow the network to learn to undo or scale the normalisation if the identity mapping or a shifted distribution is optimal.
> $y = \gamma \hat{x} + \beta$

![[media/Batch Normalisation-1793299712890.webp|392]]

> [!bug] Testing Problems
>
> - Batch normalisation requires a group of samples but you usually only test with one item so $\mathcal{B}=1$ and you can't calculate the standard deviation for it.
> - Predictions must be deterministic, if I upload 1 picture of a dog and 99 of cats that 1 picture should still be classified as a dog, not a cat just because the mean of the batch is cat.
>
> Solution: during training, keep a running average of the mean and standard deviation which is frozen when training stops and used during testing

#### References

- [[Batch Normalization Accelerating Deep Network Training by Reducing Internal Covariate Shift]]
