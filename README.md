# happybird05.github.io

`jekyll-theme-chirpy` 기반으로 구성한 개인 연구 블로그입니다.

## 현재 구조

- `_config.yml`: Chirpy 사이트 설정
- `_tabs/`: 사이드바 탭 페이지
  - `cv.md`
  - `paper-reviews.md`
  - `research.md`
  - `categories.md`, `tags.md`, `archives.md`, `about.md`
- `_posts/`: 실제 게시글 (논문 리뷰/개인 연구 로그)
- `_data/contact.yml`: 사이드바 연락처 아이콘
- `_plugins/posts-lastmod-hook.rb`: Git 기반 last modified 자동 반영

## 로컬 실행 (WSL Ubuntu)

```bash
cd /mnt/c/Users/aqmn8/Desktop/min_blog/happybird05.github.io
~/.local/share/gem/ruby/3.0.0/bin/bundle install
~/.local/share/gem/ruby/3.0.0/bin/bundle exec jekyll serve --host 0.0.0.0 --port 4000
```

브라우저: `http://127.0.0.1:4000`

## 글 작성 규칙

모든 글은 `_posts`에 작성합니다.

- 논문 리뷰 글: `categories: [paper-review]`
- 개인 연구 글: `categories: [research-log]`

예시:

```yaml
---
title: "글 제목"
date: 2026-03-11 09:00:00 +0900
categories: [paper-review]
tags: [llm]
summary: "짧은 요약"
---
```

## 참고

- 기존 커스텀 구조 파일은 `_legacy_pre_chirpy/`에 보관했습니다.
- 이전 정적 템플릿 파일(`template-*.html`, `template-*.css`)은 그대로 남겨두었습니다.
