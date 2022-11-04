# Hypothesis testing

Hypothesis testing has been mentioned briefly in Chapter 2 {doc}`Linear regression <../02-linear-reg/>`, but it has not been explained in detail. This chapter will explain the basics of hypothesis testing and how it can be used to conduct _inference_.

## Inference via hypothesis testing

Hypothesis testing is a way to make inferences about a population based on a sample (of the population). Inference is the process of using sample data to make conclusions about a population. Inference is a key part of data science because we often do not have access to the entire population of interest. Instead, we have a sample of the population. Inference allows us to make conclusions about the population based on the sample.

A statistical hypothesis test answers simple "yes-or-no" questions about data, to decide whether the data at hand sufficiently support a particular hypothesis, for example

- Q1. Is the coefficient $\beta_d$ in a linear regression of $y$ onto $x_1, . . . , x_D$ equal to zero?
- Q2. Is there a difference in the mean blood pressure of laboratory mice in the control group and laboratory mice in the treatment group?

As a formal procedure for testing a hypothesis, the hypothesis test is based on a null hypothesis and an alternative hypothesis. The null hypothesis is a statement about the population that is assumed to be true. The alternative hypothesis is a statement about the population that is assumed to be false. The null hypothesis is often denoted by $H_0$ and the alternative hypothesis is often denoted by $H_1$.

Watch the 14-minute video below for a visual explanation of hypothesis testing in the context of testing drugs for treatment.

```{admonition} Video

<iframe width="700" height="394" src="https://www.youtube.com/embed/0oc49DyA3hU?start=16" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

[Explaining Hypothesis Testing, by StatQuest](https://www.youtube.com/embed/0oc49DyA3hU?start=16)

```

## Four steps of hypothesis testing

The four steps of hypothesis testing are:

1. Define the null hypothesis and the alternative hypothesis.
2. Construct a test statistic that summarizes the strength of evidence against the null hypothesis.
3. Compute a $p$-value that quantifies the probability of having obtained a comparable or more extreme value of the test statistic under the null hypothesis.
4. Decide whether to reject the null hypothesis based on the $p$-value.

### Step 1: Define the null and alternative hypotheses

In hypothesis testing, we consider two possibilities: the null hypothesis and the alternative hypothesis. The null hypothesis $H_0$ is the _default_ state of belief about the world. For example, the null hypotheses
associated with the two questions Q1 and Q2 above are:

- Q1. The coefficient $\beta_d$ in a linear regression of $y$ onto $x_1, . . . , x_D$ is equal to zero.
- Q2. There is no difference between the mean blood pressure of mice in the control and treatment groups.

The alternative hypothesis $H_1$ is the _opposite_ of the null hypothesis, representing something different and often more interesting to us, e.g., there is a difference between the mean blood pressure of the mice in the two groups.

Typically, we focus on using data to reject $H_0$, if there is sufficient evidence in favor of $H_1$. We
can consider rejecting $H_0$ as making a _discovery_ about our data, i.e., we are discovering that $H_0$ does not hold! However, if we fail to reject $H_0$, we are not making a discovery, but we are not necessarily saying that $H_0$ is true. We are simply saying that we do not have sufficient evidence to reject $H_0$, since there can be multiple reasons for failing to reject $H_0$, e.g., the null hypothesis is true, or the sample size is too small, or the test statistic is not sensitive enough to detect a difference between the two groups.

### Step 2: Construct a test statistic

