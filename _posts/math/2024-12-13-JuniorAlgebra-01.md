---
layout: post
title: 上海高中自主招生-真题精讲（代数）
tags: math,education,algebra
category: math
---

# 1

因式分解：$6x^3 - 11x^2 + x + 4$

***Solution***

> 高次分解，先猜简单的根，这里显然$x=1$

$$
\begin{aligned}
    &6x^3 - 11x^2 + x + 4 \\
    &= 6x^3 - 6x^2 - 5x^2 + 5x - 4x + 4 \\
    &= 6x^2(x-1) - 5x(x-1) - 4(x-1) \\
    &= (6x^2 - 5x - 4)(x-1) \\
    &= (2x + 1)(3x - 4)(x-1)
\end{aligned}
$$

# 2

在实数范围内因式分解：$x^3 - 3x^2 + 2$

***Solution***

$$
\begin{aligned}
    x^3 - 3x^2 + 2 &= (x^3 - x^2) - 2(x^2 - 1) \\
    &= x^2(x-1) - 2(x+1)(x-1) \\ 
    &= (x^2 - 2x - 2)(x-1) \\
    &= (x^2 - 2x + 1 - 1)(x-1) \\
    &= ((x-1)^2 - 3)(x-1) \\
    &= (x-1 - \sqrt{3})(x-1+\sqrt{3})(x-1) \\
\end{aligned}
$$

# 2 

设 $a > b > 0$, $a^2 + b^2 = 4ab$，求 $ \frac{a+b}{a-b} $

***Solution***

由条件，配方可知 $ (a+b)^2 = 6ab $, $(a-b)^2 = 2ab$

所以

$$
    \frac{a+b}{a-b} = \frac{\sqrt{6ab}}{\sqrt{2ab}} = \sqrt{3}
$$

> 注意$a>b>0$保证了我们可以开平方

# 3

若 $x^2 + x - 1 = 0$，求$x^3 + 2x^2 + 3$

***Solution***

> 整体代换的思想

$$
\begin{aligned}
    &x^3 + 2x^2 + 3 \\
    & = (x^3 + x^2)  + x^2 + 3  \\
    & = (x^2 + x)x  + x^2 + 3  \\
    & = x  + x^2 + 3  \\
    & = 1 + 3 = 4  \\
\end{aligned}
$$

> 降次的思想

将条件写为$x^2 = 1 - x$，则
$$
\begin{aligned}
    &x^3 + 2x^2 + 3 \\
    & = x(1-x) + 2(1-x) + 3 \\
    & = x - x^2 + 2-2x + 3 \\
    & = x - (1-x) + 2-2x + 3 \\
    & = -1 + 2 + 3 = 4
\end{aligned}
$$

# 4

已知

$$
    \frac{1}{4}(b-c)^2 = (a-b)(c-a)
$$

且$a \not = 0$, 求$\frac{b+c}{a}$

***Solution***

> 正常做配方就好了

原条件整理为

$$
\begin{aligned}
    &\frac{1}{4}(b-c)^2 = (a-b)(c-a) \\ 
    \implies & (b-c)^2 - 4(a-b)(c-a) = 0 \\
    \implies & (c-b)^2 - 4(a-b)(c-a) = 0 \\
    \implies & \Big((c-a) + (a-b)\Big)^2 - 4(a-b)(c-a) = 0 \\
    \implies & \Big((c-a) - (a-b)\Big)^2  = 0 \\
    \implies & (c-a) - (a-b) = 0 \\
    \implies &b+c = 2a \\
    \implies & \frac{b+c}{a}= 2
\end{aligned}
$$

# 5

已知$a,b,c$是互不相等的实数，$x$是任意实数，化简

$$
    \frac{(x-a)^2}{(a-b)(a-c)}
    + \frac{(x-b)^2}{(c-b)(a-b)}
    + \frac{(x-c)^2}{(c-a)(c-b)}
$$

***Solution***

> 先放一个普通的做法

$$
\begin{aligned}
    &\frac{(x-a)^2}{(a-b)(a-c)}
    + \frac{(x-b)^2}{(c-b)(a-b)}
    + \frac{(x-c)^2}{(c-a)(c-b)} \\
    =& \frac{-1}{(a-b)(b-c)(c-a)} \cdot \Big( 
            (x-a)^2(b-c) + 
            (x-b)^2(c-a) + 
            (x-c)^2(a-b) 
            \Big) \\
    =& \frac{-1}{(a-b)(b-c)(c-a)} \cdot \Big(  
            (b-c + c-a + a-c)x^2 + 
            - 2(ab - ac + bc - ba + ca - cb) x +
            a^2(b-c) + b^2(c-a) + c^2(a-b)
        \Big) \\
    =& \frac{-1}{(a-b)(b-c)(c-a)} \cdot \Big(  
            a^2(b-c) + b^2(c-a) + c^2(a-b)
        \Big) \\
    =& \frac{-1}{(a-b)(b-c)(c-a)} \cdot \Big(  
            a^2(b-a + a-c) + b^2(c-a) + c^2(a-b)
        \Big) \\
    =& \frac{-1}{(a-b)(b-c)(c-a)} \cdot \Big(  
            (b^2 - a^2)(a-c) + (c^2 - a^2)(a-b)
        \Big) \\
    =& \frac{-1}{(a-b)(b-c)(c-a)} \cdot \Big(  
            (b - a)(b+a)(c-a) + (c - a)(c+a)(a-b)
        \Big) \\
    =& \frac{-1}{(a-b)(b-c)(c-a)} \cdot \Big(  
            (a - b)(-b-a)(c-a) + (c - a)(c+a)(a-b)
        \Big) \\
    =& \frac{-1}{(a-b)(b-c)(c-a)} \cdot \Big(  
            (a - b)(c-b)(c-a)
        \Big) \\
    =& 1
