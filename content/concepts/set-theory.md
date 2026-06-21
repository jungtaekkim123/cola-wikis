---
title: 집합론 (Set Theory) — 기초
created: 2026-06-21
updated: 2026-06-21
type: concept
tags: [set-theory, definition, study-note]
sources: [raw/transcripts/set-theory-2026-06-21.md]
confidence: high
---

# 집합론 (Set Theory) — 기초

## 집합이란
**집합(set)** = collection = family. 즉 **잘 정의된(well-defined) 대상들의 모임**이다.

핵심 조건은 **"기준이 명확해야 한다"**는 것. 어떤 대상이 그 모임에 속하는지 아닌지를
**누구나 객관적으로 판정**할 수 있어야 집합이다.

- ✅ 집합: `{x | x는 10보다 작은 자연수}` — 판정 기준이 명확
- ❌ 집합 아님: "잘생긴 사람들의 모임" — '잘생김'은 주관적이라 소속 판정 불가 (**not well-defined**)

기호로는 `{definable objects}` 처럼 *정의 가능한* 대상들만 원소로 받는다.

## 원소와 소속 (∈)
대상 `a`가 집합 `A`에 속하면 `a ∈ A`, 속하지 않으면 `a ∉ A`.

> 예) `A = {-1, 2, 4, 5}` 이면 `-1 ∈ A`, 하지만 `0 ∉ A`.

## 집합을 적는 두 방법
1. **원소나열법 (roster)**: 원소를 직접 나열. 예) `A = {-1, 2, 4, 5}`
2. **조건제시법 (set-builder)**: 조건을 만족하는 원소로 정의. 예) `B = {x | P(x)}`
   — "성질 `P(x)`를 만족하는 모든 `x`의 집합". 여기서 `P(x)`가 바로 위에서 말한
   **well-defined 기준**에 해당한다.

## 더 들어가기
- 어떤 집합의 모든 부분집합을 모으면 → [[power-set]] (멱집합)
- 대표적인 수의 집합들 (자연수·정수·유리수) → [[number-sets]]
sp
## 출처
- [[set-theory-2026-06-21]] (손글씨 공부 노트, raw/transcripts)
