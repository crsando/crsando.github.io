---
layout: post
title: 上海高中自主招生-USAJMO-1
tags: math,education,algebra
category: math
---

# 1

*2024 USAJMO Problems - Problem 5*

Find all functions $f:\mathbb{R}\rightarrow\mathbb{R}$ that satisfy

$$
    f(x^2-y)+2yf(x)=f(f(x))+f(y)
$$

for all $x,y\in\mathbb{R}$.

***Solution***

我们分步骤逐步分析

### 1

先取 $y = 0$可知

$$
    f(x^2) = f(f(x))
$$

### 2

代回，原函数方程简化为

$$
    f(x^2 - y) + 2yf(x) = f(x^2) + f(y)
$$

我们称这个方程为方程一。

### 3

取$x = y =0$，则有$f(0) = 2f(0)$，所以$f(0) = 0$，再取$x = 0$，可知

$$
    f(-y) = f(y)
$$

即$f(x)$是偶函数。

### 4

取$y = x^2$，则有

$$
    f(0) + 2 x^2 f(x) = f(x^2) + f(x^2) \\
    \implies f(x^2) = x^2f(x)
$$

### 5

显然$f(x) \equiv 0$是一个解。
我们来说明，若$f(x)$若有非$0$的零点$f(a) = 0$，则$f(x) \equiv 0$

事实上，若存在$a \not = 0$满足$f(a) = 0$，
由于$f(x)$为偶函数满足$f(x) = f(-x)$，我们不妨取$a > 0$。

注意到$f(a^2) = a^2 f(a) = 0$。

在方程一中令$x^2 = a$，则有

$$
    f(a - y) = f(y) \quad \forall y \in R
$$

再在方程一中令$y = a$，有

$$
\begin{aligned}
    & f(x^2 - a) + 2af(x) = f(x^2) + f(a) \\ 
    \implies & f(a - x^2) + 2af(x) = f(x^2) \\
    \implies & f(x^2) + 2af(x) = f(x^2) \\
    \implies & 2af(x) = 0  \\
    \implies & f(x) = 0 \quad \forall x \in R
\end{aligned}
$$

### 6

我们考察 $ f(f(f(x))) $，用两种不同的角度去拆解:

（为方便：$f^2(x) = f(x) \cdot f(x)$）

首先：
$$
\begin{aligned}
    f(f(f(x))) &= f(f(x^2)) \\
        &= f(x^4) \\
        &= x^4f(x^2) \\ 
        &= x^6 f(x)
\end{aligned}
$$

另一方面：

$$
\begin{aligned}
    f(f(f(x))) &= f(f^2(x)) \\
        &= f^2(x)f(f(x)) \\ 
        &= f^2(x)f(x^2) \\ 
        &= f^2(x) \cdot x^2 f(x) \\ 
        &= x^2 f^3(x) \\ 
\end{aligned}
$$

两式结合，可知，对一切$x \in R$，均成立

$$
    f(f(f(x))) = x^6 f(x) = x^2 (f(x))^3 \\
    \implies x^2 f(x) \Big( f(x) - x^2 \Big) \Big ( f(x) + x^2 \Big) = 0
$$