---
publish: true
created: 2026-09-30T13:02:55.080Z
modified: 2026-10-29T14:24:12.072Z
tags:
  - school
  - machinelearning
  - deeplearning
---

> [!definition] Residual Network
> A [[Neural Network Architectures|neural-net architecture]] that adds shortcut connections between layers, passing the input of the previous layer and combining it with the output of the current layer.

> [!question] Use
> As a result of [[Convolutional Neural Networks]], deeper networks were vital to improving performance, however, deeper networks struggled with [[Vanishing Gradient Problem]]/[[Exploding Gradient Problem]] and degradation – models inexplicably performed worse with more depth.

> [!tldr] How does it work?
> In a traditional deep network, stacked layers try to learn the complete desired mapping $\mathcal{H}(x)$ directly from scratch at every step.
>
> The idea of Res-Net is to introduce shortcut connections that perform [[Identity Function|identity]] mapping to connect the input and output of a layer.
>
> We use these in combination to try fit a new mapping $\mathcal{F}(x)=\mathcal{H}(x)-x$ which is the residual (difference) between the output and the input.
> The original mapping $\mathcal{H}(x)$ is recast into $\mathcal{F}(x)+x$.
>
> This way, each layer is making incremental changes instead of starting from scratch, and if no improvement can be made, it will return the identity, so no degradation will occur.
>
> ![[media/Deep Residual Learning for Image Recognition-1793283065412.webp]]

#### References

- https://www.geeksforgeeks.org/deep-learning/residual-networks-resnet-deep-learning/
- [[Deep Residual Learning for Image Recognition]] – He et al.
