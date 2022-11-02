# Cross Validation and Bootstrap

<!-- Capitalise initials. As compact as possible, prefer ONE line. -->
<!-- We use **UK** English spelling. -->
<!-- File names should be all lowercase, with words separated by hyphens (-), and no spaces.  Each chapter must include an "overview.md" and "quiz-sum-ref.md"-->

```{admonition} Status
Drafting
```

```{admonition} Objectives
- Understand the basic concepts of cross validation and bootstrap
- Evaluate the performance of machine learning models using cross validation
- Quantify the uncertainty associated with a machine learning model using bootstrap
```

**Expected time to complete**: 2.5 hours

In this chapter, we will learn two resampling methods: cross-validation and bootstrap. They involve repeatedly drawing samples from a training set and refitting a model of interest on each sample in order to obtain additional information about the fitted model. For example, to estimate the variability of a linear regression fit, we can repeatedly draw different samples from the training data, fit a linear regression to each new sample set, and then examine the extent to which the resulting fits differ. Such an approach may allow us to obtain information that would not be available from fitting the model only once using the original training sample.

```{admonition} Ingredients
- Input: ...
- Output: ...
- Model: ...
- Hyperparameter(s): ...
- Loss function: ...
- Learning algorithm: ...
```

```{admonition} Transparency
System logic
- Condition to produce certain output:
```

<!-- - What input to produce certain output:
- How to produce certain output: -->
