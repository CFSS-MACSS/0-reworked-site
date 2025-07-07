---
title: "A6: Collecting and analyzing data from the web"
date: 2023-07-13T13:30:00-06:00  # Schedule page publish date
publishdate: 2019-04-01
weight: 6
type: docs
description: Assignment 6 due 7/14/25
output:
  md_document:
    preserve_yaml: true
draft: false


summary: "Collect data from the web and analyze it."
---

# Overview

We learned two main ways of collecting data from the web:

- Using APIs, with two options:
  - Accessing data using ad-hoc packages that wrap APIs
  - Running API queries by interacting directly with APIs
- Web scraping

For the homework, you will create a new dataset using an API or web
scraping and analyze it.

# Accessing the `A6` repository

Go [to this link]() and find your copy of the `a6` repository. It
follows the naming convention `a6-<USERNAME>`. Clone the repository to
your computer. \* Once your repository has been created, click on the
link you see, which will take you to your repository. \* Finally, clone
the repository to your computer (or R workbench) following the process
below.

Notice the repo you clone for this assignment is empty: **you will have
to fill it with your data and code, and push them to your github repo**.

# Cloning your `a6` repository

After you have accessed the `a6` repository (see above), follow the
[same steps you completed for `a1`](/homework/edit-readme/) to clone the
repository.

# General workflow

Your general workflow will be as follows:

- Accept the repo and clone it (see above)
- Make changes locally to the files in RStudio
- Save your changes
- Stage-Commit-Push: stage and commit your changes to your local Git
  repo; then push them online to GitHub. You can complete these steps
  using the Git GUI integrated into RStudio. In general, you do not want
  to directly modify your online GitHub repo (if you do so, remember to
  pull first); instead modify your local Git repo, then
  stage-commit-push your changes up to your online GitHub repo.

# Assignment description

## Overview

In this assignment, you will:

**Part 1: API data**

- Define a *clear question or hypothesis* that you want to answer using
  data from an API.
- Collect data using **one API** from a curated list or choose your own.
- Clean, analyze, and visualize the data to address your question.

**Part 2: Web scraping**

