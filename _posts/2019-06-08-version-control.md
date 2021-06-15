---
title: "Version-Control"
excerpt: "Overview of version control"
date: 2019-06-02
toc: true
categories:
  - onboarding
tags:
  - version-control
  - git
  - github
---

There are many resources available on version control.  Here is a simple overview as it relates to the NOAA Fisheries Integrated Toolbox.

## What is version control?

Simply, version control tracks the changes to files and allows for revisions backward to previous versions ( [more](https://build-me-the-docs-please.readthedocs.io/en/latest/Using_Git/OnVersionControl.html
) ).
There are many types of [version control](https://en.wikipedia.org/wiki/List_of_version-control_software).


We will focus here on the Distributed Model:
In this approach individual contributors work directly ( generally locally) in their repository, and changes are shared and merged between repositories as a separate step.
Although there are several open source tools available for this approach. We use [Git](https://en.wikipedia.org/wiki/Git).

> Git is a distributed version control system for tracking changes in source code during software development.[8] It is designed for coordinating work among programmers, but it can be used to track changes in any set of files. Its goals include speed,[9] data integrity, and support for distributed, non-linear workflows.

> Git was created by Linus Torvalds in 2005 for development of the Linux kernel, with other kernel developers contributing to its initial development. Its current maintainer since 2005 is Junio Hamano.

> As with most other distributed version-control systems, and unlike most client-server systems, every Git directory on every computer is a full-fledged repository with a complete history and full version-tracking abilities, independent of network access or a central server.

> Git is free and open-source software distributed under the terms of the GNU General Public License version 2.

## [GIT](https://git-scm.com/)
### Installing GIT
General installation [directions](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
You will need administrative privileges to install.  Git can be used at the command line or with graphical user interfaces depending on your preferences. Herein we focus on command line information.

Once installed, you'll need to configure git with your identity information.
The user name and user email you use for git will be needed later for setting up your GitHub account.  It is likely you may need to set up a system to track your identity for both work and personal use.  See information below on using multiple accounts if this is the case.

Although you could just use Git locally for version control, it is best to use with a server system.  Locally, Git alone will allow you to track and revert changes.  By using it in conjunction with a server, you'll have backups of your code and be able to easily collaborate.


## GIT Server as a Service
There are many open-source and private systems that offer Git Server as a Service that each has additional tools and benefits.  The main one being the ability to push code to a server for backup and easy collaboration.  Some of the  systems are:
- [GitHub](https://github.com/)
- [Gitlab](https://about.gitlab.com/)
- [Bitbucket](https://bitbucket.org/)

We will focus on the use of GitHub herein.


### Creating a GitHub account
- General information on [creating a GitHub account](https://help.github.com/en/articles/signing-up-for-a-new-github-account);
 - For NOAA specific users there are specific requirements ( some listed in the NOAA checklist) which include but are not limited to:

1. User-specific:
- NOAA users must have a GitHub account using their NOAA email
- They must have a photo of themselves associated with the account
- They must use 2-factor authentication
- They can only have NOAA related work under their account

>**Note**: it is good practice that your GitHub user name for NOAA is FirstLast-NOAA which clearly identifies it as an NOAA linked account versus a personal account.

2. Repository specific:
- Only allowing write access to NOAA users
- All non-NOAA users can only have pull-request access
- Must include a disclaimer in the README 
- Must include specific wording in License 
- Must have a "gold standard" backup of the repo


> **Note**: If you have multiple GitHub identities (perhaps a personal one and a work one).  You will want to be careful about which identity you use.  See Multiple Identities below to set up automated ways of dealing with this.


### Multiple Identities
There are various ways to deal with multiple identities.
To check which identity you are using inside of a git repository by default
'''
git config user.name
gi config user.email
'''
- you can set user.name and user.email for each repository as you go.  This works however, there is a global setting and if you forget to initialize your repository with the correct credentials , the global choice will be used
- better: set up a .gitconfig to deal with multiple identities

For more information on setting up configuration files on your computer for multiple accounts:
- [Git Config Files using a folder structure](https://www.motowilliams.com/conditional-includes-for-git-config)
- [Windows Machine Multiple Git ID's](https://medium.com/@pinglinh/how-to-have-2-github-accounts-on-one-machine-windows-69b5b4c5b14e)
- [Multiple Emails per Git Repo](https://orrsella.com/2013/08/10/git-using-different-user-emails-for-different-repositories/)


## SSH and security measures


## Basic workflows
More information on workflows will be found in other resources on this site.
Starting from scratch:
- Make a directory folder on your computer where you will work
- Initialize it as a  git repo by  changing directory to within that folder and calling the command at the command prompt:

```git init```

check user config for the repo is correct

If you have multiple identities it is a good idea to check which identity this folder is using and change if necessary

```
   git config user.email
   git config user.name
```

- create a README document as text or markdown which will hold basic information about your code repository


```
   echo README.md > README file for Repo Name
   git add README.md
   git commit -m"addd readme"
```


go onto GitHub and create an empty repository

    git push main ssh... -u

- once you are set up you will want to get into a standard git [workflow]
(https://www.atlassian.com/git/tutorials/comparing-workflows)
where you commit changes locally often and push to your remote main at least daily if changes have been made or when many changes have occurred.  Committing often will help when you want to revert ( go backward) or if you are actively working with several others


### Branching
Branching can be thought of as creating a copy of your code with a flag at the point where you started the branch.  This allows you to try out a different path or set of function.  It is good practice when you are adding a new feature to solid working code or working on a significant piece of code that will likely need to be incorporated to the larger code base at a later time.  If you do not like it then you can always just go back to your branching point.  You may choose to use local branches only and merge your code or send your branch up to the main repository.  Good practice dictates not having several " orphan" branches  or using branches as specific features;  Once a branch is ready to be merged into the main repository, the branch should be deleted so it does not cause any confusion in the development process

### Helpful git commands
Quick reference [guide](https://git-scm.com/docs)
- ```git stash``` [Hold onto all changes since the last commit and save for the future but change back my working files to the last commit](https://git-scm.com/docs/git-stash)
- ```git stash pop``` [Put back the changes stashed](https://git-scm.com/docs/git-stash#Documentation/git-stash.txt-pop--index-q--quietltstashgt)
- ```git revert```  [Undo some of the previous commits](https://git-scm.com/docs/git-revert)
- ```git remote -v``` [Show the address of the remote server this repo is set up to push to](https://git-scm.com/docs/git-remote)
- ```git checkout -b name``` Create a new branch called "name" and check it out locally to work on

# Version Control Best Practices

## General principles of change management

Some principles of software management and review are true across all
workflows. These are presented first; for more details on possible
workflows in GitHub, see "GitHub workflow" section below.

1.  The `main` branch is always stable. To ensure stability, a
    combination of automated testing and manual review needs to be
    undertaken everytime a change is merged into `main.` At minimum
    complete the following checklist:

-   A series of unit tests are ran. Realistically, this means using a
    continous integration tool (we recommend
    [TravisCI](https://docs.travis-ci.com/user/tutorial/). Manual
    running of test suites at the frequency we expect changes to be
    merged becomes way too cumbersome. For a more basic introduction to
    Travis for R packages, see Julia Silge's excellent \[blog post\]
    (<https://juliasilge.com/blog/beginners-guide-to-travis/>)
-   All documentation is updated. This includes auto-update of code
    reference documentation generated by `doxygen, sphinx`, etc. and
    manual examination that any changes that break example code,
    vignettes, or tutorials are updated in the respective materials. For
    `R` packages, it also means ensuring your DESCRIPTION file is
    updated with any new package dependencies.
-   Manual code review. At least one package collaborator should review
    changes, suggest alternative approaches, and approve as necessary.

1.  Changes in `main` are pulled to working location (this could be a
    development or feature branch, or fork depending on the workflow)
    every time the new code is tested. This ensures the remote location
    stays up to date.

2.  Changes that are the subject of pull requests do not exceed 500
    lines of code. Changes of larger magnitude are difficult to review
    and test in one go. Similarly, changes that are intended to be
    merged in should be on a weekly basis.

### More GitHub workflow options

My main critique of GitHub is its tendency to provide too many parallel
options that achieve the same end goal. One of these is illustrated with
choosing between git forking and branching workflows. Both are
legitimate workflows but it is unclear what the pros and cons of each
are. My pros and cons are presented below:

#### Pros of forking:

1.  The only option if you intend to keep code divergent forever.
2.  Does not require contributors to be added as collaborators to the
    project.

#### Cons of forking:

1.  Harder to stay up-to-date with `main`.
2.  Harder to make "feature forks" than "feature branches."
3.  Doesn't integrate quite as well with releases.

#### Pros of branching:

1.  Allows for multi-branch workflow, i.e. a `main`, `development`,
    and feature branches. Feature branches are one way to keep changes
    more modular and improve testability.
2.  Seamless to manage GitHub releases.
3.  Branch protection rules to enforce more protocols on everyone,
    including administrators.

#### Cons of branching:

1.  Authors need to be collaborators.
2.  Not ideal for permanently divergng codebases.

For our toolbox, NOAA git policy dictates non-NOAA affiliates cannot
have push access to the repository. For this reason, you can only use
the branch workflow if your repository exists under an organization,
which allows you to tweak the permissions of collaborators. A
non-organization git repo gives all collaborators push access. We
recommend creating an organization for your repository if you have more
than one repository and/or more than 2 or 3 collaborators and using the
branching workflow for changes you expect to be merged back into the
main branch. If you expect changes to diverge and not rejoin main,
or you have one repository with non-NOAA collaborators, the forking
workflow may suit your needs better.

## Software versioning and GitHub Releases

The standard for software versioning is [semantic
versioning](https://semver.org/) in which major changes that break the
application programmatic interface (API) constitute version changes,
backwards-compatible changes constitute minor versions, and patches are
backwards compatible-bug fixes. We recommend not trying to always
maintain backwards compatibility, which can lead to testing nightmares,
but instead being clear about versioning and maintaining access to
legacy software binaries for users who are unable to migrate to later
software versions. Patches may be applied to legacy versions to port bug
fixes when necessary.

A good way to manage this is using GitHub releases. GitHub
[releases](https://help.github.com/en/categories/releases) are designed
to keep a consistent log of the most recent software version. You can
create a release by pushing a commit with a tag that corresponds to a
semantic version (for example, tag 1.0.0 to release version 1.0), or by
selecting "Draft a new release" in your GitHub repository. Drafting
releases comes with the benefit of marking something a draft or
preliminary release. In a GitHub release, compiled binaries up to 2.0 MB
are provided for download and others watching your repository will be
notified when a new release is pushed.


## Free online GitHub tutorials
- [More info from Atlassian](https://www.atlassian.com/git/tutorials)
