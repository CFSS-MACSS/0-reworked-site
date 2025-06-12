---
date: "2018-09-09T00:00:00-05:00"
draft: false
weight: 30
title: "Syllabus"
toc: true
type: docs
output:
  md_document:
    preserve_yaml: true
---

Professor: Jean Clipperton, clipperton@uchicago.edu, OH: TBA.  
TA: Sarthak Dhanke, sarthakdhanke@uchicago.edu, OH: TBA

# Course Description

This is an applied course for social scientists with little-to-no
programming experience who wish to harness growing digital and
computational resource with interest in data science and/or
computational social science. In this course, we will cover the
programming language R, the importance of version control (Git and
GitHub), and best practices for programming. By the end of the course,
students will have worked through most of the basics in R as a
programming language, completed assignments on the core components of
it, be adept in using the tidyverse package, and have applied practice
using data of their choice.

## Course Objectives

By the end of the course, students will:

- Construct and execute basic programs in R using elementary programming
  techniques and tidyverse. packages (e.g. loops, conditional
  statements, user-defined functions)  
- Learn the basics of Git, RStudio, and R markdown for computing.  
- Understand and incorporate packages within R.  
- Apply stylistic principles of coding to generate reusable,
  interpretable code  
- Apply Git and GitHub workflows for version control  
- Implement best practices for reproducible research  
- Visualize information and data using appropriate graphical
  techniques  
- Import data from files or the internet  
- Scrape websites to collect data for analysis

## Books and Materials

