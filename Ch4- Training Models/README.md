In many situations, we need to understand the implementation of specific algorithms. Understanding the underlying logic of machine learning algorithms will help us to:

- Pick the right one for the task
- Pick a good initial set of hyper-parameters
- Pick a good training algorithm
Lastly, most of the topics discussed in this chapter will be essential for understanding neural networks.

In this chapter, we will start by looking at linear regression training from two different angles:

- Using a direct "closed-form" analytical method to get the optimal parameters for the linear model.
- Using an interative optimization method called gradient descent.
GD gradually tweaks the model parameters until it converges to the same set of parameters found by method 1. We will take a look at multiple types of gradient descent: stochastic GD, batch GD, Mini-batch GD.

Next we will look at polynomial regression, or models that can fit non-linear datasets. Then we will look at several regularization techniques that will help up reduce the overfitting typically found in polynomial models.