Next, we use our data to find evidence for or against the null hypothesis. A [test statistic](https://en.wikipedia.org/wiki/Test_statistic), often denoted by $T$, is a function of the data that summarises the strength of evidence against the null hypothesis. Such function is often constructed from the sample mean and the sample standard deviation.

For example, denote the blood pressure measurements for the $D_t$ mice in the treatment group as $x^t_1, \cdots, x^t_{D_t}$ and the blood pressure measurements for the $D_c$ mice in the control group as $x^c_1, \cdots, x^c_{D_c}$. Denote their means as $\mu_t$ and $\mu_c$, respectively. Then, the test statistic for the two-sample $t$-test for testing $H_0: \mu_t = \mu_c$ versus $H_1: \mu_t \neq \mu_c$ is

T = $\frac{\hat{\mu}_t - \hat{\mu}_c}{\sqrt{\frac{s^2_t}{D_t} + \frac{s^2_c}{D_c}}}$,

where $\hat{\mu}_t$ and $\hat{\mu}_c$ are the sample means of the treatment and control groups, respectively, and $s^2_t$ and $s^2_c$ are the sample variances of the treatment and control groups, respectively.

```{admonition} How to interpret this statistic?
:class: tip, dropdown
This test statistic $T$ is a measure of the difference between the two sample means, scaled by the standard deviation of the two samples. The larger the test statistic $T$, the more evidence there is against the null hypothesis $H_0$ (and in support of the alternative hypothesis $H_1$). The smaller the test statistic $T$, the more evidence there is in favor of the null hypothesis $H_0$ (and against the alternative hypothesis $H_1$).
```

### Step 3: Compute a $p$-value

The test statistic above is typically used to compute the [$p$-value](https://en.wikipedia.org/wiki/P-value), which is the probability of obtaining a test statistic at least as extreme as the one observed, assuming that the null hypothesis is true. The $p$-value is a measure of the strength of evidence against the null hypothesis. The smaller the $p$-value, the more evidence there is against the null hypothesis. The larger the $p$-value, the more evidence there is in favor of the null hypothesis.

Watch the 11-minute video below for a visual explanation of $p$-value in the context of testing drugs for treatment.

```{admonition} Video

<iframe width="700" height="394" src="https://www.youtube.com/embed/vemZtEM63GY?start=11" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

[Explanation and interpretation of $p$-value, by StatQuest](https://www.youtube.com/embed/vemZtEM63GY?start=16)
```

```{admonition} How to interpret the $p$-value?
:class: tip, dropdown
The $p$-value is as the fraction of the time that we would expect to see such an extreme value of the test
statistic if we repeated the experiment many many times, provided that the null hypothesis is true. If the $p$-value is small, then we would expect to see such an extreme value of the test statistic only a small fraction of the time, if we repeated the experiment many many times, provided that the null hypothesis is true. In this case, we would have strong evidence against the null hypothesis. If the $p$-value is large, then we would expect to see such an extreme value of the test statistic a large fraction of the time, if we repeated the experiment many many times, provided that the null hypothesis is true. In this case, we would have weak evidence against the null hypothesis.
```

In Step 2, we pointed out that a large (absolute) value of the test statistic provides evidence against $H_0$. Suppose
a data analyst conducts a statistical test, and reports a test statistic of $T$ = 17.3. Does this provide strong evidence against $H_0$? It’s impossible to know without more information: we would need to know what value of the test statistic should be expected, under $H_0$, if the data analyst had repeated the experiment many times. If the data analyst had repeated the experiment many times, and the test statistic was typically around 0, then a value of 17.3 would be very unusual, and we would have strong evidence against $H_0$. However, if the data analyst had repeated the experiment many times, and the test statistic was typically around 10, then a value of 17.3 would be less unusual, and we would have weaker evidence against $H_0$.

This is exactly what a $p$-value measures. A $p$-value allows us to transform (or standardise) our test statistic, which is measured on some arbitrary and uninterpretable scale, into a number between 0 and 1 that can be _more easily interpreted_.

### Step 4: Decide whether to reject the null hypothesis $H_0$

Finally, we decide whether to reject $H_0$ or not (we do not usually talk about "accepting" $H_0$: instead, we talk about "failing to reject" $H_0$). We reject $H_0$ if the $p$-value is less than a pre-specified significance level $\alpha$. The significance level $\alpha$ is a number between 0 and 1 that we choose before we conduct the statistical test. We typically choose $\alpha$ = 0.05 or $\alpha$ = 0.01, which is a common convention in the scientific community (with 0.05 being more common). If the $p$-value is less than $\alpha$, then we reject $H_0$. If the $p$-value is greater than or equal to $\alpha$, then we _fail to reject_ $H_0$. Furthermore, a data analyst
should typically report the $p$-value itself, rather than just whether or not it exceeds a specified threshold value.

```{admonition} How to interpret the significance level $\alpha$?
:class: tip, dropdown
The significance level $\alpha$ is the probability of rejecting $H_0$ when it is true. For example, if $\alpha$ = 0.05, then there is a 5% chance of rejecting $H_0$ when it is true. In other words, if $H_0$ holds, we would
expect to see such a small $p$-value no more than 5% of the time. On the other hand, there is a 95% chance of _not_ rejecting $H_0$ when it is true. Nothing is absolute here.
```

## Type I and Type II errors

### Definition

In the context of hypothesis testing, we can distinguish between two types of errors: Type I errors and Type II errors. A Type I error occurs when we reject $H_0$ when it is true. A Type II error occurs when we fail to reject $H_0$ when it is false. A Type I error is also known as a _false positive_, and a Type II error is also known as a _false negative_. A summary of the possible scenarios associated with testing the null hypothesis $H_0$ is shown in table below.

```{list-table} Possible scenarios associated with testing the null hypothesis $H_0$ (equivalent to Table 13.1 of the textbook). Type I errors are also known as false positives, and Type II errors as false negatives.
:header-rows: 1
:align: center
:widths: "auto"
:name: table-13-1
* -
  - Reject $H_0$
  - Fail to reject $H_0$
* - $H_0$ is true
  - Type I error
  - Correct decision
* - $H_0$ is false
  - Correct decision
  - Type II error
```

The table above summarises the possible scenarios associated with testing the null hypothesis $H_0$. The first row of the table shows the two possible outcomes of the statistical test (that we know after performing the test): either we reject $H_0$ or we fail to reject $H_0$. The first column of the table shows the two possible ground-truth values of $H_0$ (that we do not know): either $H_0$ is true or $H_0$ is false. The four cells in the table show the four possible scenarios that can occur when we test $H_0$.

If we reject $H_0$ when it is true, then we have made a Type I error. If we fail to reject $H_0$ when it is false, then we have made a Type II error. If we reject $H_0$ when it is false, then we have made a correct decision. If we fail to reject $H_0$ when it is true, then we have made a correct decision too.

The _Type I error rate_ is defined as the probability of making a Type I error given that $H_0$ is true, i.e., the probability of incorrectly rejecting $H_0$. The power of the hypothesis test is defined as the probability of NOT making a Type II error given that $H_1$ holds, i.e., the probability of correctly rejecting $H_0$.

```{admonition} Connections to classification
:class: note
The Type I error rate is equivalent to the false positive rate in binary classification, i.e. predicting a positive (non-null) label when the true label is in fact negative (null). The power of the hypothesis test is equivalent to the true positive rate in classification.
```

### Trade-off between Type I and Type II errors

Ideally we would like both the Type I and Type II errors to be small. But there typically is a trade-off: we can make the Type I error small by only rejecting $H_0$ when we have strong evidence against it, but this will increase the Type II error. We can make the Type II error small by rejecting $H_0$ even when we have weak evidence against it, but this will increase the Type I error.

The significance level $\alpha$ is a trade-off between the Type I and Type II errors. If we choose a small value of $\alpha$, then we will have strong evidence against $H_0$ when we reject it, but this will increase the Type II error. If we choose a large value of $\alpha$, then we will have weak evidence against $H_0$ when we reject it, but this will increase the Type I error. By only rejecting $H_0$ when the $p$-value is below $\alpha$, we ensure that the Type I error
rate will be less than or equal to $\alpha$.

In practice, we typically view Type I errors as more "serious" than Type II errors, because the former involves
declaring a scientific finding that is not correct, which is more serious than failing to declare a scientific finding. Therefore, when we perform hypothesis testing, we typically require a low Type I error rate — e.g. at most $\alpha$ = 0.05 — while trying to make the Type II error small (or, equivalently, the power large).
