## Notes

standard (explicit feature) approach vs kernel approach
Standard

- focuses on transforming individual data points
- explicitly calculating a set of features $\phi(x)$ from an input $x$
- make prediction for $x'$ by plugging into $\phi$ and multiply by learned weights
  Kernel
- focuses on comparing pairs of data points
- define a kernel function $k(x_m, x_n)$ that computes the similarity between two points, model learns weights associated with individual training instances
- see how similar the new point is to the training points using $k$

kernels functions are scalar products in feature space
![[Images/Kernels and Support Machine Vectors-1791403369177.webp|407]]
therefore we can use the feature vectors without ever calculating them with implicit mappings to high-dimensional spaces

high kernel value = high similarity

Gram Matrix $\mathbf{K} - \Phi \Phi ^T$
![[Images/Kernels and Support Machine Vectors-1791404101367.webp]]
$\mathbf{K}$ is symmetrical

https://www.youtube.com/watch?v=efR1C6CvhmE

support vector classification - split data with line (margin between two classes)
machine - adapt data into higher dimensions, use kernels to figure out the correct split
kernel trick - treat data as if it were in higher dimension but don't do the computation

- pooling - downsampling image
  - max pooling, take max value of neighbourhood

## Reading
