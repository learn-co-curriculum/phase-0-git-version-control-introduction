# Introduction to Version Control

## Learning Goals

- Define the purpose of a version control system
- Identify benefits of version control systems
- Recognize useful Git vocabulary terms

## Introduction

Let's imagine a very stressful situation. Your manager comes to you and says:

> Hi there, we're looking to present a report to investors. If we get this
> investment, we'll all be millionaires. If we don't get this investment, we're
> going to have to close down the company. The key to success is going to be a
> report that **you** are going to manage. Three things will make it stand out:
>
> 1. It must be absolutely correct: no errors, no typos, the math has to check
>    out in every figure.
> 2. It must have the most up-to-date information
> 3. The investors will tolerate _slightly_ older data if it means that we can
>    be _sure_ the facts are correct.
>
> One last requirement is that for auditing purposes we need to be able to save
> a unique version of all the versions of this report. We have to know what the
> report looked like, for example, 3 days ago, or 3 weeks ago.
>
> Marge, Bob, and Amelia will all be doing research for you and contributing
> new data as much as possible. You have to make sure that all the parts
> integrate correctly. Thanks! And we're all counting on you!

How could you achieve these goals? Take a few minutes to imagine, or sketch out
what your strategy might be.

## Naive Strategy

A _naive_ way of managing _versions_ would be to start with a file called
`investor-report-latest.txt`. You'd also copy that to
`investor-report-master.txt`.

You'd share `investor-report-latest.txt` with Marge, Bob, and Amelia.

When they made a change to the report, you'd find the changes, verify them, and
then update them into `investor-report-master.txt`.

You'd make a copy of `investor-report-master.txt` and give it a date-stamp like
`investor-report-2019-02-13T1017.txt` (here you've added an [ISO8601][]
date-time label to the end of the file. This means when `ls` prints out the
directory all the file names will be shown in ascending date order).

You'd then overwrite `investor-report-latest.txt` with
`investor-report-master.txt` and tell everyone to start working off of the
newly updated `investor-report-latest.txt`.

Before long, we might have a directory full of files like:

```bash
investor-report-2019-1-01T1017.txt
investor-report-2019-1-02T1123.txt
investor-report-2019-1-04T4340.txt
investor-report-2019-1-05T1017.txt
investor-report-2019-1-08T2217.txt
investor-report-2019-2-08T2317.txt
investor-report-2019-2-09T0017.txt
investor-report-2019-2-10T914.txt
investor-report-2019-2-13T1017.txt
investor-report-2019-2-15T1127.txt
investor-report-2019-2-20T1237.txt
investor-report-2019-2-21T1330.txt
investor-report-2019-2-22T1545.txt
investor-report-latest.txt
investor-report-master.txt
...
```

Wow! What a mess! And there are other messes waiting.

What if Amelia and Marge both start work from the latest
`investor-report-latest.txt` and Amelia makes changes to the same section Marge
was working on. Amelia gets her work in first and that gets integrated by you.
Now Marge's changes no longer apply. Marge is frustrated because her work will
have to be re-done!

## Reflection

This is a pretty stressful bit of imagination. You've got to make sure that a
report is as current as possible and absolutely, positively, correct. You might
think this manager is a jerk or that these expectations are unreasonable. Maybe
this could be possible with _one_ writer, not _four_.

But the expectations that manager gave you for the report are ***the exact same
expectations we have for code***. It should be as good as possible, absolutely
correct, and ready to ship to users at a moments' notice.

The great news is that _all_ the manual work you had to do (and so much more!)
can be done by a type of software called a _version control system (VCS)_. That
is, software that _controls_ our collection of _versions_. The most popular VCS
is called "Git." When we have a VCS on our side we can work confidently; we can
even experiment without fear. Getting back to a "last known good state" is just
a few key-clicks away. You're going to love writing code, text, letters,
knowing a VCS is on your side!

## Define the Purpose of a Version Control System

"Version Control System (VCS)" describes a whole group of software. VCS
software includes Git, Mercurial, Subversion, and others. Some other web-based
applications like Google Docs have embraced the idea of "versions" and have
added features like "tracked changes" or "view change history."

The key benefit of version control is that you can experiment and **throw away
bad ideas** and _instantly_ get back to your last-known "good" state.

Think about it this way: when you were learning arithmetic, you knew the way to
undo a bad calculation was to turn the pencil upside down and erase. As a result,
you were **free** to try, experiment, and explore, knowing you could always
easily get back to the original starting point. Because of this, most of us
did our math homework in pencil, not ink!

Because of the **freedom** that VCS provides, we can be **unafraid** to look
at an ugly bit of code and _try_ something new. We can take a new technique a
co-worker told us about and we can _try_ to replace our old code with this new idea.
We can read about a new feature provided in a framework and _try_ it out in our
old code. **VCS helps us be unafraid to try new and improved techniques**.

> **ASIDE** The programmer, entrepreneur, and venture capitalist Paul Graham
> notes that oil paints unlocked a revolution in experimentation in visual arts
> because they were undo-able. Oils provided the **freedom** to err and recover
> that other paint media did not provide (e.g. watercolor). Because of this
> **freedom** these painters were free to explore perspective, light, and
> composition in completely new ways. Because of their _tools_ they had more
> _freedom_ and were able to make their burst of exploration a _movement_: The
> Renaissance.  
> 
> Read more in his essay ["Hackers and Painters."][hp]

## Identify Benefits of Version Control Systems

Beyond the advantage of being able to safely experiment, there are several
_other_ benefits we get when we manage our work with Git:

  - Automatically create a backup of your work
  - Provide an easy way to undo mistakes and restore a previous version of your work
  - Document changes, including a log of what's changed with messages explaining why it was changed
  - Keep file names and hierarchies consistent and organized
  - Branch work off into multiple "sandboxes" that can be experimented with but won't impact each other
  - Collaborate with others without disturbing each other's or our own work

And beyond these are even more advanced features that will help you optimize
your workflow, once you master the basics. If that feels daunting, it's OK. Most
people learn a few patterns of Git and never learn more until they absolutely
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
  happened in it since the last _commit_. The "diff" of a repo is all the diffs
  in all the _tracked_ files in the _repo_ that have been made, but which have not
  yet been _committed_ (sometimes programmers call this "the diffset").
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
Version control helps us maintain the overall stability of our code so that we
can feel free to explore.

## Resources

* [Getting Started - About Version Control][about-version-control]
* [Git Basics - What is Git?][git-getstarted]

[about-version-control]: http://git-scm.com/book/en/Getting-Started-About-Version-Control
[git-getstarted]: http://git-scm.com/video/what-is-git
[hp]: http://www.paulgraham.com/hp.html
[ISO8601]: https://en.wikipedia.org/wiki/ISO_8601
