---
title: 관계 (Relation)
created: 2026-06-21
updated: 2026-06-21
type: concept
tags: [set-theory, definition, study-note]
sources: [raw/transcripts/set-theory-5-2026-06-21.md]
confidence: high
---

# 관계 (Relation)

## 정의
두 집합 `A, B`에 대해, **관계(relation)** `R`은 [[cartesian-product]] `A×B`의 **부분집합**이다:

$$ R \subseteq A \times B $$

`(a,b) ∈ R`이면 "`a`가 `b`와 관계 맺음"이라 하고 $a \sim_R b$로 적는다.

## 함수는 관계의 특수한 경우
[[function]] `f: A→B`는 그 자체가 $S_f \subseteq A\times B$, 즉 **관계의 일종**이다.
다만 함수는 "각 `x∈A`마다 짝이 **유일하게 하나**"라는 추가 조건을 만족하는 특별한 관계다.
일반 관계는 그런 제약이 없다 — 한 `a`가 여럿과 관계 맺거나, 아무와도 안 맺을 수 있다.

## 예시
- `A={1,2}, B={4,5}`. `A×B={(1,4),(1,5),(2,4),(2,5)}`. `R={(1,4),(2,5)}` → `1∼ᵣ4`, `2∼ᵣ5`.
- `S=`{대학교 학생들}. `a∼ᵣb ⟺ a와 b가 친구` → `R⊆S×S` (한 집합 안에서의 관계).

## 한 집합 위의 관계 (R ⊆ A×A)
같은 집합 안에서의 관계 `R⊆A×A`는 특히 중요하다. 이때 세 성질
(반사·대칭·추이)을 물을 수 있고, 셋을 다 만족하면 [[equivalence-relation]]이 된다.

> 위 친구 관계의 세 질문 — `a∼ᵣa?` / `a∼ᵣb ⟹ b∼ᵣa?` / `a∼ᵣb, b∼ᵣc ⟹ a∼ᵣc?` — 이
> 정확히 반사·대칭·추이 점검이다. → [[equivalence-relation]]

## 관련
- 관계의 무대 → [[cartesian-product]]
- 유일성 조건을 더한 특수 관계 → [[function]]
- 반사·대칭·추이를 만족하는 관계 → [[equivalence-relation]]

## 출처
- [[set-theory-5-2026-06-21]] (손글씨 공부 노트 part 5)
