---
layout: page-hero
title: Academia
nav_title: Academia
head_title: Publicaciones
subtitle: 
weight: 3
title: Academia
header: failosophy
description: Academia
---

Aquí quiero publicar documentos que me parecen son de interés general para la comunidad filosófica.


<h2>{{ page.name }}</h2>

{{ content }}

<h2>Entradas escritas por {{ page.name }}:</h2>
<ul>
{% for post in site.posts %}
{% if post.author == page.name %}
<li><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
{% endif %}
{% endfor %}
</ul>
