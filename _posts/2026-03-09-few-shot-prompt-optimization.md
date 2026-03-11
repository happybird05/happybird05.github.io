---
title: "Few-shot Prompt Optimization"
date: 2026-03-09 09:00:00 +0900
categories: [research-log]
tags: [prompting, experiments]
status: "Ongoing"
summary: "Prompt 구조 변경에 따른 성능 차이를 추적한 실험 로그."
---

## 연구 질문

Few-shot 예시의 배치 순서가 모델 정확도와 안정성에 어떤 영향을 주는가?

## 실험 설정

- 모델: baseline-small-llm
- 데이터: task-set-v2
- metric: accuracy / consistency

## 중간 결과

- Prompt v2에서 정확도 +2.1%
- consistency score는 소폭 증가(+0.6%)

## 다음 액션

1. seed를 고정한 재실험 3회
2. error case 50개 수동 분류
3. paper review #1 방법론과 비교
