---
title: 역상 (Preimage / Inverse Image) f⁻¹(B₁)
created: 2026-06-21
updated: 2026-06-21
type: concept
tags: [set-theory, theorem, proof]
sources: [raw/transcripts/set-theory-3-2026-06-21.md]
confidence: high
---

# 역상 (Preimage / Inverse Image) f⁻¹(B₁)

## 정의
함수 [[function]] `f: A→B`와 부분집합 `B₁ ⊆ B`에 대해, **역상(inverse image)** 은
"`f`로 보냈을 때 `B₁` 안에 떨어지는" 정의역 원소들의 집합:

$$
f^{-1}(B_1) := \{ x \in A \mid f(x) \in B_1 \} \subseteq A
$$

- 노트 표현: "B₁의 역상". `f`가 역함수를 가질 필요는 **없다** — `f⁻¹(B₁)`은 단지 기호이고,
  항상 잘 정의된다(역함수와 무관).

## Proposition 2 (역상과 집합 연산) — Proof Exercise
`B₁, B₂ ⊆ B`일 때 **세 연산 모두 등호**:

$$
f^{-1}(B_1 \cup B_2) = f^{-1}(B_1) \cup f^{-1}(B_2)
$$
$$
f^{-1}(B_1 \cap B_2) = f^{-1}(B_1) \cap f^{-1}(B_2)
$$
$$
f^{-1}(B_1^{\,c}) = \big(f^{-1}(B_1)\big)^{c}
$$

> ✅ **상([[image-of-set]])과 달리 ∩·여집합에서도 등호가 성립**한다. 이유: 역상은
> "원소 `x`에 대한 조건 `f(x)∈B₁`"으로 정의되므로, 불리언 연산(or/and/not = ∪/∩/ᶜ)이
> 조건에 **그대로 분배**된다. 즉 역상은 [[set-identities]]의 논리 구조를 깨지 않고 끌어온다.

## Exercise — 풀이 완료
세 증명 모두 **"$x$를 $f(x)\in\cdot$ 조건으로 바꾸면 불리언 연산이 그대로 통과"**한다.
[[image-of-set|상]]과 달리 $\exists$가 없어 `and`/`not`에서도 깨지지 않는 게 핵심.

> [!example]- (a) 합집합 $f^{-1}(B_1\cup B_2)=f^{-1}(B_1)\cup f^{-1}(B_2)$ (펼쳐보기)
>
> $$
> x\in f^{-1}(B_1\cup B_2) \iff f(x)\in B_1\cup B_2 \iff f(x)\in B_1 \ \text{or}\ f(x)\in B_2
> $$
>
> $$
> \iff x\in f^{-1}(B_1)\ \text{or}\ x\in f^{-1}(B_2) \iff x\in f^{-1}(B_1)\cup f^{-1}(B_2). \qquad\blacksquare
> $$

> [!example]- (b) 교집합 $f^{-1}(B_1\cap B_2)=f^{-1}(B_1)\cap f^{-1}(B_2)$ (펼쳐보기)
>
> $$
> x\in f^{-1}(B_1\cap B_2) \iff f(x)\in B_1 \ \text{and}\ f(x)\in B_2
> $$
>
> $$
> \iff x\in f^{-1}(B_1)\ \text{and}\ x\in f^{-1}(B_2) \iff x\in f^{-1}(B_1)\cap f^{-1}(B_2). \qquad\blacksquare
> $$

> [!example]- (c) 여집합 $f^{-1}(B_1^{\,c})=(f^{-1}(B_1))^{c}$ (펼쳐보기)
>
> $$
> x\in f^{-1}(B_1^{\,c}) \iff f(x)\in B_1^{\,c} \iff f(x)\notin B_1
> $$
>
> $$
> \iff x\notin f^{-1}(B_1) \iff x\in (f^{-1}(B_1))^{c}. \qquad\blacksquare
> $$

## 관련
- 함수의 정의 → [[function]]
- 비대칭을 갖는 짝 개념 → [[image-of-set]]
- 왜 역상이 더 잘 작동하나 → [[image-vs-preimage]]
- 사용된 논리=집합 대응 → [[set-identities]]

## 출처
- [[set-theory-3-2026-06-21]] (손글씨 공부 노트 part 3)
