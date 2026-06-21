---
title: 분할 (Partition)
created: 2026-06-21
updated: 2026-06-21
type: concept
tags: [set-theory, definition, study-note]
sources: [raw/transcripts/set-theory-5-2026-06-21.md]
confidence: high
---

# 분할 (Partition)

## 정의
집합 `E`와 첨자집합(index set) `I` (각 `i∈I`마다 부분집합 `E_i⊆E`)에 대해,
$\mathcal{F}=\{E_i \mid i\in I\}$ 가 **분할(partition)** 이라는 것은 세 조건을 만족한다는 뜻:

| 조건 | 식 | 뜻 |
|---|---|---|
| ① 비어있지 않음 | $E_i \neq \varnothing$ | 빈 조각 없음 |
| ② 서로소 (disjoint) | $\alpha \neq \beta \Rightarrow E_\alpha \cap E_\beta = \varnothing$ | 조각끼리 안 겹침 |
| ③ 덮음 (cover) | $\bigcup_{i\in I} E_i = E$ | 빠짐없이 다 덮음 |

$$ \bigcup_{i\in I} E_i = \{ x \in E \mid \exists i\in I,\ x \in E_i \} $$

> 한마디로: **`E`를 겹침 없이·빠짐없이 조각낸 것**. 각 원소는 정확히 한 조각에 속한다.

## 예시 — ℤ를 3으로 나눈 나머지
정수 [[number-sets|ℤ]]에서 $[k] = \{ x\in\mathbb{Z} \mid x = 3a+k,\ a\in\mathbb{Z} \}$ (3으로 나눈 나머지가 `k`):

$$ [0]\cap[1] = [1]\cap[2] = [2]\cap[0] = \varnothing, \qquad [0]\cup[1]\cup[2] = \mathbb{Z} $$

따라서 $\mathcal{F}=\{[0],[1],[2]\}$ 는 ℤ의 분할. (이 `[k]`가 바로 동치류 → [[equivalence-class]])

## 동치관계와의 관계
모든 [[equivalence-relation|동치관계]]는 분할을 만들고, 모든 분할은 동치관계를 만든다 —
둘은 사실상 같은 것. → [[equivalence-partition-correspondence]]

## 관련
- 조각이 곧 동치류 → [[equivalence-class]]
- 동치관계 ↔ 분할 대응 → [[equivalence-partition-correspondence]]
- 서로소·합집합 개념 → [[set-operations]]

## 출처
- [[set-theory-5-2026-06-21]] (손글씨 공부 노트 part 5)
