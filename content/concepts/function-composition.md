---
title: 합성함수 (Function Composition) g∘f
created: 2026-06-21
updated: 2026-06-21
type: concept
tags: [set-theory, definition, study-note]
sources: [raw/transcripts/set-theory-4-2026-06-21.md]
confidence: high
---

# 합성함수 (Function Composition) g∘f

## 정의
두 함수 [[function]] `f: A→B`, `g: B→C`가 주어졌을 때, **합성** `g∘f: A→C`는
`f`를 먼저, `g`를 나중에 적용:

$$
(g \circ f)(x) = g(f(x))
$$

$$
A \xrightarrow{\ f\ } B \xrightarrow{\ g\ } C, \qquad x \mapsto f(x) \mapsto g(f(x))
$$

집합으로 보면 ([[cartesian-product]]의 부분집합):
$$
S_{g \circ f} = \{ (x,\, g(f(x))) \mid x \in A \} \subseteq A \times C
$$

> ⚠️ 합성 가능 조건: `f`의 **공역**과 `g`의 **정의역**이 맞아야 한다(`f`의 도착=`g`의 출발=B).
> 순서가 중요: `g∘f`는 "f 먼저". 일반적으로 `g∘f ≠ f∘g`.

## 항등함수
`id_A: A→A, x↦x`는 합성의 항등원: `f∘id_A = f = id_B∘f`.
이 항등함수가 [[inverse-via-composition]]에서 단사/전사 특징짓기의 기준이 된다.

## 합성과 단사·전사 보존 (보조정리) — Exercise 풀이
`f: A→B`, `g: B→C`. [[injective-surjective-bijective]] 성질이 합성에서 어떻게 전해지나.

> [!example]- 1) `g∘f` 전사 ⟹ `g` 전사 (펼쳐보기)
> 임의의 `c∈C`. `g∘f`가 전사이므로 $\exists a\in A,\ g(f(a))=c$. 그러면 $b=f(a)\in B$ 가 $g(b)=c$.
> 따라서 `g`는 전사. $\blacksquare$ (단, `f`는 전사가 아닐 수 있음 — 뒤쪽 `g`만 보장됨)

> [!example]- 2) `g∘f` 단사 ⟹ `f` 단사 (펼쳐보기)
> $f(a_1)=f(a_2)$이면 $g(f(a_1))=g(f(a_2))$, 즉 $(g\circ f)(a_1)=(g\circ f)(a_2)$.
> `g∘f`가 단사이므로 $a_1=a_2$. 따라서 `f`는 단사. $\blacksquare$ (앞쪽 `f`만 보장됨)

> [!example]- 3) `f`,`g` 둘 다 단사 ⟹ `g∘f` 단사 (펼쳐보기)
> $(g\circ f)(a_1)=(g\circ f)(a_2) \Rightarrow g(f(a_1))=g(f(a_2)) \xRightarrow{g\,1\text{-}1} f(a_1)=f(a_2) \xRightarrow{f\,1\text{-}1} a_1=a_2.$ $\blacksquare$

> [!example]- 4) `f`,`g` 둘 다 전사 ⟹ `g∘f` 전사 (펼쳐보기)
> 임의의 `c∈C`. `g` 전사 ⟹ $\exists b,\ g(b)=c$. `f` 전사 ⟹ $\exists a,\ f(a)=b$. 그러면 $g(f(a))=c$. $\blacksquare$

> 💡 1)·2)는 "합성이 좋으면 **부분**도 좋다"(바깥 g의 전사, 안쪽 f의 단사), 3)·4)는 "부분이 좋으면 **합성**도 좋다". 이 네 보조정리가 [[equivalence-relation]]의 P(A) 예시(대칭·추이) 증명에 그대로 쓰인다.

## 관련
- 합성되는 대상 → [[function]]
- 합성으로 단사/전사를 특징짓기 → [[inverse-via-composition]]
- 역함수는 `f⁻¹∘f = id` 를 만족 → [[inverse-function]]
- 보조정리의 응용 → [[equivalence-relation]]

## 출처
- [[set-theory-4-2026-06-21]] (손글씨 공부 노트 part 4)
