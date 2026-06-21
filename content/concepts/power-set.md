---
title: 멱집합 (Power Set)
created: 2026-06-21
updated: 2026-06-21
type: concept
tags: [set-theory, definition, study-note]
sources: [raw/transcripts/set-theory-2026-06-21.md, raw/transcripts/set-theory-2-2026-06-21.md]
confidence: high
---

# 멱집합 (Power Set)

## 정의
집합 `C`의 **멱집합** `P(C)`는 **`C`의 모든 부분집합을 원소로 갖는 집합**이다.
(노트의 "set of collection" 표현이 이것 — *부분집합들의 집합*.)

$$ P(C) = \{ S \mid S \subseteq C \} $$

## 예시
`C = {1, 2}` 이면:

$$ P(C) = \{\ \varnothing,\ \{1\},\ \{2\},\ \{1, 2\}\ \} $$

- 공집합 `∅` 과 자기 자신 `{1,2}` 도 항상 부분집합이므로 멱집합의 원소에 포함된다.

## 원소 개수
유한집합 `C`의 원소가 `n`개이면 멱집합의 원소는 **`2^n`개**.

> 위 예시는 `n = 2` → `2^2 = 4`개 (`∅, {1}, {2}, {1,2}`). 노트의 결과와 일치.

### 📝 Exercise (노트) — `|A|=n` 이면 `|P(A)|=2ⁿ`
> [!example]- 풀이 (펼쳐보기)
> **방법 1 — 특성함수(지시함수) 일대일 대응.**
> 각 부분집합 `B⊆A`에 함수 $\chi_B: A\to\{0,1\}$ 를 대응시킨다 ($x\in B$면 1, 아니면 0).
> 이 대응 `B ↦ χ_B`는 $P(A)$와 "함수 $A\to\{0,1\}$ 전체"의 [[inverse-function|일대일 대응(전단사)]]이다.
> 그런 함수는 `n`개 원소 각각에 2지선다(`0/1`)를 독립으로 주므로 $2^n$개.
> 따라서 $|P(A)| = 2^n$. $\blacksquare$
>
> **방법 2 — 수학적 귀납법.**
> $n=0$: $A=\varnothing$, $P(A)=\{\varnothing\}$, $|P(A)|=1=2^0$. ✓
> $n\to n+1$: $a\in A$ 하나 고정, $A'=A\setminus\{a\}$ ($|A'|=n$). $A$의 부분집합은
> **`a`를 안 가진 것**(= $A'$의 부분집합, 귀납가정 $2^n$개)과 **`a`를 가진 것**(= $A'$의 부분집합에 `a` 추가, 역시 $2^n$개)으로 양분된다.
> 합쳐 $2^n + 2^n = 2^{n+1}$. $\blacksquare$

## 관련
- 부분집합·원소 개념의 토대 → [[set-theory]]
- 수의 집합들에도 멱집합을 생각할 수 있다 → [[number-sets]]

## 출처
- [[set-theory-2026-06-21]] (손글씨 공부 노트, raw/transcripts)
