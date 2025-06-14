---
title: "HW11: Build a Shiny application"
date: 2022-11-30T13:30:00-06:00  # Schedule page publish date
publishdate: 2019-04-01
weight: 11
description: Homework 11 due XXX
output:
  md_document:
    preserve_yaml: true
draft: true
aliases: ["/hw11-shiny.html"]

summary: "Build/enhance a Shiny application."
---

# Overview

Due by 11:59pm on December 6th.

# Accessing the `hw11` repository

Go [here](https://github.coecis.cornell.edu/cis-fa22) and find your copy
of the `hw11` repository. It follows the naming convention
`hw11-<USERNAME>`. Clone the repository to your computer.

# What we’ve done

We created a Shiny app that lets you search through and generate
information on city of Chicago wage employees. We used the
[`employees-wage.csv`](https://github.com/cis-ds/shiny-demo) data file
and [this code](/notes/shiny/#final-shiny-app-code) for our app.

# What you need to do

## Option A - extend the Chicago employees app

The app is functional, but is also missing a major segment of employees
in the city: salaried employees. For the homework, you need to revise
the app to incorporate salaried employees and present information
relevant to both sets of employees (use the `employees-all.csv` file).
Consider drawing inspiration from the city’s [employee
dashboard](https://data.cityofchicago.org/Administration-Finance/Current-Employee-Names-Salaries-and-Position-Title/aned-ke5c).
Potential features could be (but are not limited to):

- Separate filters for salaries and hourly wages
- Tabset layouts
- Use the `DT` package to present an employee-level table of results in
  an interative table.
- Visually improve the appearance of the plots (adjust the themes, color
  palettes, add labels, etc.)
- Show the number of results found whenever the filters change. For
  example, when searching for employees in the department of finance,
  the app would show the text “We found 560 employees matching these
  criteria”
- Experiment with packages that add extra features to Shiny, such as
  `shinyjs`, `leaflet`, `shinydashboard`, `shinythemes`, `ggvis`
- Implement the app using a `flexdashboard` format
- If you know CSS, add CSS to make your app look nicer
- Allow the user to download the results table as a .csv file

## Option B - create a new Shiny app

This app can use an entirely different dataset. Perhaps write an app to
explore the `gapminder` dataset, or use your own data set (maybe you
collected it for another assignment). The sky is the limit here, so be
creative! Or be simple to minimize your workload over the next week. But
the more creative your effort, the more points awarded.

## Expectations for your app

Regardless of which option you select, you **must** do the following
things:

1.  Your app should be deployed online on
    [shinyapps.io](http://www.shinyapps.io). Make sure your app actually
    works online (sometimes your app will work in RStudio but will have
    errors on shinyapps.io - make sure you deploy early and often to
    make debugging easier).
2.  Update the `README.md` file in your homework repo. In it you should
    describe your app and add a link to the URL where the app is hosted.
3.  Include the code for your Shiny app in your repository so we can
    evaluate it.

# Submit the assignment

Your assignment submission includes two components:

1.  A working Shiny app hosted on shinyapps.io
2.  A GitHub repo that includes the underlying source code which created
    the app.

Follow instructions on [homework
workflow](/faq/homework-guidelines/#homework-workflow).

# Rubric

Needs improvement: The deployed app does not work or results in many
errors. There is no `README` file describing what the app does.

Satisfactory: Shiny app runs. The `README` file describes either a new
app or 3+ additions to our Chicago wage employees app. Whatever is
described in the `README` is actually implemented in the app.

Excellent: Amazing Shiny app. Lots of new features or a very cool new
app idea. App looks great visually.
