---
title: "Make your own software cheetsheet"
excerpt: "Tips and tools for making a user-friendly cheatsheet"
date: 2025-8-26
toc: true
categories:
  - Developer Resources
tags:
  - developer resources
  - NOAA resources
  - documentation
  - software
  
---


Have you been curious about making a [cheatsheet](https://posit.co/resources/cheatsheets/) for your software? This can be a helpful way to share with users the essential knowledge of how to use your software. Here are some ideas based on recent experiences of developers putting together cheatsheets.

## Sophie Breitbart: Cheatsheet for the `asar` R package

At a late August [NOAA Fisheries Openscapes](https://nmfs-openscapes.github.io/) coworking, I shared that I'd finished [the first version of the `asar` cheatsheet](https://github.com/nmfs-ost/asar/blob/0a8fd9678800e068e301b94b67b00f40106a64d5/pkgdown/assets/asar_cheatsheet.pdf). After some further feedback, [the cheatsheet was updated once more](https://github.com/nmfs-ost/asar/blob/33cebc3ee8983ab867ef598cb74bc48c08b0a258/pkgdown/assets/asar_cheatsheet.pdf). We plan to continually update the cheatsheet as our package evolves. Here's some insight into how I made this cheatsheet (my first!):

### Approach

-   I looked at several cheatsheets for design inspiration first. Here are links to cheatsheets from [Posit](https://posit.co/resources/cheatsheets/) and [contributors](https://rstudio.github.io/cheatsheets/contributed-cheatsheets.html).
-   I read [some guidance for designing a cheatsheet](https://github.com/dmvillarreal/cheatsheets/tree/master?tab=readme-ov-file). I certainly didn't follow all of it, but it had some great reminders about balancing text with visual depictions, emphasis on conciseness and differentiation from documentation, and the value of sample code.
-   I also started a back-and-forth with Gemini to see what it could produce. I supplied it a link to `asar`'s functions and asked it to make a cheatsheet that looked similar to Posit's cheatsheets. I tried several prompts to get it to produce something I liked, but I ultimately gave up. It was still useful though, in that this exercise showed me what I did and didn't want in a cheatsheet:
    -   Gemini grouped by function type but I realized I wanted `asar`'s to be structured by workflow (i.e., chronologically, so to speak).
    -   Gemini could format in HTML or markdown, but there were features I appreciated about the classic Powerpoint-based cheatsheets it couldn't replicate (or, at least, I didn't have the patience to keep trying to write the perfect prompt to achieve my vision). It's tricky to articulate exactly what those things are, but here are some:
        1.  Usage of white space
        2.  Freedom to create and position visual aids
        3.  Properly-fitting columns
        4.  Neat fit onto one page that could be printed out for future reference digitally or on paper as workshop handouts
    -   I also wanted to add other information like data science tips and links to asar resources like vignettes and issues.
-   So I opened the powerpoint template and began customizing its three-column template.
-   About 1/3 of the way through, I asked my colleague Sam Schiano for her initial thoughts and if this was going in the right direction. She gave some great feedback that invited further edits.
-   My colleague Kelli Johnson also shared some thoughts on how to make the first version clearer and more useful. One of my biggest takeaways was that the cheatsheet would be stronger if more space was devoted to depicting *how functions work* and *what the expected output should look like*. Ideally, the cheatsheet would allow the user to start understanding the workflow and intuiting how to navigate it. A deepener familiarity with the tool will encourage adoption and more productive troubleshooting.
-   I'm sure we'll edit it as we learn more from our users about what's most important for them. Maybe we'll make a more reproducible version based in a format like Quarto, too.

### Tools

-   I used open source icons from [Ionicons](https://ionic.io/ionicons) and [Feather](https://feathericons.com/) to symbolize the purpose of each section.
-   I used [this Posit cheatsheet pptx template](https://github.com/rstudio/cheatsheets/blob/main/powerpoints/0-template.pptx), then downloaded it as a PDF.

### Current cheatsheet snapshot

[![Screenshot of the August 2025 \`asar\` cheatsheet.](images/asar_cheatsheet_20250908.png)](https://github.com/nmfs-ost/asar/pull/348)

## Kelli Johnson: Cheatsheet for the FIMS package

TODO: Check in with Kelli to see if she would be interested in adding text here.

## NASA Earthdata Cloud Cookbook

Cheatsheets can also be used to illustrate essential steps for processes larger than working with a software package. For example, NASA Earthdata put together a series of [Cheatsheets and Guides for the Earthdata Cloud data](https://nasa-openscapes.github.io/earthdata-cloud-cookbook/glossary.html), including a [workflow cheatsheet](https://nasa-openscapes.github.io/earthdata-cloud-cookbook/glossary.html#workflow-cheatsheet) to help users learn the essential workflow components needed to work with NASA Earthdata Cloud data.
