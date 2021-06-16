---
title: "Create a NOAA Themed pkgdown Landing Page"
excerpt: "NOAA pkgdown"
date: 2021-06-11
toc: true
categories:
  - workshops
tags:
  - resources
  - fish and fisheries
---

## How to create a NOAA themed pkgdown landing site for your tool

Steps for creating a NOAA themed pkgdown website for your tool on the toolbox. The website uses NOAA colors and a NOAA logo footer. 

1. Set up a pkgdown website for your tool following the instructions from [here](https://pkgdown.r-lib.org/).
2. Create a pkgdown folder in your repository and add `pkgdown/extra.ss`. Add the code below to the `extra.ss` file. See [extra.css](https://github.com/nmfs-fish-tools/r4MAS/blob/master/pkgdown/extra.css) for an example of the CSS code.

```
@import url("https://nmfs-general-modeling-tools.github.io/nmfspalette/extra.css");
```
3. Add the code below to README.md to add a footer. See bottom of the [README.md](https://raw.githubusercontent.com/nmfs-fish-tools/r4MAS/master/README.MD) for an example of the html code.


```
<img src="https://raw.githubusercontent.com/nmfs-general-modeling-tools/nmfspalette/main/man/figures/noaa-fisheries-rgb-2line-horizontal-small.png" height="75" alt="NOAA Fisheries">

[U.S. Department of Commerce](https://www.commerce.gov/) | [National Oceanographic and Atmospheric Administration](https://www.noaa.gov) | [NOAA Fisheries](https://www.fisheries.noaa.gov/)
````

More examples of what the website looks like:

- [nmfspalette landing page](https://nmfs-general-modeling-tools.github.io/nmfspalette/)
- [r4MAS landing page](https://nmfs-fish-tools.github.io/r4MAS/)
- [adnuts landing page](https://cole-monnahan-noaa.github.io/adnuts/)


