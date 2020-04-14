---
title:  "[SS] Ch02 Differential Equation : RL 회로"
last_modified_at: 2019-03-11 11:33:59
categories:
 - SS
use_math: true
tags:
 - math
 - signal
---

# [SS] Differential Equation : RL System 

@(Signal and System)

다음의 RL회로를 미분방정식을 이용한 고전적 방식으로 풀어본다.


![!RL_circuit](https://docs.google.com/drawings/d/e/2PACX-1vTVCCDNR7e2eYa_ulsCEP86hGDh9Xp_HRjybb-OMhw0dwHzwDw0GcFiw17T5Y9nMkP4Y7k9PQzzdyeA/pub?w=927&h=434)

* $t=0$에서 스위치가 닫힘.

입출력 및 초기조건은 다음과 같음.

* input : $E$
* output : $i(t)$
* initial condition
	* $i_0=0$ (inductor의 초기값)


## Differential Equation

KVL에 의하여 다음이 성립

$$
\begin{align*}
L\frac{di(t)}{dt}+Ri(t) &= E \\
\frac{di(t)}{dt}+\frac{R}{L}i(t) &= \frac{E}{L}
\end{align*}
$$

### Homogeneous solution

$$
\begin{align*}
\frac{di_h(t)}{dt}+\frac{R}{L}i_h(t) &= 0 \\
\frac{di_h(t)}{dt} &= -\frac{R}{L}i_h(t) \\
\frac{1}{i_h(t)}di_h(t) &= -\frac{R}{L}dt \\
\displaystyle{\int_{C}^{i_h(t)} \frac{1}{i_h(\tau)}di(\tau)} &= \displaystyle{-\frac{R}{L} \int_0^{t} d\tau} \\
\left[ \ln i_h(\tau) \right] _{C}^{i_h(t)} &= \left[ -\frac{R}{L} \tau \right]_0^t \\
\ln i_h(t) - \ln C &= -\frac{R}{L} t \\
\ln \frac{i_h(t)}{C} &= -\frac{R}{L} t \\
\frac{i_h(t)}{C} &= e^{-\frac{R}{L} t} \\
i_h(t) &= C e^{-\frac{R}{L} t} \\
\end{align*}
$$

> 특성방정식으로 풀면 다음과 같음.
>
>$$
\begin{align*}
\frac{di_h(t)}{dt}+\frac{R}{L}i_h(t) &= 0 \\
Di_h(t)+\frac{R}{L}i_h(t) &= 0 \\
(D+\frac{R}{L})i_h(t) &= 0 \\
\lambda &= -\frac{R}{L}  \\
i_h(t) &= C e^{-\frac{R}{L} t} \\
\end{align*}
$$

### Particular solution

$$
\begin{align*}
\frac{di(t)}{dt}+\frac{R}{L}i(t) &= \frac{E}{L}
\end{align*}
$$

$\frac{E}{L}$이 상수이므로, particular solution $i_p(t)$도 상수의 형태를 가짐 (흔히, 입력함수와 같은 형태의 출력함수를 가짐). 즉, 다음과 같음.

$$
i_p(t) = n
$$

이를 미분방정식에 대입하여 풀면,

$$
\begin{align*}
\frac{di(t)}{dt}+\frac{R}{L}i(t) &= \frac{E}{L} \\
\frac{dn}{dt}+\frac{R}{L}n &= \frac{E}{L} \\
0+\frac{R}{L}n &= \frac{E}{L} \\
n &= \frac{E}{R} \\
\therefore i_p(t) &= \frac{E}{R} 
\end{align*}
$$

### Complete solution

$$
\begin{align*}
i(t) &= i_h(t) + i_p(t) \\
&=C e^{-\frac{R}{L} t} +  \frac{E}{R}
\end{align*}
$$

초기조건을 대입하여 상수 $C$를 구함.

$$
\begin{align*}
i_0=i(0&)=C e^{-\frac{R}{L} 0} +  \frac{E}{R}=0 \\
\therefore C&=-\frac{E}{R}
\end{align*}
$$

즉, $i(t)$는 다음과 같음.

$$
\begin{align*}
i(t) &=-\frac{E}{R} e^{-\frac{R}{L} t} +  \frac{E}{R} \\
&=\frac{E}{R} (1-e^{-\frac{R}{L} t})
\end{align*}
$$

