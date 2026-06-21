---
title: 동치관계 (Equivalence Relation)
created: 2026-06-21
updated: 2026-06-21
type: concept
tags: [set-theory, definition, theorem, proof]
sources: [raw/transcripts/set-theory-5-2026-06-21.md]
confidence: high
---

# 동치관계 (Equivalence Relation)

[[relation]] `R ⊆ A×A`가 다음 세 성질을 모두 만족하면 **동치관계(equivalence relation)**다.

| 성질 | 기호 정의 | 뜻 |
|---|---|---|
| ① 반사 (Reflexive) | $\forall x,\ (x,x)\in R$ | $x \sim_R x$ — 자기 자신과 관계 |
| ② 대칭 (Symmetric) | $(x,y)\in R \Rightarrow (y,x)\in R$ | $x\sim_R y \Rightarrow y\sim_R x$ |
| ③ 추이 (Transitive) | $(x,y),(y,z)\in R \Rightarrow (x,z)\in R$ | $x\sim_R y,\ y\sim_R z \Rightarrow x\sim_R z$ |

> 직관: 동치관계는 "**같다고 볼 만한**" 관계를 추상화한 것. 셋이 모이면 집합을 깔끔히
> 묶을 수 있고, 그 묶음이 [[partition]]이 된다 → [[equivalence-partition-correspondence]].

## 예시 (작은 것)
`A={1,2,3,4}`, `R={(1,1),(2,2),(3,3),(4,4),(1,2),(2,1)}`.
- 대각선 `(i,i)` 4개는 **반사**를 위해 필수(necessary). `(1,2),(2,1)`는 선택(optional)이지만
  대칭 짝이 함께 있어야 한다. → 동치관계 ✓ (이 관계는 `{1,2}`와 `{3},{4}`로 묶는다)

## 친구 관계는 동치관계인가? (개념 점검)
> [!example]- 논의 (펼쳐보기)
> `S=`{학생}, `a∼b ⟺ a와 b가 친구`.
> - **반사** `a∼a`? — "자기 자신과 친구"인가? 보통 정의에서 제외 → ✗ (반사 실패 가능).
> - **대칭** `a∼b ⟹ b∼a`? — 친구는 보통 상호적 → ✅.
> - **추이** `a∼b, b∼c ⟹ a∼c`? — "친구의 친구가 내 친구"는 일반적으로 거짓 → ✗.
> 따라서 친구 관계는 (대개) **동치관계가 아니다**. 이런 반례 점검이 세 공리의 독립성을 체감하게 한다.

## 핵심 예시 — P(A) 위 "전단사 존재" 관계는 동치관계
`F=P(A)` ([[power-set]]). `X∼_R Y ⟺ ∃ 전단사 f: X→Y` ([[injective-surjective-bijective]]).
이 관계가 동치관계임을 보인다 (세 성질 = id/역함수/합성).

> [!example]- ① 반사: `X∼X` (펼쳐보기)
> 항등함수 $\mathrm{id}_X: X\to X,\ x\mapsto x$ 는 전단사. 따라서 $X\sim_R X$. $\blacksquare$

> [!example]- ② 대칭: `X∼Y ⟹ Y∼X` (펼쳐보기)
> $X\sim_R Y$ 면 전단사 $f:X\to Y$ 존재. 전단사이므로 [[inverse-function|역함수]] $f^{-1}:Y\to X$ 가 존재하고
> 그 역시 전단사다 (이전 강의: $g\circ f=\mathrm{id}_X,\ f\circ g=\mathrm{id}_Y$ 인 $g=f^{-1}$).
> 따라서 $Y\sim_R X$. $\blacksquare$
> (노트의 보조 Exercise "g∘f onto⟹g onto", "g∘f 1-1⟹f 1-1"로 그 `g`가 전단사임을 확인 →
> [[function-composition]] 보조정리 1)·2).)

> [!example]- ③ 추이: `X∼Y, Y∼Z ⟹ X∼Z` (펼쳐보기)
> 전단사 $f:X\to Y$, $g:Y\to Z$ 가 있으면 합성 $g\circ f: X\to Z$.
> [[function-composition]] 보조정리 3)(단사·단사⟹단사)·4)(전사·전사⟹전사)에 의해 $g\circ f$도 전단사.
> 따라서 $X\sim_R Z$. $\blacksquare$

세 성질 모두 성립 → **동치관계**. (이 관계의 동치류가 "같은 크기의 집합"이라는 개념, 즉 cardinality로 이어진다 — 📌 나중에 공부.)

## 관련
- 토대: 한 집합 위의 관계 → [[relation]]
- 증명에 쓰인 합성 보조정리 → [[function-composition]]
- 역함수(대칭에 사용) → [[inverse-function]]
- 동치류와 분할로의 연결 → [[equivalence-class]], [[equivalence-partition-correspondence]]

## 출처
- [[set-theory-5-2026-06-21]] (손글씨 공부 노트 part 5)
