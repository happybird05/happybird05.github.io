---
title: Paper Reviews
icon: fas fa-book-open
order: 2
---

`paper-review` 카테고리 글을 자동으로 모아 보여줍니다.

{% assign reviews = site.posts | where_exp: "post", "post.categories contains 'paper-review'" | sort: "date" | reverse %}

{% if reviews.size > 0 %}
{% for post in reviews %}
- [{{ post.title }}]({{ post.url | relative_url }})
  - {{ post.date | date: "%Y-%m-%d" }}{% if post.venue %} · {{ post.venue }}{% endif %}
  - {{ post.summary }}
{% endfor %}
{% else %}
아직 등록된 논문 리뷰가 없습니다.
{% endif %}
