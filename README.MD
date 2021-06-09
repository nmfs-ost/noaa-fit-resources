# README

## Contribute to the FIT Resources Page

### How to add a post 
1. Fork the NOAA FIT [resources repo](https://github.com/noaa-fisheries-integrated-toolbox/resources)
2. Create a blog post .md file and add it to the [posts folder](https://github.com/noaa-fisheries-integrated-toolbox/resources/tree/master/_posts) in your forked repo
3. Label the .md file YYYY-MM-DD-**post-name**.md
4. Add a category
> See [Version Control Best Practices](https://raw.githubusercontent.com/noaa-fisheries-integrated-toolbox/resources/master/_posts/2019-06-14-best-practices-version-control.md) for an example of the .md file code (you can copy, paste, and edit the header of your .md file)
5. Add the blog to the contents by adding it to the navigation file - this adds your post to the sidebar
6. In the navigation file, choose the header it lies under and add a title for your new page
```
title: "~ Version Control Best Practices"
url: /best-practices/best-practices-version-control
```
> The url will be /category/**post-name** depending on the category indicated in the .md file and the name of the .md file after the date in the posts folder
 
### How to embed a video on .md page
Using a link from YouTube or Vimeo:
1. Click ‘share’
2. Click ‘embed link’ 
3. Copy and Paste into the .md file where you want the video to appear

Example code from YouTube embed link:
```
<figure class="video_container">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/A7qDN2oYSxc" frameborder="0" allowfullscreen="true"> </iframe>
</figure>
```
 
***** *******

> ## Disclaimer

> “The United States Department of Commerce (DOC) GitHub project code is provided on an ‘as is’ basis and the user assumes responsibility for its use. DOC has relinquished control of the information and no longer has responsibility to protect the integrity, confidentiality, or availability of the information. Any claims against the Department of Commerce stemming from the use of its GitHub project will be governed by all applicable Federal law. Any reference to specific commercial products, processes, or services by service mark, trademark, manufacturer, or otherwise, does not constitute or imply their endorsement, recommendation or favoring by the Department of Commerce. The Department of Commerce seal and logo, or the seal and logo of a DOC bureau, shall not be used in any manner to imply endorsement of any commercial product or activity by DOC or the United States Government.”
