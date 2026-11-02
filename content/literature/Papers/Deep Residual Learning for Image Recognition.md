---
publish: true
aliases:
  - ResNet Paper
created: 2026-10-29T14:02:53.892Z
modified: 2026-10-29T14:27:38.170Z
tags:
  - deeplearning
  - scientific-papers
---

> [!garden] Summary
> This paper introduces [[Residual Neural Networks]] as a way to combat model degradation for deeper and deeper [[Convolutional Neural Networks]].

#### Notes

aim: ease burden of training deeper networks

as a result of CNNs models are getting deeper

- we want increasing depth as model performance improves
- at some point however it starts to degrade inexplicably

problem: At every layer we are trying to find an underlying mapping $\mathcal{H}(x)$ that is the ideal mapping, at every layer we take an input and then from scratch try formulate a new mapping
solution: Make layers fit a different residual mapping $\mathcal{F}(x)=\mathcal{H}(x)-x$ which is the difference between the output mapping and the input, this way every layer is making small adjustments to the mapping instead of remaking it from scratch every time, and if it can't make an improvement it can just return the identity and pass it onto the next layer. Original mapping is now $\mathcal{H}(x)=\mathcal{F(x)}+x$.

![[media/Deep Residual Learning for Image Recognition-1793283065412.webp]]

We add shortcut connections that perform identity mapping and their outputs are added to the outputs of the stacked layer.

_"Identity shortcut connections add neither extra parameter nor computational complexity. The entire network can still be trained end-to-end by SGD with backpropagation."_

#### References
