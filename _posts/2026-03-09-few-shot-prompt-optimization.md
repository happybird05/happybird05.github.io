---
title: "Few-shot Prompt Optimization"
date: 2026-03-09 09:00:00 +0900
categories: [research-log]
tags: [prompting]
status: "Ongoing"
summary: "An experiment log tracking performance changes from prompt structure updates."
---

## Research Question

How does the ordering of few-shot examples affect model accuracy and stability?

## Experimental Setup

- Model: baseline-small-llm
- Data: task-set-v2
- metric: accuracy / consistency

## Intermediate Results

- +2.1% accuracy with Prompt v2
- Slight consistency increase (+0.6%)

## Next Actions

1. Run 3 additional experiments with a fixed seed
2. Manually classify 50 error cases
3. Compare against the method in paper review #1
