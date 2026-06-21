---
title: 동치류 (Equivalence Class) [x]
created: 2026-06-21
updated: 2026-06-21
type: concept
tags: [set-theory, definition, theorem, proof]
sources: [raw/transcripts/set-theory-5-2026-06-21.md]
confidence: high
---

# 동치류 (Equivalence Class) [x]

## 정의
집합 `X` 위의 [[equivalence-relation|동치관계]] `∼_R`가 있을 때, `x∈X`의 **동치류**는
`x`와 관계 맺는 모든 원소의 집합:

$$
[x] = \{ y \in X \mid x \sim_R y \}
$$

"`x`의 동치류". (예: [[partition|ℤ mod 3]]의 `[0],[1],[2]`가 각각 0,1,2의 동치류.)

## 정리 — 동치류들은 분할을 이룬다 (Exercise 풀이)
$\mathcal{F} = \{ [x] \mid x\in X \}$ 는 `X`의 [[partition|분할]]이다.

> [!example]- ① 비어있지 않음 (펼쳐보기)
> 반사성에 의해 $x\sim_R x$ 이므로 $x\in[x]$. 따라서 모든 동치류 $[x]\neq\varnothing$. $\blacksquare$

> [!example]- ③ 덮음 (펼쳐보기)
> 임의의 $x\in X$ 는 $x\in[x]$ 이므로 어떤 동치류엔 반드시 속한다. 따라서 $\bigcup_{x\in X}[x]=X$. $\blacksquare$

> [!example]- ② 서로소 — 핵심: 겹치면 같다 (펼쳐보기)
> $[x]\cap[y]\neq\varnothing$ 이면 $[x]=[y]$ 임을 보이면 충분(서로 다른 류는 안 겹침).
> $z\in[x]\cap[y]$ 라 하자. 그러면 $x\sim z$ 이고 $y\sim z$. 대칭으로 $z\sim y$, 추이로 $x\sim y$.
> 이제 임의의 $w\in[x]$ ($x\sim w$): 대칭으로 $y\sim x$, 추이로 $y\sim w$, 즉 $w\in[y]$. 따라서 $[x]\subseteq[y]$.
> 대칭적으로 $[y]\subseteq[x]$. 그러므로 $[x]=[y]$. $\blacksquare$
> (대칭·추이가 "겹치면 통째로 같다"를 만든다 — 이게 동치류가 깔끔히 조각나는 이유.)

## 관련
- 동치류를 만드는 관계 → [[equivalence-relation]]
- 동치류들이 이루는 구조 → [[partition]]
- 역방향까지 묶은 대응 정리 → [[equivalence-partition-correspondence]]

## 출처
- [[set-theory-5-2026-06-21]] (손글씨 공부 노트 part 5)
