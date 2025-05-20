# README

## Contribute to the FIT Resources Page

THe FIT Resources page is built [using the Github Pages plug in for Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll). Specifically, it uses [minimal mistakes](https://github.com/mmistakes/minimal-mistakes) as a [remote theme](https://github.com/mmistakes/minimal-mistakes#remote-theme-method).

Note that the GitHub pages plug in requires a [specific version of Jekyll](https://pages.github.com/versions/) that is not the latest. [Learn more about the GitHub pages plug in](https://www.moncefbelyamani.com/making-github-pages-work-with-latest-jekyll/).

Post by year can be seen at https://nmfs-ost.github.io/noaa-fit-resources/posts/

### How to add a post 

1. [Fork](https://docs.github.com/en/github/getting-started-with-github/quickstart/fork-a-repo) this NOAA FIT [resources repo](https://github.com/nmfs-ost/noaa-fit-resources)
2. Create a blog post [markdown file](https://guides.github.com/features/mastering-markdown/) and add it to the [posts folder](https://github.com/nmfs-ost/noaa-fit-resources/tree/main/_posts) in your forked repo
3. Label the `.md` file `YYYY-MM-DD-post-name.md`
4. Create a header and add a category and tags (to search by). Here's an example header: 

```
---
title: "Contributing to R tools in the Toolbox"
excerpt: "R tools"
date: 2021-06-11
toc: true
categories:
  - NOAA FIT
tags:
  - R
  - NOAA resources
---
```

For the categories and tags available for use, please see the lists at https://nmfs-ost.github.io/noaa-fit-resources/categories and https://nmfs-ost.github.io/noaa-fit-resources/tags. Note that the case
needs to be matched. Please also avoid adding new tags or categories, unless there really isn't a similar tag in the list already and adding the new tag would help users find it.
Only 1 category should be included for a post, but unlimited tags can be added.

> See [contributing.md](https://raw.githubusercontent.com/nmfs-ost/noaa-fit-resources/main/_posts/2021-06-11-contributing.md) for an example of the `.md` file code.
5. Once a post is created in the post folder, build the site locally using github codespaces (instructions below).
6. [create a pull request](https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request) so we can merge the changes and update the FIT site.

Need more details? Check out the [Minimal Mistakes working with posts documentation](https://mmistakes.github.io/minimal-mistakes/docs/posts/).

### Build the site locally using GitHub codespaces.

1. Open a codespace from this repo.
2. In the terminal run `bundle update`
3. Finally run `bundle exec jekyll serve`. This can be viewed using the "Ports" tab.

Changes can then be made and the website will be updated as they are made.

Note the extension "code spell checker" can be used to spell check posts. After installing, refresh the page.

Note: don't save any new files under the "_site" directory.

### Updating dependencies
Locally, run `bundle update` and commit changes to the Gemfile and Gemfile.lock.
 
### How to embed a video in a `.md` page
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

### How to embed a google calendar in a `.md` page
1. Find the embeded link in the "settings" for the google calendar.

Example code:
```
<iframe src="https://calendar.google.com/calendar/embed?src=c_43jjc1ei4kujqki7o5ud918ea8%40group.calendar.google.com&ctz=America%2FNew_York" style="border: 0" width="800" height="600" frameborder="0" scrolling="no"></iframe>
```
## Disclaimer

“The United States Department of Commerce (DOC) GitHub project code is provided on an ‘as is’ basis and the user assumes responsibility for its use. DOC has relinquished control of the information and no longer has responsibility to protect the integrity, confidentiality, or availability of the information. Any claims against the Department of Commerce stemming from the use of its GitHub project will be governed by all applicable Federal law. Any reference to specific commercial products, processes, or services by service mark, trademark, manufacturer, or otherwise, does not constitute or imply their endorsement, recommendation or favoring by the Department of Commerce. The Department of Commerce seal and logo, or the seal and logo of a DOC bureau, shall not be used in any manner to imply endorsement of any commercial product or activity by DOC or the United States Government.”
