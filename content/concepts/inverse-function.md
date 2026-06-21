---
title: 역함수 (Inverse Function) f⁻¹
created: 2026-06-21
updated: 2026-06-21
type: concept
tags: [set-theory, definition, study-note]
sources: [raw/transcripts/set-theory-4-2026-06-21.md]
confidence: high
---

# 역함수 (Inverse Function) f⁻¹

## 정의 (전단사일 때만)
`f: A→B`가 **전단사(bijective)** ([[injective-surjective-bijective]])이면, 역함수
`f⁻¹: B→A`를 정의할 수 있다:

$$
f^{-1}(b) = a \quad\text{where } f(a) = b
$$

- 잘 정의되는 이유: **전사**라서 각 `b`에 대응되는 `a`가 **존재**하고,
  **단사**라서 그 `a`가 **유일**하다. 둘 다 있어야 역함수가 함수가 된다.
- 집합으로: $S_{f^{-1}} = \{ (b, a) \in B \times A \mid f(a) = b \}$ — `f`의 순서쌍을 뒤집은 것.

## ⚠️ 역함수 f⁻¹ vs 역상 f⁻¹(B₁) — 표기 충돌 주의
같은 기호 `f⁻¹`를 쓰지만 **완전히 다른 두 대상**이다:

| | [[inverse-function]] `f⁻¹` | [[preimage]] `f⁻¹(B₁)` |
|---|---|---|
| 정체 | **함수** `B→A` | **집합** (A의 부분집합) |
| 입력/출력 | 원소 `b` ↦ 원소 `a` | 집합 `B₁` ↦ 집합 `{x | f(x)∈B₁}` |
| 존재 조건 | `f`가 **전단사일 때만** | **항상** (f가 어떤 함수든) |

> 핵심: 역상은 역함수가 없어도 늘 쓸 수 있다. 표기가 같다고 같은 것이 아니다.

## 관련
- 존재 전제: 전단사 → [[injective-surjective-bijective]]
- 헷갈리는 짝: 역상 → [[preimage]]
- `f⁻¹∘f = id_A`, `f∘f⁻¹ = id_B` → [[function-composition]], [[inverse-via-composition]]

## 출처
- [[set-theory-4-2026-06-21]] (손글씨 공부 노트 part 4)
