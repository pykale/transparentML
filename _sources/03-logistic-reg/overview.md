# Logistic Regression

<!-- Capitalise initials. As compact as possible, prefer ONE line. -->
<!-- We use **UK** English spelling. -->
<!-- File names should be all lowercase, with words separated by hyphens (-), and no spaces.  Each chapter must include an "overview.md" and "quiz-sum-ref.md"-->

```{admonition} Status
Drafting
```

```{admonition} Objectives
- Understand the basic concepts of logistic regression
- Apply logistic regression to real data
- Evaluate the performance of a logistic regression model
- Interpret the results of a logistic regression
```

**Expected time to complete**: 2.5 hours

The linear regression model discussed in {doc}`Linear regression <../02-linear-reg/overview>` assumes that the response variable $y$ is quantitative. But in many situations, the response variable is instead qualitative. In this chapter, we will study approaches for predicting qualitative responses, a process that is known as _classification_. There are many possible classification techniques, or classifiers, that can be used to predict a qualitative response. In this chapter, we will focus on logistic regression, which is a classification technique that is commonly used to predict a binary response (i.e. a response with only two possible outcomes, such as pass/fail, win/lose, alive/dead or healthy/sick).
<!-- Logistic regression is an extension of linear regression that is used when the response variable is categorical. It is also known as _logit regression_ or _logit model_. In this chapter, we will learn how to use logistic regression to make predictions and understand the relationship between variables. We will learn the basic concepts of logistic regression and apply it to real data. We will also learn how to evaluate the performance of a logistic regression model and interpret the results. -->

```{admonition} Ingredients
- Input: features of data samples
- Output: class labels of data samples
- Model: fit a line (or plane/hyperplane) via the logistic (sigmoid) function to the training data and assign the label on the fitted line (or plane/hyperplane) to the test data
  - Hyperparameter(s): None
  - Parameter(s): the intercept(s) and slope(s) of the fitted line (or plane/hyperplane), also known as the bias(es) and weight(s), respectively
- Loss function: maximise the likelihood (probability) of the classes for given training data points
- Learning algorithm: Gradient descent
```

```{admonition} Transparency
```

```{admonition} Transparency
System logic
- Condition to produce certain output: to produce a sample with label $c$, find a data point $x$ such that $\mathbb{P}(c|\mathbf{x}, \boldsymbol{\beta}) > 0.5$ where $\boldsymbol{\beta}$ is the vector of parameters of the logistic regression model.
```

<!-- - What input to produce certain output:
- How to produce certain output: -->
