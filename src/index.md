---
title: "Hello First"
layout: "base.njk"
templateEngineOverride: njk,md
---

This is a home page.

## From the Blog

<ul><li>
{% for post in collections.posts | randomPost -%}
<a href="{{ post.url }}">{{ post.data.title }}</a>
{%- endfor -%}
</li></ul>


## Articles

<ul>
{% for article in collections.articles -%}
<li><a href="{{ article.url }}">{{ article.data.title }}</a></li>
{%- endfor -%}
</ul>