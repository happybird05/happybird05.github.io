# happybird05.github.io

Jekyll 기반으로 구성한 개인 연구 블로그입니다.

## 핵심 구조
- `_config.yml`: 사이트 설정 + 컬렉션(`paper_reviews`, `research_logs`)
- `_layouts/default.html`: 공통 레이아웃
- `_layouts/post.html`: 리뷰/연구 상세 레이아웃
- `index.html`: 홈 (최신 논문 리뷰/개인 연구 자동 목록)
- `cv.md`: CV 페이지
- `paper-reviews.md`: 논문 리뷰 목록 페이지
- `research.md`: 개인 연구 목록 페이지
- `_paper_reviews/*.md`: 논문 리뷰 원고
- `_research_logs/*.md`: 개인 연구 원고
- `assets/css/main.css`: 공통 스타일

## 로컬 실행
1. Ruby/Bundler 설치
2. 의존성 설치
   - `bundle install`
3. 개발 서버 실행
   - `bundle exec jekyll serve`
4. 브라우저에서 `http://127.0.0.1:4000` 접속

### WSL(Ubuntu)에서 실행 예시
```bash
cd /mnt/c/Users/aqmn8/Desktop/min_blog/happybird05.github.io
~/.local/share/gem/ruby/3.0.0/bin/bundle install
~/.local/share/gem/ruby/3.0.0/bin/bundle exec jekyll serve --host 0.0.0.0 --port 4000
```

## 새 글 작성
- 논문 리뷰: `_paper_reviews/날짜-슬러그.md`
- 개인 연구: `_research_logs/날짜-슬러그.md`

각 파일의 front matter 예시:

```yaml
---
title: "글 제목"
date: 2026-03-11
summary: "짧은 요약"
---
```

## 참고
- 이전 정적 HTML 템플릿(`template-*.html`, `template-*.css`) 파일은 그대로 보관되어 있습니다.
