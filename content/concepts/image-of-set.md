---
title: 집합의 상 (Image) f(A₁)
created: 2026-06-21
updated: 2026-06-21
type: concept
tags: [set-theory, theorem, proof]
sources: [raw/transcripts/set-theory-3-2026-06-21.md]
confidence: high
---

# 집합의 상 (Image) f(A₁)

함수 [[function]] `f: A→B`와 부분집합 `A₁ ⊆ A`에 대해, **상(image)** 은 `A₁`의 원소들을 `f`로
보낸 결과들의 집합:

$$
f(A_1) = \{ f(x) \mid x \in A_1 \} \subseteq B
$$

(`A₁ = A`이면 `f(A) = Im f` = 치역. → [[function]])

## Proposition 2 (상과 집합 연산) — Proof Exercise
`A₁, A₂ ⊆ A`일 때:

$$
f(A_1 \cup A_2) = f(A_1) \cup f(A_2) \qquad\text{(등호)}
$$
$$
f(A_1 \cap A_2) \subseteq f(A_1) \cap f(A_2) \qquad\text{(}\subseteq\text{ 뿐!)}
$$

> ⚠️ **핵심 비대칭**: 합집합은 등호지만 **교집합은 한쪽 포함(⊆)만** 성립한다.
> 반례: 서로 다른 `x₁∈A₁`, `x₂∈A₂` 가 `f(x₁)=f(x₂)=y` 인데 `A₁∩A₂=∅`이면,
> 좌변 `f(∅)=∅` 이지만 우변엔 `y`가 들어간다. **`f`가 단사(injective)가 아니면** 등호가 깨진다.
> 이 깨짐이 없는 쪽이 역상이다 → [[preimage]], 둘의 대비는 [[image-vs-preimage]].

## Exercise — 풀이 완료
> [!example]- 풀이 ① 합집합은 등호 (펼쳐보기)
>
> $$
> y \in f(A_1\cup A_2) \iff \exists x \in A_1\cup A_2,\ f(x)=y
> $$
>
> $$
> \iff \exists x\,\big[(x\in A_1 \ \text{or}\ x\in A_2)\ \text{and}\ f(x)=y\big]
> $$
>
> 존재기호 $\exists$가 `or`와는 **분배**된다:
>
> $$
> \iff (\exists x\in A_1,\ f(x)=y)\ \text{or}\ (\exists x\in A_2,\ f(x)=y)
> $$
>
> $$
> \iff y\in f(A_1)\ \text{or}\ y\in f(A_2) \iff y \in f(A_1)\cup f(A_2). \qquad\blacksquare
> $$

> [!example]- 풀이 ② 교집합은 포함(⊆)만 (펼쳐보기)
>
> $$
> y \in f(A_1\cap A_2) \implies \exists x\in A_1\cap A_2,\ f(x)=y
> $$
>
> 그 $x$는 $A_1$에도 $A_2$에도 있으므로 $y\in f(A_1)$ 이고 $y\in f(A_2)$:
>
> $$
> \implies y\in f(A_1)\cap f(A_2). \qquad\blacksquare
> $$
>
> ⚠️ 역방향은 일반적으로 거짓: $\exists$는 `and`와 **분배되지 않는다**. $y\in f(A_1)\cap f(A_2)$는
> "$A_1$의 어떤 $x$"와 "$A_2$의 어떤 $x'$"가 각각 $y$로 갈 뿐, **같은 원소**라는 보장이 없다.

> [!example]- 반례 — 등호가 깨지는 경우 (펼쳐보기)
> $f:\{1,2\}\to\{0\}$, $f(1)=f(2)=0$ (비단사). $A_1=\{1\},\ A_2=\{2\}$.
> 좌변: $f(A_1\cap A_2)=f(\varnothing)=\varnothing$.
> 우변: $f(A_1)\cap f(A_2)=\{0\}\cap\{0\}=\{0\}$.
> $\varnothing \subsetneq \{0\}$ 이므로 등호 깨짐. **`f`가 단사([[injective-surjective-bijective]])이면 등호 성립.**

## 관련
- 함수·치역의 정의 → [[function]]
- 연산을 모두 보존하는 짝 개념 → [[preimage]]
- 상 vs 역상 비교 → [[image-vs-preimage]]

## 출처
- [[set-theory-3-2026-06-21]] (손글씨 공부 노트 part 3)
