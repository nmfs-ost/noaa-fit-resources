---
title: "Sound practices for maintaining software"
excerpt: "Tricks and tips for software maintainers"
date: 2025-11-19
toc: false
categories:
  - Developer Resources
tags:
  - software
  - NOAA resources
  - developer resources

---
*By Megsie Siple and the NOAA Fisheries Integrated Toolbox Committee*

Congratulations, you have planted your software in the NOAA software ecosystem. It is functioning as it should, it looks great, and it’s producing fruits for the people who use it.

You can choose whatever metaphor suits you: a growing plant, a pet, even a child if you are particularly proud of – and exhausted by– this software. Any living organism that requires stewardship will do, because software is a living thing. Software requires maintenance to 1\) address bugs, 2\) keep software compatible with changing environments and dependencies, and 3\) respond to user needs for new or changed functionality.  At NOAA Fisheries, the features and functionality of a piece of software also need to respond to management needs, which can change with new legislation or changing management priorities. 

However, a lot of the time software ends up functioning more like a tool: it gets built, it gets used, and then when it’s no longer useful, someone makes a new tool or completely refactors the old one. And it makes sense that it is treated this way: software maintenance is more costly than development (Boehm 1981, p. 142). For individual developers, the time spent fixing bugs and keeping software updated can outweigh the time spent developing new software or new features. 

At NOAA Fisheries as in the academe, there are significant challenges to software maintenance: developers or maintainers may retire without a proper handover, programs may depend on operating systems or architectural software that become obsolete, and developers may simply have demands on their time that end up being prioritized over software maintenance– including the maintenance of other software\! 

Well-maintained software builds trust with its user base and is robust. A software maintenance plan can ensure that maintenance is part of the software development process, not just an afterthought once the software is released. The NOAA Fisheries Integrated Toolbox (FIT) is interested in helping NOAA Fisheries developers make useful maintenance decisions for their software, and directing developers to helpful resources.

Here are some sound practices for software maintenance:

1. **Budget for maintenance**  
   Put maintenance and testing into your time budget for software development– from the beginning, if you can.

2. **Collect user feedback**  
   Decide if and how you are going to get user feedback (including bug reports and feature requests) and who will watch for that feedback/filter it if needed. Communicate clearly to users how you plan to incorporate their feedback and what you will do with it.

3. **Foster ownership**  
   Within your team, [foster a culture of ownership over your software](https://www.forbes.com/councils/forbestechcouncil/2025/07/03/proven-ways-to-foster-project-ownership-among-dev-teams/), so when it is time to work on maintenance tasks, it is more a “joy of stewardship” and less a “thankless chore”.

4. **Keep documentation updated**  
   Documentation should be updated whenever corresponding software is updated. Consider using in-program documentation (i.e., pop-up help, frequently asked questions, Roxygen documentation for R code) as it may be easier to maintain than an external document.

5. **Nourish your will (and skill\!) to maintain**  
   If you are a maintainer, balance your energies and nourish yourself. [Here is some guidance we liked](https://opensource.guide/maintaining-balance-for-open-source-maintainers/).

Some software development best practices will also streamline your maintenance plan, especially these:

6. **Automate your unit tests**  
   This way, [regular testing of your code](https://nmfs-ost.github.io/noaa-fit-resources/developer%20resources/code-testing/) happens with development.  
     
7. **Use [version control](https://nmfs-ost.github.io/noaa-fit-resources/developer%20resources/version-control/)**   
   Release changes to users in small “batches” (i.e., a few functional changes at a time).  
     
8. **Include a clear license**  
   Including a clear license up front ensures all contributors understand what they are agreeing to by contributing to your project.  Working on an open source, collaborative project is not the antithesis of protecting your intellectual property. The NOAA [NAO 201-118](https://drive.google.com/file/d/15k6XOfNWGLFHGeb4AvyEAxuKHNuToy_3/view) covers procedures for intellectual property/licensing as well as quality assurance (briefly summarized in the FIT blog [here](https://nmfs-ost.github.io/noaa-fit-resources/noaa%20resources/nao-software/)).

There are also some [helpful tips from Open Source Guides](https://opensource.guide/best-practices/) for best practices for maintainers. These best practices require teamwork and institutional support.

Tool maintenance and continuity are important parts of a healthy software ecosystem, and a solid maintenance practice is also important for getting mandated science work done and done well. 

