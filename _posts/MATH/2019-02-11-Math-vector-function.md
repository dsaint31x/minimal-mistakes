---
title:  "[Math] 벡터 함수"
last_modified_at:   2019-02-11
author: dsaint31
categories: 
  - Mathematics
  - Physics
use_math: true
tags: 
  - math 
  - physics
  - vector
---

# [Math] Vector (2) : Vector Function

@(Mathematics)[physics, vector, mathematics]

## Foundation

A vector function is simply a function whose codomain(공역) is $\text{R}^n$.

In other words, rather than taking on real values, it takes on vector values.

We will often use the notation $\vec{v} = \vec{v}(t)$ to denote a vector function.

> **Note:** 
> 
> 일반적으로 vector function은 많은 책에서 $\text{r}(t)$로 표현됨.

이를 수식적으로 표현하면 다음과 같음.

$$ 
\begin{align*}
\vec{v} &= \vec{v}(t) \\
&=\textbf{v}(t)\\
&= P(t) \vec{i} + Q(t)\vec{j} + R(t)\vec{k}
\end{align*}
$$

벡터 $\vec{v}$를 base unit vector로 표현한 위의 식에서 각 component, $P(t),Q(t),R(t)$가 임의의 변수 $t$에 의한 function일 경우  vector function이라고 함.

### 일반적 vector function의 표현식 (Cartesian coordinate system)

$$ 
\begin{align*}
\vec{v} &= \vec{v}(t) \\
&= \textbf{v}(t) = \left< P(t), Q(t), R(t) \right> \\
&= P(t)\vec{i} +Q(t)\vec{j}+R(t)\vec{k} 
\end{align*}
$$

> **Note: Scalar function**
>
> A scalar function is simply a function whose codomain(공역) is $\text{R}$. 
>
> $ f=f(p_{\text{parameters}})= f(x,y,z) = Scalar $
>
> 함수의  Scalar로 주어짐.

---

## Limit of Vector Function

Vector function $\vec{v} = \left< P(t), Q(t),R(t) \right>$ 에 대하여 $t=a$에서 $\vec{v}(t)$의 limit은 다음과 같이 정의함.

$$
\begin{align*}
\lim_{t\rightarrow a}\vec{v}(t) = \left< \lim_{t\rightarrow a}P(t), \lim_{t\rightarrow a}Q(t), \lim_{t\rightarrow a}R(t)  \right>
\end{align*}
$$

* Vector function $\vec{v} = \left< P(t), Q(t),R(t) \right>$ 의 limit(극한)은 **component function $P(t),Q(t),R(t)$의 limit을 이용**하여 정의함.

## Continuity of Vector Function

Vector function $\vec{v} = \left< P(t), Q(t),R(t) \right>$ 가 $t=a$에서 연속(continuity)이라면, 다음을 모두 만족해야 함.

1. $\displaystyle{\lim_{t\rightarrow a} \vec{v}(t)}$가 존재함.
2. $\vec{v}(a)$가 존재함.
3. $\displaystyle{\lim_{t\rightarrow a} \vec{v}(t) = \vec{v}(a)}$ 가 성립.

## Derivative of Vector Function

Vector function $\vec{v}(t)$의 derivative(도함수)는 다음과 같이 정의됨.

$\vec{v}'(t)$는 **tangent vector**라고 불림.

$$
\begin{align*}
\vec{v}' = \lim_{\Delta t\rightarrow 0} \frac{\vec{v}(t+\Delta t)-\vec{v}(t)}{\Delta t}
\end{align*}
$$ 

component function 을 이용하여 derivative of vector function을 구하는 건 다음과 같음.

$$
\begin{align*}
\vec{v}' = \left< P'(t), Q'(t), R'(t) \right>
\end{align*}
$$

다음의 법칙들이 성립.

$$
\begin{align*}
(u+v)' &= u'+v' \\
(u \cdot v)' &=  u'\cdot v +u\cdot v' \\
(u \times v)' &= u' \times v + u \times v' \\
(u v w)' &= (u' v w) + (u v' w) + (u v w')
\end{align*}
$$

----

## Unit Tangent Vector

**Tangent vector (derivative of vector function)**를 자신의 norm (크기,*L2-norm*)으로 나눈 것.
즉, **크기가 1인 tangent vector**.

$$
\begin{align*}
T(t) = \frac{v'(t)}{\left\|v'(t)\right\|_2} = \frac{v'(t)}{|v'(t)|}
\end{align*}
$$

Tangent vector의 norm은 다음과 같음.

$$
\begin{align*}
\left\| v'(t) \right\|_2  = \sqrt{P'(t)^2 + Q'(t)^2 + R'(t)^2}
\end{align*}
$$

----

## Definite Integral of Vector Function

Vector function $\vec{v}(t)=\left< P(t),Q(t),R(t) \right>$ 가 구간 $[t_1,t_2]$에서 연속(continuity)일 때, 구간 $[t_1,t_2]$에서 $\vec{v}$의 definite integral(정적분) 은 다음과 같이 정의됨.

$$
\begin{align*}
\int^{t_2}_{t_1} \vec{v}(t) dt = \left< \int^{t_2}_{t_1} P(t) dt, \int^{t_2}_{t_1} Q(t) dt, \int^{t_2}_{t_1} R(t) dt \right>
\end{align*}
$$

