---
title:  "[SS] Ch03 Half Wave Rectifier"
last_modified_at: 2020-04-28
categories: 
 - SS 
use_math: true
tags: 
 - math
---

# [SS] Ch03 half-wave rectifier
@(Signal and System)

$$
\begin{align*}
x(t) &= A \sin (\omega_0 t) \\
\omega_0 &= \frac{2\pi}{T} \\
\\
X_m &= \frac{1}{T} \int ^{T/2}_{-T/2}x(t) e^{-jm\omega_0t}dt\\
&= \frac{1}{T} \int ^{T/2}_{0} A \sin (\omega_0 t) e^{-jm\omega_0t}dt\\
&= \frac{1}{T} \int ^{T/2}_{0} A \frac{e^{j\omega_0 t}-e^{-j\omega_0 t}}{2j}e^{-jm\omega_0t}dt\\
&= \frac{A}{2Tj} \int ^{T/2}_{0}(e^{j\omega_0 t}-e^{-j\omega_0 t})e^{-jm\omega_0t}dt \\
&= \frac{A}{2Tj} \int ^{T/2}_{0}e^{-j\omega_0 (m-1)t}-e^{-j\omega_0 (m+1)t}dt
\end{align*}
$$

$m=1$ 인 경우,

$$
\begin{align*}
X_{1} &= \frac{A}{2Tj} \int ^{T/2}_{0}e^{-j\omega_0 (1-1)t}-e^{-j\omega_0 (1+1)t}dt \\
&= \frac{A}{2Tj} \int ^{T/2}_{0}e^{-j\omega_0 0t}-e^{-j\omega_0 2t}dt\\
&= \frac{A}{2Tj} \int ^{T/2}_{0} 1-e^{-j\omega_0 2t}dt\\
&= \frac{A}{2Tj} \left[ t-\frac{e^{-j\omega_0 2t}}{-j\omega_0 2}\right]^{T/2}_{0}\\
&= \frac{A}{2Tj} \left[ \frac{T}{2}-\frac{e^{-j\frac{2\pi}{T}T}}{-j\omega_0 2} - 0 + \frac{e^0}{-j\omega_0 2}\right]\\
&= \frac{A}{2Tj} \left[ \frac{T}{2}-\frac{1}{-j\omega_0 2} - 0 + \frac{1}{-j\omega_0 2}\right]\\
&= \frac{A}{2Tj} \frac{T}{2}\\
&= \frac{A}{4j}\\
&= -j\frac{A}{4}
\end{align*} 
$$

$m=-1$ 인 경우,

$$
\begin{align*}
X_{-1} &= \frac{A}{2Tj} \int ^{T/2}_{0}e^{-j\omega_0 (-1-1)t}-e^{-j\omega_0 (1-1)t}dt \\
&= \frac{A}{2Tj} \int ^{T/2}_{0}e^{-j\omega_0 (-2)t}-e^{-j\omega_0 0t}dt\\
&= \frac{A}{2Tj} \int ^{T/2}_{0} e^{j\omega_0 2t}-1dt\\
&= \frac{A}{2Tj} \left[ \frac{e^{j\omega_0 2t}}{j\omega_0 2}-t\right]^{T/2}_{0}\\
&= \frac{A}{2Tj} \left[ \frac{1}{j\omega_0 2}-\frac{T}{2}  - \frac{1}{j\omega_0 2}+0\right]\\
&= \frac{A}{2Tj} \frac{-T}{2}\\
&= \frac{-A}{4j}\\
&= j\frac{A}{4}
\end{align*} 
$$

$m \ne \pm 1$ 인 경우,

