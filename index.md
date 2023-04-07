---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: single
title: Welcome to the NOAA Fisheries Integrated Toolbox (NOAA FIT) Resources!
sidebar:
  nav: "docs"
---

The [NOAA Fisheries Integrated Toolbox Resources site](..) includes resources for both [tool developers](../categories/#developer-resources) and [tool users](../categories/#software-user-resources). Browse by [category](../categories) or [tag](../tags) menu options to find resources, or use the search bar.

## Latest Posts

<ul>
  {% for post in site.posts limit:5%}
    <li>
      <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>


