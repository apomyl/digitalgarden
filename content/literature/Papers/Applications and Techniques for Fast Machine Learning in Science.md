---
publish: true
created: 2026-11-01T18:05:04.829Z
modified: 2026-11-01T18:41:05.872Z
tags:
  - scientific-papers
  - machinelearning
  - ai-research
---

> [!garden] Summary
> A community review report by a collection of experts who are part of the Fast ML for Science community.
>
> Breaks down:
>
> - applications for fast ML such as at CERN
> - techniques for training and implementation
> - architectures, technologies and platforms for deployment

#### Notes

goal: "accelerating and improving data processing and real-time decision-making"

- ML models take too long to compute to be useful in settings such as data analysis at the Large Hadron Collider

- "we refer to the concept of Fast Machine Learning in Science as the integration of ML into the experimental data processing infrastructure to enable and accelerate scientific discovery."

- ML used at CERN LHC in detector gates, to sort through and detect rare collision events

- techniques for fast ML:
  - hardware integration - building with the hardware in mind
    - using `hls4ml` to convert models into hardware logic gates
  - quantisation (extreme model compression)
  - pruning and structural sparsity
  - pre-computed lookup tables for mathematical operations (non-linear activation functions or trigonometry)
  - knowledge distillation - massive, slow neural network teaches smaller, faster one to mimic its outputs

#### References
