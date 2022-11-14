# Feature Selection and Regularisation

<!-- Capitalise initials. As compact as possible, prefer ONE line. -->
<!-- We use **UK** English spelling. -->
<!-- File names should be all lowercase, with words separated by hyphens (-), and no spaces.  Each chapter must include an "overview.md" and "quiz-sum-ref.md"-->

```{admonition} Status
Ready for HP review
```

```{admonition} Objectives
- Understand the basic concepts of feature selection and regularisation
- Apply feature selection to reduce the number of variables in a dataset
- Use regularisation approaches (e.g. LASSO and Ridge Regression) on real-world datasets and understand the concepts of underfit, overfit, and bias-variance trade-off
```

**Expected time to complete**: 2.5 hours

In this chapter, we will learn about two approaches to improve the performance of a machine learning model, feature selection and regularisation. Feature selection is a process of selecting a subset of relevant features for use in model construction. Regularisation is a process of introducing additional information in order to solve an ill-posed problem or to prevent overfitting. Both approaches are used to improve the performance of a machine learning model. In particular, regularisation is used to reduce the variance of a model, while feature selection is used to reduce the complexity of a model.

```{admonition} Process transparency: Feature selection
- **Starting point**: a standardised dataset for a machine learning task with a performance metric defined and a machine learning model for feature selection
- Determine the feature selection method to use (e.g. best subset selection, forward selection, backward elimination, LASSO)
- Compute the average performance metric using cross-validation
- **End point**: Select the subset of features that gives the best performance metric
```

```{admonition} Ingredients: Ridge Regression and LASSO
- Input: features of data samples
- Output: target values of data samples
- Model: fit a line (or plane/hyperplane) to the training data and assign the value on the fitted line (or plane/hyperplane) to the test data
  - Hyperparameter(s): $\lambda$, the importance of the regularisation term / shrinkage penalty
  - Parameter(s): the intercept(s) and slope(s) of the fitted line (or plane/hyperplane), also known as the bias(es) and weight(s), respectively
- Loss function: minimise the total distances of the training data points to the fitted line (or plane/hyperplane) and the sum of the squares or absolute values of the weights
- Learning algorithm:
  - Ridge regression:
    - closed-form analytical solution based on linear algebra, or
    - [Gradient descent](https://en.wikipedia.org/wiki/Gradient_descent): update the weights and intercepts by solving a _multivariate_ optimisation problem iteratively to minimise the loss function
  - Lasso:
    - [Coordinate descent](https://en.wikipedia.org/wiki/Coordinate_descent): update the weights and intercepts by solving a _univariate_ optimisation problem (along one coordinate direction) iteratively to minimise the loss function
```

```{admonition} Transparency: Ridge Regression and LASSO
Same as {doc}`../02-linear-reg/overview`.
```

<!-- - What input to produce certain output:
- How to produce certain output: -->
