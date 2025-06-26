---
title: "A3: Wrangling and tidying data"
date: 2023-06-27T13:30:00-06:00  # Schedule page publish date
weight: 3
description: Assignment 3 due 6/27/25, Wrangle and explore messy datasets in practical research environments.
output:
  md_document:
    preserve_yaml: true
type: docs
#type: post
aliases: ["/a3-wrangle-data.html"]

---

# Overview

The goal of this assignment is to practice wrangling and exploring
social science data in a research context. NOTE: This will take some
time!

# Accessing the `A3` repository

- Go [to this link](https://classroom.github.com/a/c1SZ2aIf) to accept
  and create your private `A3` repository on GitHub. Once you do so,
  your repository will be built in a few seconds. It follows the naming
  convention `a3-wrangling-<USERNAME>`  
- Once the your repository has been created, click on the link you see,
  which will take you to your repository.
- Finally, clone the repository to your computer (or R workbench)
  following the process below.

# Cloning your `A3` repository

After you have accessed the `A3` repository (see above), follow the
[same steps you completed for `A1`](/homework/1-edit-readme/) to clone
the repository.

# General workflow

Your general workflow will be:

- Accept the repo and clone it (see above)
- Make changes locally to the files in RStudio
- Save your changes
- Stage-Commit-Push: stage and commit your changes to your local Git
  repo; then push them online to GitHub. You can complete these steps
  using the Git GUI integrated into RStudio. In general, you do not want
  to directly modify your online GitHub repo (if you do so, remember to
  pull first); instead modify your local Git repo, then
  stage-commit-push your changes up to your online GitHub repo.

# PART 1: Tidying messy data

Tidy the following dataset – first, copy this code and load it at the
top of a file you name `tidying.Rmd` set your output to `md_document`

    drinks <- data.frame(
      ID = c(1, 1, 3, 4, 4),
      FirstName = c("Jean", "Jean", "Taylor", "Travis", "Travis"),
      Beverage = c("Tea", "Tea", "Coffee", "Tea", "Coffee"),
      stringsAsFactors = FALSE
    )

Tidy this data frame so that it adheres to the tidy data principles:

1.  Each variable must have its own column.
2.  Each observation must have its own row.
3.  Each value must have its own cell.

Your final product (tidy data frame) should look like this:

    ## # A tibble: 3 × 4
    ##      ID FirstName   Tea Coffee
    ##   <dbl> <chr>     <int>  <int>
    ## 1     1 Jean          2      0
    ## 2     3 Taylor        0      1
    ## 3     4 Travis        1      1

Check the [Transform](https://r4ds.hadley.nz/data-transform.html)
chapter, readings, and in-class exercises before starting this part.

# PART 2: Wrangling and visualizing messy(ish) data

## **Context**

[Bihar](https://en.wikipedia.org/wiki/Bihar) is a state in eastern
India, bordering Nepal to the north and several Indian states including
Uttar Pradesh, Jharkhand, and West Bengal. It is one of India’s most
populous states and is historically significant, with sites such as
[Nalanda](https://en.wikipedia.org/wiki/Nalanda_mahavihara) and [Bodh
Gaya](https://en.wikipedia.org/wiki/Bodh_Gaya). Bihar has experienced
notable GDP growth in recent decades, yet it faces persistent challenges
in socio-economic development, with wide disparities across its
districts.

In this assignment, you will work with two datasets:

1.  `gdp_Bihar.csv` – GDP data for Bihar districts over several years.
    Rows represent year/description combinations (e.g. GDP, growth rate)
    and columns represent districts.
2.  `district_category.csv` – A mapping of each district to a category:
    Urban, Suburban, or Rural.

Your task is to tidy, summarize, visualize, and reflect on the data,
building both technical skills and reasoning abilities.

For this assignment, we are giving you the baseline repo BUT NOT the rmd
file. You will need to build that yourself, being sure to provide all
the sections, etc. You can follow the guides from prior assignments.

## **Part 2.1: Reasoning about the data**

### Question 1

What are the three characteristics of tidy data?

Write a sentence or two explaining each characteristic.

### Question 2

Based on your answer above, is the given dataset (`gdp_Bihar.csv`) tidy?

Explain briefly. What clues tell you this? Be specific, giving relevant
details from the dataset.

### Question 3

Will it help to have the data in tidy format? Why or why not?

Think about how tidy data might affect your ability to analyze,
summarize, or visualize this dataset.

### Question 4

Describe how you would rearrange the columns and rows to make this data
tidy.

- What would you like rows to represent?
- What would you like columns to represent?

Write your plan clearly, without jumping into code yet.

### Question 5

Based on your plan above, what R verbs or functions might help you
implement this transformation?

List some dplyr/tidyr verbs you think could help. You don’t have to know
the exact syntax.

## **Part 2.2: Tidying the data**

Transform your dataset into tidy format based on your plan above. Once
tidied inspect the data using `head()` or `glimpse()`. In your Rmd file,
include this output as part of the document.

## **Part 2.3: Observing the tidy data**

What patterns or issues do you notice in the `Growth Rate %` values for
the year `2004-05` across the districts?

Write a brief note:

- What do you observe that you could not easily see in the original CSV
  file?
- Why might this pattern have been hidden in the original format?

Hints:

- Focus on rows where `year` is `2004-05` and the variable is
  `Growth Rate %`
- Are these values mostly present, mostly missing, or a mix?

Follow-up:

- Can you quantify this pattern? For example, how many rows have missing
  `Growth Rate %` for `2004-05`?
- How might this insight affect your analysis or visualization?

## **Part 2.4: Merging district categories**

Load `district_category.csv` into your R session. Perform a left join to
merge this with your tidy GDP dataset. After joining:

- Check for any rows where `category` is NA. What could this indicate?
- Make sure every row in your tidy GDP dataset retains its data.

Hints

- Remember: joins match on a column that is common to both datasets.
  What’s the matching column here? (if you’re not sure, use
  `names(dataframe)` to get a list of column names.)
- Check your results after joining: use `summary()`,
  `count(category, sort = TRUE)`, or filter for `NA` in `category`.
- If you encounter `NA` categories, think: are the district names
  spelled/formatted exactly the same in both datasets?

## **Part 2.5: Renaming and enhancing the dataset**

Use pipes to chain your steps:

- Rename your columns to be consistent: lowercase, no spaces (use
  underscores), meaningful names

- Use `mutate()` to add a new column: GDP in USD million

  Remember:

  - 1 crore (Cr) = 10^7 rupees

  - $1 = Rs 85

    Formula: `(gdp_in_rs_cr * 10^7) / (85 * 10^6)`

### **Questions**

- Why is it helpful to standardize and clean your column names?
- Why do you think we’re converting GDP to USD million? How might this
  help in communicating your results to a broader audience?

## **Part 2.6: Grouping, summarizing, filtering**

Create summaries:

1.  Group by district:
    - Compute the mean growth rate
    - Arrange the results in descending order of mean growth rate
2.  Group by year and category:
    - Compute the mean growth rate (ignore NA values)
    - Compute total GDP in USD million

Reason about:

- Why do you need to handle NA values carefully in growth rate?
- How did you handle NA values in the two summaries and why ?
- What would happen if you filtered out all rows for `2004-05` vs using
  `na.rm = TRUE` in the mean ? How would that affect total GDP?

Hints

- Think carefully before filtering:
  - Growth rate has some `NA` values, so including it will distort your
    mean.
  - GDP is *complete* — so if you remove any rows/observations
    completely, you’ll lose valuable GDP data!

------------------------------------------------------------------------

## **AI usage guidelines**

You may use AI tools to help you with:

- Understanding error messages
- Writing or debugging R code
- Clarifying concepts

You must document:

- The exact prompt you used
- The AI’s response
- How you applied or modified the advice

------------------------------------------------------------------------

## **Deliverables**

Submit:

- Your written responses to reasoning and reflection questions (within
  the README.Rmd and README.md) files
  - Have `echo = T` for this assignment
- Your AI usage log (save the session with chatGPT/Claude/Gemini etc on
  internet as html file and add it to your repo)
- A description of your process and what resources you used (including
  AI but also things like stack overflow, etc.)

# Submit the assignment

To submit the assignment, simply push to your repository the last
version of your assignment before the deadline.

Then copy your repository URL (e.g.,
`https://github.com/cfss-hmwks/a3-wrangling-jmclip`) and submit it to
Canvas under A3 before the deadline.

Make sure to stage-commit-push: all of your files (recall that you will
need to generate the RMD and md files yourself!)

# Rubric

Needs improvement: Doesn’t complete all components. Code contain errors
and/or is not clearly written and/or not documented. Uses the same type
of plot for each graph, or doesn’t use plots appropriate for the
variables being analyzed. No record of commits other than the final push
to GitHub.

Satisfactory: Solid effort. Hits all the elements. Finished all
components of the assignment with only minor deficiencies. Easy to
follow (both the code and the output).

Excellent: Finished all components of the assignment correctly and used
efficient code to complete the exercises. Code is well-documented (both
self-documented and with additional comments as necessary). Graphs and
tables are properly chosen and labeled. Use multiple commits to back up
and show a progression in the work. Analysis and interpretation of
results are clear and easy to follow.

For further details, see the [general
rubric](/faq/homework-evaluations/) we adopt for grading.

# Acknowledgments

- This page (and assignment) developed with Sarthak Dhanke
