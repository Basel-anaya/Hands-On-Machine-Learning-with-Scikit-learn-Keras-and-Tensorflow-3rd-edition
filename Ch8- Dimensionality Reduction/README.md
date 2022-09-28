Many ML problems will involve thousands or even millions of features per instance. Not only all of these features make training extremly slow, but they can also make it much harder for an optimization method to find a good solution.

This problem is often referred to as the `curse of dimensionality`. In real world problem, it is often possible to reduce the number of features considerably. This results in turning an intractable problem into a tractable one.

The goal is to remove the maximum number of features while minimizing information loss that relates to a specific task (example: Classifying MNIST digits). However, dimensionality reduction will always cause some information loss. It will also make our pipeline a bit more complex and thus harder to maintain.

Dimensionality reduction is usually conducted to `speed up training` and is extremly useful for data visualization by projecting the data to a 2-3 dimensional space for visualization.

DataViz is also important to communicate your findings to people who are not data scientists. In Particular, to decision makers who will use the results.

In this chapter we will:

- Discuss the curse of dimenstionality.
- Get a sense of what goes on in a high-dimenstional space.
- Consider the main two approaches to dimensionality reduction:
1. Projection
2. Manifold Learning
- Go through 3 popular dimensionality reduction techniques:
1. PCA
2. Kernel PCA
3. LLE
