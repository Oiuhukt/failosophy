---
layout: full-width
title: blog
---

<ul class="content-listing">
    {% for post in site.posts %}
    <li class="listing">
        <hr class="slender" />
        <a href="{{ post.url | prepend: site.baseurl }}">
        	<h3 class="contrast">{{ post.title }}</h3>
        </a>
        <span class="smaller post-date">{{ post.date | date: "%B %-d, %Y" }}</span>
        <div class="excerpt-container">{{ post.excerpt }}</div>
    </li>
    {% endfor %}
</ul>
