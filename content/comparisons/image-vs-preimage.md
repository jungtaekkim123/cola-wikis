---
title: 상(image) vs 역상(preimage) — 집합 연산 보존 비교
created: 2026-06-21
updated: 2026-06-21
type: comparison
tags: [set-theory, comparison, study-note]
sources: [raw/transcripts/set-theory-3-2026-06-21.md, raw/transcripts/set-theory-4-2026-06-21.md]
confidence: high
---

# 상(image) vs 역상(preimage) — 집합 연산 보존 비교

## 비교 대상
함수 [[function]] `f: A→B`에서 두 방향의 대응:
- **상** `f(A₁) = {f(x) | x∈A₁}` ⊆ B  → [[image-of-set]]
- **역상** `f⁻¹(B₁) = {x∈A | f(x)∈B₁}` ⊆ A  → [[preimage]]

## 연산 보존 비교

| 연산 | 상 `f(·)` | 역상 `f⁻¹(·)` |
|---|---|---|
| 합집합 ∪ | `f(A₁∪A₂) = f(A₁)∪f(A₂)` ✅ 등호 | `f⁻¹(B₁∪B₂) = f⁻¹(B₁)∪f⁻¹(B₂)` ✅ 등호 |
| 교집합 ∩ | `f(A₁∩A₂) ⊆ f(A₁)∩f(A₂)` ⚠️ 포함만 | `f⁻¹(B₁∩B₂) = f⁻¹(B₁)∩f⁻¹(B₂)` ✅ 등호 |
| 여집합 ᶜ | 일반적으로 등호 ✗ | `f⁻¹(B₁ᶜ) = (f⁻¹(B₁))ᶜ` ✅ 등호 |

**한 줄 결론: 역상은 ∪·∩·여집합을 모두 보존하지만, 상은 ∪만 보존한다.**

## 왜 이런 차이가 나나 (synthesis)
- **역상**은 원소 `x`에 대한 *조건* `f(x)∈B₁`으로 정의된다. 불리언 연산(or/and/not)이
  이 조건에 **그대로 분배**되므로 [[set-identities]]의 논리 구조가 깨지지 않는다.
- **상**은 `∃x` (존재)로 정의된다. `∃`는 `or`(∪)와는 잘 맞지만 `and`(∩)와는 충돌한다:
  서로 다른 입력이 같은 출력으로 합쳐질 수 있어(비단사) 교집합에서 정보가 새어 등호가 깨진다.
- 따라서 등호 회복 조건: **`f`가 단사(injective)이면 상도 ∩에서 등호**가 된다.

> 교훈(사용자 학습 메모): "어디서 공리적 비약이 일어나나" — 여기선 `∃`(상) vs 조건판정(역상)의
> 차이가 핵심. 위상수학에서 연속함수를 **역상**으로 정의하는 이유도 이 깔끔함 때문이다.

## 왕복(round-trip) 부등호 — 풀이 완료
상과 역상을 연달아 적용하면 제자리로 안 돌아오고 **한쪽으로만 포함**된다.

> [!example]- ① $f(f^{-1}(B_1)) \subseteq B_1$ — 증명 + 반례 (펼쳐보기)
>
> $$
> y\in f(f^{-1}(B_1)) \implies \exists x\in f^{-1}(B_1),\ f(x)=y \implies f(x)\in B_1 \ \text{and}\ f(x)=y \implies y\in B_1. \quad\blacksquare
> $$
>
> **등호 조건**: $B_1\subseteq \operatorname{Im}f$ (특히 `f`가 [[injective-surjective-bijective|전사]]면 항상 등호).
> **반례**: $f:\{1\}\to\{a,b\},\ f(1)=a$ (비전사). $B_1=\{b\}$ → $f^{-1}(\{b\})=\varnothing$ → $f(\varnothing)=\varnothing \subsetneq \{b\}$.

> [!example]- ② $f^{-1}(f(A_1)) \supseteq A_1$ — 증명 + 반례 (펼쳐보기)
>
> $$
> x\in A_1 \implies f(x)\in f(A_1) \implies x\in f^{-1}(f(A_1)). \quad\blacksquare
> $$
>
> **등호 조건**: `f`가 [[injective-surjective-bijective|단사]].
> **반례**: $f:\{1,2\}\to\{0\},\ f(1)=f(2)=0$ (비단사). $A_1=\{1\}$ → $f(A_1)=\{0\}$ → $f^{-1}(\{0\})=\{1,2\}\supsetneq\{1\}$.

> [!note]- ③ 정리 — 왜 한쪽으로만? (펼쳐보기)
> ①은 "출발이 `f(x)`" 라 항상 $B_1$ 안. 단 $B_1$ 중 **상에 없는 원소**는 못 돌아옴 → 전사면 해결.
> ②는 `x`가 $A_1$에 있으면 당연히 돌아옴. 단 **`x`와 같은 값을 갖는 다른 원소**가 딸려 들어옴 → 단사면 해결.
> 즉 ① 깨짐 = 전사 실패, ② 깨짐 = 단사 실패. 둘 다이면(전단사) 양쪽 등호.

## 관련
- [[image-of-set]] · [[preimage]] · [[function]] · [[set-identities]]
- 등호 조건과 직결 → [[injective-surjective-bijective]]

## 출처
- [[set-theory-3-2026-06-21]] (손글씨 공부 노트 part 3)
