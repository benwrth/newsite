---
layout: page
title: Blog
permalink: /blog
---

I occasionally write some blog posts - and you can find all of them authored by myself below. Enjoy! This is a relatively new thing so I may update the site to support things such as search if thing get a little cluttered. [Click here to filter posts by category](/blog/categories).


<div class="info-box">
<p class="info-box-title">ALL POSTS</p>
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
        <td class="post-table desktop-only right" width="100px">
            <span class="post-meta">{{ post.date | date: date_format }}</span>
        </td>
        </tr>
    {%- endfor -%}
    </table>
    {%- endif -%}
    {%- if site.posts.size == 0 -%}
    <table class="post-list">
        <tr class="post-table nopost">
        <td class="post-table">No posts can be found.</td>
        </tr>
    </table>
    {%- endif -%}
  </div>