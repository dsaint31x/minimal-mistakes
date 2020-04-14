---
title:  "[SS] Ch02 Differential Equation : RC 회로"
last_modified_at: 2019-04-10 11:33:59
categories:
 - SS
use_math: true
tags:
 - math
 - signal
---

# [SS] Differential Equation : RC System 

@(Signal and System)

다음의 RC회로를 미분방정식을 이용한 고전적 방식으로 풀어본다.

![RC](https://docs.google.com/drawings/d/e/2PACX-1vR2kKN5ZCcOWG17FavDIqii5uGvgJ6QQUprB6G1upB9Wj9PbAUyLAdhLU5hGJiDxa9d5l7R2VrIP3FA/pub?w=460&h=219)

* $t=0$에서 스위치가 닫힘.

입출력 및 초기조건은 다음과 같음.

* input : $E$
* output : $i(t)$
* initial condition
	* $q_c(0)=0$ (capacitor의 초기 전하량)


## Differential Equation

KVL에 의하여 다음이 성립

$$
\begin{align*}
Ri(t) + \frac{1}{C}\int_0^{t}i(\tau)d\tau &= E
\end{align*}
$$ 

$ i(t)=\frac{dq(t)}{dt}$를 이용하여, 위 식을 $q(t)$로 다시 기재하면 다음과 같음.

$$
\begin{align*}
R\frac{dq(t)}{dt} + \frac{1}{C}q(t) &= E \\
\frac{dq(t)}{dt} + \frac{1}{RC}q(t) &= \frac{E}{R}
\end{align*}
$$

### Homogeneous solution

$$
\begin{align*}
\frac{dq_h(t)}{dt} + \frac{1}{RC}q_h(t) &= 0 \\
\frac{dq_h(t)}{dt} &= -\frac{1}{RC}q_h(t) \\
\frac{1}{q_h(t)}dq_h(t) &= -\frac{1}{RC}dt \\
\displaystyle{\int_{A}^{q_h(t)} \frac{1}{q_h(\tau)}dq_h(\tau)} &= \displaystyle{-\frac{1}{RC} \int_0^{t} d\tau} \\
\left[ \ln q_h(\tau) \right] _{Q}^{q_h(t)} &= \left[ -\frac{1}{RC} \tau \right]_0^t \\
\ln q_h(t) - \ln A &= -\frac{1}{RC} t \\
\ln \frac{q_h(t)}{A} &= -\frac{1}{RC} t \\
\frac{q_h(t)}{A} &= e^{-\frac{1}{RC} t} \\
q_h(t) &= Ae^{-\frac{1}{RC} t} \\
\end{align*}
$$

$ i(t)=\frac{dq(t)}{dt}$를 이용하여, 위 식을 $i(t)$로 다시 기재해야 하나 complete solution에서 한번에 처리하는게 편함.

> 특성방정식으로 풀면 다음과 같음.
>
>$$
\begin{align*}
\frac{dq_h(t)}{dt}+\frac{1}{RC}q_h(t) &= 0 \\
Dq_h(t)+\frac{1}{RC}q_h(t) &= 0 \\
(D+\frac{1}{RC})q_h(t) &= 0 \\
\lambda &= -\frac{1}{RC}  \\
q_h(t) &= A e^{-\frac{1}{RC} t} \\
\end{align*}
$$

### Particular solution

$$
\begin{align*}
\frac{dq_p(t)}{dt}+\frac{1}{RC}q_p(t) &= \frac{E}{R}
\end{align*}
$$

$\frac{E}{R}$이 상수이므로, particular solution $q_p(t)$도 상수의 형태를 가짐 (입력함수와 같은 형태의 출력함수를 가짐). 즉, 다음과 같음.

$$
q_p(t) = n
$$

이를 아까의 미분방정식에 대입하여 풀면,

$$
\begin{align*}
\frac{dq_p(t)}{dt}+\frac{1}{RC}i(t) &= \frac{E}{R} \\
\frac{dn}{dt}+\frac{1}{RC}n &= \frac{E}{R} \\
0+\frac{1}{RC}n &= \frac{E}{R} \\
n &= CE \\
\therefore q_p(t) &= CE
\end{align*}
$$

### Complete solution

$$
\begin{align*}
q(t) &= q_h(t) + q_p(t) \\
&=A e^{-\frac{1}{RC} t} +  CE
\end{align*}
$$

초기조건을 대입하여 상수 $A$를 구함.

$$
\begin{align*}
q_c(0)=0&=A e^{-\frac{1}{RC} 0} +  CE \\
&=A+CE\\
\\
\therefore A&=-CE
\end{align*}
$$

즉, $q(t)$는 다음과 같음.

$$
\begin{align*}
q(t) &=-CE e^{-\frac{1}{RC} t} +  CE \\
&=CE (1-e^{-\frac{1}{RC} t})
\end{align*}
$$

출력이 $i(t)$ 이므로 $i(t)=\frac{dq(t)}{dt}$를 이용하여 구하면 다음과 같음.

$$
\begin{align*}
i(t) &=\frac{dq(t)}{dt}\\
&= -CE\left(-\frac{1}{RC}\right) e^{-\frac{1}{RC} t} \\
&=\frac{E}{R}e^{-\frac{1}{RC} t}
\end{align*}
$$


