---
publish: true
created: 2026-10-23T11:01:39.593Z
modified: 2026-10-29T10:58:36.352Z
tags:
  - deeplearning
  - school
---

> [!definition]
> A [[Regularisation Techniques|Regularisation]] technique applied on the dataset before training. We aim to increase the size of our dataset by augmenting it with different transformations, turning 1 image into multiple variants.

> [!tldr] Methods
> We can apply many different image transformations to our image **as long as the label isn't changed**:
>
> - Flip
> - Crop
> - Rotate
> - Change brightness
> - Add random noise
> - Add occlusion (cutout)
> - Change colour
> - etc
>
> Special techniques that change the label:
>
> - [[Mixup]]
> - [[Cutmix]]

![[media/Data Augmentation-1793271038576.webp|700]]

![[media/Data Augmentation-1793271077335.webp]]

#### References
