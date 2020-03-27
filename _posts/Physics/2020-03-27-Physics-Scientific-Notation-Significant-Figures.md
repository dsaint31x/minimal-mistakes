---
title:  "과학적표기법 과 유효숫자"
last_modified_ate:   2020-03-27 14:47:59
author: dsaint31
categories: 
  - Physics
tags: 
  - chemistry
---

# Scientific Notations and Significant Figures

@(Physics)

## What is Measurements?

Measurement is a **quantity** that has bot a **number** and a **unit**!

In physics and chemistry, the numbers of measurement are commonly expressed by **scientific notation (과학적표기법)**.

## Scientific Notation

Scientific notation is an expression of numbers in the form of as follow:

$$
m \times 10^n
$$

where

* $m$ is equal or greater than 1.0 and less than 10.
	* It is consist of *significant figures*!
* $n$ is an integer

## Examples

| measurement | scientific notation |
|:---:|:---:|
|$0.93 \times 10^{-5}$ | $9.3 \times 10^{-6}$ |
|$162 \times 10^2$ | $1.62 \times 10^4$ |
|$15,010,000$|$1.501 \times 10^7$|

## Significant figures (유효숫자)

* 모든 측정값은 근본적으로 **근사값** 임.
* 측정의 정확도에 한계(즉 오차가 존재)가 있기 때문에, 해당 오차보다 작은 수의 기재는 아무 의미가 없음.
* 즉, 유효한 (효력을 가지는) 수만을 표시해야 하며, 이를 significant figures(유효숫자) 라고 함.
	* 단, significant figure의 마지막 자리의 수는 *uncetainty* 를 가짐.
* 유효숫자의 개수가 많을수록 높은 **정확도**를 가짐. 

> 유효숫자는 가급적 scientific notation 으로 표기하는게 좋지만, 일반 측정치의 경우 다음과 같은 규칙을 사용한다.
>  
>  1. **모든 자리의 숫자가 0 이 아닌 경우** 모두 **유효숫자**.
>  2. **0이 아닌 숫자로 둘러싸인 자리의 0**은 **유효숫자**. 
>  3. 단지, 자리수만 표시하기 위한 0은 유효숫자가 아님.
>  4. 하지만, 소수점을 포함하지 않는 수 중에서 유효숫자의 뒤를 따르는 0은 *유효숫자일 수도 있고 유효숫자가 아닐 수도 있다*. (이 때문에 scientific notation을 권장!)
>  5. 소수점 아래의 끝자리에 있는 0 들은 유효숫자.
>  6. 단, 0.000과 같이 모든 자리의 숫자가 0이면 유효숫자가 없음.
>  7. 광속, 아보가드로 수와 같은 과학적 상수와 물건의 개수를 counting한 경우 유효숫자는 무한대로 간주.
>  8. Scientific notation(과학적 기수법)에서는 자리수가 10의 지수로 표현되고 유효숫자만이 $10^n$를 곱하는 수로 표현.
>  9. 덧셈(뺄셈)의 경우, 가장 **부정확한 수 (유효숫자의 자리수가 가장 큰 것!)** 에 의해 결과의 유효숫자 결정됨.
>> $4.5 + 0.3352 = 4.8$
>> 
>> * 가장 부정확한수는 $4.5$임. 
>> * 그렇기 때문에 결과값은 소수점 둘째 자리에서 반올림하여 얻어짐 ($4.8352 \rightarrow 4.8$).
>  10. 곱셈(나눗셈)의 경우, 결과값은 입력값들 중 가장 적은 유효숫자의 갯수에 의해 유효숫자가 결정됨.
>> $4.5 \times 0.3352 = 1.5$
>> 
>> * 가장 작은 유효숫자 수는 2개임.
>> * 곱셈 결과를 반올림하여 유효숫자를 맞춤 ($1.5084 \rightarrow 1.5$).

## Question

자신의 키가 170cm 라고 애기할 때, 발생가능한 uncertainty는
* 실제 키 166cm 에서 반올림 하여 170cm 인지
* 실제 키 170.3cm 에서 반올림 하여 170cm 인지
* 실제 키 174cm 에서 반올림 하여 170cm 인지

라고 할 수 있음.

이 같은 경우, scientific notation으로 다음과 같이 표현하면 위의 uncertainty가 줄어들게 됨.

$$
1.700 \times 10^2 \text{cm}
$$

이경우, 170까지는 정말 확실하지만 마지막 유효숫자인 0.0cm는 불확실성을 포함하고 있다. 즉 170cm의 눈금위에 거의 일치하게 측정된 경우임을 의미함.
* $1.700 \times 10^2 \text{cm}$ : 0.1 cm 의 정확도
* $1.70 \times 10^2 \text{cm}$ : 1cm 의 정확도

> 참고 : 
>  
>  측정 도구의 눈금이 0.5 mm 간격이라면 $1.70 \times 10^2 \text{cm}$ 표현이 보다 적합하다. 







