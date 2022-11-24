# GLM and SVM

<!-- Capitalise initials. As compact as possible, prefer ONE line. -->
<!-- We use **UK** English spelling. -->
<!-- File names should be all lowercase, with words separated by hyphens (-), and no spaces.  Each chapter must include an "overview.md" and "quiz-sum-ref.md"-->

```{admonition} Status
Ready for HP review
```

```{admonition} Objectives
- Understand the relationships between linear regression, poisson regression, and logistic regression under GLM framework.
- Understand the basic concepts of support vector machine.
- Apply support vector machine in training and testing a classification model.
- Evaluate the performance of a classifier using ROC curve and confusion matrix.
- Interpret the results of a SVM classifier.
```

**Expected time to complete**: x hours

In this chapter, we will introduce generalised linear models (GLMs) and support vector machines (SVMs). GLM is a a flexible generalisation of ordinary linear regression. The GLM generalises linear regression by allowing the linear model to be related to the response variable via a link function and by allowing the magnitude of the variance of each measurement to be a function of its predicted value. It is a general framework that includes linear regression, poisson regression, logistic regression, and many other regression models.

SVM is an approach for classification that was developed in the computer science community in the 1990s and that has grown in popularity since then. SVMs have been shown to perform well in a variety of settings, and are often considered one of the best "out of the box" classifiers.

```{admonition} Ingredients: SVM
- Input: features of data samples.
- Output: class labels of data samples.
- Model: fit a plane/hyperplane to the training data to separate the data points by their class labels with the largest margin.
  - Hyperparameter(s): $C$ for controlling the trade-off between the margin and the misclassification/margin violation penalty. Other hyper-parameters include the kernel type and the kernel parameters.
  - Parameter(s): Intercept ($\beta_0$) and coefficients ($\alpha_1, \alpha_2, \ldots, \alpha_N$) for each training observation.
- Loss function: maximises the margin and minimises the misclassification/margin violation penalty.
- Learning algorithm: quadratic programming.
```

```{admonition} Transparency: SVM
System logic
- Condition to produce certain output: to produce an output $y$, find out this class on which side of the fitted hyperplane, and then all corresponding data points $x$ (or $\mathbf{x}$) on this side of the hyperplane will be classified as $y$.
```
<!-- - What input to produce certain output:
- How to produce certain output: -->
