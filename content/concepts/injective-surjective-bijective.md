---
title: 단사 · 전사 · 전단사 (Injective · Surjective · Bijective)
created: 2026-06-21
updated: 2026-06-21
type: concept
tags: [set-theory, definition, study-note]
sources: [raw/transcripts/set-theory-4-2026-06-21.md]
confidence: high
---

# 단사 · 전사 · 전단사

함수 [[function]] `f: A→B`의 세 가지 핵심 성질.

## 단사 (1-1, Injective)
서로 다른 입력은 서로 다른 출력으로 간다 — **겹쳐 들어오지 않음**.

$$
f(x_1) = f(x_2) \implies x_1 = x_2 \qquad(\text{대우: } x_1 \neq x_2 \implies f(x_1) \neq f(x_2))
$$

## 전사 (Onto, Surjective)
공역 `B`의 모든 원소가 **누군가의 상**이다 — **빠짐없이 덮음**.

$$
\operatorname{Im} f = f(A) = B \qquad\Longleftrightarrow\qquad \forall y \in B,\ \exists a \in A \text{ s.t. } f(a) = y
$$

(치역=공역. → [[image-of-set]], [[function]])

## 전단사 (Bijective)
**단사 + 전사**. 입력과 출력이 완벽히 1:1로 짝지어진다.

$$
\text{bijective} \iff \text{1-1 and onto}
$$

전단사일 때만 [[inverse-function]] `f⁻¹: B→A`를 정의할 수 있다.

## 다음 단계
- 전단사 → 역함수 정의 → [[inverse-function]]
- 단사/전사를 합성으로 특징짓기(선택공리 등장) → [[inverse-via-composition]]

> 📌 **나중에 공부 (TODO)**: **집합의 개수 / 농도(cardinality)**. "두 집합이 전단사로 이어지면
> 크기가 같다"는 정의가 여기서 출발한다([[equivalence-relation]]의 P(A) 예시가 그 씨앗). 이번 단원
> 범위 밖이라 별도로 다룰 것.

## 관련
- 함수·치역의 정의 → [[function]]
- 상(전사 정의에 쓰임) → [[image-of-set]]

## 출처
- [[set-theory-4-2026-06-21]] (손글씨 공부 노트 part 4)
