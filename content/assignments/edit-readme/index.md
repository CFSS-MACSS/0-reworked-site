---
title: "A1: Practice editing .Rmd and generating .md"
date: 2022-09-29T13:30:00-06:00  # Schedule page publish date
#publishdate: 2019-03-01
weight: 1
type: docs
description: Assignment 1 due 6/20/25, Test software installation, GitHub setup, and homework submission process, as well as demonstrate basic competency in Markdown and R Markdown.
output:
  md_document:
    preserve_yaml: true
aliases: ["/a1-edit-README.html"]

---

# Overview

The goal is to test your software installation, your GitHub setup, and
the homework submission process, as well as demonstrate basic competency
in Markdown and R Markdown.

## Accessing your `A1` repository

- Go [to this link](https://classroom.github.com/a/B8DreZI2) to accept
  and create your private `a1` repository on GitHub. Once you do so,
  your repository will be built in a few seconds. It follows the naming
  convention `a1-<USERNAME>`  
- Once the your repository has been created, click on the link you see,
  which will take you to your repository.
- Finally, clone the repository to your computer following the process
  below.

## Cloning your `a1` repository

After you have accessed the `a1` repository (see above), follow these
steps to clone it. Whenever possible, this will be the preferred route
for setting up your R projects:

- In RStudio, start a new Project with *File &gt; New Project &gt;
  Version Control &gt; Git*. In the “repository URL” paste the URL of
  your newly created GitHub repository: go back to the repository, click
  on the green button “Code” and grab the correct link, either SSH or
  HTTPS (the one you used to set up your cache credentials). The
  repository name should automatically populate; if not, type your
  `a1-<USERNAME>` as name.
- Decide where to store the local directory for the project. Don’t
  scatter everything around your computer - have a central location, or
  some meaningful structure. For example, for repositories you create in
  this course, you can setup a `css` directory and clone all your repos
  there.
- Before proceeding, check the little box “Open in new session”, as
  that’s what you’ll usually do in real life.
- Click “Create Project” to create a new sub-directory, which will be
  all of these things:
  - a directory on your computer
  - a Git repository, linked to a remote GitHub repository
  - an RStudio Project

{{% callout note %}} Before completing the above steps, ensure you
followed the configuration steps [here](/setup/git-configure/), and
everything works as expected. {{% /callout %}}

## General workflow

Your general workflow will be:

<!--
* Pull from GitHub (just an empty precaution now, but it will matter when you collaborate with others)
-->

- Accept the repo and clone it (see above)
- Make changes locally to the files (here `README.md` and `README.rmd`)
  in RStudio
- Save your changes
- Stage-Commit-Push: stage and commit your changes to your local Git
  repo; then push them online to GitHub. You can complete these steps
  using the Git GUI integrated into RStudio – if you have not yet, I
  strongly recommend to go through the [Using Git with R
  Studio](/setup/git/git-with-rstudio) tutorial to get comfortable with
  the workflow. In general, you do not want to directly modify your
  online GitHub repo; instead modify your local Git repo, then
  stage-commit-push your changes up to your online GitHub repo.

## What you need to submit

Written assignments for this course will be submitted using Markdown and
R Markdown: [Markdown](https://daringfireball.net/projects/markdown/)
(.md) is a lightweight text formatting language that easily converts
between file formats. Regular Markdown files (.md) are rendered on the
GitHub website and can be directly read on the website. They are also
integrated directly into [R Markdown](https://rmarkdown.rstudio.com/)
(.rmd or .Rmd), which combines R code, output, and written text into a
single document. GitHub includes a
[guide](https://guides.github.com/features/mastering-markdown/) for
writing Markdown documents.

For this assignment, you need to modify and push to your GitHub homework
repository the following file: `README.rmd` Note that we have set up the
rmd file so that when you `knit` it, it will create your md file for
you!

#### `README.md`

You will notice there is already a `README.md` file in the repo. A
README is usually a plain .txt or .md file. The purpose of a README file
in a repository is to communicate important information about your
project (software, how to run the code, preview of the results, etc.).
The goal of this assignment is to practice generating your README.

#### `Rcode.rmd`

You will notice there is already a `Rcode.rmd` file in the repo. Your
task is to edit this file by adding more YAML arguments (see readings)
and at least two R code chunks.

### Deliverables: items to complete

To achieve full marks, your `README.rmd` should include the following
elements:

- At least one new YAML Header argument. You can modify one of three
  arguments that are already there or add a new one to them (e.g.,
  author, subtitle, table of contents, etc.)
- At least two R code chunks:
  - Rely on the in-class materials “intro to R” as starting point, but
    do not copy the exact code we have seen in class: make some changes
    to customize or expand it
  - Notice the code chunks must execute correctly and your final knitted
    document (which you should submit as well) must display both the
    code and the results
- Before each code chunk, add a brief text that explains what each code
  chunk does
- Headers (one or more)
- Emphasis (italics or/and bold)
- Lists
- Images: add a picture (of yourself or something else) to your repo and
  embed it in your README (see example files present)
- Links
- A summary and reflection of the Git/GitHub workflow you adopted for
  this homework, and of your experience with Markdown (e.g., provide a
  summary of the workflow you adopted, and add some comments about
  something new you learned, something that surprised you, etc.)
- AI/resources statement: All assignments need about one paragraph
  describing the resources you used (including links and prompts, as
  relevant) in completing the assignment. This helps us learn about your
  process.

## Submit the assignment

To submit the assignment, simply push to your repository the last
version of your assignment before the deadline. Then copy your
repository URL
(e.g. <https://github.com/cfss-hmwks/a1-edit-readme-jmclip>) and submit
it to Canvas under A1 before the deadline.

## Rubric

Needs improvement: `README.md` says the equivalent of “This is the
repository of Name Surname” with little details. `README.rmd` contains R
code chunks, but no explanation nor additional YAML headers are added.
All work done via Git/Github … but that’s just a guess, because the
student doesn’t explain how it was done.

Satisfactory: Something in between.

Excellent: `README.md` provides a proper introduction of the student. It
also demonstrates experimentation with several aspects of the Markdown
syntax (e.g., section headers, links, bold, italic, bullet points,
image, etc.). The student describes how they got the changes into
`README.md` and offers a few reflections on their Git/GitHub workflow
and their experience with Markdown. `README.rmd` knits properly and
contains one or more new YAML headers, R code chunks, with a detailed
explanation of them.

For further details, see the [general
rubric](/faq/homework-evaluations/) we adopt for grading.
