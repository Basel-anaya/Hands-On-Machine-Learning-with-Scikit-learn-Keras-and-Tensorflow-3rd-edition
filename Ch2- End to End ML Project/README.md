## In this chapter, we will work on an end-to-end machine learning project, pretending to be a recently hired data scientist at a real estate company.

#### Here are the main steps we will go through:

### 1- Framing the problem & looking at the big picture
##### We Define the objective in business terms and answer the following questions:

- How would the solution be used?
- What are the current solutions/workarounds?
- How should we frame this problem? (Supervised/Unsupervised, Batch/Online, Instance-based/Model-based)
- How should performance be measured?
- Is the performance measure aligned with the business objective?
- What would be the minimum performance needed to reach the business objective?
- What are comparable problems? can we use previous methods or tools?
- Is human expertise available?
- How would we solve the problem manually?
- List the assumptions we/others have made so far?
- Verify assumptions if possible


### 2- Get the data
##### The second step is about data acquisition, we go through the following steps:

- We list the data we need and how much.
- We find & Document where can we get that data.
- We check how much space it will take.
- We check the legal obligations & get authorization if necessary.
- We get access authorization.
- We create a workspace with enough storage space.
- We get the data.
- We convert the data into a format we can easily manipulate.
- We ensure sensitive information is either deleted or protected.
- We check the size & type of data.
- We sample a test set, put it aside, and never look at it

### 3- Explore the Data
##### After acquiring the necessary data, we explore its properties by doing the following:

- We create a copy of the data for exploration and sample it down if necessary
- We create a Jupyter notebook to save our data exploration sessions.
- We study each attribute (column) and its characteristics:
1. Name
2. Type (Categorical, Continuous, Int/Float, Structured/Unstructured, Text ..)
3. % of missing values
4. Noisiness and type of noise (Stochastic, rounding error, ..)
5. Usefulness for the task
6. Type of distribution (Gaussian, Logarithmic, Uniform ..)
- For supervised Learning tasks, we identify the target attribute
- We visualize the data
- We study the correlations between attributes
- We study how we would solve the problem manually
- We identify the promising transformations we may want to apply
- We Identify Extra data that would be useful
- We Document what we have learned in report

### 4- Data Preparation
##### Now's the time to prepare the data for machine learning. We go through the following list:

- We create a copy of the data.
- We write functions for all the data transformations we want to apply: we do this once for reproducibility on test and production data. Packaging functions like this will also allow us to treat preprocessing steps as hyper-parameters.
- We clean the data by fixing or removing outliers, and filling missing values with 0, mean, median, inference, .. or drop their rows/columns.
- We conduct feature selection: we drop the attributes that provide no useful information for the task
- We conduct feature engineering. Examples of feature engineering:
1. Discretize continuous features
2. Decompose features (Categorical, datetime, ...)
3. Add promissing feature transformations (, , 
, ..)
4. Aggregate features into promising new features
- We scale the features of interest by standarizing and/or normalize them.

### 5- Shortlist promising models
##### After preparing the data, we select and shortlist potential models that may solve the problem:

- If the data set is big, we sample smaller datasets for experimentation.
- We try many models from different categories (NB, Linear regression, RF, NN, ..) using standard parameters.
- We measure and compare their performances: for each model, we measure N-fold cross validation and capture the mean and standard diviation of the performance.
- We analyze the most significant variable for each algorithm.
- We analyze the types of errors the models make. What data would we use to avoid these errors?
- We perform a quick round of feature selection and engineering.
- We perform one or two more quick iterations of the previous steps.
- We shortlist the top-3-to-5 most performant algorithms that make different types of errors.

### 6- Fine-tune your models & combine them into a great solution
##### After shortlisting the most promising algorithms, it's time to fine-tune their performance, ensemble them and export a final model.

- We should use the whole dataset
- We fine-tune hyper-parameters using cross-validation
##### We treat our data transformation choices as hyper-parameters. Unless there are very few hyper-parameters to explore, we should prefer random search to grid search. If training takes a long time, we try out Bayesian Optimization.

- We try ensemble methods. Combining the best models will often produce better results than running them individually.
- Once we are confident about the model, we measure its performance on the test set to estimate its generalization error.

### 7- Present the solution
##### After exporting a final model, it's time to present the work in an accessible fashion:

- We document what we have done
- We create a nice presentation
- We explain why our solution achieves the business objective
- We showcase interesting things we noticed along the way
- We ensure the key findings are easily communicated through beautiful visualization and one-line statements

### Launch, Monitor, and maintain your system
##### After presenting our findings, it's time to launch, monitor, and maintain the system:

- We get our solution ready for production
- We write monitoring code to check our system's performance while running in production and run interval-based checks to alert when it drops.
##### During this step, we should be aware of the "slow degradation" phenomena: models tend to rot as data evolves. We should also monitor ourr inputs quality. Finally, we re-train the model on a regular basis on fresh data