Required. \* [R for Data Science (2e)](https://r4ds.hadley.nz/). –
Garrett Grolemund and Hadley Wickham. We will be reading most chapters
from this book. The open-source online version is available for free;
the hardcover version available for purchase online.

### Additional resources.

- [ggplot2: Elegant Graphics for Data Analysis, 3rd Edition. – Hadley
  Wickham.](https://ggplot2-book.org/) Excellent resource for the
  ggplot2. graphics library.
- [Advanced R. – Hadley Wickham](https://adv-r.hadley.nz/). A deep dive
  into R as a programming language, not just a tool for data science.  
- [An Introduction to Statistical Learning: with Applications in R. –
  Gareth James, Daniela Witten, Trevor Hastie, and Robert
  Tibshirani.](https://hastie.su.domains/ISLR2/ISLRv2_corrected_June_2023.pdf.download.html)
  A thorough introduction to statistical learning and machine learning
  methods, focusing on the fundamentals of how these methods work and
  the assumptions that go into them. See also ISLR tidymodels Labs..
  This site demonstrates how to implement all the labs.  
- [RStudio Cheatsheets](https://posit.co/resources/cheatsheets/). -
  printable cheat sheets for common R tasks and features.

## General Policies Academic Integrity

University education is predicated on original work and the intellectual
integrity of the persons engaged in creative discovery. The University
of Chicago is committed to maintaining a cooperative, open intellectual
climate in which those who search for knowledge and understanding
receive credit for their personal contributions. Accordingly, all
students in this course are expected to abide by scholarly norms and
University policies regarding academic integrity. These policies, and
resources about best practices to employ in order to abide by them, are
available through UChicago’s website. Violations of these standards,
even if “unintentional,” may result in serious sanctions.

### ChatGPT/CoPilot/LLMs/Generative AI

We are living in an exciting age! The advent of LLMs has transformed the
educational experience and programming is now fundamentally different
from prior educational experiences. It can be very tempting to use LLMs
such as ChatGPT and you are permitted to do so in this class under the
following conditions:

1.  You first attempt the assignment on your own
2.  You use AI to troubleshoot NOT in place of your own work
3.  You are capable of understanding what comes out of your model and
    you acknowledge that you are responsible for ALL work submitted in
    your assignments

#### Homework and AI statements

Every single assignment needs to include a statement about how/if you
used AI in the completion of the assignment (if you did not use it, you
can say so; if you used other sources, you can document them). For your
assignment, you need to document how you sought help, the prompts you
used, and how the model helped you move forward on your assignment.

In this particular class, you should aim to have ~95% of your work
completed solo, with your first stop for assistance either your
instructor or TA, then the web, and then ChatGPT / LLMs.

**Important Note** Just because AI is permitted does not mean that you
can use it to complete your assignment for you. If you are suspected of
using AI in some form to complete your assignment on your behalf, that
will not be tolerated and you will be immediately reported for a
violation of academic integrity.

## Access & Inclusion

Difference enhances both the teaching and learning experiences. The
classroom is a space where all students are welcome, regardless of age,
dis/ability, ethnicity, gender identity and/or expression, national
origin, race, religious non/belief, sex, sexual orientation,
socioeconomic status, and alignment with other identities or contexts.
Furthermore, if any student has a particular consideration, including
learning and participation style, that affects their ability to meet
course expectations, please see me as soon as possible. I am personally
committed to creating and maintaining an inclusive learning environment
for each and every student. Please, do not hesitate to contact me with
specific needs or concerns, and the sooner the better. Maintaining
transparency (and communication in general) with your instructor is not
only a good professional skill, but also a good way to develop a more
one-on-one relationship. Furthermore, accommodations are far easier and
effective to arrange when planned than when rushed. In short, I will
make every effort to ensure students equal access. Please let me know
how I can help make this class work for you.

My classroom is intended to be a constructive and critical space,
wherein all students feel comfortable engaging openly with the material,
each other, and oneself. However, this is only possible when everyone
commits to this endeavor. I expect you to do so, and to help your peers
(and me) to do the same. While I very much encourage (and celebrate)
dissent and/or debate, I will not tolerate disrespect in my classroom.
Please let me know if you feel the principles expressed in this syllabus
are not being upheld so that I can address it as soon as possible.

## Communication

I am generally available via email at the address above, and will do my
best to respond within 24 hours of contact during the week and 48 hours
on weekends–I try not to check email much on weekends FYI. In addition
to the office hours above, there will likely be time at the end of each
class meeting to discuss individual issues. Please do not hesitate to be
in touch with any questions or concerns. It’s helpful for me if you put
‘MACS 30500’ in the heading. I do ask that you check the syllabus before
contacting me because the answer you seek is most likely there already.

# FAQ

## What do I need for this course?

You will need a computer each day. Class sessions are a mix of lecture,
demonstration, and live coding. It is essential to have a computer so
you can follow along and complete the exercises. By the end of the first
week, you should make sure you can access the following software: \*
R. - the easiest approach is to select a pre-compiled binary appropriate
for your operating system.. \* RStudio’s IDE (available via Posit). -
this is a powerful user interface for programming in R. \* Git. - Git is
a version control system. which is used to manage projects and track
changes in computer files. Once installed, it can be integrated into
RStudio to manage your course assignments and other projects.
Comprehensive instructions for downloading and setting up this software
can be found here..

## How will I be evaluated?

Students will complete a series of (roughly) weekly programming
assignments linked to class materials.Each assignment will be evaluated
by myself or a TA. Assignments will initially come with starter code, or
an initial version of the program where you need to fill in the blanks
to make it work. As the quarter moves on and your skills become more
developed, less help upfront will be provided. While students are
encouraged to assist one another in debugging programs and solving
problems in these assignments, it is imperative students also learn how
to do this for themselves. That is, students need to understand, write,
and submit their own work.

## Weekly topics:

- Intro to computing
- Visualizations/grammar of graphics
- Data transformation
- Exploratory data analysis
- Pipes and functions
- Reproducible workflow
- Version control
- Web scraping
- Text analysis

### Acknowledgments

• This page has been developed starting from Benjamin Soltoff’s
“Computing for the Social Sciences” course materials, licensed under the
CC BY-NC 4.0 Creative Commons License and building on materials
developed by Sabrina Nardin. This version of the course also contains
novel assignments and slides created by Jean Clipperton.
