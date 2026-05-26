---
title: Totes les entrades
layout: default
permalink: /totes-les-entrades/
---

## Llista completa d'entrades

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      ({{ post.date | date: "%d/%m/%Y" }})
    </li>
  {% endfor %}
</ul>
