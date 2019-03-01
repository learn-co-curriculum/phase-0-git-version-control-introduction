# Introduction to Version Control

## Learning Goals

- Define the purpose of a version control system
- Identify benefits of version control systems
- Recognize useful Git vocabulary terms

## Introduction

Let's imagine we're in the job market. We're going to apply for a job and we're
going to write a very simple text-based resume and store it in the file
`my-resume-January-2017.txt`.

We apply for the job...and we get it! When we start working we forget about
our resume and leave it, forgotten, on our Desktop 
with downloaded cat GIFs, receipts, and emails.
For the next three blissful, paid months, we don't think about our
resume at all.

But when the three months are done, we are ready to find a new contract. We have
some new skills that we'd like to add to our resume, but we don't want to lose
our original resume from three months ago. We would like to create a new
_version_ of the resume.

A _basic_ way of managing a new _version_ would be to copy `my-resume-
January-2017.txt` to `my-resume-April-2017.txt` and create a new _version_. We
could plan to create new _versions_ every time we need to apply for a new job **or**
if we want to highlight different
skills.

Before long, we might have a directory full of files like:

```bash
my-resume-January-2017.txt
my-resume-April-2017-full-stack.txt
my-resume-April-2017-full-stack-JavaScript-focused.txt
my-resume-April-2017-full-stack-JavaScript-focused-angular.txt
my-resume-April-2017-full-stack-JavaScript-focused-react.txt
my-resume-April-2017-full-back-end-ruby.txt

my-resume-April-2017-full-stack.txt
my-resume-April-2017-full-stack-JavaScript-focused.txt
my-resume-April-2017-full-stack-JavaScript-focused-angular.txt
my-resume-April-2017-full-stack-JavaScript-focused-react.txt
my-resume-April-2017-full-stack-JavaScript-focused-react-hooks.txt
my-resume-April-2017-full-stack-JavaScript-focused-vue.txt
my-resume-April-2017-full-back-end-ruby.txt
my-resume-April-2017-full-back-end-python.txt
...
```

Wow! What a mess! Multiple files is a good strategy for a _basic_ version
strategy, but software developers generate many, many updates to many, many files.
This strategy simply will not work. We need software to help.

The secret is to use a _version control system_. That is, software that
_controls_ our collection of _versions_.

## Define the Purpose of a Version Control System

"Version Control System (VCS)" describes a whole group of software. VCS software
include Git, Mercurial, Subversion, and others. Some other web-based
applications like Google Docs have embraced the idea of "versions" and have
added features like "tracked changes" or "view change history."

The key benefit of version control is that you can experiment and **throw away
bad ideas** and _instantly_ get back to your last-known "good" state.

Think about it this way: when you were learning arithmetic, you knew the way to
undo a bad calculation was to turn the pencil upside down and erase. As a result,
you were **free** to try, experiment, and explore, knowing you could always
easily get back to the original starting point. When we were learning, most of us
did our math homework in pencil, not ink!

Because of the **freedom** that VCS provides, we can be **unafraid** to look
at an ugly bit of code and _try_ something new. We can take a new technique a 
co-worker tellus about and we can _try_ to replace our old code with this new idea.
We can read about a new feature provided in a framework and _try_ it out in our 
old code. **VCS helps us be unafraid to try new and improved techniques**.

> **ASIDE** The programmer, entrepreneur, and venture capitalist Paul Graham
> notes that oil paints unlocked a revolution in experimentation in visual arts
> because they were undo-able. Because of the **freedom** that oils provided, 
> Italian Renaissance painters were able to create the revolutions in constructing
> painting that made the leaps of the renaissance so important. Read more in his
> essay ["Hackers and Painters."][hp]

## Identify Benefits of Version Control Systems

Beyond the advantage of being able to safely experiement, there are several
_other_ benefits we get when we manage our work with Git:

  - Automatically create a backup of your work
  - Provide an easy way to undo mistakes and restore a previous verison of your work
  - Document changes, including a log of what's changed with messages explaining why it was changed
  - Keep file names and hierarchies consistent and organized
  - Branch work off into multiple "sandboxes" that can be experimented with, but won't impact each other
  - Collaborate with others without disturbing each other's or our own work

And beyond these are even more advanced features that will help you optimize
your workflow, once you master the basics. If that feels daunting, it's OK. Most
people learn a few patterns of Git and never lean more until they absolutely
have to. Over years they build up a rich set of techniques, but it's rare to find
someone who knows **everything** about Git. You don't need to memorize every command
and optional flag to get some of its best benefits.

## Recognize Useful Git Vocabulary Terms

We're about to get busy learning Git, but we first need to establish some common
vocabulary. Git, perhaps more than any other software, has some special words
that you'll hear a lot. Don't worry if you're not sure how some of these terms
work in practice—that part will come later.

- **repository (or repo, for short)**: A directory of files that are _tracked_ by
  Git.
- **track**: When a file is _tracked_ by Git, it means that Git will notice any
  changes to that file. We call these changes "differences" or "diffs". Git will
  allow you to choose whether to _add_ the change, or "diff," in order to keep it
- **diff**: Short for "difference," the "diff" of a file is all the changes that
  happened in it since the last _commit_. The "diff" of a repo are all the diffs
  in all the _tracked_ files in the _repo_ that have been made, but which have not
  yet been _committed_.
- **commit**: When a diff is decided to be a good thing to save, we _commit_ the
  diff to the repo's history using the `commit` command. When we make a commit we
  are asked to write a "log" message which describes what happened in the diff.
  Each commit also knows when it happened and what the repo's "diff" was.
- **log**: The record of what happened in each commit
- **local/remote**: When we start working with a git repo, we "clone" it from a
  _remote_ source and have a copy of that directory on our own system. We call
  the repo on our personal system the _local_ repo. (We'll talk more about the
  "clone" command later.)
- **`master` branch**: You'll learn in advanced Git that a repo can support multiple
  branches (we called those "sandboxes" earlier). For the moment, just remember this:
  by default, when you create a Git repo, you will be working on the `master` branch.
- **branch**: The combined history of all the changes of all the files in the repo.

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
[hp]: http://www.paulgraham.com/hp.html
