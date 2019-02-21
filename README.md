# Git Version Control: Introduction to Version Control

## Learning Goals

- Define the purpose of a version control system
- Recognize Benefits of Version Control Systems
- Identify Git vocabulary terms

## Introduction

Let's imagine we're in the job market. We're living the fabulous digital nomad
lifestyle (working from the beaches of Koh Samui, Thailand, this time) and we
want to land a 3-month contract for the duration of our visa.

We're going to apply for a job and we're going to write a very simple
text-based resume and store it in the file `my-resume-January-2017.txt`.

We apply for the job, and, (congratulations!) we get it. We leave that resume
file with other downloaded cat GIFs, receipts, and emails on our desktop for a
few months. The job is for three months and we don't think about our resume in the
blissful, paid weeks that go by.

Three months later, we are ready to find a new contract. We have some new
skills that we'd like to add on to our resume, but we don't want to lose our
original resume from three months ago. We would like to create a new _version_
of the resume.

A basic way of managing a new _version_ would be to copy
`my-resume-January-2017.txt` to `my-resume-April-2017.txt` and create a new
_version_. We could then create new _versions_ every time we need to apply for
a new job. And what about the case where we want to use (more-or-less) the same
resume, but maybe want to emphasize different skills. How are we going to keep
all those versions organized? The secret is to use a _version control system_.
That is, software that _controls_ our collection of _versions_.

## Recognize Benefits of Version Control Systems

"Version Control System" describes a whole group of software. Graphics Programs
includes Photoshop and Illustrator and MS-PAINT. Version Control System
software include Git, Mercurial, Subversion, and others. Some other web-based
applications like Google Docs have embraced this idea and have included
"tracked changes" or "change history."

Ultimately, while it's **awesome** to have backup of your work, one of the
biggest benefits of version control is that you can experiment and **throw away
bad ideas** and _instantly_ get back to your last known "good" state. Think
about it this way, when you were learning arithmetic, you knew how to undo a
bad calculation: turn the pencil upside down and erase. As a result you were
**free** to try and experiment and explore knowing you could always get back to
the original problem easily. When we're learning, most of us prefer to do our
math homework in pencil, not ink!

If we are afraid to edit our code we won't remove complicated code that's hard
to work with. If we are afraid to edit our code, we wont' want to try awesome
new libraries. So, Git lets us feel free to explore!

> **ASIDE** The programmer, entrepreneur, and venture capitalist Paul Graham
> notes that oil paints unlocked a revolution in experimentation in visual arts
> because they were undo-able. Read more in his essay "Hackers and Painters."

- Version control is a system that saves and tracks changes to files so that you can later access specific versions of those files.
- We use a VCS in code to keep track of all the changes we, and, later, our team members, make to code as time goes on.
- also called "revision control" or source control management"
- key advantages of version control:
  - backup
  - consistent file naming (`resume.txt` versus `resume-09102018.txt`, `resume-09102019.txt)`
  - undo mistakes
  - document changes
    - see what's changed
    - use messages to understand why it's changed
  - test new work in a "sandbox"
  - create copies of work (branches)
  - collaborate among teams
- VCS is even better than snapshots, because it also allows us to record the intention of the change.
- logging: we can keep track of the date we made the change, what exactly we changed, and a short description why
- And more... (advanced features)
  - branches
  - diffs
  - revision history
  - sharing history
  - Code collaboration and sharing via GitHub

## Identify Git Vocabulary Terms

We're about to get busy learning Git, but we need to establish some common
vocabulary. Git, perhaps more than any other software, has some special words
that _seem like they're the same_....blah

- a quick run-down of terms used a lot with Git, just to establish their general meaning
- technical info on how they relate to commands comes in the next lesson

- diff: Short for "difference" the "diff" of a repo is all the ***changed, but
  not committed edits to the files in the repo***
- commit: When a diff is decided to be a good thing to save, we _commit_ the
  diff to the repo's history using the commit command. When we make a commit we
are asked to add a "log" message which describes what happened in the diff
  (e.g. added Mr. Pajamas as a cat I known in `cats.txt`)
- repository (repo, for short): A directory that has files that are _tracked_ by
  Git
- track: When a file is _tracked_ by Git, it means that Git will notice any
  changes to that file, and will allow you to _add_ the change ("diff") and
  _commit_ the change to be part of the file's _history_
- local/remote: When we start working with a git repo, we "clone" it from a
  remote source and have a "clone" of that directory on our own system. We call
  the repo on our personal system the "local" repo. We'll talk more about the
  "clone" command later.
- `master` branch: You'll learn in advanced git that a repo can support multiple
  branches. But for the moment, accept this: by default, when you create a git
  repo, you will be working on the `master` branch.
- branch: A simple definition is: the combined history of all the histories of
  all the files in the repo
- log: The logfile of what happened in each commit. The log can be investigated
  to show the diff between commits


(broaded ad lib.)

## Conclusion

Version control is a powerful tool to use when creating and maintaining projects. The commonly-used VCS called Git provides us with a number of features and actions for keeping our code clean, organized and complete. Remember: mastering Git makes you FREE to experiment and LEARN from your code.

## Resources

* [Getting Started - About Version Control][about-version-control]
* [Git Basics - What is Git?][git-getstarted]

[about-version-control]: http://git-scm.com/book/en/Getting-Started-About-Version-Control
[git-getstarted]: http://git-scm.com/video/what-is-git
