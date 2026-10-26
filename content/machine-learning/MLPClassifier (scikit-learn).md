---
publish: true
created: 2026-10-10T09:10:48.339Z
modified: 2026-10-25T15:45:50.033Z
tags:
  - machinelearning
  - sklearn
---

Coding [[Neural Networks]] with one hidden layer:

- calculated weighted sum of input
- pass through non-linear activation function ([[Rectifying Linear Unit|ReLU]])
- use optimisation technique ([[Adaptive Moment Estimation]], [[Gradient Descent|Stochastic Gradient Descent]])
- pass through final activation function ([[Sigmoid]])

Example

```python
clf = MLPClassifier(
    hidden_layer_sizes = (64, ),
    activation = 'relu',
    solver = 'sgd',
    learning_rate_init = 0.001,
    alpha = 0,
    max_iter = 2000,
    n_iter_no_change=50
)

clf.fit(train_x.T, train_y.flatten())

plt.plot(clf.loss_curve_)
plt.show()
```

#### References

- https://scikit-learn.org/stable/modules/generated/sklearn.neural\_network.MLPClassifier.html#sklearn.neural\_network.MLPClassifier
