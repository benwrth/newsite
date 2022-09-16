---
layout: page
title: Blog Categories
permalink: /blog/categories
---

Looking for something more specific? Find an individual category to explore its contents.

  <div class="info-box">
  <p class="info-box-title">TECHNOLOGY/IT</p>
{%- if site.posts.size > 0 -%}
<table class="post-list">
    {% for post in site.categories.IT %}
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
  </div>

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
  </div>

  <p class="right"><a href="/blog">Back to all posts</a></p>