---
title: Research
icon: fas fa-flask
order: 3
---

`research-log` 카테고리 글을 자동으로 모아 보여줍니다.

{% assign logs = site.posts | where_exp: "post", "post.categories contains 'research-log'" | sort: "date" | reverse %}

{% if logs.size > 0 %}
{% for post in logs %}
- [{{ post.title }}]({{ post.url | relative_url }})
  - {{ post.date | date: "%Y-%m-%d" }}{% if post.status %} · {{ post.status }}{% endif %}
  - {{ post.summary }}
{% endfor %}
{% else %}
아직 등록된 개인 연구 로그가 없습니다.
{% endif %}
