---
title:  "[SS] Ch02 Differential Equation and Responses (zero-input, zero-state, natural, forced) w/o Laplace transform"
last_modified_at: 2020-10-06 18:14:59
categories: 
 - SS
use_math: true
tags: 
 - Differential Equation
 - method of undetermined coefficients
---

# Differential Equation and Response (zero-input, zero-state, natural, forced) w/o LT

다음 미분방정식 의 시스템이 있다고 하자

$$\frac{d^2 y(t)}{dt^2} + 3\frac{dy(t)}{dt}+2y(t)=\frac{dx(t)}{dt}$$

아래와 같은 입력과 초기조건에서

- zero-state response (초기조건이 0.)
- zero-input response (input이 0.)
- natural response (system mode만으로 구성.)
- forced response (input signal에만 의한 항으로 구성.)

를 구하라.

## input signal

$$x(t)=t^2+5t$$

## initial conditions

$$y(0^-)=2 \\
\frac{dy(0^-)}{dt} = 3$$

## Sol 1. Classic Method

1. **Homogeneous Solution 구하기**
    1. Characteristic Equation을 구한다.

        $$\begin {aligned}
        \frac{d^2 y(t)}{dt^2} + 3\frac{dy(t)}{dt}+2y(t) &=\frac{dx(t)}{dt} \\
        (D^2 +3D +2) y(t) &= D x(t)
        \end {aligned}$$

    2. Characteristic Equation으로부터 Eigen value, $\lambda$들을 구하여 $Ce^{\lambda}t$ 항으로 구성된 general homogeneous solution을 구한다.

        $$D^2+3D+2 = (D+2)(D+1)\\ \lambda_1=-2, \lambda_2=-1 \\\text{}\\\therefore y_\text{h}(t)=C_1e^{\lambda_1t}+C_2e^{\lambda_2t}=C_1e^{-2t}+C_2e^{-1t}$$

2. **Particular Solution 구하기 ( by method of undetermined coefficients, 미정계수법)**
    1. 입력 함수 $x(t)$의 형태에 따라 $y_\text{p}(t)$를 정한다.

        $$x(t)=t^2+5t\\\therefore y_\text{p}(t)=C_3t^2+C_4t+C_5$$

    2. 정한 $y_p(t)$를 미분방정식에 대입하여 풀어서 각 계수를 구한다.

        $$\begin {aligned}
        \frac{d^2 y_\text{p}(t)}{dt^2} + 3\frac{dy_\text{p}(t)}{dt}+2y_\text{p}(t) &=\frac{dx(t)}{dt} \\
        2C_3+3(2C_3t+C_4)+2(C_3t^2+C_4t+C_5)&=2t+5\\2C_3t^2+(6C_3+2C_4)t+2C_3+3C_4+2C_5&=2t+5
        \end {aligned}$$

        $$\therefore 2C_3=0, 6C_3+2C_4=2,2C_3+3C_4+2C_5=5\\C_3=0, C_4=1,C_5=1$$

        $$y_\text{p}(t)=t+1$$

3. Complete Solution 구하기.
    1. $y(t)=y_\text{h}(t)+y_\text{p}(t)$ 이며, 현재 모르는 계수들은 initial condition으로 찾는다.

        $$\begin{aligned} y(0^-)=C_1e^{-2\cdot0}+C_2e^{-1\cdot0}+0+1=2\\\therefore C_1+C_2=1\\\text{}\\Dy(0^-)=-2C_1e^{-2\cdot0}-1C_2e^{-1\cdot0}+1&=3\\\therefore-2C_1-C_2=2\\\end{aligned}$$

        $$\therefore C_1=-3,C_2=4$$

    2. 최종 결과는 다음과 같음.

        $$y(t)=-3e^{-2t}+4e^{-t}+t+1$$

4. Zero-input vs. Zero-state
    1. Zero-state 에서는 init state가 모조리 0 이므로 다음이 성립.

        $$\begin{aligned} y(0^-)=C_1e^{-2\cdot0}+C_2e^{-1\cdot0}+0+1=0\\\therefore C_1+C_2=-1\\\text{}\\Dy(0^-)=-2C_1e^{-2\cdot0}-1C_2e^{-1\cdot0}+1&=0\\\therefore-2C_1-C_2=-1\\\end{aligned}$$

        $$\therefore C_1=2,C_2=-3$$

        $$y_\text{zs}(t)=2e^{-2t}-3e^{-t}+t+1$$

    2. Zero-input response는 이전의 Complete solution에서 Zero-state response를 뺀 항임.

        $$y_\text{zi}(t)=-5e^{-2t}+7e^{-t}$$

5. Natural response vs. Forced response
    1. Natural response는 Homogeneous solution을 구성하고 있는 system mode들로 구성됨. 즉, 다음과 같음.

        $$y_\text{n}(t)=-3e^{-2t}+4e^{-t}$$

    2. Forced response는 Complete solution에서 system mode들을 제외한 항들로 구성됨. 즉, 다음과 같음.

        $$y_\text{f}(t)=t+1$$

## Sol 2.

보통은 이처럼 풀지 않고, Laplace transform을 이용하여 s-domain에서 미방을 푸는게 일반적임. 
[[SS] Ch02 Differential Equation and Responses (zero-input, zero-state, natural, forced)](https://www.dsaint31.me/ss/ss-ch02-de-and-responses/)
