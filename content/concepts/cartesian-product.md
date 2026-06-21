---
title: 곱집합 (Cartesian Product) A×B
created: 2026-06-21
updated: 2026-06-21
type: concept
tags: [set-theory, definition, study-note]
sources: [raw/transcripts/set-theory-2-2026-06-21.md]
confidence: high
---

# 곱집합 (Cartesian Product) A×B

## 정의
두 집합 `A, B`에 대해 **곱집합** `A×B`는 **순서쌍(ordered pair) `(a,b)`들의 집합**:

$$ A \times B = \{ (a, b) \mid a \in A,\ b \in B \} $$

- `a`는 `A`에서, `b`는 `B`에서 뽑은 원소. 첫째·둘째 자리의 **순서가 의미를 가진다**
  ((a,b) ≠ (b,a) 일반적으로).
- `A`의 원소 `m`개, `B`의 원소 `n`개면 `A×B`의 원소는 `m·n`개.

## 왜 중요한가 — 함수의 토대
[[function]]이 바로 이 곱집합의 **부분집합**으로 정의된다. "함수는 집합으로 정의되는 대상"이라는
관점(사용자 메모)의 출발점이 곱집합이다: `f: A→B` 는 `A×B`에서 조건을 만족하는
부분집합 `S_f ⊆ A×B`로 본다.

## 관련
- 순서쌍·부분집합의 토대 → [[set-theory]]
- 곱집합의 부분집합으로 정의되는 대응 → [[function]]

## 출처
- [[set-theory-2-2026-06-21]] (손글씨 공부 노트 part 2)
