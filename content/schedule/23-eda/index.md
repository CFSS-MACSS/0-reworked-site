---
title: "EDA: exploratory data analysis"
date: 2023-06-21T12:25:00-05:00
publishDate: 2019-04-15T12:25:00-05:00
draft: false
toc: true
output:
  md_document:
    preserve_yaml: true
type: docs
weight: 22


aliases: ["/cm005.html"]

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
#time_end: 2022-09-07T14:20:00-05:00
all_day: false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors: []

# Abstract and optional shortened version.
abstract: ""
summary: "Importing data files and tidying data."

# Location of event.
location: ""

# Is this a selected talk? (true/false)
selected: false

# Tags (optional).
#   Set `tags: []` for no tags, or use the form `tags: ["A Tag", "Another Tag"]` for one or more tags.
tags: []

# Links (optional).
url_pdf: ""
url_slides: "/slides/data-wrangling-tidy-data/"
url_video: ""
url_code: ""

# Does the content use math formatting?
math: false
---

## Overview

- Layers: understanding ggplot
  - [revisit prior slides if
    needed!](https://cfss-macss.netlify.app/slides/12-visualizations-and-the-grammar-of-graphics/#1)
- Intro to EDA
  - aesthetics (aes)
  - geometric objects (geoms)
  - facets
  - stats transformations
  - position adjustments
  - coordinate systems
  - layer cake approach!

<!--
* Demonstrate how vectors can be read and parsed
* Define various data file formats and functions for importation
-->

## Before class

- Required: read [Ch 9](https://r4ds.hadley.nz/layers.html), [Ch
  10](https://r4ds.hadley.nz/EDA.html)

<!--
* [Importing data into R](/notes/importing-data/)
* [Tidy data](/notes/tidy-data/)
* [Practice tidying data](/notes/tidy-exercise/)
-->

## Additional resources

- Antony Unwin [Graphical Data Analysis with
  R](https://catalog.lib.uchicago.edu/vufind/Record/11609643#). It
  covers a range of graphical methods for data exploration and analysis;
  draws on packages beyond `ggplot2` for statistical graphics.Add
  commentMore actions
- Cheat Sheet [Data visualization with
  ggplot2](https://raw.githubusercontent.com/rstudio/cheatsheets/main/data-visualization.pdf)

## What you need to do after class

- Review today’s lecture materials, and prepare for next class
- Continue [Assignment 3](/assignments/3-wrangle-data)
