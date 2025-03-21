---
layout: post
title: 因式分解与方程求解
tags: math,education,algebra
category: math
---

# 1

> [Source](https://www.bilibili.com/video/BV1T44y1g7CS/?spm_id_from=333.999.0.0&vd_source=2c3b1cf87d67c244536d57d4d5b68285)


求解

$$
    4x^3 - 6x^2 + 3x - 3 = 0
$$

***Solution***

方程两边乘以$2$，并令$y = 2x$，则方程可整理为：

$$
\begin{aligned}
    &y^3 - 3y^2 + 3y - 6 = 0 \\
    \implies &(y-1)^3 = 5
\end{aligned}
$$

> 解答很简单，关键是为啥要考虑$y =2x$？
> 代数功底好，数感强，这里还是比较容易看出来的
> 另外两个思路：
> 1. 把最高次项的系数化为1，所以自然要考虑$2x$
> 2. 先求导，看函数的单调区间，然后猜到和$\frac{1}{2}$有关

$$
    f'(x) = 3(2x-1)^2
$$

所以函数单调递增，有唯一解，且局部极值在$x = \frac{1}{2}$处

实验一下，发现$f(2) > 0 > f(1)$，所以解在$1,2$中间，显然不是整数

# 2

*2005 AIME I Problems - Problem 6*

Let $P$ be the product of the nonreal roots of $x^4-4x^3+6x^2-4x=2005$ Find $\lfloor P\rfloor$

***Solution***

原方程可整理为

$$
    (x-1)^4 = 2006
$$

令 $\alpha = 2006^{1/4}$，则原方程的4个根可以表示为$1+\alpha$, $1-\alpha$, $1 + i\alpha$, $1 - i\alpha$

显然后两个根为非实数根，两个根的乘积$P = 1 + \alpha^2 = 1 + \sqrt{2006}$

不难发现$44 < \sqrt{2006} < 45$，因此$\lfloor P \rfloor = 45$

> 这题的核心是这个因式分解为$(x-1)^4$，怎么看出来的呢？
> 其实，虽然代数功底好的确实能一眼看出来，但我们提供一个更加实用的做法：利用对称性
> 因为$x^3$和$x$项的系数是一样的，补一个常数项$1$，则$x^4$和$x^0$的系数也是一样的。
> 所以如果能做因式分解，各项大概率也是对称的

可以这么分解：
$$
\begin{aligned}
    g(x) &= x^4 - 4x^3 + 6x^2 - 4x + 1 \\
        &= (x^4 - 2x^2 + 1) -4 x^3 + 8x^2 - 4x \\
        &= (x^2 - 1)^2 - 4x(x-1)^2 \\
        &= (x-1)^2(x+1)^2 - 4x(x-1)^2 \\ 
        &= (x-1)^2( (x+1)^2 - 4x ) \\ 
        &= (x-1)^4
\end{aligned}
$$

# 3 

因式分解 $x^7 + x^5 + 1$

***Solution***

> 这种就是典型的：初中范围内，但其实最好是用复数根的知识来看：
> 猜有某个单位根$x^k = 1$

大概试一下，我们猜单位根$x^3 = 1$，即猜原式子有因子$x^2 + x + 1 = 0$


下面的思路是去凑$x^3 - 1$： 

$$
\begin{aligned}
    & x^7 + x^5 + 1  \\
    = & \frac{(x^7 + x^5 + 1)(x-1)}{x-1} \\
    = & \frac{x^8 + x^6 + x - x^7 - x^5 - 1}{x-1} \\
    = & \frac{(x^8 - x^5) + (x^6 - 1) + (x - x^7)}{x-1} \\
    = & \frac{x^5(x^3 - 1) + (x^3 - 1)(x^3 + 1) - x(x^3 + 1)(x^3 - 1)}{x-1} \\
    = & \frac{x^3 - 1}{x-1}( x^5 + (x^3 + 1) - x(x^3 + 1)) \\
    = & (x^2 + x + 1)( x^5 - x^4 + x^3 - x + 1) \\
\end{aligned}
$$

# 4

求所有的整数$n$，使得 $ 2^n + 7^n $ 为完全平方数。

***Solution***

显然$n = 1$满足条件，下面说明不存在其它符合题意得整数$n$。

记分类讨论，若$n =2k$为偶数，存在正整数$x$使得

$$
\begin{aligned}
    & x^2 = 2^{2k} + 7^{2k} \\
    \implies & 7^{2k} = (x - 2^k)(x + 2^k) \\
\end{aligned}
$$

由于上式左右两边必然有因子$\gcd(x-2^k, x+2^k) = \gcd(x - 2^k, 2^{k+1})$，但该因子必然不是$7$的幂，因此唯一的可能只能是$x - 2^k = 1$

代回，有$2^{k+1} + 1 = 7^{2k}$，这是不可能的，因为对于$k > 1$的情况，有

$$
    2^{k+1} + 1  = 7^{2k} > 4^{2k} = 2^{4k} > 2^{k+2} > 2^{k+1} + 1
$$

矛盾。因此不存在偶数$n$使得$2^n + 7^n$为完全平方数。

若$n = 2k + 1$为奇数，且$k \geqslant 1$。考虑模$3$的余数，可知$2^n + 7^n \equiv -1 + 1 \equiv 0 $，因此为3的倍数，由于是完全平方数，故必然是9的倍数，因此
不妨设：

$$
\begin{aligned}
    &2^{2k+1} + 7^{2k+1} = 9x^2 \\
    \implies &2 \cdot (2^k)^2 + 7 \cdot (7^k)^2 = 9 x^2 \\
    \implies &2(x - 2^k)(x + 2^k) = 7 (7^k - x)(7^k + x) \\
\end{aligned}
$$

由于上式左边为偶数，故$x$为奇数。对于$k \geqslant 1$的情况下，左边是2的倍数但不是4的倍数，而右边必然是4的倍数，矛盾。

综上，当且仅当$n=1$时，$2^n + 7^n$为完全平方数。

# 5

以下均考虑轮换堆成，记$x_3$为方程2和方程3的公共根（$x_1,x_2$类推，下略），则显然

$$
    x_3 = - \frac{c-a}{b-c}
$$

由轮换对称，显然$\prod x_i = -1$

另一方面，注意到方程1的两个根一定是$x_1$和$x_2$，所以

$$
    F = \prod (x-x_i) = (x^2 + ax+b)(x-x_3) = x^3 + (a-x_3) + (b-ax_3) - bx_3
$$

比较两边的系数，显然有

$$
    bx_3 = \prod x_i = -1 \implies x_3 = - \frac{1}{b}
$$

所以显然 $abc = - \frac{1}{\prod x_i} = 1$

比较$x^2$的系数，有

$$
    a - x_3 = - \sum x_3 \implies a = \frac{1}{c} + \frac{1}{a}
$$

轮换对称求和，有（利用$abc = 1$）

$$
    \sum a = 2 \sum ab
$$

另一方面，由于$x_3 = - \frac{1}{b}$，所以有

$$
    - \frac{1}{b} = - \frac{c-a}{b-c} \implies 1 - \frac{c}{b} = c - a
$$

轮换求和，有

$$
    3 - \sum \frac{c}{b} = \sum (c-a) = 0 \implies \sum \frac{c}{b} = 3
$$

另一方面，比较$F$的$x$的系数，有

$$
    b + \frac{a}{b} = \sum x_i x_j = a + b + c \\
    \implies a = ba + bc \\
    \implies a^2 = ba^2 + 1 \\
    \implies a^2 = \frac{a}{c} + 1 \\
$$

同样轮换求和，得到

$$
    \sum a^2 = 3 + \sum \frac{a}{c} = 3 + \sum \frac{c}{b} = 6
$$

# 6

[Source: 广州初中数学竞赛题](https://www.bilibili.com/video/BV18QqqYWEoB/?spm_id_from=333.1007.tianma.2-1-4.click&vd_source=2c3b1cf87d67c244536d57d4d5b68285)

解方程

$$
    x^3 + (2x^3 + x - 3)^3 = 3
$$

***Solution***

> 这种降次的基本思路是消掉常数项目

令$y = 2x^3 - 3$，原方程$\times 2$之后整理可得

$$
    y + 2(x+y)^3 = 3
$$

另一方面，由$y$的定义：

$$
    y - 2x^3 = -3
$$

两式子相加，可知

$$
    2y - 2\Big((x+y)^3 - x^3) \Big ) = 0 \\
    \implies 2y\Big ( 1 + 3x^2 + 3xy + y^2\Big) = 0 \\
    \implies 2y \cdot \frac{3}{4}\Big ( \frac{1}{3} + 4x^2 + 4xy + \frac{4}{3}y^2\Big) = 0 \\
    \implies \frac{3}{2}y \Big ( \frac{1}{3} + (2x+y)^2 + \frac{1}{3}y^2\Big) = 0
$$

显然最后一式中括号内$ > 0$，因此只能是$y = 0$即$2x^3 = 3$，解得$x = \sqrt[3]{3/2}$