---
date: "2018-09-09T00:00:00-05:00"
draft: true
weight: 70
title: "Cache credentials"
toc: true
type: docs
output:
  md_document:
    preserve_yaml: true
aliases: ["/git07.html", "/setup/git-cache-credentials/"]
---

**You only have to do this once per machine.**

## Why cache credentials?

As you have probably gathered by now, it will be annoying to enter your
username and password each time you push changes to GitHub. It may even
discourage you from pushing as frequently as you should. By storing your
credentials on the computer, you won’t have to authenticate yourself
manually each time you push to GitHub, and your credentials will be
stored in a secure manner.

{{% callout note %}}

As of January 2019, if you install Git using [these
instructions](/setup/git/), it is possible that Git will use a
credential helper provided by your operating system. That is, you may
not need to do anything special in order to cache your GitHub username
and password. Specifically, if you are on macOS or Windows, don’t do
anything described here until you have actual proof that it’s necessary,
i.e. that you have experienced repeated challenges for your username and
password when attempting to push/pull to GitHub.

{{% /callout %}}

## Get a test repository

You need a functioning test Git repository. One that exists locally and
remotely on GitHub, with the local repo tracking the remote. If you just
setup [Git with GitHub](/setup/github/), you have a test repository. If
you setup [Git to work within RStudio](/setup/git-with-rstudio/), you
have a test repository. If you already deleted those repositories, set
one of them back up again.

You may proceed when

- You have a test repo.
- You know where it lives on your local computer. Example:
  - `/home/benjamin/Github/myrepo`
- You know where it lives on GitHub. Example:
  - `https://github.com/bensoltoff/myrepo`
- You know local is tracking remote. In a [shell](/setup/shell/) with
  working directory set to the local Git repo, enter these commands:

<!-- -->

    benjamin-laptop:Github benjamin $ git remote -v
    origin  https://github.com/bensoltoff/myrepo (fetch)
    origin  https://github.com/bensoltoff/myrepo (push)

    benjamin-laptop:Github benjamin $ git branch -vv
    * main b8e03e3 [origin/main] line added locally

We want to see that fetch and push are set to remote URLs that point to
your GitHub repo. We also want to see that your local main branch has
your GitHub main branch as upstream remote. Gibberish? Just check that
your output looks similar to this.

## Verify Git is up-to-date

In a shell, enter `git --version` and verify that you have 1.7.10 or
newer. If you don’t, update Git.

## Turn on the credential helper

### Windows

In the shell, enter `git config --global credential.helper wincred`

### Mac

Find out if the credential helper is already installed. In the shell,
enter `git credential-osxkeychain`. You should see something like this:
`Usage: git credential-osxkeychain <get|store|erase>`. If you do not,
follow step 2 on the [GitHub help
page](https://help.github.com/articles/caching-your-github-password-in-git/#platform-mac).

Once you’ve confirmed you have the credential helper, enter
`git config --global credential.helper osxkeychain`.

### Linux

In the shell, enter
`git config --global credential.helper 'cache --timeout=10000000'` to
store your password for ten million seconds (that’s roughly 16 weeks).

## Trigger a username/password challenge

Change a file in your local repo and commit it. Do that however you
wish. Here are shell commands that will work:

    echo "adding a line" >> README.md
    git add -A
    git commit -m "A commit from my local computer"

Now push!

    git push -u origin main

One last time you will be asked for your username and password, which
hopefully will be cached.

Now push AGAIN.

    git push

You should NOT be asked for your username and password, instead you
should see `Everything up-to-date`.

Rejoice and close the shell. From now on your “Push” button in RStudio
will just work.

## More options: SSH

Secure Shell (SSH) is an alternative method for authenticating trusted
computers without using a password. There are some benefits to this
approach over HTTPS, however it is generally more complicated to
initially set up. If you wish to use this approach, see
[here](https://help.github.com/articles/generating-an-ssh-key/) for
instructions on generating an SSH key and pairing it with your GitHub
account.

<!-- ## Acknowledgments -->
<!-- ```{r child = here::here("R", "_ack_stat545.Rmd")} -->
<!-- ``` -->

- [“Chapter 10: Cache credentials for HTTPS” from Happy Git and GitHub
  for the useR](https://happygitwithr.com/credential-caching.html)
