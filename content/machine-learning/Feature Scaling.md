---
publish: true
aliases:
  - Data Normalisation
created: 2026-10-08T10:51:47.164Z
modified: 2026-10-08T11:14:28.746Z
tags:
  - school
  - machinelearning
---

> [!definition] Feature Scaling
> Pre-processing step in machine learning, adjusting input data so it's on the same scale.
> e.g. If we have a dataset of occupant age (0-100) and house price (50,000-1,000,000) they differ massively so we want to normalise them.

> [!question] Why normalise something like colour from 0-255 to 0-1?
> Helps our weighted sum not explode beyond measure since we're multiplying all inputs with weights and summing them.
> Helps with sigmoid function being flat at extreme values, at 4000+ sigmoid returns 0.9999999.
> See [[Vanishing Gradient Problem]] and [[Exploding Gradient Problem]]

#### References

- https://en.wikipedia.org/wiki/Feature\_scaling
