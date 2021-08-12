---
title: "First page"
layout: "base.njk"
templateEngineOverride: njk, md
---

This is home page.

## From the Blog
{% for post in collections.post | randomPost %}
    <a href="{{ post.url }}">{{ post.data.title }}</a>
{% endfor %}