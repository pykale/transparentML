# Overview

Welcome to **An Introduction to Transparent Machine Learning**. This self-paced online learning course aims to introduce essential materials on transparent machine learning for learners of diverse backgrounds to understand and apply transparent machine learning in real-world applications with confidence and trust, targeting a missing gap in the online educational space. It is an adaptation of the book [An Introduction to Statistical Learning with Applications in R](https://www.statlearning.com/) {cite}`james2021statistical`, from the perspective of AI transparency detailed in the [AI in Financial Services](https://www.turing.ac.uk/sites/default/files/2021-06/ati_ai_in_financial_services_lores.pdf) report {cite}`ostmann2021ai`.

```{admonition} Version
Pre-alpha: under design and development
```

## Learning objectives [LOs]

By the end of the course, a learner will be able to demonstrate the ability to

- [LO1] understand the theoretical issues and wider context related to transparent machine learning systems and processes

- [LO2] understand the inner-working of a selected number of transparent machine learning algorithms with the capability of interpret the modelling process and the input-output relationships

- [LO3] deploy a practical implementation of transparent machine learning systems and processes in a real-world setting using Python libraries such as scikit-learn

- [LO4] visualise, interpret, and explain transparent machine learning systems and processes in a real-world setting to help stakeholders understand these systems and processes

## Target audience

Learners from diverse backgrounds, preferably with knowledge and skills of basic mathematics (particularly probability and linear algebra) and Python programming for machine learning.

## How to go through the course

The course is designed to be self-paced and self-directed. The course materials are organised into a [Jupyter Book](https://jupyterbook.org/) consisting of 10 chapters, plus prerequisites. Each chapter has a number of sections. Each section is a self-contained unit of learning and should take no more than 30 minutes to complete, ending with an exercise. Each chapter will have a quiz for assessment. For each chapter, we suggest you to go through the materials of each section in the browse (html) first and then launch (via <i class="fas fa-rocket"></i>) the corresponding Jupyter notebook to run the code and complete the exercises. _Optional: You can also download the Jupyter notebooks and [run them locally on your machine](https://jupyter-notebook-beginner-guide.readthedocs.io/en/latest/execute.html) after [installation](https://jupyter-notebook-beginner-guide.readthedocs.io/en/latest/install.html)._

The course is designed to be completed in 40 hours, but you can take as long as you need to complete the course.

## Course outline and structure (subject to change)

- [Prerequisites](https://pykale.github.io/transparentML/00-prereq/overview.html): Basic mathematics and Python programming for machine learning

### Basics

- [Chapter 1](https://pykale.github.io/transparentML/01-intro/overview.html): [System and Process] Introduction to machine learning and AI transparency
- [Chapter 2](https://pykale.github.io/transparentML/02-linear-reg/overview.html): [System] Linear regression
- [Chapter 3](https://pykale.github.io/transparentML/03-logistic-reg/overview.html): [System] Logistic regression and linear discriminant analysis
- [Chapter 4](https://pykale.github.io/transparentML/04-cross-val-bootstrap/overview.html): [Process] Cross validation and bootstrap
- [Chapter 5](https://pykale.github.io/transparentML/05-hypo-test-sw-dev/overview.html): [Process] Hypothesis testing and software development

### Advanced

- [Chapter 6](https://pykale.github.io/transparentML/06-ftr-select-shrink/overview.html): [System] Feature subset selection and shrinkage
- [Chapter 7](https://pykale.github.io/transparentML/07-dec-trees-rnd-forest/overview.html): [System] Decision trees and random forest
- [Chapter 8](https://pykale.github.io/transparentML/08-nb-glm-svm/overview.html): [System] Naive Bayes, generalised linear models, and support vector machines
- [Chapter 9](https://pykale.github.io/transparentML/09-pca-kmeans/overview.html): [System] Principal component analysis and k-means clustering
- [Chapter 10](https://pykale.github.io/transparentML/10-deep-cnn-rnn/overview.html): [System] Deep learning with convolutional/recurrent neural networks*

## Instructors

This course is developed by [Haiping Lu](https://haipinglu.github.io/), a Senior Lecturer in Machine Learning, and [Shuo Zhou](https://shuo-zhou.github.io/), an Academic Fellow in Machine Learning, both at the [Department of Computer Science](https://www.sheffield.ac.uk/dcs), [The University of Sheffield](https://www.sheffield.ac.uk/). H. Lu has developed and taught two machine learning courses [Machine Learning and Adaptive Intelligence - University of Sheffield](https://github.com/maalvarezl/MLAI) from 2018 to 2021 and [Scalable Machine Learning - University of Sheffield](https://github.com/haipinglu/ScalableML) since 2017. S. Zhou was a student and then a head teaching assistant of the [Machine Learning and Adaptive Intelligence - University of Sheffield](https://github.com/maalvarezl/MLAI) course and earned a PhD in machine learning from the University of Sheffield in 2022.

## References

- Book
  - **The Textbook:** James G, Witten D, Hastie T, Tibshirani R., [An Introduction to Statistical Learning](https://www.statlearning.com/), Second Edition,  Springer, 2021. [PDF](https://hastie.su.domains/ISLR2/ISLRv2_website.pdf) {cite}`james2021statistical`
  - Ostmann F, Dorobantu C., [AI in Financial Services](https://www.turing.ac.uk/sites/default/files/2021-06/ati_ai_in_financial_services_lores.pdf), [Alan Turing Institute](https://www.turing.ac.uk/), 2021. {cite}`ostmann2021ai`
  - The Turing Way Community, [The Turing Way: A Handbook for Reproducible Data Science](https://the-turing-way.netlify.app/) {cite}`TheTuringWay`
- Code
  - [ISL_python: An Introduction to Statistical Learning with Applications in PYTHON](https://github.com/qx0731/Sharing_ISL_python)
  - [ISLR-python](https://github.com/JWarmenhoven/ISLR-python)
  - [python-novice-gapminder](https://github.com/swcarpentry/python-novice-gapminder/tree/gh-pages/_episodes)
- Course
  - [Scikit-learn Course](https://inria.github.io/scikit-learn-mooc/index.html)
  - [Deep Learning for Molecules & Materials](https://dmol.pub/)
  - [Coding for Economists](https://aeturrell.github.io/coding-for-economists/)
  - [MIMIC WFDB Tutorials](https://wfdb.io/mimic_wfdb_tutorials/)
  - [Jupyter Guide to Linear Algebra](https://bvanderlei.github.io/jupyter-guide-to-linear-algebra/intro.html)
  - [Machine Learning and Adaptive Intelligence - University of Sheffield](https://github.com/maalvarezl/MLAI)
  - [Scalable Machine Learning - University of Sheffield](https://github.com/haipinglu/ScalableML)

- Teaching
  - [Good practice by design](https://onlinelearning.london.ac.uk/2020/06/08/good-practice-by-design/)
  - [Planning your online module (DIY, lockdown style)](https://onlinelearning.london.ac.uk/2020/05/24/planning-your-online-module-diy-lockdown-style/)

## Acknowledgements

This development is supported by the [Funding call for online learning courses in responsible AI](https://www.turing.ac.uk/funding-call-online-learning-courses-responsible-ai) from the [Alan Turing Institute](https://www.turing.ac.uk/).