----

## Position Vector를 이용한 선, 직선, 타원(원 포함)의 표현

* 3차원 공간에서 곡선 $C$의 방정식 

$$
\begin{align*}
\vec{v} = v(t) &= \left< a(t), b(t), c(t) \right> \\
&= a(t)\vec{i} +b(t)\vec{j}+c(t)\vec{k} 
\end{align*}
$$

* $t$가 증가할 때 곡선의 방향이 positive direction.
	* $t$가 감소할 때 곡선의 방향이 negative direction.

* 3차원 공간에서 직선의 방정식
  * 점 $$ q=\left< q_x, q_y,q_z \right> $$ (=position vector)를 지나고 
  * constant vector $$g=\left< g_x, g_y,g_z \right>$$의 방향으로 진행하는 직선
  
$$ 
\begin{align*}
\vec{v} &= \vec{q}+\vec{g}t \\
&= v(t) \\
&= \left< q_x+g_x t, q_y+g_y t,q_z+g_z t \right>
\end{align*}
$$ 



* x-y 평면에서 타원 혹은 원의 방정식

$$ 
\begin{align*}
\vec{v} &= a \cos{t}\vec{i} + b \sin{t} \vec{j} \\
&=  \left< a \cos{t}, b \sin{t}\right>
\end{align*}
$$ 

**sol.**

$$
\begin{align*}
x(t) = a \cos{t}, &\quad y(t) = b \sin{t} \\
\cos{t} = \frac{x(t)}{a}, &\quad  \sin{t} = \frac{y(t)}{b} \\
\cot^2{t} = \frac{x(t)^2}{a^2}, &\quad  \sin^2{t} = \frac{y^2(t)}{b^2} \\
\\
\cot^2{t} + \sin^2{t} &= \frac{x(t)^2}{a^2} + \frac{y^2(t)}{b^2} \\
1 &= \frac{x(t)^2}{a^2} + \frac{y^2(t)}{b^2} \\
\end{align*}
$$

즉, **타원**의 방정식.

만약, $a=b$ 라면,

$$ 
\begin{align*}
1 &= \frac{x(t)^2}{a^2} + \frac{y^2(t)}{b^2} \\
1 &= \frac{x(t)^2}{a^2} + \frac{y^2(t)}{a^2} \\
x(t)^2+y(t)^2 &= a^2
\end{align*}
$$

즉, **원**의 방정식.

---

# Velocity and Acceleration

앞에서 보였듯이 시간에 따라 변하는 특정 물체의 위치를 position vector를 이용하여 표현 가능.

(움직인 track이 곡선, 직선, 타원 등등인 경우를 앞에서 보인 방식으로 표현가능)

또한 vector를 통해 **velocity**와 **acceleration**을 구할 수 있음.

## Velocity Vector and Acceleration Vector

Position vector $\vec{r}(t)$에 대한 velocity vector $\vec{v}(t)$와 acceleration vector $\vec{a}(t)$, speed $v(t)$ 는 다음과 같음.

$$
\begin{align*}
\vec{v}(t) &= \displaystyle{\lim_{\Delta t\rightarrow 0} \frac { \vec{r}(t+\Delta t) - \vec{r}(t)}{\Delta t}} =\vec{r}'(t)\\
\vec{a}(t) &= \displaystyle{\lim_{\Delta t\rightarrow 0} \frac { \vec{v}(t+\Delta t) - \vec{v}(t)}{\Delta t}} =\vec{v}'(t) =\vec{r}''(t) \\
v(t) &= \left\| \vec{v}(t) \right\|
\end{align*}
$$

## Normal(법선) Vector

* $\vec{T}'(t)$를 normal vector라고 부름.
* Normal vector, $\vec{T}'(t)$는 tangent vector와 orthogonal함.
* Unit tangent vector, $\vec{T}(t)$의 정의로부터 **normal vector**를 구하면 다음과 같음.

$$
\begin{align*}
\vec{T}(t) &= \frac{\vec{r}' (t)}{\left\| \vec{r}' (t) \right\|} \\
\left\|\vec{T}(t)\right\| &= 1 \rightarrow \left[\vec{T}(t)\right]^2=1 \\
\end{align*}
$$

* 위 식에서 $\left[\vec{T}(t)\right]^2=1$ 를 $t$에 대해 미분하면 다음과 같음.

$$
\begin{align*}
2\vec{T}(t)\cdot\vec{T}'(t) &= 0 \\
\vec{T}(t)\cdot\vec{T}'(t) &= 0
\end{align*}
$$

* 여기서 **inner product가 0**이라는 애기는 orthogonal(직교)하다는 뜻이며, unit tangent vector $\vec{T}(t)$와 orthogonal한 $\vec{T}'(t)$를 normal vector라고 함.

## Unit Normal(법선) Vector

* Normal vector 의 크기(*L2-norm*)가 1인 경우, unit normal vector라고 부름.

$$
\begin{align*}
\vec{N}(t) = \frac{\vec{T}'(t)}{\left\|\vec{T}'(t)\right\|}
\end{align*}
$$
