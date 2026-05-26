---
title: Todas las entradas
layout: default
permalink: /all_posts/
---

## Lista completa de entradas

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      ({{ post.date | date: "%d/%m/%Y" }})
    </li>
  {% endfor %}
</ul>
