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

3. If you don't have one already, add a [NOAA Disclaimer](https://raw.githubusercontent.com/nmfs-fish-tools/Resources/master/Disclaimer.md) to the footer of your README.md that will be automatically added to your pkgdown page.

  ```
  ## Disclaimer
  The United States Department of Commerce (DOC) GitHub project code is
  provided on an ‘as is’ basis and the user assumes responsibility for 
  its use. DOC has relinquished control of the information and no longer
  has responsibility to protect the integrity, confidentiality, or 
  availability of the information. Any claims against the Department of
  Commerce stemming from the use of its GitHub project will be governed
  by all applicable Federal law. Any reference to specific commercial 
  products, processes, or services by service mark, trademark, 
  manufacturer, or otherwise, does not constitute or imply their 
  endorsement, recommendation or favoring by the Department of Commerce.
  The Department of Commerce seal and logo, or the seal and logo of a 
  DOC bureau, shall not be used in any manner to imply endorsement of any
  commercial product or activity by DOC or the United States Government.”
  ```

4. Add the code below to your repository's README.md to add a footer.

    ```
    <img src="https://raw.githubusercontent.com/nmfs-fish-tools/nmfspalette/main/man/figures/noaa-fisheries-rgb-2line-horizontal-small.png" height="75" alt="NOAA Fisheries Logo">

    [U.S. Department of Commerce](https://www.commerce.gov/) | [National Oceanographic and Atmospheric Administration](https://www.noaa.gov) | [NOAA Fisheries](https://www.fisheries.noaa.gov/)
    ```
## Automate your pkgdown rendering

Want your pkgdown site to always be up to date with your code? Use the [`use_update_pkgdown()`](https://nmfs-fish-tools.github.io/ghactions4r/reference/use_update_pkgdown.html) workflow from the [`{ghactions4r}` package](https://nmfs-fish-tools.github.io/ghactions4r/) to set up a GitHub Action that renders the pkgdown site automatically on changes to the main branch. Note that this workflow will deploy the pkgdown site to a branch called gh-pages, so the [publishing source for GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site) will need be set to the root of the gh-pages branch. There is also a [`{usethis}` method](https://usethis.r-lib.org/reference/use_pkgdown.html) for automatically rendering your pkgdown site. The difference between the `{usethis}` approach and `{ghactions4r}` is that `{ghactions4r}` makes it so you only have to update the ghactions workflow once. 

### Examples of tools and packages with NOAA themed pkgdown sites

- [nmfspalette](https://nmfs-fish-tools.github.io/nmfspalette/)
- [r4MAS](https://nmfs-fish-tools.github.io/r4MAS/)
- [adnuts](https://cole-monnahan-noaa.github.io/adnuts/)
- [bayesdfa](https://fate-ewi.github.io/bayesdfa/)
- [wham](https://timjmiller.github.io/wham/)

## Going further

Optional steps to improve your pkgdown page

### Adding a video tutorial to your landing page

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



