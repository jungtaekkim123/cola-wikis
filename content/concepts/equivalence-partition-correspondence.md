---
title: 동치관계 ↔ 분할 1:1 대응
created: 2026-06-21
updated: 2026-06-21
type: concept
tags: [set-theory, theorem, proof]
sources: [raw/transcripts/set-theory-5-2026-06-21.md]
confidence: high
---

# 동치관계 ↔ 분할 1:1 대응

집합 `X` 위에서 **동치관계와 분할은 본질적으로 같은 것**이다. 두 방향으로 서로를 만들 수 있고,
그 둘은 정확히 역과정이라 1:1 대응을 이룬다.

## 방향 ①: 동치관계 → 분할
[[equivalence-relation|동치관계]] `∼_R`가 주어지면, 동치류들의 모임 $\{[x] \mid x\in X\}$ 가 [[partition|분할]]이 된다.
→ 증명은 [[equivalence-class]]에 있음 (비어있지 않음·덮음·서로소).

## 방향 ②: 분할 → 동치관계 (Exercise 풀이)
분할 $\mathcal{F}=\{E_i \mid i\in I\}$ 가 주어지면, **같은 조각에 있으면 관계**라고 정의:
$$
x \sim_R y \iff \exists i\in I \text{ s.t. } x,y\in E_i
$$
이 `∼_R`이 동치관계임을 보인다.

> [!example]- 반사·대칭·추이 증명 (펼쳐보기)
> - **반사**: 덮음 조건(③)에 의해 임의의 $x$는 어떤 $E_i$에 속한다. 그러면 $x,x\in E_i$ 이므로 $x\sim_R x$.
> - **대칭**: $x\sim_R y$ 면 어떤 $E_i$에 $x,y$가 함께 있다. 그러면 $y,x\in E_i$ 이므로 $y\sim_R x$.
> - **추이**: $x\sim_R y$ ($x,y\in E_i$), $y\sim_R z$ ($y,z\in E_j$) 라 하자. 그러면 $y\in E_i\cap E_j$ 이므로
>   $E_i\cap E_j\neq\varnothing$. 분할의 **서로소 조건(②)**에 의해 $i=j$. 따라서 $x,z\in E_i$ 이므로 $x\sim_R z$. $\blacksquare$
> 👉 추이성이 분할의 "서로소"에서 곧장 나온다 — 두 구조가 같은 정보임을 보여주는 핵심 고리.

## 방향 ③: 1:1 대응 (두 방향은 서로 역)
$$
\{\,X \text{ 위 동치관계}\,\} \;\longleftrightarrow\; \{\,X \text{ 의 분할}\,\}
$$
$$
\sim_R \;\longmapsto\; \{[x]_R \mid x\in X\}, \qquad P \;\longmapsto\; \sim_{R(P)}
$$

> [!example]- 왜 서로 역인가 (펼쳐보기)
> - 동치관계 $\sim_R$ → 분할 $\{[x]\}$ → 다시 관계: "같은 동치류에 속함". 그런데 $x,y$가 같은 동치류에
>   있음 $\iff x\sim_R y$ 이므로, **원래 관계가 그대로 복원**된다.
> - 분할 $P$ → 관계 $\sim_{R(P)}$ → 다시 분할: 그 관계의 동치류는 정확히 원래 조각 $E_i$. **원래 분할 복원**.
> 두 합성이 모두 항등이므로 두 방향은 서로 [[inverse-function|역]]이고, 따라서 1:1 대응(전단사). $\blacksquare$

## 의미
"같다고 볼 기준"(동치관계)을 정하는 것과 "묶음으로 쪼개기"(분할)는 **완전히 같은 행위**다.
ℤ를 3으로 나눈 나머지로 묶는 것([[partition]] 예시)이 곧 "3으로 나눈 나머지가 같다"는 동치관계.

## 관련
- 방향 ① 증명 → [[equivalence-class]]
- 두 끝의 구조 → [[equivalence-relation]], [[partition]]

## 출처
- [[set-theory-5-2026-06-21]] (손글씨 공부 노트 part 5)
