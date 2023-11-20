---
title: "Resources for working with confidential data"
excerpt: "Helpful links for working with secrets"
date: 2023-11-20
toc: true
categories:
  - NOAA Resources
tags:
  - git
  - GitHub
  - software user resources
  - developer resources
---

## What is confidential data?

Confidential data can be secrets like passwords or API keys. In NOAA Fisheries, many of us also work with confidential fisheries data that must be kept private when it is identifiable.

Working with confidential data can cause challenges when working on GitHub, where confidential data should **never** be stored, even if your code is private. Likewise, care must be taken when creating public products from summarized confidential data.

Luckily, there are resources to help keep confidential data private.

## For R users: Confidentiality Confidence Builder

Ady Rios (SEFSC) put together this [Confidentially Confidence Builder](https://github.com/nmfs-opensci/Confidentiality-Confidence-Builder) to learn tools for working with confidential data in R.

## Preventing accidental commits of confidential data in the GitHub Guide

The NOAA Fisheries Open Science GitHub Best Practices Guide provides some [tips for avoiding accidental commits containing confidential data](https://nmfs-opensci.github.io/GitHub-Guide/#preventing-inadvertent-committing-of-secrets-or-credentials-to-github)

## Community support for working with fisheries confidential data

Reaching out to the [NMFS R User Group](https://noaa-fisheries-integrated-toolbox.github.io/resources/noaa%20resources/nmfs-r-ug-calendar/) with questions can help you connect with others in NOAA Fisheries who are processing confidential data.

Fisheries confidential data is unfortunately not something that is as easy to define or catch using tools designed to catch accidental commits of API keys or passwords. However, there are many scientists at NOAA Fisheries that have designed workflows based on processing confidential fisheries data.
