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

Los autores que vamos a colaborar con esto somos:

{% for person in site.people %}

* <a href="{{ site.baseurl }}{{ person.url }}">{{ person.name }}</a>

{% endfor %}

<h3>Entradas escritas por {{ page.name }}:</h3>
<ul>
{% for post in site.posts %}
{% if post.author == page.name %}
<li><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
{% endif %}
{% endfor %}
</ul>
