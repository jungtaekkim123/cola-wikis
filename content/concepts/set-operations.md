---
title: 집합 연산 (합·교·여집합) 과 집합의 상등
created: 2026-06-21
updated: 2026-06-21
type: concept
tags: [set-theory, definition, study-note]
sources: [raw/transcripts/set-theory-2-2026-06-21.md]
confidence: high
---

# 집합 연산과 집합의 상등

## 전체집합 (Universal Set)
모든 논의의 바탕이 되는 집합을 **전체집합** `X`라 한다. 이후 모든 집합은 `A, B ⊆ X`로 본다.
여집합(ᶜ)은 항상 이 전체집합 `X`를 기준으로 정의된다.

## 세 가지 기본 연산
조건제시법([[set-theory]])으로 정의한다. `A, B ⊆ X` 일 때:

| 연산 | 정의 | 의미 |
|---|---|---|
| 합집합 `A ∪ B` | $\{x \mid x \in A \text{ or } x \in B\}$ | 둘 중 **하나라도** 속함 |
| 교집합 `A ∩ B` | $\{x \mid x \in A \text{ and } x \in B\}$ | **둘 다** 속함 |
| 여집합 `Aᶜ` | $\{x \mid x \notin A\}$ | `X`에서 `A`에 **안** 속함 |

> 논리어 `or`/`and`/`not`이 각각 `∪`/`∩`/`ᶜ`에 대응한다 — 집합 연산은 사실 논리 연산의 집합 버전.

## 집합의 상등 (A = B)
두 집합이 같다는 것은 **서로가 서로의 부분집합**이라는 뜻:

$$
A = B \iff A \subseteq B \text{ and } B \subseteq A
$$

원소 수준으로 풀면:
$$
A = B \iff (x \in A \Rightarrow x \in B) \text{ and } (y \in B \Rightarrow y \in A)
$$

이 **"양쪽 포함을 각각 보인다"**는 전략이 집합 등식 증명의 표준 틀이다 → [[set-identities]]에서 실제로 사용.

## 관련
- 집합·원소·조건제시법의 토대 → [[set-theory]]
- 이 연산들이 만족하는 법칙(분배·드모르간) → [[set-identities]]

## 출처
- [[set-theory-2-2026-06-21]] (손글씨 공부 노트 part 2)
