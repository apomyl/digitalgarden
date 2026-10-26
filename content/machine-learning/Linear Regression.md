---
publish: true
created: 2026-09-23T10:57:28.955Z
modified: 2026-10-03T10:55:24.442Z
tags:
  - machinelearning
  - school
---

> [!definition] [[Regression]]
> A statistical method used to model and analyse the relationship between a dependent output variable and one (Linear) or more independent input variables.

To find the best-fit line for linear regression, we use the [[Least Squares]] formula.

> [!eg] Practice Example
> https://colab.research.google.com/drive/1IDAS4-WdktghX8tYK0xcYMShrAh4Ytoe#scrollTo=TiR9wtjxQUq
>
> ```python
> import numpy as np
>
> # Generate our dataset, random sample of linear equation with noise
> x = np.sort(np.random.sample((200,1)))*10
> y = (6 * x) + 7 + np.random.normal(0, 5, (200, 1))
>
> # Pre-processing - add bias as ones to matrix of x
> ones = np.ones((200, 1))
> x_bias = np.concatenate((x, ones), axis=1)
>
> # Use Ordinary Least Squares to calculate line of best fit
> y_pred = np.linalg.inv((np.transpose(x_bias) @ x_bias)) @ (np.transpose(x_bias) @ y)
>
> print(f"a: {y_pred[0][0]}")
> print(f"b: {y_pred[1][0]}")
> ```

#### References
