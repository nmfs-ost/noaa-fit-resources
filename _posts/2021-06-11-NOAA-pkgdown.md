---
title: "Create a NOAA Themed pkgdown Landing Page"
excerpt: "NOAA themed pkgdown"
date: 2021-06-11
toc: true
categories:
  - workshops
tags:
  - resources
  - GitHub
---

## How to create a NOAA themed pkgdown landing site for your tool

Below are steps for creating a NOAA themed pkgdown webpage, with NOAA colors and a NOAA logo footer, for your tool on the toolbox. You can also fork [this repo](https://github.com/nmfs-fish-tools/pkgdownTemplate) and follow directions. 

1. Set up a pkgdown website for your tool following the instructions from [here](https://pkgdown.r-lib.org/).
2. Create a pkgdown folder in your repository and add `pkgdown/extra.css`. Add the code below to the `extra.css` file. See [extra.css](https://github.com/nmfs-fish-tools/r4MAS/blob/master/pkgdown/extra.css) for an example of the CSS code.

```
@import url("https://nmfs-fish-tools.github.io/nmfspalette/extra.css");
```
3. Add the code below to README.md to add a footer. See bottom of the [README.md](https://raw.githubusercontent.com/nmfs-fish-tools/r4MAS/master/README.MD) for an example of the html code.


```
<img src="https://raw.githubusercontent.com/nmfs-fish-tools/nmfspalette/main/man/figures/noaa-fisheries-rgb-2line-horizontal-small.png" height="75" alt="NOAA Fisheries">

[U.S. Department of Commerce](https://www.commerce.gov/) | [National Oceanographic and Atmospheric Administration](https://www.noaa.gov) | [NOAA Fisheries](https://www.fisheries.noaa.gov/)
````

### Examples of tools and packages with NOAA themed pkgdown sites

- [nmfspalette](https://nmfs-general-modeling-tools.github.io/nmfspalette/)
- [r4MAS](https://nmfs-fish-tools.github.io/r4MAS/)
- [adnuts](https://cole-monnahan-noaa.github.io/adnuts/)
- [bayesdfa](https://fate-ewi.github.io/bayesdfa/)
- [wham](https://timjmiller.github.io/wham/)

## Adding a video tutoral to your landing page

Follow the instructions below to add a video demo or overview of your tool on your pkgdown landing page. Examples of this can be seen on the [wham](https://timjmiller.github.io/wham/) and [bayesdfa](https://fate-ewi.github.io/bayesdfa/) pages. 

### Embed a video in a `.md` page

Using a link from YouTube or Vimeo:
1. Click `share`
2. Click `embed link`
3. Copy and Paste the embed link into the `.md` file where you want the video to appear

Example code from YouTube embed link:
```
<figure class="video_container">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/A7qDN2oYSxc" frameborder="0" allowfullscreen="true"> </iframe>
</figure>
```




