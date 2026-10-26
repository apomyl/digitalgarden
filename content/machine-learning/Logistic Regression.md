---
publish: true
created: 2026-10-08T11:23:21.783Z
modified: 2026-10-08T12:25:29.239Z
tags:
  - school
  - machinelearning
---

> [!definition] Logistic Regression
> [[Supervised learning]] algorithm for classification that predicts the probability of each outcome.

> [!vs] Binary vs Categorical
> For binary classification we used the [[Sigmoid]] function and for categorical (more than two) we use [[Soft-Max]] function.

![[Images/Logistic Regression-1791459836420.webp]]

#### Coding Example

```python
clf = LogisticRegression(max_iter=1000) # Initialise Model

clf.fit(train_x.T, train_y.flatten()) # Train model using .fit()

train_acc = clf.score(train_x.T, train_y.flatten()) * 100
test_acc = clf.score(test_x.T, test_y.flatten()) * 100

print(f"Training accuracy: {train_acc:.2f}%") # 100%
print(f"Test accuracy: {test_acc:.2f}%") # 72%
```

#### References
