---
layout: page
title: Física
permalink: /fisica/
---

<h2>Artículos de Física</h2>

<ul>
{% for post in site.posts %}
  {% assign cats = post.categories | join: "," | downcase %}
  {% if cats contains "física" or cats contains "fisica" or cats contains "fí" %}
    <li>
      {{ post.date | date: "%d/%m/%Y" }}
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endif %}
{% endfor %}
</ul>
