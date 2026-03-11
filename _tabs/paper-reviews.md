---
title: Paper Reviews
icon: fas fa-book-open
order: 2
---

This page automatically lists posts in the `paper-review` category.

{% assign reviews = site.posts | where_exp: "post", "post.categories contains 'paper-review'" | sort: "date" | reverse %}

{% if reviews.size > 0 %}
{% for post in reviews %}
- [{{ post.title }}]({{ post.url | relative_url }})
  - {{ post.date | date: "%Y-%m-%d" }}{% if post.venue %} · {{ post.venue }}{% endif %}
  - {{ post.summary }}
{% endfor %}
{% else %}
No paper reviews have been published yet.
{% endif %}
