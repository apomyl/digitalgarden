---
publish: true
aliases:
  - Maximum-margin Classifier
created: 2026-10-11T10:10:56.895Z
modified: 2026-10-11T10:36:48.628Z
tags:
  - machinelearning
  - school
---

> [!definition] SVMs
> [[Supervised learning|Supervised]] (non-linear) machine learning model, finding an optimal hyperplane to split the data.
>
> - What's optimal? Max-margin, no error
>   - Enforcing constraints - [[Dual Parameters]]

> [!definition] Support Vectors
> Data points closest to the hyperplane

> [!eg] Finding (Hard) Max-Margin
> Equation of Hyperplane - $\mathbf{w}^T\mathbf{x} - b=0$
> Total Margin - $2 / ||\mathbf{w}||$
>
> ```plaintext
> Class +1  (+1)
>                     (+1)        (+1) [Support Vector]
> =====================================================  w^T x - b =  1  (Positive margin boundary)
>                  .           ^
>                  .           |  Distance = 1 / ||w||
>                  .           v
> - - - - - - - - - - - - - - - - - - - - - - - - - - -  w^T x - b =  0  (Decision boundary)
>                  .        ^
>                  .        |  Distance = 1 / ||w||   Total Margin = 2/||w||
>                  .        v
> =====================================================  w^T x - b = -1  (Negative margin boundary)
>            (-1) [Support Vector]
>    (-1)             (-1)
>               Class -1
> ```

#### References

- https://www.youtube.com/watch?v=ny1iZ5A8ilA
