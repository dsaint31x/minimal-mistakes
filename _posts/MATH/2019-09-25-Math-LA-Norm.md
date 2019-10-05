---
title:  "[Math] What is Norm"
last_modified_at:   2019-09-25
author: dsaint31
categories: 
  - Mathematics
use_math: true
tags: 
  - Math 
  - Linear Algebra
  - Norm
---

# norm

* vector의 length 혹은 magnitude로 불림.
* 3차원 공간에서 Euclidean Norm은 다음과 같이 정의됨.
* norm is commonly used to measure **the distance between two vectors**

$$ 
\left\| \textbf { a }  \right\| ={ \left\| \textbf { a }  \right\|  }_{ 2 }={ \left( { a }_{ 1 }^{ 2 }+{ a }_{ 2 }^{ 2 }+{ a }_{ 3 }^{ 2 } \right)  }^{ \frac { 1 }{ 2 }  } 
$$

## *P*-norm (L*P* norm)
* 일반화된 *P*-norm은 다음과 같음.

$$ 
{ \left\| \textbf { a }  \right\|  }_{ P }=\left\{ \sum _{ i=1 }^{ n }{ { \left| { a }_{ i } \right|  }^{ P } }  \right\} ^{ \frac { 1 }{ P }  }
$$

* Euclidean norm의 경우 $P$=2임.
* **norm**은 다음의 조건을 만족함.
1. $${ \left\| \textbf { a }  \right\|  }_{ P }\ge 0$$ , $$\textbf { a } =\vec{0}$$일 경우, $${ \left\| \textbf { a }  \right\|  }_{ P }=0$$.
2. $${ \left\| c \textbf{a} \right\| }_P = \left| c \right| { \left\| \textbf{a} \right\| }_{P}$$. 여기서 c는 상수. (positive homogeniety)
3. $${ \left\| \textbf { a } +\textbf { b }  \right\|  }_{ P }\le { \left\| \textbf { a }  \right\|  }_{ P }+{ \left\| \textbf { b }  \right\|  }_{ P }$$.


## RMSE and MAE

Both the **RMSE** and the **MAE** are *ways to measure **the distance between two vectors*** : the vector of predictions and the vector of target values. 

Various distance measures, or **norms**, are possible:

* l0-norm : $$\left\| \cdot \right\|_0$$
  * reqularization : spare weight 
  * NP-hard problem
* Manhattan norm (l1-norm, MAE, Lasso) : $$\left\| \cdot \right\|_1$$
  * reqularization : smaller and spare weight 
  * Relaxing L0 norm regularization, because the case of L0 norm is NP hard problem
* Euclidean norm (l2-norm, RMSE, Ridge, the root of a sum of square) : $$\left\| \cdot \right\|_2$$
  * reqularization : smaller and uniform weight 
  * Equivalent to MAP estimation with Gaussian prior 
* l*P*-norm
  * The higer the norm index (*P*), **the more it focuses on large values** and neglects small ones.
  * requlrization (~minimize problem)
    * All p-norm penalize larger weights.
    * p<2 tends to create sparse (i.e. lots of 0 weights)
    * p>=2 tends to like similar weights.
    * $$l\infty$$-norm gives the maximum absolute value in the vector.
