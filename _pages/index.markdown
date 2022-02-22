---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

permalink: /
title: home
layout: default
description: giacomowm
---

## Project pages:

### - [Proportional Area Radar Chart](/pa_radar/)


## Recent Blog Posts:

<h3>
  {% for post in site.posts %}
	<p><a href="{{ post.url }}" class="post-preview">{{ post.title }}</a></p>
  {% endfor %}
</h3>

### see all: [Blog](/blog/)

## [Contact](/contact/)



