---
title: 집합 항등식 — 분배법칙 · 드모르간 법칙
created: 2026-06-21
updated: 2026-06-21
type: concept
tags: [set-theory, theorem, proof]
sources: [raw/transcripts/set-theory-2-2026-06-21.md]
confidence: high
---

# 집합 항등식 — 분배법칙 · 드모르간 법칙

`A, B, C ⊆ X`. 모든 증명의 핵심 전략은 [[set-operations]]의 상등 정의 —
**양쪽 포함을 각각 보인다(`⊆` 둘 다)** — 이다. 합·교·여집합 정의는 [[set-operations]] 참고.

## Proposition (a) — 분배법칙 ✅ 증명됨
$$
A \cap (B \cup C) = (A \cap B) \cup (A \cap C)
$$

**증명 (NTS: 양쪽 포함).** 노트에서는 `⊆`, `⊇`를 한 줄씩 보였고, 각 단계가 **동치(⟺)**라
한 줄기로 양방향이 동시에 증명된다:

$$
\begin{aligned}
x \in A \cap (B \cup C)
&\iff x \in A \ \text{and}\ (x \in B \ \text{or}\ x \in C) \\
&\iff (x \in A \ \text{and}\ x \in B)\ \text{or}\ (x \in A \ \text{and}\ x \in C) \\
&\iff x \in A\cap B \ \text{or}\ x \in A\cap C \\
&\iff x \in (A\cap B) \cup (A\cap C). \qquad \blacksquare
\end{aligned}
$$

> 🔑 **핵심 비약 지점**: 둘째 줄 `and`가 `or` 위로 분배되는 단계는 **집합론이 아니라 논리(명제)의
> 분배법칙**이다. 즉 집합 분배법칙은 *논리 분배법칙을 원소 단위로 옮긴 것*. (사용자 메모: "어디서
> 공리적 비약이 일어나는지 파악하기" — 여기선 집합↔논리 대응이 그 지점.)

## Exercises — 풀이 완료
모두 (a)와 같은 **동치 사슬(⟺)** 전략. 핵심은 매 단계가 *집합 연산 = 논리 연산*의 대응이라는 것.

### (b) 분배법칙 (쌍대형) — $A \cup (B \cap C) = (A \cup B) \cap (A \cup C)$
> [!example]- 풀이 (펼쳐보기)
>
> $$
> x \in A \cup (B \cap C)
> $$
>
> $$
> \iff x \in A \ \text{or}\ (x \in B \ \text{and}\ x \in C)
> $$
>
> $$
> \iff (x \in A \ \text{or}\ x \in B)\ \text{and}\ (x \in A \ \text{or}\ x \in C)
> $$
>
> 위 줄이 핵심: **논리에서 `or`가 `and` 위로 분배**된다 ($P \lor (Q \land R) = (P\lor Q)\land(P\lor R)$).
>
> $$
> \iff x \in (A\cup B)\ \text{and}\ x \in (A\cup C) \iff x \in (A\cup B)\cap(A\cup C). \qquad \blacksquare
> $$

### (c) 드모르간 I — $(A \cup B)^c = A^c \cap B^c$
> [!example]- 풀이 (펼쳐보기)
>
> $$
> x \in (A\cup B)^c \iff x \notin A\cup B \iff \lnot(x\in A \ \text{or}\ x\in B)
> $$
>
> 논리 드모르간 $\lnot(P\lor Q) = \lnot P \land \lnot Q$ 적용:
>
> $$
> \iff (x\notin A)\ \text{and}\ (x\notin B) \iff x\in A^c \ \text{and}\ x\in B^c \iff x\in A^c \cap B^c. \qquad \blacksquare
> $$

### (d) 드모르간 II — $(A \cap B)^c = A^c \cup B^c$
> [!example]- 풀이 (펼쳐보기)
>
> $$
> x \in (A\cap B)^c \iff \lnot(x\in A \ \text{and}\ x\in B)
> $$
>
> 논리 드모르간 $\lnot(P\land Q) = \lnot P \lor \lnot Q$ 적용:
>
> $$
> \iff (x\notin A)\ \text{or}\ (x\notin B) \iff x\in A^c \cup B^c. \qquad \blacksquare
> $$

## 관련
- 합·교·여집합·상등 정의 → [[set-operations]]
- 집합·조건제시법 토대 → [[set-theory]]

## 출처
- [[set-theory-2-2026-06-21]] (손글씨 공부 노트 part 2)
