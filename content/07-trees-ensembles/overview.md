# Trees and Ensembles

<!-- Capitalise initials. As compact as possible, prefer ONE line. -->
<!-- We use **UK** English spelling. -->
<!-- File names should be all lowercase, with words separated by hyphens (-), and no spaces.  Each chapter must include an "overview.md" and "quiz-sum-ref.md"-->

```{admonition} Status
Drafting
```

```{admonition} Objectives
- Objective 1
```

**Expected time to complete**: x hours

In this chapter, we will study classification and regression models that are based on trees and ensembles. These models are very popular in practice, and are used in a wide range of applications. We will start by studying [decision trees](https://en.wikipedia.org/wiki/Decision_tree), which are the simplest form of tree-based models. We will then study bagging and random forests, which are ensemble methods that combine multiple decision trees. Finally, we will study boosting, which is another ensemble method that combines multiple decision trees.

Tree-based models involves dividing (stratifying, segmenting) the feature space into a number of simple regions, and then making a prediction for each region. This is in contrast to linear models, which involve fitting a single linear function to the data. The main advantage of tree-based models is that they are very easy to **interpret**. The main disadvantage is that they are prone to overfitting, and have limited predictive power.

To overcome these disadvantages, we can use ensemble methods, which combine multiple trees to produce a single model for a single consensus prediction. The main advantage of ensemble methods is that they are less prone to overfitting, and have better predictive power. The main disadvantage is that they are more difficult to interpret.

```{admonition} Ingredients
- Input: ...
- Output: ...
- Model: ...
  - Hyperparameter(s): ...
  - Parameter(s): ...
- Loss function: ...
- Learning algorithm: ...
```

```{admonition} Transparency
System logic
- Condition to produce certain output:
```
<!-- - What input to produce certain output:
- How to produce certain output: -->
