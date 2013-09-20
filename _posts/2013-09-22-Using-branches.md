---
layout: post
title:  Using branches
date:   2013-09-22 17:30:09
categories: lesson
---

# About isolated work areas ("branches")

* no collissions between multiple editors on the same file
* easy to compare the changes you make to the existing code
* have a staging area for an entire feature, not just a single change at a time
* infinitesimal storage space is used for branching
* switching between branches is incredibly fast
* git was built for branching

# Getting started with branches

You're already using a branch -- the default branch is called "master." To see a
list of branches run `git branch`.

Create a new branch to work on a feature. Lets pretend our app is used to keep
phone tree of all our party-animal frineds that we want to call on Friday night.

    git checkout -b call-list

You have now created a new branch and switched to it. Use `git branch` to
confirm the change.

The `checkout` command is used to switch between branches, and the `-b` flag
will create a branch if it doesn't yet exist.

# Making changes

Lets make a change to the README to indicate we'll be using a list of "animals"
and "plants" to categorize our contacts.

Then, make a new file called "animals.md" (`nano animals.md`) and put the
following contents in it:

    # Animals
    Who | Number | Animal Status
    ----|--------|--------------
    Jerry Springer | (123) 555 - 1212 | Level 7
    Hank Jr | (123) 555 - 1212 | Old Man Club

This will be the basic list.  Make a similar list for "plants.md" file.

# Git versus actual files

This is a good time to look at how what you've created and what you've asked git
to monitor can diverge.  Run `git status`.

Those untracked files need to be tracked!  `git add FILENAME` adds files to that
objects that git watches over. You can add multiple filenames at once: `git add
plants.md animals.md`.

Now when you commit, you will start tracking changes to those files. Go ahead
and do that with `git commit --all`.

# Compare to the base of the branch

Confirm that your changes are isolated. Checkout the master banch and look at
the files there. Checkout the call-list branch again. Confirm that the history
of the parent branch is included in the branch you made. `git log` shows the
commits made to a branch. Look back and find the commits that started on master.
`git diff master` will display the differences between the working branch and
master.

# Push this branch into github

Run `git push` to send this branch to github. Open your web browser to the
project's github page.

# Make a pull request in github

A pull request lets collaborators know there are changes to review and consider
for including in the project. Pull requests are the staple of collaboration in
the github workflow.

Once your pull request is open, review the files affected by the pull request.
Make a comment on one of the changes inline with the diff listing. Other
collaborators would get email from this comment and get a chance to respond or
update their code.

Once you have tinkered with the pull request, merge it. Merging is how branches
end up in the main product (the master branch).

# Delete your unused branch

Github will let you delete your branch, which will clean up the number of branch
references you see when you run the `git branch` command.  Don't worry, all the
commit history still exists, it is just a matter of hygene.

# Pull back to your local machine

The last few steps made extensive use of github to make some big changes to the
repository. Now it is time to make sure those changes are synced back to your
working copy.

Check out the master branch and run `git pull` to load the changes from github.

# Next Lesson

[Project Management][next-lesson]

[next-lesson]: ../23/Project-management.html
