# Git Version Control: Introduction to Version Control

## Learning Goals

- Define the purpose of a version control system
- Identify benefits of version control systems
- Recognize useful Git vocabulary terms

## Introduction

Let's imagine we're in the job market. We're going to apply for a job and we're
going to write a very simple text-based resume and store it in the file `my-
resume-January-2017.txt`.

We apply for the job, and we get it (congratulations!). We leave that resume
file with other downloaded cat GIFs, receipts, and emails on our desktop for a
few months. For the next three blissful, paid months, we don't think about our resume at all.

But when the three months are done, we are ready to find a new contract. We have
some new skills that we'd like to add to our resume, but we don't want to lose
our original resume from three months ago. We would like to create a new
_version_ of the resume.

A basic way of managing a new _version_ would be to copy `my-resume-
January-2017.txt` to `my-resume-April-2017.txt` and create a new _version_. We
could then create new _versions_ every time we need to apply for a new job. And
if we want to use more-or-less the same resume but want to emphasize different
skills, we can create a new version that focuses on that.

However, that will create several different files that we need to organize. As
we accumulate files, how can we best keep track of all the different versions
and changes?

The secret is to use a _version control system_. That is, software that
_controls_ our collection of _versions_.

## Define the Purpose of a Version Control System

"Version Control System" describes a whole group of software. VCS software
include Git, Mercurial, Subversion, and others. Some other web-based
applications like Google Docs have embraced this idea and have included tracked
changes or change history.

The key benefit of version control is that you can experiment and **throw away
bad ideas** and _instantly_ get back to your last known "good" state.

Think about it this way: when you were learning arithmetic, you knew the way to
undo a bad calculation was to turn the pencil upside down and erase. As a result
you were **free** to try, experiment, and explore, knowing you could always
easily get back to the original starting point. When we're learning, most of us
prefer to do our math homework in pencil, not ink!

> **ASIDE** The programmer, entrepreneur, and venture capitalist Paul Graham
> notes that oil paints unlocked a revolution in experimentation in visual arts
> because they were undo-able. Read more in his essay "Hackers and Painters."

While there are many version control systems, one of the most well-known and
widely-used is Git, which is the VCS we're going to use for our own code.

## Identify Benefits of Version Control Systems

Beyond the advantage of being able to safely experiement, there are several
other benefits of managing your work with a VCS like Git:

  - Automatically create a backup of your work
  - Provide an easy way to undo mistakes and restore a previous verison of your work
  - Document changes, including a log of what's changed with messages explaining why it was changed
  - Keep file names and hierachies consistent and organized
  - Branch work off into copies that can be edited in different ways at the same time
  - Collaborate with others without disturbing each other's work

And beyond these are even more advanced features that will help you optimize
your workflow, once you master the basics.

## Recognize Useful Git Vocabulary Terms

We're about to get busy learning Git, but we first need to establish some common
vocabulary. Git, perhaps more than any other software, has some special words
that you'll hear a lot. Don't worry if you're not sure how some of these terms
work in practice—that part will come later.

- **repository (or repo, for short)**: A directory of files that are _tracked_ by
  Git.
- **track**: When a file is _tracked_ by Git, it means that Git will notice any
  changes to that file, and will allow you to _add_ the change, or "diff."
- **diff**: Short for "difference," the "diff" of a repo is all the edits that have been _changed_, but have not yet been _committed_.
- **commit**: When a diff is decided to be a good thing to save, we _commit_ the
  diff to the repo's history using the `commit` command. When we make a commit we
are asked to add a "log" message which describes what happened in the diff.
- **log**: The record of what happened in each commit, including when the commit happened and which files had changes committed.
- **local/remote**: When we start working with a git repo, we "clone" it from a
  _remote_ source and have a copy of that directory on our own system. We call
  the repo on our personal system the _local_ repo. (We'll talk more about the
  "clone" command later.)
- **`master` branch**: You'll learn in advanced Git that a repo can support multiple
  branches. But for the moment, just remember this: by default, when you create a Git
  repo, you will be working on the `master` branch.
- **branch**: The combined history of all the histories of all the files in the repo.

## Conclusion

If we are afraid to edit our code we won't remove complicated code that's hard
to work with, try awesome new libraries, or take chances with fun new features.
Verson control helps us maintain the overall stability of our code so that we
can feel free to explore.

## Resources

* [Getting Started - About Version Control][about-version-control]
* [Git Basics - What is Git?][git-getstarted]

[about-version-control]: http://git-scm.com/book/en/Getting-Started-About-Version-Control
[git-getstarted]: http://git-scm.com/video/what-is-git
