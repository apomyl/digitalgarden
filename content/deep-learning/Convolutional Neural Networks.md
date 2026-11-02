---
publish: true
aliases:
  - Parameter sharing
  - Weight sharing
  - CNNs
created: 2026-10-27T17:36:07.989Z
modified: 2026-10-29T22:36:09.488Z
tags:
  - deeplearning
  - school
---

> [!definition]
> A [[Neural Network Architectures|neural-net architecture]] build around the idea of sharing weights between neighbouring neurons.
>
> The idea is to have a filter (of weights) that slides across the input.
>
> ```
> Input: [ 1, 2, 3, 4, 5 ]
> Filter: [ a, b, c ] ---> slide right --->
> ```
>
> This is cross-correlation:
> $(\text{Input} \star \text{Filter})(i) = \sum_j \text{Input}(j) \cdot \text{Filter}(i + j)$
> However, we use [[Convolutions]] instead, as they are commutative ($f * g = g * f$), meaning filters can be applied in any order. We just flip the filter backwards and upside down:
> $(f * w)(i) = \sum_j f(j) \, w(i - j)$

_We achieve the sliding filter by have local connectivity and shared weights, a filter doesn't actually have to slid across each time._

> [!question] Why? What issues do Fully-Connected Networks face?
>
> - Huge parameter space - the no. of parameters grows exponentially
>   - e.g. for images 224x224 pixels and RGB there are 150,528 input dimensions, for 10 outputs there will be 1,505,280 weights with a single layer.
> - Not translationally invariant
>   - e.g. for two sentences that have the same meaning but are written differently, in a FCN, multiple neurons would have to learn the same words in different positions
> - Don't treat similar inputs the same, ignores local dependencies
>   - e.g. for a repeating signal, model will relearn the same shapes for different times because it doesn't know they're the same

> [!bug] Local Connectivity & Receptive Field – how can these models see the big picture?
> Considering that every neuron is only connected to a local neighbourhood: starting from an output neuron, as you go further back, the no. of neurons it "sees" grows, this is the neuron's receptive field.
>
> We can improve their receptive field by adding more layers.
>
> ![[media/Convolutional Neural Networks-1793274413750.webp]]

> [!tldr] Convolutional Parameters
> CNNs introduce new [[Hyperparameter Tuning|Hyperparameters]]:
>
> - Padding - adding blank rows/columns on edges so data doesn't shrink
> - Stride - how much the kernel moves each step
> - Dilation - distance between elements in kernel
>   - both stride and dilation allow for larger receptive field but also down-sample features
>
> $\text{Output Size} = \left\lfloor \frac{\text{Input Size} - \text{Kernel Size} + 2 \times \text{Padding}}{\text{Stride}} \right\rfloor + 1$
> $\text{or}$
> $W_{\text{out}} = \left\lfloor \frac{W_{\text{in}} - K + 2P}{S} \right\rfloor + 1$
> hacks:
>
> - compare ratio of output input to determine stride
> - with guessed stride and padding = 0 check size, if it's equal to output padding is 0, if not padding is present

> [!question] How can we build CNNs?
>
> - [[Convolutional Neural Network Architecture Design]]
> - [[Residual Neural Networks]]

#### References

- [Goodfellow et al. (2016) – _Deep Learning_, Ch. 9: Convolutional Networks](https://www.deeplearningbook.org/contents/convnets.html)
- https://colab.research.google.com/drive/14L8F5MQWsYCVSGu3k3fLLw\_dEUVcP2tA
- [[Convolutional Neural Network Coding|Convolutional Neural Network Coding]]
