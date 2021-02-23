---
layout: default
title: Blog
header: Blog
description: Blog!
permalink: /blog/
---

{% for post in site.posts %}
  <p><a href="{{ post.url }}">{{ post.title }}</a><br>
  {{ post.description }}<br>
   {{ post.date | date_to_string }}</p>
{% endfor %}



{% for post in site.posts %}
<div class="post-preview">
    <a href="{{ post.url | prepend: site.baseurl }}">
        <h2 class="post-title">
            {{ post.title }}
        </h2>
        {% if post.subtitle %}
        <h3 class="post-subtitle">
            {{ post.subtitle }}
        </h3>
        {% endif %}
        <div class="post-content-preview">
            {% if post.lang == 'en' %}
                {{ post.content | strip_html | truncate:300 }}
            {% else %}
                {{ post.content | strip_html | truncate:200 }}
            {% endif %}
        </div>
    </a>
    <p class="post-meta">
        Posted by {% if post.author %}{{ post.author }}{% else %}{{ site.title }}{% endif %} on {{ post.date | date: "%B %-d, %Y" }}
    </p>
</div>
<hr>
{% endfor %}
