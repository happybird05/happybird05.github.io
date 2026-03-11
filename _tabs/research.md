---
title: Research
icon: fas fa-flask
order: 3
---

This page automatically lists posts in the `research-log` category.

{% assign logs = site.posts | where_exp: "post", "post.categories contains 'research-log'" | sort: "date" | reverse %}

{% if logs.size > 0 %}
{% for post in logs %}
- [{{ post.title }}]({{ post.url | relative_url }})
  - {{ post.date | date: "%Y-%m-%d" }}{% if post.status %} · {{ post.status }}{% endif %}
  - {{ post.summary }}
{% endfor %}
{% else %}
No research logs have been published yet.
{% endif %}
