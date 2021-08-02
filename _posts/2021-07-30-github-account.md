---
title: "NOAA GitHub Guidelines"
excerpt: "NOAA approved GitHub account and repositories"
date: 2021-07-30
toc: true
categories:
  - onboarding
tags:
  - git
  - github
---

[GitHub](https://github.com/), which offers [GIT](https://git-scm.com/) server as a service, is a great way to share code and work collaboratively.

More information and resources for using GitHub: 
- [Get started with GitHub](https://docs.github.com/en/get-started)
- [GitHub Guides](https://guides.github.com/)
- [Git and GitHub learning resources](https://docs.github.com/en/get-started/quickstart/git-and-github-learning-resources)
- [Happy GIT and GitHub for the useR](https://happygitwithr.com/)
- [Basic GIT workflows](https://noaa-fisheries-integrated-toolbox.github.io/resources/onboarding/version-control2/#basic-git-workflows)

## How to create a NOAA GitHub account

To set up a NOAA approved GitHub account, [create an account with GitHub](https://help.github.com/en/articles/signing-up-for-a-new-github-account) with your NOAA email and follow the below requirements:

- NOAA users must have a GitHub account using their NOAA email
- They must have a photo of themselves associated with the account
- They must use 2-factor authentication
- They can only have NOAA related work under their account

>**Note**: it is good practice that your NOAA GitHub username is `FirstLast-NOAA` which clearly identifies it as an NOAA linked account versus a personal account.

## Setting up a code repository 

To set up a repository to keep your code, [create a repo] under your NOAA GitHub account and follow the below requirements:

- Only allowing write access to NOAA users
- All non-NOAA users can only have pull-request access
- Must include this [disclaimer](https://github.com/nmfs-fish-tools/Resources/blob/master/Disclaimer.md) in the README 
- Must include specific wording in [License](https://github.com/nmfs-fish-tools/Resources/blob/master/LICENSE.md)
- Must have a "gold standard" backup of the repo

One way to set administrative privileges on your repo is to create an “organization” in GitHub. Repos will then fall under that org, and Github allows for more admin ability under organizations. 

> **Note**: If you have multiple GitHub identities (perhaps a personal one and a work one).  You will want to be careful about which identity you use.  See Multiple Identities below to set up automated ways of dealing with this.

## Multiple Identities
There are various ways to deal with multiple identities. To check which identity you are using inside of a git repository by default
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
