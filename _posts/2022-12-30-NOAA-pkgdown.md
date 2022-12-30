---
title: "NOAA Themed pkgdown"
excerpt: "Create a NOAA themed pkgdown Landing Page in 3 steps"
date: 2022-12-30
toc: true
categories:
  - NOAA Resources
tags:
  - NOAA resources
  - GitHub
  - developer resources
  - software
  - app and website hosting
---

## How to create a NOAA themed pkgdown landing site for your tool

Below are the 3 steps for creating a NOAA themed pkgdown webpage, with NOAA colors and a NOAA logo footer, for your tool on the toolbox.

1. Set up a pkgdown website for your tool using the [pkgdown readme instructions](https://pkgdown.r-lib.org/).
2. Create a pkgdown folder in your repository and add a file called `pkgdown/extra.css`. Add the code below to the `extra.css` file:

```
@import url("https://nmfs-fish-tools.github.io/nmfspalette/extra.css");
```

This will allow the [CSS file with NMFS styling](https://nmfs-fish-tools.github.io/nmfspalette/extra.css) to be used for your pkgdown site. Optional: For those who wish to dive deeper, read an [overview on what CSS is](https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps/What_is_CSS) to understand what the css file is doing.
3. Add the code below to your repository's README.md to add a footer.

```
<img src="https://raw.githubusercontent.com/nmfs-fish-tools/nmfspalette/main/man/figures/noaa-fisheries-rgb-2line-horizontal-small.png" height="75" alt="NOAA Fisheries Logo">

[U.S. Department of Commerce](https://www.commerce.gov/) | [National Oceanographic and Atmospheric Administration](https://www.noaa.gov) | [NOAA Fisheries](https://www.fisheries.noaa.gov/)
````

### Examples of tools and packages with NOAA themed pkgdown sites

- [nmfspalette](https://nmfs-general-modeling-tools.github.io/nmfspalette/)
- [r4MAS](https://nmfs-fish-tools.github.io/r4MAS/)
- [adnuts](https://cole-monnahan-noaa.github.io/adnuts/)
- [bayesdfa](https://fate-ewi.github.io/bayesdfa/)
- [wham](https://timjmiller.github.io/wham/)

## Going further

Optional steps to improve your pkgdown page

### Adding a video tutoral to your landing page

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
### Automate your pkgdown rendering

Want your pkgdown site to always be up to date with your code? Use the `update_pkgdown()` workflow from the [ghactions4r package](https://nmfs-fish-tools.github.io/ghactions4r/) to set up rendering the pkgdown site automatically on changes to the main branch. Note that this workflow will deploy the pkgdown site to a branch called gh-pages, so the publishing source for GitHub Pages will need be set to the root of the gh-pages branch.



