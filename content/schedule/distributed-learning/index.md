## Overview

- Discuss the need for distributed computing
- Illustrate the split-apply-combine analytical pattern
- Define parallel processing
- Define SQL
- Demonstrate how to access local and remote SQL databases
- Introduce Hadoop and Spark as distributed computing platforms
- Introduce the `sparklyr` package
- Demonstrate how to use `sparklyr` for machine learning using the
  Titanic data set

## Before class

- Install `sparklyr` and H2O on your local computer. Run the code below
  to install all necessary packages and set the correct options.

      install.packages(c("sparklyr", "rsparkling"))
      options(rsparkling.sparklingwater.version = "2.1.0")

      library(sparklyr)
      spark_install(version = "2.1.0")

  Last year, 70% of students were able to successfully install these
  packages without problems. The others ran into problems. Make sure to
  attempt installing these packages before class so if you have errors
  we can debug them before you need to use the packages.

## Class materials

- [Accessing databases using `dbplyr`](/notes/sql-databases/)

- [Split-apply-combine and parallel
  computing](/notes/split-apply-combine/)

- [Spark and `sparklyr`](/notes/sparklyr/)

- [The split-apply-combine strategy for data
  analysis](http://www.jstatsoft.org/v40/i01/paper) - paper by Hadley
  Wickham establishing a general overview of split-apply-combine
  problems. Note that the `plyr` package is now deprecated in favor of
  `dplyr` and the other `tidyverse` packages

- [Accessing databases using
  `dbplyr`](https://cran.r-project.org/web/packages/dbplyr/vignettes/dbplyr.html)

- [Taxi
  dataset](https://cloud.google.com/bigquery/public-data/nyc-tlc-trips)

- [`bigrquery`](https://github.com/rstats-db/bigrquery) - instructions
  for setting up an account to access Google Bigquery databases

- [`sparklyr`](http://spark.rstudio.com/) - introduction to the
  `sparklyr` interface for Spark

## What you need to do after class
