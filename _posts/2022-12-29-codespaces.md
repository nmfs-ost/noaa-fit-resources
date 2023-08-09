---
title: "Codespaces"
excerpt: "Resources for using GitHub Codespaces"
date: 2022-12-29
toc: true
categories:
  - Git and GitHub Resources
tags:
  - GitHub
  - git
  - developer resources
  - R
  - software user resources
  - cloud
---
## What is GitHub Codespaces?

GitHub Codespaces allows you to spin up ephemeral machines for running and developing software. It is similar to developing on your personal computer, but without the need for set up and installation. All GitHub users get 60 hours of GitHub Codespaces free of charge. To learn more see the [GitHub Codespaces Documentation](https://docs.github.com/en/codespaces) or for a quick overview, this [NMFS R Users Group Presentation on Codespaces](https://docs.google.com/presentation/d/17BYfqPWTh6zyZNj0ejXo0mX44O_h9KNMTv6iaZTa7fQ/edit?usp=share_link) (NOAA sign-in required to view).

## How do I use Codespaces for running or developing code?

Codespaces can be easily used from a repository on GitHub, if the specification files have already been set up. Follow the [GitHub Documentation for using Codespaces from a repository](https://docs.github.com/en/codespaces/developing-in-codespaces/creating-a-codespace-for-a-repository#creating-a-codespace-for-a-repository).

## What if there are no specification files?

If the specification files still need to be set up, there is [detailed documentation for how to set up Codespaces](https://docs.github.com/en/codespaces/setting-up-your-project-for-codespaces/introduction-to-dev-containers). Below, we provide guidance for setting up codespaces for R package development. 

## How do I set up Codespaces for R package development?

There are many ways to configure Codespaces for R development. Some options include:
1. Use [r-vscode-codespaces](https://github.com/nmfs-opensci/r-vscode-codespaces) to try out codespaces for R in a new project. This includes all the features needed to make it easy to edit and use R code with the VScode IDE.
2. Lightest weight option: r-verse (follows steps in [github documentation](https://docs.github.com/en/codespaces/setting-up-your-project-for-codespaces/setting-up-your-project-for-codespaces#step-1:-open-your-project-in-a-codespace)). This has R, but maybe not all the features you want to use it easily within codespaces. If the goal is just to run a few lines of R code without needing to extensively edit and test R code, this would be the best option.
3. [r-codespaces](https://github.com/jakubnowicki/r-codespaces) many features and uses [renv](https://rstudio.github.io/renv/articles/renv.html), so startup takes a while. This option also takes a large amount of storage space.
4. Get an environment with Python, R, Julia and Jupyter notebooks by following [Eli Holmes’s Demo](https://youtu.be/YDfZ5raWbs4). This is a good option if you are using Jupyter notebooks or Python and Julia in addition to R.

