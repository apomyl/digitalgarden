---
publish: true
created: 2026-10-25T13:25:32.513Z
modified: 2026-10-25T15:45:05.164Z
tags:
  - deeplearning
  - school
  - scientific-papers
---

> [!garden] Summary
> Provides an overview for [[Optimisation Techniques]], different variants of [[Gradient Descent]] and summarises challenges.

#### Notes

three types of gradient descent

- batch, stochastic, mini-batch
  momentum + NAG
- accelerate gradient by letting it accumulate
-

adagrad - adapt learning rates by making the learning rate for large features smaller
rmsprop - seeks to reduce adagrad's aggressive, monotonically decreasing learning rate

- adagrad gradient sum only ever grows, eventually learning rate approaches 0
- rmsprop approach - only remember recent history, not entire history

#### References
