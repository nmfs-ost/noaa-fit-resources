---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: single
title: Welcome to the NOAA Fisheries Integrated Toolbox (NOAA FIT) Resources!
sidebar:
  nav: "docs"
---

Use the [Categories](./categories) or [Tags](./tags) menu options to find resources, or use the search bar.

Looking for software tools? Navigate back to the [NOAA FIT Homepage](https://noaa-fisheries-integrated-toolbox.github.io/).

For questions, comments, or ideas for the the Resources page, [contact the team](https://noaa-fisheries-integrated-toolbox.github.io/resources/noaa%20fit/contact/).

## Latest Posts

<ul>
  {% for post in site.posts limit:5%}
    <li>
      <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>


