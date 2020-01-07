---
title: "[Math] Function (함수)"
last_modified_at: 2018-04-23 18:33:59
author: dsaint31
categories: 
 - Mathematics
use_math: true
tags: 
 - function
 - transform
---

# [Math] Function (함수)
@(Mathematics)[math, mathematics, function]

**Function**은 흔히 mapping(사상), transformation(변환)이라는 용어로 불리기도 함.

## 수학적 정의

두 set $X$와 $Y$의 원소 간에 관계 $f$가 다음을 만족할 경우, function이라 한다.

* $\all x \in X$에 대해 $y=f(x)$인 $\all y \in Y$가 반드시 존재함.
* $x_1, x_2 \in X$일 경우, $x_1=x_2$이며 $f(x_1) = f(x_2)가 반드시 성립함.

위 두 조건을 만족하는 function $f$는 다음과 같이 표기된다.

$$
f: X \mapsto Y
$$

### 관련 용어.

domain (정의역) : $X$
codomain (공역) : $Y$
image (상) : $Y$의 원소 중 $X$의 원소와 mapping이된 원소 또는 해당 원소로 구성된 set. 항상 codomain의 subset임.
preimage (원상) : image에 대응하는 $X$의 원소.
range (치역) : 모든 image들의 set.
indepedent variable (독립변수) : domain의 임의의 원소.
dependent variable (종속변수) : range의 임의의 원소.

## Types of function

### one-to-one (단사) function

$f:X \mapsto Y$에서 $\all x_1, x_2 \in X$ 라 하자.
이때 $f(x_1) = f(x_2) \Rightarrow x_1 = x_2$가 성립하는 경우,
$f$를 one-to-one(or injection) function이라고 함. 

### onto (전사) function

$f:X \mapsto Y$에서 $\all y \in Y$가 적어도 하나의 $x \in X$의 image인 경우
$f$를 onto (surjection) function이라고 함.

* functon $f$의 range는 codomain가 일치함.


### one-to-one correspondence (전단사) function

* onto 이면서 one-to-one.
* bijection이라고 함.
