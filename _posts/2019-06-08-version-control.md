---
title: "Version Control"
excerpt: "Overview and guidance for using version control systems, such as Git."
date: 2023-08-07
toc: true
categories:
  - Developer Resources
tags:
  - git
  - GitHub
  - software
  - developer resources
---

## What is version control?

[Version control](https://build-me-the-docs-please.readthedocs.io/en/latest/Using_Git/OnVersionControl.html) tracks the changes to files and allows for revisions backward to previous versions. There are many systems of [version control](https://en.wikipedia.org/wiki/List_of_version-control_software).

## Which version control system should I use?

We recommend using [`Git`](https://git-scm.com/) for tools in the NOAA Fisheries Integrated Toolbox, as it is widely used and integrates well with our infrastructure. `Git` is a "distributed model" of version control. In distributed models of version control, individual contributors work directly in their repository, and then changes are shared and merged between repositories as a separate step. Git is free and open-source software distributed under the terms of the GNU General Public License version 2.

## How do I use `Git`?

### Installing Git

Follow the general installation [directions](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git). You will need administrative privileges to install. 

### Setup and Getting started with Git

Once installed, you'll need to configure Git with your identity information. The user name and user email you use for Git will be needed later for setting up your GitHub account. For work, use your noaa.gov email address.

Git can be used at the command line (e.g., Powershell or from Git bash downloaded when you download Git) or with [graphical user interfaces](https://git-scm.com/downloads/guis) depending on your preferences. IDEs such as VScode and Rstudio include Git user interfaces.

A great reference for setting up and using Git for R users is the [Happy Git and GitHub for the useR book](https://happygitwithr.com/).

The [Get Going with Git](https://git-scm.com/video/get-going) contains information on how to set up Git using the command line.

If you would like to use multiple accounts (e.g., work and personal GitHub accounts) on the same computer, see [using multiple accounts](https://noaa-fisheries-integrated-toolbox.github.io/resources/noaa%20resources/github-account/#multiple-identities).

### Using Git with a server system (e.g., GitHub)

Although you could just use Git locally for version control, it is best to use with a server system (e.g., GitHub).  Locally, Git alone will allow you to track and revert changes. By using it in conjunction with a server, you'll have your code and a history of changes stored off of your computer and be able to easily collaborate.

There are many open-source and private systems that offer Git Server as a Service that each has additional tools and benefits.  The main one being the ability to push code to a server for backup and easy collaboration. Some of the  systems are:
- [GitHub](https://github.com/)
- [Gitlab](https://about.gitlab.com/)
- [Bitbucket](https://bitbucket.org/)

For NOAA Fisheries Integrated Toolbox tools, we recommend GitHub for maximum integration with the toolbox; however, other server systems will also work.

For more information about using Rstudio with Git and Github, see the [Practical R workflow workshop series](https://rverse-tutorials.github.io/RWorkflow/intro-git.html).

## Basic Git workflows

There are many ways to work with Git and GitHub, and there is no "one size fits all" solution.
Using Git and GitHub on your own can be as simple as making commits and pushing
them up to your main branch.

However, as you collaborate with more people, more complex workflows are necessary
to help organize changes being done simultaneously. [GitHub flow](https://docs.github.com/en/get-started/quickstart/github-flow) is common while working on GitHub, but [other workflows](https://www.atlassian.com/git/tutorials/comparing-workflows) are valid. What is important is for the group working together 
to decide on a workflow and modify it as needed so that it works for them.

### Some helpful Git commands

- [The Git Everyday page](https://git-scm.com/docs/giteveryday) shows the most commonly used Git commands based on role.
- For Git and GitHub users, [this Git and GitHub reference guide](https://training.github.com/downloads/github-git-cheat-sheet/) may provide a quick summary of useful information.
