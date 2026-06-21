---
title: 함수 (Function) — 집합론적 정의
created: 2026-06-21
updated: 2026-06-21
type: concept
tags: [set-theory, definition, study-note]
sources: [raw/transcripts/set-theory-2-2026-06-21.md]
confidence: high
---

# 함수 (Function) — 집합론적 정의

## 핵심 관점: 함수도 "집합"이다
함수는 별도의 원시 개념이 아니라 **집합으로 정의되는 대상**이다(사용자 메모). 구체적으로
[[cartesian-product]] `A×B`의 **특정 부분집합**으로 정의한다.

## 정의
두 집합 `A, B`에 대해, `f: A → B`가 **함수**라는 것은 다음 조건을 만족하는
부분집합 `S_f ⊆ A × B`가 존재한다는 뜻이다:

$$
\forall a \in A,\ \exists!\, b \in B \ \text{such that}\ (a, b) \in S_f
$$

즉 **정의역 `A`의 각 원소 `a`마다, `(a,b) ∈ S_f`인 `b`가 정확히 하나(`∃!`, 유일하게)** 존재한다.
이때 그 유일한 `b`를 `f(a)`로 적는다: `b = f(a)`.

> 두 가지가 함수의 조건: ① **빠짐 없이**(모든 `a`에 대해 존재) ② **겹침 없이**(그 `b`가 유일).
> 한 `a`가 두 값으로 가거나, 어떤 `a`에 값이 없으면 함수가 아니다(노트 하단 다이어그램).

## 정의역 · 공역 · 치역
| 용어 | 기호 | 뜻 |
|---|---|---|
| 정의역 (domain) | `A` | 입력이 되는 집합 |
| 공역 (codomain) | `B` | 출력이 담길 수 있는 집합 |
| 치역 (range / image) | `Im f` | **실제로** 대응된 출력들의 모임 |

$$
\operatorname{Im} f = \{ b = f(a) \mid a \in A \} \subseteq B
$$

- 치역은 항상 공역의 **부분집합**이며, 같을 수도(전사) 아닐 수도 있다.
- 사용자 메모: "실제로 대응시켜준 원소들을 치역이라고 부른다" — 즉 `B` 전체가 아니라 *닿은* 부분.

## 관련
- 함수의 정의 무대가 되는 곱집합 → [[cartesian-product]]
- 부분집합·원소·조건제시법 토대 → [[set-theory]]
- 부분집합을 `f`로 보낸 결과 → [[image-of-set]] (상)
- `B`의 부분집합을 거꾸로 끌어온 것 → [[preimage]] (역상)
- 상 vs 역상의 연산 보존 차이 → [[image-vs-preimage]]
- 함수의 성질: 단사·전사·전단사 → [[injective-surjective-bijective]]
- 함수끼리 잇기 → [[function-composition]]
- 전단사일 때의 역함수 → [[inverse-function]]

## 출처
- [[set-theory-2-2026-06-21]] (손글씨 공부 노트 part 2)
