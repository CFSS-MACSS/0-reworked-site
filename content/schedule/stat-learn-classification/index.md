## Overview

- Define a decision tree
- Demonstrate how to estimate a decision tree
- Define and estimate a random forest
- Introduce the `caret` package for statistical learning in R
- Define resampling method
- Compare and contrast the validation set approach with leave-one-out
  and *k*-fold cross-validation
- Demonstrate how to conduct cross-validation using `rsample`

## Before class

This is not a math/stats class. In class we will **briefly** summarize
how these methods work and spend the bulk of our time on estimating and
interpreting these models. That said, you should have some understanding
of the mathematical underpinnings of statistical learning methods prior
to implementing them yourselves. See below for some recommended
readings:

- Chapters 8.1, 8.2.2, and 5.1 in [*An Introduction to Statistical
  Learning*](https://www.statlearning.com/)

## Class materials

- [Decision trees and random forests](/notes/decision-trees/)

- [Cross-validation methods](/notes/cross-validation/)

- [The `caret` Package](https://topepo.github.io/caret/) - introductory
  book for the `caret` package. Tells you what models you can implement
  and all the nitty-gritty details to customize `train` for different
  cross-validation methods.

- [Working with
  `rset`s](https://tidymodels.github.io/rsample/articles/Working_with_rsets.html) -
  documentation for `rsample` and demonstration implementing it for
  resampling and model assessment

## What you need to do after class

- [Complete the statistical learning
  homework](/homework/statistical-learning/)
