---
layout: post
title: Última entrada
---

{% assign posts_es = site.posts | where_exp:"post","post.url contains '/es/'" %}
{% if posts_es.size > 0 %}
  <h1>{{ posts_es.first.title }}</h1>
  <p><em>{{ posts_es.first.date | date: "%d %B %Y" }}</em></p>
  {{ posts_es.first.content }}
{% else %}
  <p>No hay entradas aún.</p>
{% endif %}
