---
layout: default
title: 개인 연구
permalink: /research/
---
<section class="section-panel">
  <p class="eyebrow">Research Logs</p>
  <h1>개인 연구</h1>
  <p>새 연구 로그는 `_research_logs` 폴더에 Markdown 파일로 추가하면 됩니다.</p>

  {% assign logs = site.research_logs | sort: "date" | reverse %}
  <div class="grid-2">
    {% for log in logs %}
    <article class="list-card">
      <p class="item-meta">{{ log.date | date: "%Y-%m-%d" }} · {{ log.status }}</p>
      <a href="{{ log.url | relative_url }}">
        <h3>{{ log.title }}</h3>
      </a>
      <p>{{ log.summary }}</p>
    </article>
    {% endfor %}
  </div>
</section>
