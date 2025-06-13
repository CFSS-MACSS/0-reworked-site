---
date: "2018-09-09T00:00:00-05:00"
draft: true
weight: 40
title: "Personalize Git"
toc: true
type: docs
output:
  md_document:
    preserve_yaml: true
aliases: ["/git03.html", "/setup/personalize-git/"]
---

**You only have to do this once per machine.**

In order to track changes and attribute them to the correct user, we
need to tell Git your name and email address.

The [`usethis`](https://usethis.r-lib.org/) package includes helpful
functions for common setup and development operations in R. Install it
by running the command

    install.packages("usethis")

from the console in RStudio. Then run the following commands:

    library(usethis)
    use_git_config(user.name = "Benjamin Soltoff", user.email = "ben@bensoltoff.com")

Replace `Benjamin Soltoff` and `ben@bensoltoff.com` with your name and
email address. Your name could be your GitHub username, or your actual
first and last name. **Your email address must be the email address
associated with your GitHub account.**

<!-- ## Acknowledgments -->
<!-- ```{r child = here::here("R", "_ack_stat545.Rmd")} -->
<!-- ``` -->
