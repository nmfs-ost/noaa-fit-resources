---
title: "Version Control"
excerpt: "Version control"
date: 2021-07-30
toc: true
categories:
  - Developer Resources
tags:
  - git
  - GitHub
  - software
  - developer resources
---

There are many resources available on version control. Here is a simple overview as it relates to the NOAA Fisheries Integrated Toolbox. 

## What is version control?

Simply, version control tracks the changes to files and allows for revisions backward to previous versions ( [more](https://build-me-the-docs-please.readthedocs.io/en/latest/Using_Git/OnVersionControl.html
) ).
There are many types of [version control](https://en.wikipedia.org/wiki/List_of_version-control_software).


We will focus here on the Distributed Model:

In this approach individual contributors work directly (generally locally) in their repository, and changes are shared and merged between repositories as a separate step.
Although there are several open source tools available for this approach, we use [Git](https://en.wikipedia.org/wiki/Git).

- Git is a distributed version control system for tracking changes in source code during software development. It is designed for coordinating work among programmers, but it can be used to track changes in any set of files. Its goals include speed, data integrity, and support for distributed, non-linear workflows.
- Git was created by Linus Torvalds in 2005 for development of the Linux kernel, with other kernel developers contributing to its initial development. Its current maintainer since 2005 is Junio Hamano.
- As with most other distributed version-control systems, and unlike most client-server systems, every Git directory on every computer is a full-fledged repository with a complete history and full version-tracking abilities, independent of network access or a central server.
- Git is free and open-source software distributed under the terms of the GNU General Public License version 2.


## [GIT](https://git-scm.com/)
### Installing GIT
General installation [directions](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
You will need administrative privileges to install.  Git can be used at the command line or with graphical user interfaces depending on your preferences. Herein we focus on command line information.

Once installed, you'll need to configure git with your identity information.
The user name and user email you use for git will be needed later for setting up your GitHub account.  It is likely you may need to set up a system to track your identity for both work and personal use.  See [using multiple accounts](https://noaa-fisheries-integrated-toolbox.github.io/resources/noaa%20resources/github-account/#multiple-identities) if this is the case.

Although you could just use Git locally for version control, it is best to use with a server system.  Locally, Git alone will allow you to track and revert changes.  By using it in conjunction with a server, you'll have backups of your code and be able to easily collaborate.

### GIT Server as a Service
There are many open-source and private systems that offer Git Server as a Service that each has additional tools and benefits.  The main one being the ability to push code to a server for backup and easy collaboration.  Some of the  systems are:
- [GitHub](https://github.com/)
- [Gitlab](https://about.gitlab.com/)
- [Bitbucket](https://bitbucket.org/)

## Basic GIT workflows
The following offers a basic Git workflow using the command line. For more information about using Rstudio with Git and Github, see the Practical R workflow workshop series or [these resources](https://noaa-fisheries-integrated-toolbox.github.io/resources/noaa%20resources/github-account/#general-information-and-resources-for-using-github)

Starting from scratch:
1. Make a directory folder on your computer where you will work
2. Initialize it as a  git repo by  changing directory to within that folder and calling the command at the command prompt:

```git init```

Check that the user config for the repo is correct.

If you have multiple identities, it is a good idea to check which identity this folder is using and change it if necessary.

```
   git config user.email
   git config user.name
```

3. create a README document as text or markdown which will hold basic information about your code repository

```
   echo README.md > README file for Repo Name
   git add README.md
   git commit -m"addd readme"
```

4. go onto GitHub and create an empty repository

    git push main ssh... -u

Once you are set up you will want to get into a standard git [workflow](https://www.atlassian.com/git/tutorials/comparing-workflows) where you commit changes locally often and push to your remote main at least daily if changes have been made or when many changes have occurred.  Committing often will help when you want to revert (go backward) or if you are actively working with several others

### Branching
Branching can be thought of as creating a copy of your code with a flag at the point where you started the branch.  This allows you to try out a different path or set of function.  It is good practice when you are adding a new feature to solid working code or working on a significant piece of code that will likely need to be incorporated to the larger code base at a later time.  If you do not like it then you can always just go back to your branching point.  You may choose to use local branches only and merge your code or send your branch up to the main repository.  Good practice dictates not having several "orphan" branches  or using branches as specific features;  Once a branch is ready to be merged into the main repository, the branch should be deleted so it does not cause any confusion in the development process

### Helpful git commands
Quick reference [guide](https://git-scm.com/docs)

| Command | Description |
| ------------- | --------- |
| `git stash` | [Hold onto all changes since the last commit and save for the future but change back my working files to the last commit](https://git-scm.com/docs/git-stash) |
| `git stash pop` | [Put back the changes stashed](https://git-scm.com/docs/git-stash#Documentation/git-stash.txt-pop--index-q--quietltstashgt) |
| `git revert` | [Undo some of the previous commits](https://git-scm.com/docs/git-revert) |
| `git remote -v` | [Show the address of the remote server this repo is set up to push to](https://git-scm.com/docs/git-remote) |
| `git checkout -b name` | Create a new branch called "name" and check it out locally to work on |
