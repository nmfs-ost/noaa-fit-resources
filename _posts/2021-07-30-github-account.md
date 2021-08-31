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

[GitHub](https://github.com/), which offers [GIT](https://git-scm.com/) server as a service, is a great way to share code and work collaboratively. Below are guidelines for creating a NOAA GitHub account and repositories under that account. More about the NOAA guidelines can be found [here](https://ufscommunity.org/wp-content/uploads/2019/11/20170823_NOAA_GitHub_Usage_Guidelines.pdf). Also see the main [NOAA GitHub site](https://github.com/NOAAGov) and [information](https://github.com/NOAAGov/Information), as well as the current [NOAA affiliated GitHub projects](https://github.com/NOAAGov/NOAA-Affiliated-Projects). 

## How to create a NOAA GitHub account

To set up a NOAA approved GitHub account, [create an account with GitHub](https://help.github.com/en/articles/signing-up-for-a-new-github-account) with your NOAA email and follow the below requirements:

- NOAA users must have a GitHub account using their NOAA email
- They must have a photo of themselves associated with the account
- They must use [2-factor authentication](https://docs.github.com/en/github/authenticating-to-github/securing-your-account-with-two-factor-authentication-2fa)
- They can only have NOAA related work under their account

>**Note**: it is good practice that your NOAA GitHub username is `FirstLast-NOAA` which clearly identifies it as an NOAA linked account versus a personal account.

## How to set up a repository with your NOAA account

To set up a repository to keep your code, [create a repo] under your NOAA GitHub account and follow the below requirements:

- Only allow write access to NOAA users
  - All non-NOAA users can only have pull-request access
- Must include a `DISCLAIMER.md` like [this one](https://github.com/nmfs-fish-tools/Resources/blob/master/Disclaimer.md), or a disclaimer in the README
- Must include specific wording in the `LICENCE.md` like [this](https://github.com/nmfs-fish-tools/Resources/blob/master/LICENSE.md)
- Must have a "gold standard" backup of the repo

One way to set administrative privileges on your repo is to create an [organization](https://docs.github.com/en/organizations/collaborating-with-groups-in-organizations/creating-a-new-organization-from-scratch) in GitHub. Repos will then fall under that org, and Github allows for more admin ability under organizations. 

## Multiple Identities
If you have multiple GitHub identities (perhaps a personal one and a work one).  You will want to be careful about which identity you use.  Here are some ways to deal with multiple identities. 

To check which identity you are using inside of a git repository by default:

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

## A Beginner's Tutorial on Git and GitHub

The following video provides an intro to using Git and GitHub. The corresponding tutorial can be found [here](https://github.com/aomlomics/tutorials). This webinar is presented by Luke Thompson, an Associate Research Professor at the Northern Gulf Institute at Mississippi State University & Atlantic Oceanographic and Meteorological Laboratory (AOML). The webinar was hosted by the [NOAA Central Library](https://library.noaa.gov/). 

<iframe width="560" height="315" src="https://www.youtube.com/embed/LLWBv5nPQys" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## More GitHub Resources
- [Get started with GitHub](https://docs.github.com/en/get-started)
- [GitHub Guides](https://guides.github.com/)
- [Git and GitHub learning resources](https://docs.github.com/en/get-started/quickstart/git-and-github-learning-resources)
- [Happy GIT and GitHub for the useR](https://happygitwithr.com/)
- [Basic GIT workflows](https://noaa-fisheries-integrated-toolbox.github.io/resources/onboarding/version-control2/#basic-git-workflows)
- [Practical R Workflow for Scientists](https://rverse-tutorials.github.io/RWorkflow-NWFSC-2021/index.html)
  - Specifically [week 1](https://rverse-tutorials.github.io/RWorkflow-NWFSC-2021/week1.html), [week 2](https://rverse-tutorials.github.io/RWorkflow-NWFSC-2021/week2.html), and [week 3](https://rverse-tutorials.github.io/RWorkflow-NWFSC-2021/week3.html)
- [Collaborate with R and GitHub](https://noaa-iea.github.io/r3-train/collaborate.html)
- [How to Use Git/GitHub with R](https://rfortherestofus.com/2021/02/how-to-use-git-github-with-r/)
- [Git and GitHub with R](https://r-pkgs.org/git.html)
