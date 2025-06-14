## Overview

- Review the major goals of machine learning
- Introduce the `tidymodels` and `parsnip` packages for estimating
  regression models
- Define resampling methods for evaluating model performance
- Demonstrate how to conduct cross-validation using `rsample`

## Before class

- Read [Statistical learning: the basics](/notes/statistical-learning/)
- Read [Build a model](/notes/start-with-models/)
- Read [Evaluate your model with resampling](/notes/resampling/)

This is not a math/stats class. In class we will **briefly** summarize
how these methods work and spend the bulk of our time on estimating and
interpreting these models. That said, you should have some understanding
of the mathematical underpinnings of statistical learning methods prior
to implementing them yourselves. See below for some recommended
readings:

##### For those with little/no statistics training

- Chapters 7-8 of [*OpenIntro
  Statistics*](https://www.openintro.org/stat/textbook.php?stat_book=os) -
  an open-source statistics textbook written at the level of an
  introductory undergraduate course on statistics

##### For those with prior statistics training

- Chapters 2-3, 4.1-3 in [*An Introduction to Statistical
  Learning*](https://www.statlearning.com/) - a book on statistical
  learning written at the level of an advanced undergraduate/master’s
  level course
- Chapters 4-5 in [*Hands-On Machine Learning with
  R*](https://bradleyboehmke.github.io/HOML/) - a recent publication
  which approaches these methods from the perspective of machine
  learning rather than traditional statistical inference. Includes code
  examples using R and the `caret` package.

## Class materials

{{% callout note %}}

Run the code below in your console to download the exercises for today.

    usethis::use_course("cis-ds/machine-learning")

{{% /callout %}}

{{% callout note %}}

Materials derived from [Tidymodels, Virtually: An Introduction to
Machine Learning with Tidymodels](https://tmv.netlify.app/site/) by
[Allison Hill](https://alison.rbind.io/).

{{% /callout %}}

### Additional readings

- [`caret`](https://topepo.github.io/caret/) - a package which unifies
  hundreds of separate algorithms for generating statistical/machine
  learning models into a single standardized interface. Very robust, but
  pre-`tidyverse` and on the path to deprecation.
- [`tidymodels`](https://www.tidymodels.org/start/) - a collection of
  packages for machine and statistical learning using `tidyverse`
  principles.

## What you need to do after class
