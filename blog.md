---
layout: default
title: Blog
header: Blog
description: Blog!
permalink: /blog/
---

{% for post in site.posts %}
  <p><a href="{{ post.title }}">{{ post.title }}</a><br>
  {{ post.description }}<br>
   {{ post.date | date_to_string }}</p>
{% endfor %}



