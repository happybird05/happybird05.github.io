---
title: 1-Day Analysis
icon: fas fa-bug
order: 5
---

This page automatically lists posts in the `1day-analysis` category.

{% assign analyses = site.posts | where_exp: "post", "post.categories contains '1day-analysis'" | sort: "date" | reverse %}

{% if analyses.size > 0 %}
{% for post in analyses %}
- [{{ post.title }}]({{ post.url | relative_url }})
  - {{ post.date | date: "%Y-%m-%d" }}{% if post.cve %} · {{ post.cve }}{% endif %}{% if post.target %} · {{ post.target }}{% endif %}
  - {{ post.summary }}
{% endfor %}
{% else %}
No 1-day analyses have been published yet.
{% endif %}
