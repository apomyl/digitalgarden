---
publish: true
created: 2026-10-08T10:49:55.775Z
modified: 2026-10-08T11:16:36.367Z
tags:
  - school
  - machinelearning
---

> [!definition] Min-Max
> A [[Feature Scaling]] technique to shift and scale data so it fits into a specific range, usually 0 to 1.

$x' = \frac{x - \min(x)}{\max(x) - \min(x)}$

e.g. for images with RGB value 0-255 all we have to do is divide by 255 which is the max.

#### References
