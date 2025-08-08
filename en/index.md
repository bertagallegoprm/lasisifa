---
layout: post
title: Latest Post
---

{% assign posts_en = site.posts | where_exp:"post","post.url contains '/en/'" %}
{% if posts_en.size > 0 %}
  <h1>{{ posts_en.first.title }}</h1>
  <p><em>{{ posts_en.first.date | date: "%B %d, %Y" }}</em></p>
  {{ posts_en.first.content }}
{% else %}
  <p>No posts yet.</p>
{% endif %}
