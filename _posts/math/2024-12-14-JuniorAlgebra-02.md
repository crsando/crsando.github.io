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

先取$x = y = 0$，可知 

$$
    f(0) + 0 = f(f(0)) + f(0)
    \implies f(f(0)) = 0
$$

在原方程中取 $y = 0$可知

$$
    f(x^2) = f(f(x)) + f(0)
$$

代回原方程，可知

$$
    f(x^2 -y ) +2y f(x) = f(x^2) - f(0) + f(y)
$$

取$y = x^2$，可知

$$
    f(0) + x^2 f(x) = f(x^2)
$$

用$-x$代替$x$，易于发现

$$
    f(x) = f(-x)
$$

对一切$x \in R$成立，所以$f(x)$是偶函数。

### 2

再回到原题中取$x = 0$，则有

$$
\begin{aligned}
    & f(-y) + 2yf(0) = f(f(0)) + f(y) \\
    \implies & f(y) + 2yf(0) = f(y) \\
    \implies & f(0) = 0
\end{aligned}
$$

进一步的，将$f(0) = 0$代回前面推演的结论，有

$$
    x^2 f(x) = f(x^2) = f(f(x))
$$

### 3

故原函数方程简化为

$$
    f(x^2 - y) + 2yf(x) = f(x^2) + f(y)
$$

我们称这个方程为方程一。

### 4

引理：$ f(nx) = n^2 f(x) $对一切$n \in Z$成立

由于$f(x)$为偶函数且$n = 0$的情形是显然的，只需要考虑$n > 0$的情形即可。

在方程一中取$y = -x^2$，则

$$
    f(2x^2) = f(x^2) + f(-x^2) + 2x^2f(x) = 4 f(x^2)
$$

再结合$f(x)$为偶函数，上式等价于$f(2x) = 4f(x)$

用归纳法，不难验证$f(n x) = n^2 f(x)$ 对一切$n$成立，事实上，若对$n-1$已证明成立，则我们进一步在方程一中取$y = - (n-1)x^2$，则

$$
\begin{aligned}
    f(nx^2) &= f(x^2) + f( - (n-1)x^2 ) +2 (n-1)x^2 f(x)  \\
        &= (1 + (n-1)^2 + 2n - 2) f(x^2) \\
        &= n^2 f(x^2)
\end{aligned}
$$

用$x$替换$x^2$，得证。

### 6

显然$f(x) \equiv 0$是一个解。
我们来说明，若$f(x)$若有非$0$的零点$f(a) = 0$，则$f(x) \equiv 0$

事实上，若存在$a \not = 0$满足$f(a) = 0$，
由于$f(x)$为偶函数满足$f(x) = f(-x)$，我们不妨取$a > 0$。

注意到$f(a^2) = a^2 f(a) = 0$。以及$a f(\sqrt{a}) = f(a) = 0$，所以
$f(\sqrt{a}) = 0$

在方程一中令$x = \sqrt{a}$，则有

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


### 7

我们考察 $ f(f(f(x))) $，用两种不同的角度去拆解:

（为方便，记$f^2(x) = f(x) \cdot f(x)$）

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

称上述结论为方程二。

除了$f(x) \equiv 0$这个平凡解之外，易于验证$f(x) \equiv x^2$和$f(x) \equiv -x^2$ 均是符合题意要求的解。下面证明不存在其它解.

用反证法，若存在其它符合要求的$f(x)$，则显然必然存在一个$a \not = 0$满足$f(a) \not = a^2$。由于前面已经证明的结论， 若$f(a) = 0$，由前面已经证明的结论，则此时 必然有$f(x) \equiv 0$，因此只需要讨论$f(a) = -a^2$的情况

由$f(n a) = n^2 f(a) = -(na)^2 $，且$a \not = 0$，可知满足$f(x) = -x^2$的$x \in R$有无数多个。

同理可得，必然存在无穷多个不同的$b \in R$，使得$f(b) = b^2$。

由于这样的$a,b$有无数多个，我们总能取出一组$a,b$，满足

$$
    f(a) = - a^2 \\
    f(b) = b^2 \\
    a \not = b^2 \\
    2a \not = b^2 \\
$$

带入方程一，则

$$
    f(b^2 - a) + 2af(b) = b^2 f(b) + f(a) \\
    \implies f(b^2 - a) + 2ab^2 = b^4 - a^2 \\
    \implies f(b^2 - a) = (b^2 - a)^2 - 2a^2
$$

由于$a \not = 0$，上式右边严格小于$(b^2 - a)^2$，由于$a \not = b^2$，
所以易于发现$f(b^2 - a) \not = 0$,
带入方程二，可知只能是 $f(b^2 -a) = - (b^2 -a)^2$，此时

$$
    -(b^2 -a )^2 = (b^2-a)^2 - 2a^2  \\
    \implies (b^2 -a)^2 = a^2  \\
    \implies b^2 = 0 \; \text{or} \; b^2 = 2a
$$

与假设矛盾。

综上，方程有且仅有三个解

$$
    f(x) \equiv 0 \\ 
    f(x) \equiv x^2 \\
    f(x) \equiv -x^2
$$