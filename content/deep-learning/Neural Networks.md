---
publish: true
created: 2026-09-24T21:12:14.076Z
modified: 2026-10-23T11:02:01.496Z
tags:
  - school
  - deeplearning
---

> [!definition] Multi-Layer Neural Network
> A computational model made up of multiple layers of artificial neurons (hidden units), based on [[Single-Layer Perceptrons (SLP)|Perceptrons]]. They take an input and compute an output based on learnt weights, this could be for problems like [[Regression]] or [[Classification]].
>
> ![[Images/Multi-Layer Perceptrons (MLP)-1790583544791.webp|345x307]]

> [!error] Difference between perceptrons and hidden units
> In real neural network hidden units we use continuous [[Sigmoid|sigmoidal]] or [[Rectifying Linear Unit|ReLU]] nonlinearities whereas the perceptron uses [[Step Functions|step-function]] nonlinearites.
>
> This is because the step functions can't be differentiated at the "steps".

> [!eg] Recipe
>
> 1. Prepare data ([[Data Augmentation]], [[Feature Scaling|Data Normalisation]])
> 2. Define [[Neural Network Architectures|architecture]]
> 3. Define [[Cost Functions|cost function]]
> 4. Compute gradients using [[Backpropagation Algorithm]]
> 5. [[Optimisation Techniques|Optimise]] weights

> [!question] What can we represent?
> With 1 hidden layer:
>
> - Boolean functions
> - Any continuous functions
>
> With 2 hidden layers:
>
> - Any mathematical function

#### References

- [[MLPClassifier (scikit-learn)]]
