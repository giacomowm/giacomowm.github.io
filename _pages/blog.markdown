---
layout: default
title: Blog
permalink: /blog
---

# Blog Posts

<ul>
  {% for post in site.posts %}
  <h4><li><a href="{{ post.url }}" class="post-preview">{{ post.title }}</a></li></h4>
  {% endfor %}
</ul>