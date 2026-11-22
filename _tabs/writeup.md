---
title: Writeup
icon: fas fa-flag
order: 4
---

This page automatically lists posts in the `writeup` category.

{% assign writeups = site.posts | where_exp: "post", "post.categories contains 'writeup'" | sort: "date" | reverse %}

{% if writeups.size > 0 %}
{% for post in writeups %}
- [{{ post.title }}]({{ post.url | relative_url }})
  - {{ post.date | date: "%Y-%m-%d" }}{% if post.ctf %} · {{ post.ctf }}{% endif %}{% if post.challenge_category %} · {{ post.challenge_category }}{% endif %}
  - {{ post.summary }}
{% endfor %}
{% else %}
No writeups have been published yet.
{% endif %}
