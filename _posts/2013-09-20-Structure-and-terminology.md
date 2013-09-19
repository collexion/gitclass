---
layout: post
title:  "Git Structure and Terminology"
date:   2013-09-20 17:30:09
categories: lesson
---

# Repository

Code will live in a repository. On your local machine, it looks like any other
directory (folder, in Windows terminology). We will create a repository using
github and download it to our machines. We could also use git to create the
repo locally and then push it up to github.

# Remotes (origin)

Git is a distributed system, meaning the code can live many places at once, and
be shared between all of them. Typically all developers use their own system and
a common remote called "origin". We will be use github as our common origin.

# Commit

Changes you make to the code are "commited" to the repository. After they are
commited they can be shared with other developers. Newly created files will need
to be added to the repository (eg, using `git add`) before git will detect them.

# Push

To send newly commited code to other developers, we will push the code to the
remote that everyone esle is looking to pull their source from.

# Pull

We get changes others have made to the code by pulling the changes from a
remote.

# Branch (master)

A branch is a method of isolating changes. The default branch is called master.
By creating a new branch before you make changes you isolate your changes so you
don't have conflicts with work other people are performing. You also make it
easier to reivew your changes in the context of the larger project.

# Next Lesson

[Hands on with git][start-git]

[start-git]: ../21/Start-git.html