$$
\begin{align*}
X_m &= \frac{A}{2Tj}\left\{  \left[ \frac{e^{-j\omega_0 (m-1)t}}{-j\omega_0(m-1)}\right]^{T/2}_{0}-\left[ \frac{e^{-j\omega_0 (m+1)t}}{-j\omega_0(m+1)}\right]^{T/2}_{0}\right\}\\
&= \frac{A}{2Tj}\left\{  \left[ \frac{e^{-j\frac{2\pi}{T} (m-1)t}}{-j\omega_0(m-1)}\right]^{T/2}_{0}-\left[ \frac{e^{-j\frac{2\pi}{T} (m+1)t}}{-j\omega_0(m+1)}\right]^{T/2}_{0}\right\}\\\\
&= \frac{A}{2Tj}\left\{  \left[ \frac{e^{-j\pi (m-1)}-1}{-j\omega_0(m-1)}\right]-\left[ \frac{e^{-j\pi (m+1)}-1}{-j\omega_0(m+1)}\right]\right\}\\
&= \frac{-Aj}{2T}\left\{  \left[ j\frac{e^{-j\pi (m-1)}-1}{\omega_0(m-1)}\right]-\left[j \frac{e^{-j\pi (m+1)}-1}{\omega_0(m+1)}\right]\right\}\\
&= \frac{A}{2T}\left\{  \left[ \frac{e^{-j\pi (m-1)}-1}{\omega_0(m-1)}\right]-\left[ \frac{e^{-j\pi (m+1)}-1}{\omega_0(m+1)}\right]\right\}\\
&= \frac{A}{2}\frac{\omega_0}{2\pi}\left\{  \left[ \frac{e^{-j\pi (m-1)}-1}{\omega_0(m-1)}\right]-\left[ \frac{e^{-j\pi (m+1)}-1}{\omega_0(m+1)}\right]\right\}\\
&= \frac{A}{2}\frac{1}{2\pi}\left\{  \left[ \frac{e^{-j\pi (m-1)}-1}{(m-1)}\right]-\left[ \frac{e^{-j\pi (m+1)}-1}{(m+1)}\right]\right\}\\
&= \frac{A}{2}\frac{1}{2\pi}\left\{  \left[ \frac{e^{-j\pi m}e^{j\pi}-1}{(m-1)}\right]-\left[ \frac{e^{-j\pi m}e^{-j\pi}-1}{(m+1)}\right]\right\}\\
&= \frac{A}{2}\frac{1}{2\pi}\left\{  \left[ \frac{e^{-j\pi m}(-1)-1}{(m-1)}\right]-\left[ \frac{e^{-j\pi m}(-1)-1}{(m+1)}\right]\right\}\\
&= \frac{A}{2}\frac{1}{2\pi}\left\{  \left[ \frac{-e^{-j\pi m}-1}{(m-1)}\right]-\left[ \frac{-e^{-j\pi m}-1}{(m+1)}\right]\right\}\\
&= \frac{A}{4\pi} \frac{(m+1)(-e^{-j\pi m}-1)-(m-1)(-e^{-j\pi m}-1)}{(m-1)(m+1)}\\
&= \frac{A}{4\pi} \frac{(-me^{-j\pi m}-e^{-j\pi m}-m-1)-(-me^{-j\pi m}+e^{-j\pi m}-m+1)}{m^2-1^2}\\
&= \frac{A}{4\pi} \frac{-2e^{-j\pi m}-2}{m^2-1^2}\\
&= \frac{A}{2\pi(1-m^2)}(e^{-j\pi m}+1) \\
&= \frac{A}{2\pi(1-m^2)}e^{-j\frac{\pi}{2}m}(e^{-j\frac{\pi}{2} m}+e^{j\frac{\pi}{2} m}) \\
&= \frac{A}{2\pi(1-m^2)}e^{-j\frac{\pi}{2}m}2 \cos \left(\frac{\pi}{2}m\right) \\
&= \frac{A}{\pi(1-m^2)}e^{-j\frac{\pi}{2}m} \cos \left(\frac{\pi}{2}m\right) \\$
&= \frac{A \cos \left(\frac{\pi}{2}m\right)}{\pi(1-m^2)}e^{-j\frac{\pi}{2}m}  \\
\end{align*} 
$$

## magnitude

$m=0$

$$
|X_0| = \frac{A}{\pi}
$$

$m= \text{even}$

$$
|X_\text{even}|=\frac{A }{\pi(1-m^2)}
$$

$m=\text{odd}, m \ne \pm 1$

$$
|X_\text{odd}|=0
$$

$m=\pm1$

$$
X_{\pm 1} = \frac{A}{4} 
$$

