Suppose we ask a random question to thousands of people, then aggregate their answers. In many cases we will find that this aggregated answer is better than an expert's answer (really). This is called the wisdom of the crowd.

Similarly, if we aggregate the predictions of a group of models (such as classifiers or regressors), we will often get better predictions than the best individual predictor.

A group of predictors is called an ensemble. Thus this technique is called `ensemble learning`, and an ensemble learning algorithm is called an `Ensemble Method`.

As an example of an ensemble method, we can train a group of decision tree classifiers, each on a random subset of the training data. Such an ensemble of decision trees is called a random forest. Despite its simplicity, this is one of the most powerful machine learning algorithms available today.

You will often use ensemble methods near the end of a project, once you have already built a few good predictors, to combine them into an even better predictor.

In this chapter, we will discuss the most famous ensemble learning methods, including: `Bagging`, `Boosting`, & `Stacking`.