\end{aligned}
$$

> 用求和符号，可以大幅减少运算量

注意到原式子是轮换对称的（中间$(c-b)(a-b) = (b-c)(b-a)$，要调整一下），所以

$$
\begin{aligned}
    S &= \sum \frac{(x-a)^2}{(a-b)(a-c)} \\
    &= (-1)\cdot \sum \frac{(x-a)^2(b-c)}{(a-b)(c-a)(b-c)} \\
    &= \frac{-1}{\prod(a-b)}\cdot \sum (x-a)^2(b-c) \\
    &= \frac{-1}{\prod(a-b)}\cdot \sum (x^2-2ax + a^2)(b-c) \\
    &= \frac{-1}{\prod(a-b)}\cdot 
        \Big (
            \sum x^2(b-c)
            -2 \sum a(b-c)x
            + \sum a^2(b-c)
        \Big) \\
    &= \frac{-1}{\prod(a-b)}\cdot 
        \Big (
            -2 x\sum ab + 2x \sum ca
            + \sum a^2(b-c)
        \Big ) \\
    &= \frac{-1}{\prod(a-b)}\cdot 
        \Big (
            -2 x\sum ab + 2x \sum ab
            + \sum a^2(b-c)
        \Big ) \\
    &= \frac{-1}{\prod(a-b)}\cdot 
        \Big ( \sum a^2(b-c) \Big ) \\
\end{aligned}
$$

下同

> 实际上，考试中我们不建议以上做法，建议以下做法

不妨将原式子视为关于$x$的多项式，记为$F(x)$

注意到原式子是轮换对称的，且$F(x)$的次数不超过$2$。

但另一方面，若取$x = a$，则有

$$
\begin{aligned}
    F(a) &= 0 + \frac{(a-b)^2}{(b-c)(b-a)} + \frac{(a-c)^2}{(c-a)(c-b)} \\
        &= \frac{b-a}{b-c} + \frac{a-c}{b-c} = 1
\end{aligned}
$$

由于轮换对称性，不难验证当$x=b$, $x=c$时，原式都为$1$。由于$a,b,c$不相同，
因此可以认为$G = F(X) - 1$这个方程有三个不同的根，由于$2$次方程至多有2个不同的根，因此唯一的可能性式$F(x) -1 \equiv 0$，即$F(x) \equiv 1$

# 6

已知实数 $a,b$满足$a^2 + ab + b^2 = 1$，$t = ab - a^2 - b^2$，求$t$的取值范围

***Solution***

由条件，$t = 2ab - 1$，因此本质上是要求$ab$的取值范围。

由条件，整理得

$$
    (a+b)^2 = 1 + ab \implies ab \geqslant -1
$$

当$a=1, b=-1$（或者交换以下）时等号成立。

另一方面，原条件换一种方式配方，可知：

$$
    (a-b)^2 = 1 - 3ab \implies ab \leqslant \frac{1}{3}
$$

当$a = b = \frac{1}{\sqrt{3}}$时等号成立。

综上，$ -3 \leqslant t \leqslant - \frac{1}{3}$

# 7

（一）给定$f(x) = x^3 + ax^2 + bx +c$，满足$ 0 < f(-1) = f(-2) = f(-3) \leqslant 3$，求$c$的取值范围。

（二）给定$f(x) = x^4 + ax^3 + bx^2 + cx + d$，已知$f(1) = 10$, $f(2)=20$,
$f(3) = 30$，求$f(10) + f(-6)$

***Solution***

（一）

设$f(-1) = f(-2) = f(-3) = k$，则显然$f(x) - k$有三个根$-1,-2,-3$，
易于验证（注意比较$x^3$的系数）

$$
    f(x) - k = (x+1)(x+2)(x+3)
$$

所以$c = k+6$，由条件$0 < k \leqslant 3$，可知$6 < c \leqslant 9$


（二）

考虑 $g(x) = f(x) - 10x$，
易于验证$g(x)$有三个根$x =1,2,3$，由于$g(x)$是一个
四次多项式，不妨记最后一个根为$m$，则（注意$x^4$的系数为$1$）

$$
    g(x) = (x-1)(x-2)(x-3)(x-m)
$$


所以

$$
    f(x) = (x-1)(x-2)(x-3)(x-m) + 10x
$$

不难验证，对于任意$m \in R$，如此定义的$f(x)$均满足题意要求。

带入，可知

$$
\begin{aligned}
    &f(10) + f(-6)  \\
        &= 9 \cdot 8 \cdot 7 (10 - m) + 10\cdot 10 \\
        &\quad + (-7) \cdot (-8) \cdot (-9) \cdot (-6 -m) + 10 \cdot (-6) \\
        &= 9 \cdot 8 \cdot 7 (10 - m + m + 6) + 40 = 8064
\end{aligned}
$$

# 8 

解方程

$$
    \sqrt{a - \sqrt{a+x}} = x
$$

***Solution***

> 这题看一眼不好解，然后注意到题目没有任何
> 关于$a,x$大小的限制（比如正实数）
> 再结合开根号对于非负的需求，想到可以比较以下大小

有题意，显然$ x \geqslant 0$，由于开根号的前提是非负性，所以

$$
    a - \sqrt{a+x} \geqslant 0 \implies a \geqslant 0
$$