---
publish: true
created: 2026-10-29T18:04:32.932Z
modified: 2026-10-29T18:34:10.124Z
tags:
  - deeplearning
  - scientific-papers
---

> [!garden] Summary

#### Notes

aim: reduce [[Internal Covariate Shift]]

- "the distribution of each layer’s inputs changes during training, as the parameters of the previous layers change."

- this slows down training by requiring lower learning rates and careful parameter initialisation

- [[Feature Scaling|Data Normalisation]] / [[Batch Normalisation]] - solution
  - acts as a regulariser, sometimes eliminating the need for dropout

- Normalisation can't be done outside of training because it will cancel out the model's changes

#### References