- Define a *different question or hypothesis* that you want to answer
  using data scraped from a static website. *[\[What is static website
  ?\]](https://en.wikipedia.org/wiki/Static_web_page)*
- Collect data from one or more website or webpages from a curated list
  or choose your own.
- Clean, analyze, and visualize the data to address your question.

You will submit code, data, analysis, and reflections that document your
process.

## API options

Choose one API from the list below. These have been tested and are
accessible without complex setup:

- [USGS Earthquake Catalog](https://earthquake.usgs.gov/fdsnws/event/1/)
- [An API of Ice and Fire](https://anapioficeandfire.com/)
- [balldontlie (NBA stats)](https://www.balldontlie.io/#introduction)
- [USASpending.gov](https://api.usaspending.gov/)

*You may explore other APIs (eg [UCSD
Library](https://ucsd.libguides.com/c.php?g=90743&p=3202435)), but be
cautious: setting up access can take time, and hunting for data can
distract from the assignment goals.* See details in **advanced mode**
below (note: no additional points, etc. for advanced mode!)

## Web scraping options

Choose one **static HTML source** from the list below:

- Wikipedia (e.g., list of Nobel laureates, list of countries by
  population)
- Project Gutenberg book chapter pages
- CDC static tables (e.g., mortality data)
- Archive.org static listings

*Dynamic pages requires JavaScript or login and can be very difficult to
scrap, therefore they are not allowed for this assignment.*

------------------------------------------------------------------------

## What to submit

Your GitHub repository should include:

    data/
      - api_data.csv
      - scraped_data.csv
    analysis.rmd
    README.md (knitted from analysis.rmd)
    analysis.html (knitted from analysis.rmd)

Your `README.md` must include:

- A brief description of the **API question + source**
- A brief description of the **scraping question + source** \[YES, BOTH
  sources in the same document\]
- Explanation of what your code does and how to run it
- Reflection (1-2 paragraphs per part): For example

1.  How you approached the problem: Describe how you broke the task into
    steps and solved it part by part.
2.  Why you wrangled and visualized the data as you did: Explain your
    reasoning for data transformations (e.g., why you summarized, used
    mutate, etc.) and why you chose specific plots (e.g., bar plot
    instead of line chart).
3.  Whether you answered your question: Share whether the data allowed
    you to answer your original question. It’s perfectly fine if it
    didn’t. What matters is that you understand why the data fell short
    and what additional data you’d need.
4.  Further details (optional): Add any other insights if you wish. Keep
    your answers concise but informative; striking this balance takes
    practice and patience.

## Expectations

### API part

- A clear, feasible question
- API query written by you (wrapper or direct call)
- Clean, tidy dataset saved as `api_data.csv`
- At least **1 meaningful visualization**
- Code and narrative in Rmd or script

### Scraping part

- A clear, feasible question
- Scraping code written by you (using `rvest`)
- Clean, tidy dataset saved as `scrape_data.csv`
- At least **1 meaningful visualization**
- Code and narrative in Rmd or script

------------------------------------------------------------------------

## Grading criteria

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr>
<th>Category</th>
<th>Excellent</th>
<th>Satisfactory</th>
<th>Needs Improvement</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Question clarity</strong></td>
<td>Clear, focused, feasible</td>
<td>Clear and feasible</td>
<td>Vague or infeasible</td>
</tr>
<tr>
<td><strong>Data collection</strong></td>
<td>Correct, well-structured code; tidy data</td>
<td>Works with minor issues</td>
<td>Errors or incomplete</td>
</tr>
<tr>
<td><strong>Analysis</strong></td>
<td>Insightful, well-labeled graphs; supports question</td>
<td>Basic but functional</td>
<td>Minimal / unclear</td>
</tr>
<tr>
<td><strong>Reproducibility</strong></td>
<td>Organized repo; clear code</td>
<td>Mostly reproducible</td>
<td>Disorganized / missing files</td>
</tr>
<tr>
<td><strong>Reflection</strong></td>
<td>Thoughtful, specific</td>
<td>Basic</td>
<td>Minimal or missing</td>
</tr>
</tbody>
</table>

## Suggestions

- Keep your question feasible and well-scoped.
- Focus on clarity over complexity in code and plots.
- Save time: use the provided API and scraping options unless you’re
  confident you can manage another source.
- Commit and push regularly!

## Submission

Push your final version to your GitHub repository before the deadline.

Submit the GitHub repository URL to Canvas (e.g.,
`https://github.com/cfss-hmwks-s25/a6-yourusername`).

**For all parts:**

- You can use (but need to expand on) the examples we have reviewed in
  class. Quote all sources you consulted and explain how you used them.
  You are welcome to find inspirations/suggestions from online
  tutorials, as this frequently happens in real life. However, if
  students rely upon online sources, they must quote them and explain
  what they added/modified. The code produced for the assignment must be
  mostly novel and written by you (e.g., it cannot mirror or make only
  minimal adjustments to code found from online sources).

- The expected minimal complexity of the code, should be along the same
  lines of a full developed example (with R wrapper package for an API),
  or the “OMDb” example (API without a wrapper), or of the “presidential
  statements” example we saw in class (for scraping) including functions
  and anything else that would make the scraper more efficient and
  scalable.

- Some rules to follow: (1) everything that is publicly available
  generally can be scraped (what makes publicly available data is
  debated, but the HiQ Labs v. LinkedIn court case is the most common
  reference); (2) everything that is password protected cannot be
  scraped that is: private data that requires a username and passcode
  cannot be scraped; if you need to log in to scrape data, do not scrape
  them). For this specific assignment, I would suggest staying away from
  social media, unless you use their APIs. In general, if there is an
  API, use the API and do not scrape. Some websites have stricter rules,
  and they make them explicit, either in their robots.txt or Terms of
  Service (ToS)

- Save the data you collect in your repository as a `.csv` file and
  upload the file in the repository; the end result must be a tidy data
  frame stored in the repository with some analytical component
  (exploratory descriptions and visualizations). Submit working and
  reproducible code (e.g., no bugs, use relative paths, document your
  code, etc.)[1] [2]

### **ADVANCED MODE**:

Some additional APIs you could write your code for in R:

- [NASA API](https://api.nasa.gov/index.html)
- [The New York Times Developer Network](https://developer.nytimes.com/)
- [SWAPI - the Star Wars API](https://swapi.dev/)
- [xkcd](https://xkcd.com/json.html)
- More examples? [See this list of
  APIs](https://ucsd.libguides.com/c.php?g=90743&p=3202435) and the
  [Programmable Web](https://www.programmableweb.com/apis/directory),
  which claims to be the largest APIs directory on the web

**FYI**: I have not tested nor run code for all these suggested APIs.
These are options for you to consider if you want to really challenge
yourself. If you are newer to R, I suggest you stick with the examples
in the assignment and save advanced mode for later!. Make sure to check
if an R wrapper exists for the API you are interested into. Please, do
not ask the instructional staff questions on how to use these APIs; this
homework’s primary goal is for you to commit to one API that you find
interesting and learn how to get data from it or commit to one webpage
you want to get data from and learn how to scrape it.

## Acknowledgments

This assignment developed with Sarthak Dhanke based on prior assignments
by Sabrina Nardin and Benjamin Soltoff.

[1] If you are scraping from a web page that frequently updates its
content, we may not perfectly reproduce your results. That’s fine - just
make sure you’ve saved a copy of the data frame in the repo (as a
`.csv`).

[2] Also if you [write your own API function for a site that requires
authentication](https://cran.r-project.org/web/packages/httr/vignettes/api-packages.html#authentication),
make sure to include instructions about where to store my API key so we
can run your code **without sharing your private key**.
