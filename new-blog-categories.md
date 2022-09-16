---
layout: page
title: Blog Categories
permalink: /blog/categories/auto
---

> ## Note: Experimental Feature
> This is a work in progress, aimed at automating sorting posts by category into their own little HTML card. This will not be functioning how I would like it to until it is merged with the existing categories page - for example, posts may be duplicated or not sorted properly. Please refer to [the normal categories page](/blog/categories) for normal readership.

Looking for something more specific? Find an individual category to explore its contents.

{% for category in site.categories %}
  <div class="info-box">
  <p class="info-box-title">{{ category | first }}</p>
{%- if site.posts.size > 0 -%}
<table class="post-list">
    {% for post in site.posts %}
    {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
        <tr class="post-table">
        <td class="post-table">
          <a class="post-link" href="{{ post.url | relative_url }}">
          {{ post.title | escape }}
          </a>
          <span class=" post-meta mobile-only">{{ post.date | date: date_format }}</span>
        </td>
        <td class="post-table desktop-only right" width="110px">
            <span class="post-meta">{{ post.date | date: date_format }}</span>
        </td>
        </tr>
    {%- endfor -%}
    </table>
    {%- endif -%}
  </div>
{%- endfor -%}






  <div class="info-box">
  <p class="info-box-title">BLOG</p>
{%- if site.posts.size > 0 -%}
<table class="post-list">
    {% for post in site.categories.blog %}
    {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
        <tr class="post-table">
        <td class="post-table">
          <a class="post-link" href="{{ post.url | relative_url }}">
          {{ post.title | escape }}
          </a>
          <span class=" post-meta mobile-only">{{ post.date | date: date_format }}</span>
        </td>
        <td class="post-table desktop-only" width="100px">
            <span class="post-meta">{{ post.date | date: date_format }}</span>
        </td>
        </tr>
    {%- endfor -%}
    </table>
    {%- endif -%}
    {%- if site.posts.size == 0 -%}
    <table class="post-list">
        <tr class="post-table nopost">
        <td class="post-table">There are no posts in this category.</td>
        </tr>
    </table>
    {%- endif -%}
  </div>

  <p class="right"><a href="/blog">Back to all posts</a></p>