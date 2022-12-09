# Principal component analysis and clustering
<!-- # Principal Component Analysis & $K$-Means Clustering -->

<!-- Capitalise initials. As compact as possible, prefer ONE line. -->
<!-- We use **UK** English spelling. -->
<!-- File names should be all lowercase, with words separated by hyphens (-), and no spaces.  Each chapter must include an "overview.md" and "quiz-sum-ref.md"-->

```{admonition} Status
Ready for HP review
```

```{admonition} Objectives
- Understand the difference between supervised and unsupervised learning.
- Understand the principal component analysis (PCA) method.
- Apply PCA to a dataset to reduce the dimensionality.
- Understand the $K$-means and hierarchical clustering methods.
- Apply $K$-means and hierarchical clustering to a dataset.
```

**Expected time to complete**: 3 hours

In the previous chapters, we introduced supervised learning methods such as regression and classification. In the supervised learning setting, we typically have access to a set of $D$ features $x_1, x_2, \ldots, x_D$ and a corresponding response $y$. The goal of supervised learning is to predict $y$ using $x_1, x_2, \ldots, x_D$. This chapter will instead focus on unsupervised learning, a set of statistical tools intended for the setting in which we have only a set of features $x_1, x_2, \ldots, x_D$ measured on $N$ observations. We are not interested in prediction, because we do not have an associated response variable $y$. Rather, the goal is to discover interesting things about the measurements on $x_1, x_2, \ldots, x_D$. Is there an informative way to visualise the data? Can we discover subgroups among the variables or among the observations? Unsupervised learning refers to a diverse set of techniques for answering questions such as these. In this chapter, we will focus on two particular types of unsupervised learning: principal component analysis, a tool used for data visualisation or data pre-processing before supervised techniques are applied, and clustering, a broad class of methods for discovering unknown subgroups in data.

```{admonition} Ingredients: Principal component analysis
- Input: high-dimensional ($D$) features  of data samples
- Output: lower-dimensional ($d$) features of data samples
- Model: transformation of the data
  - Hyperparameter(s): None
  - Parameter(s): A $D \times d$ transformation matrix
- Loss function: maximise the variance of the projected data
- Learning algorithm: eigendecomposition
```

```{admonition} Transparency: Principal component analysis
System logic
- Condition to produce certain output: to produce a certain lower-dimensional representation $ \tilde{\mathbf{x}} $, we can use the transformation matrix inversely to project the lower-dimensional representation back to the original space, to reconstruct input data $ \mathbf{x} $.
```

```{admonition} Ingredients: $K$-means clustering
- Input: features of data samples
- Output: cluster assignments/labels
- Model: cluster centres
  - Hyperparameter(s): the number of clusters $K$
  - Parameter(s): coordinates of $K$ cluster centres
- Loss function: minimise the sum of squared distances between data points and their assigned cluster centres
- Learning algorithm: repeated random initialisation and local search
```

```{admonition} Transparency: $K$-means clustering
System logic
- Condition to produce certain output: to produce a certain cluster assignment $y$, locate the data point $\mathbf{x}$ whose distance to the cluster centre $\mathbf{c}_y$ is smaller than the distance to any other cluster centre.
```

<!-- - What input to produce certain output:
- How to produce certain output: -->
