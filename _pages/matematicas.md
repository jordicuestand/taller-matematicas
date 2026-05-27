---
layout: page
title: Matemáticas
permalink: /matematicas/
---

<h2>Artículos de Matemáticas</h2>

<ul>
{% for post in site.posts %}
  {% assign cats = post.categories | join: "," | downcase %}
  {% if cats contains "matem" %}
    <li>
      {{ post.date | date: "%d/%m/%Y" }}
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endif %}
{% endfor %}
</ul>
