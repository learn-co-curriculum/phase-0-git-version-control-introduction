# Git Version Control: Introduction to Version Control

## Learning Goals

- Define the purpose of a version control system
- Identify examples of version control systems
- Describe high-level features of Git
- Identify Git vocabulary terms

## Introduction

Imagine you have a document file saved on your computer as your resume, titled `my-resume-2017.txt`. You created this file in 2017, and in 2019 you decided to update the information in it—but you didn't want to lose the first version. So you make a copy of the file, name it `my-resume-2019.txt`, and make changes to the information. Likely, you will want to add an employer name or adjust the amount of time at a job. You then have two files that capture two different snapshots of that document's history, and you can access, reproduce or edit either version whenever you like. Whether you realize it or not, you're managing your resume with a version control system.

## Define the Purpose of a Version Control System

- Version control is a system that saves and tracks changes to files so that you can later access specific versions of those files.
- We use a VCS in code to keep track of all the changes we, and our team members, make to code as time goes on.
- also called "revision control" or source control management"
- key advantages of version control:
  - backup
  - undo mistakes
  - document changes
    - see what's changed
    - use messages to understand why it's changed
  - test new work in a "sandbox"
  - create copies of work (branches)
  - collaborate among teams
- VCS is even better than snapshots, because it also allows us to record the intention of the change.

## Identify Examples of Version Control Systems

- recall resume document example as demonstration of VCS in principle
- there are several version control systems that manage code
  - Subversion, Mercurial, CVS
  - most widely used and known is Git
- define Git

## Describe High-Level Features of Git

- branches
- diffs
- revision history
- sharing history

## Identify Git Vocabulary Terms

- a quick run-down of terms used a lot with Git, just to establish their general meaning
- technical info on how they relate to commands comes in the next lesson

- repository (repo)
- local/remote
- master branch
- check in/out
- log
- pull/push
- merge

## Conclusion

Version control is a powerful tool to use when creating and maintaining projects. The commonly-used VCS called Git provides us with a number of features and actions for keeping our code clean, organized and complete.

## Resources

* [Getting Started - About Version Control][about-version-control]
* [Git Basics - What is Git?][git-getstarted]

[about-version-control]: http://git-scm.com/book/en/Getting-Started-About-Version-Control
[git-getstarted]: http://git-scm.com/video/what-is-git
