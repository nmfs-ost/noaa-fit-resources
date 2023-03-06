---
title: "NOAA GitHub Guidelines"
excerpt: "NOAA approved GitHub account and repositories"
date: 2021-07-30
toc: true
categories:
  - NOAA Resources
tags:
  - git
  - GitHub
  - NOAA resources
  - developer resources
---

[GitHub](https://github.com/) is a great way to share code and work collaboratively. Below are guidelines for creating a NOAA GitHub account and repositories under that account. More about the NOAA guidelines can be found [here](https://ufscommunity.org/wp-content/uploads/2019/11/20170823_NOAA_GitHub_Usage_Guidelines.pdf). Also see the main [NOAA GitHub site](https://github.com/NOAAGov) and [information](https://github.com/NOAAGov/Information), as well as the current [NOAA affiliated GitHub projects](https://github.com/NOAAGov/NOAA-Affiliated-Projects).

For a best practices guide for using GitHub within NOAA, see the [nmfs-opensci GitHub Guide](https://nmfs-opensci.github.io/GitHub-Guide/)

## How to create a NOAA GitHub account

To set up a NOAA approved GitHub account, [create an account with GitHub](https://help.github.com/en/articles/signing-up-for-a-new-github-account) with your NOAA email and follow the below requirements:

- NOAA users must have a GitHub account using their NOAA email
- They must have a photo of themselves associated with the account
- They must use [2-factor authentication](https://docs.github.com/en/github/authenticating-to-github/securing-your-account-with-two-factor-authentication-2fa)
- They can only have NOAA related work under their account

>**Note**: it is good practice that your NOAA GitHub username is `FirstLast-NOAA` which clearly identifies it as an NOAA linked account versus a personal account.

## How to set up a repository with your NOAA account

To set up a repository to keep your code, [create a repo](https://docs.github.com/en/get-started/quickstart/create-a-repo) under your NOAA GitHub account and follow the below requirements:

- Only allow write access to NOAA users
- All non-NOAA users can only have pull-request access
- Must include a `DISCLAIMER.md` like [this one](https://github.com/nmfs-fish-tools/Resources/blob/master/Disclaimer.md), or a disclaimer in the README
- Must include specific wording in the `LICENSE.md` like [this](https://github.com/nmfs-fish-tools/Resources/blob/master/LICENSE.md)
- Must have a "gold standard" backup of the repo

> One way to set administrative privileges on your repo is to create an [organization](https://docs.github.com/en/organizations/collaborating-with-groups-in-organizations/creating-a-new-organization-from-scratch) in GitHub. Repos will then fall under that organization, and Github allows for more admin ability under organizations.

## Multiple Accounts

If you have multiple GitHub accounts (perhaps a personal one and a work one), you will want to be careful about which identity you use.

The easiest solution is to use only one account per computer, but if that is not possible, here are some ways to deal with multiple identities locally.

To check which identity you are using inside of a local clone of a git repository by default, type into the command line:

```
git config user.name
git config user.email
```

You can set `user.name` and `user.email` for each repository as you go. This works, however there is a global setting, and if you forget to initialize your repository with the correct credentials, the global choice will be used.

Better: set up a `.gitconfig` to deal with multiple identities

For more information on setting up configuration files on your computer for multiple accounts:
- [Git Config Files using a folder structure](https://www.motowilliams.com/conditional-includes-for-git-config)
- [Windows Machine Multiple Git ID's](https://medium.com/@pinglinh/how-to-have-2-github-accounts-on-one-machine-windows-69b5b4c5b14e)
- [Multiple Emails per Git Repo](https://orrsella.com/2013/08/10/git-using-different-user-emails-for-different-repositories/)

## GitHub in Government

More information about how GitHub is used in Gov [here](https://github.com/Openscapes/2021-noaa-nmfs/wiki/1-GitHub-in-gov), with example organizations [here](https://github.com/Openscapes/2021-noaa-nmfs/wiki/1-GitHub-in-gov#github-in-noaa--nmfs).

