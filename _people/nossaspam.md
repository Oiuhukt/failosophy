---
name: Mar Azuela
layout: author
---

Estudiante de posgrado blah blah...


<h3>Entradas escritas por {{ page.name }}:</h3>
<ul>
{% for post in site.posts %}
{% if post.author == page.name %}
<li><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
{% endif %}
{% endfor %}
</ul>
