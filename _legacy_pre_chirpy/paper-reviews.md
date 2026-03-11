---
layout: default
title: 논문 리뷰
permalink: /paper-reviews/
---
<section class="section-panel">
  <p class="eyebrow">Paper Reviews</p>
  <h1>논문 리뷰</h1>
  <p>새 리뷰는 `_paper_reviews` 폴더에 Markdown 파일로 추가하면 됩니다.</p>

  {% assign reviews = site.paper_reviews | sort: "date" | reverse %}
  <div class="grid-2">
    {% for review in reviews %}
    <article class="list-card">
      <p class="item-meta">{{ review.date | date: "%Y-%m-%d" }} · {{ review.venue }}</p>
      <a href="{{ review.url | relative_url }}">
        <h3>{{ review.title }}</h3>
      </a>
      <p>{{ review.summary }}</p>
    </article>
    {% endfor %}
  </div>
</section>
