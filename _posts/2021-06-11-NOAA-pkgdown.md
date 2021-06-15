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

Steps for creating a NOAA themed pkgdown landing site for your tool on the toolbox. The landing page includeds NOAA colors and a NOAA logo footer. For an example of what this looks like see the [r4MAS landing page](https://nmfs-fish-tools.github.io/r4MAS/index.html).

1. Set up a pkgdown landing page for your tool following the instructions [here](https://pkgdown.r-lib.org/)
2. Create a pkgdown folder in your repo and add the file [extra.css](https://github.com/nmfs-fish-tools/r4MAS/blob/pkgdown-site/pkgdown/extra.css)
3. Add this code to your README.MD to add a footer:

```
<img src="https://raw.githubusercontent.com/nmfs-general-modeling-tools/nmfspalette/main/man/figures/noaa-fisheries-rgb-2line-horizontal-small.png" height="75" alt="NOAA Fisheries">

[U.S. Department of Commerce](https://www.commerce.gov/) | [National Oceanographic and Atmospheric Administration](https://www.noaa.gov) | [NOAA Fisheries](https://www.fisheries.noaa.gov/)
```
