---
layout: default
title: Blog
header: Blog
description: Blog!
permalink: /blog/
---

{% for post in site.posts %}
  <p><a href="failosophy/{{ post.permalink }}">{{ post.title }}</a><br>
  {{ post.description }}<br>
  :date: {{ post.date | date_to_string }}</p>
{% endfor %}
