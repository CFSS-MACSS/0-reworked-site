---
date: "2022-09-25T00:00:00-05:00"
draft: false
weight: 10
title: "What is Git?"
toc: true
type: docs
output:
  md_document:
    preserve_yaml: true
aliases: ["/git00.html", "/setup/what-is-git/"]
---

## Why Git?

In this course (and in your own work), you will be writing lots of
programs. Generally the first draft is not the final draft, be it a
research paper or a computer script. We want a way to track our changes
over time.

Perhaps this is to make sure we have a record of what we’ve already done
that doesn’t work, so we can avoid doing it again. Or maybe we want to
share our code with collaborators who are working on a project with us.
How can we do this?

One potential solution is to email copies of files back and forth as we
make changes. But if we do this, we risk having lots of versions of
files floating around. How do we know which is the most recent? What
happens if someone edits a file and forgets to email it to us? How will
we make sure all the changes are merged into the final version?

Or perhaps instead we can do all of our work on a cloud-based storage
solution such as [Dropbox](https://www.dropbox.com) or [Google
Drive](https://drive.google.com). This ensures changes are synchronized
between computers. But they are not specifically designed to share code,
and we won’t always know who made what changes to a file. And what
happens if two people want to work on the same file at the same time?
One person will have to wait for the other to finish before they can
edit that file. Plus how will we track previous versions of the file?
Dropbox and other cloud storage services have some [version control
solutions](https://www.dropbox.com/en/help/113), but these are not
comprehensive or only store versions for a limited time. Plus every time
we save a new version of the program, the entire file has to be
retained. On large projects, this will eat up storage space quickly.

We want a solution that:

- Keeps old versions of files indefinitely. Since all these versions are
  stored, we can always go back and see who modified the file and what
  changes they made. Or if we make a mistake in the future that breaks
  the program, we can revert back to an older version to fix it.
- Since we know who modified each file, if we have questions in the
  future we can go to that person with our questions.
- When collaborating with multiple people on the same project, and when
  code is involved, we want any changes made by project members to be
  integrated to the most recent version. If I try to modify a file and
  don’t incorporate another member’s revisions, I need to be told there
  is a conflict so I can merge all the changes.

## What is Git?

{{&lt; figure src=“<https://imgs.xkcd.com/comics/git.png>”
caption=“[*Git* by xkcd](https://xkcd.com/1597/)” &gt;}}

Git is a *version control system* originally created for developers to
collaborate on large software projects. Git tracks changes in the
project over time so that there is always a comprehensive, structured
record of the project. Each project is stored in a *repository* that
includes all files that are part of the project. As social scientists,
this is more than just computer scripts - this can include data files
and reports, as well as our source code.

Git can be used locally by you on a single computer to track changes in
a project. You do not need to be connected to the internet to use Git.
However, if you want to share your work with a larger audience, the
easiest solution is to host the repository on a web site for others to
download and inspect. You can host a public (open to the world) or
private (open to just you or a few individuals) repository.
[GitHub](https://www.github.com) is the most popular hosting service of
Git repositories and includes many useful features beyond the standard
Git functions. But notice, Git and GitHub are not the same thing: Git is
a version control system, GitHub is s a cloud-based hosting service that
lets you manage your Git repositories.

Chances are that by now you’ve seen or even used GitHub. Professionally,
you should know how to use Git and GitHub to manage projects and share
code. In this class, we will use Git and GitHub to host our course site,
share code, and distribute/collect assignments.

<!-- ## Acknowledgments -->
<!-- ```{r child = here::here("R", "_ack_stat545.Rmd")} -->
<!-- ``` -->
<!-- ```{r child = here::here("R", "_ack_swcgit.Rmd")} -->
<!-- ``` -->
<!-- ```{r child = here::here("R", "_ack_ben.Rmd")} -->
<!-- ``` -->
