---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: single
title: Welcome to the NOAA Fisheries Integrated Toolbox (NOAA FIT) Resources!
sidebar:
  nav: "docs"
---

The [NOAA Fisheries Integrated Toolbox Resources site](..) includes resources for both [tool developers](https://noaa-fisheries-integrated-toolbox.github.io/resources/categories/#developer-resources) and [tool users](https://noaa-fisheries-integrated-toolbox.github.io/resources/categories/#software-user-resources). Browse by [category](https://noaa-fisheries-integrated-toolbox.github.io/resources/categories) or [tag](https://noaa-fisheries-integrated-toolbox.github.io/resources/tags) menu options to find resources, or use the search bar.

## Latest Posts

<ul>
  {% for post in site.posts limit:5%}
    <li>
      <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>


