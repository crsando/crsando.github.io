---
layout: post
title: 上海高中自主招生-USAJMO-4
tags: math,education,algebra
category: math
---

# 1

化简 

$$
    \sqrt{y + 2 + 3\sqrt{2y-5}}
    - \sqrt{y - 2 + \sqrt{2y-5}}
$$

***Solution***

分别计算，左边：
$$
\begin{aligned}
    &\sqrt{y + 2 + 3\sqrt{2y-5}}  \\
    = & \frac{1}{\sqrt{2}}\sqrt{(2y -5) + 9 + 6\sqrt{2y-5}} \\
    = & \frac{1}{\sqrt{2}}\sqrt{ (\sqrt{2y-5} + 3)^2   } \\
    = & \frac{1}{\sqrt{2}}(\sqrt{2y-5} + 3)
\end{aligned}
$$

右边：

$$
\begin{aligned}
    &\sqrt{y - 2 + \sqrt{2y-5}}  \\
    = & \frac{1}{\sqrt{2}}\sqrt{(2y -5) + 1 + 2\sqrt{2y-5}} \\
    = & \frac{1}{\sqrt{2}}\sqrt{ (\sqrt{2y-5} + 1)^2   } \\
    = & \frac{1}{\sqrt{2}}(\sqrt{2y-5} + 1)
\end{aligned}
$$

两式相减，可知：

$$
    \sqrt{y + 2 + 3\sqrt{2y-5}}
    - \sqrt{y - 2 + \sqrt{2y-5}} = \sqrt{2}
$$

# 2 

已知实数$a$，$a^2x^2 + x + a = 0$有实数根，求其实数根的最大值。

***Solution***

> 这题反过来考虑就可以了

视为关于$a$的方程，则

$$
    0 \leqslant \Delta = 1 - 4x^3 \implies x \leqslant (\frac{1}{4})^{1/3}
$$

即为所求最大值

# 3

已知 $a + b + c = 3$, $a^2 + b^2 + c^2 = 3$，求 $a^{2022} + b^{2022} + c^{2022}$

***Solution***

> 这题原题是选择题，即使当场想不出来怎么做，也要回猜，显然都是$1$是一个平凡解。

由条件，构造：

$$
    S = \sum (a-1)^2  = \sum a^2 - 2 \sum a+ 3 = 0
$$

所以只能是$a = b = c = 1$，故 $a^{2022} + b^{2022} + c^{2022} = 3$

# 4

以 $x^2 - |2m-1|x + 4(m-1) = 0$的根为两直边，$5$为斜边，可构成一直角三角形，求$m$

***Solution***

设两根为$u,v$则由条件

$$
    5^2 = u^2 + v^2 = (u+v)^2 - 2uv = (2m-1)^2 - 8(m-1) \\
    \implies 25 = (2m-3)^2
$$

该方程有两个根$m = 4$或$m = -1$

由于$u,v$可构成两直边，所以$u,v > 0$，所以$4(m-1) = uv > 0$，所以$m > 1$，
因此只能取其中的整数根$m = 4$，得解。

# 5

已知实数$a,b,c$满足

$$
    (a+c)^2 + b = 4 \\
    c^2 - 4(b+c) + 20 = 0 
$$

求$a+b+c$

***Solution***

先配方，可知：

$$
    (a+c)^2 = 4-b \\
    (c-2)^2 = 4b - 16
$$

> 这里也可以直接用不等式，第一个式子知道$ 4 -b \geqslant 0$，第二个式子知道$4b - 16 \geqslant 0$，所以$4 \leqslant b \leqslant 4$，所以$b = 4$，下略

构造

$$
    S = 4(a+c)^2 + (c-2)^2 = 4(4-b) + (4b-16) = 0
$$

所以只能是$a +c = 0$, $c- 2 = 0$，代回原方程，解得$b = 4$，所以$a + b + c = 4$

# 6

已知实数$a,b$满足$a^2 + b^2 - 4a + 3 = 0$，求$a^2 + 2b^2 + 6$的最大值。

***Solution***

原条件整理为：

$$
    (a-2)^2 + b^2 = 1 \\
    \implies 1 \leqslant a \leqslant 3, \; -1 \leqslant b \leqslant 1
$$

注意到

$$
\begin{aligned}
    &a^2 + 2b^2 + 6  \\
    = & a^2 + 6 + 2(-a^2 + 4a - 3) \\
    = & - a^2 + 8a \\
    = & - (a-4)^2 + 16
\end{aligned}
$$

带入$1 \leqslant a \leqslant 3$，可知最大值$15$在$a = 3$是取得

# 7

若实数$a,b$为方程$x^2 - x + 1 = 0$的两个实数根，满足$a \not = b$，
且$a,b$均是$x^6 + p x^2 + q = 0$ 的根，求$p+q$

***Solution***

由对称性，先考虑$a$，有 $a^2 = a - 1$，以及
$$
\begin{aligned}
    0 &= a^6 + pa^2 + q   \\
    &= (a-1)^3 + p(a-1) + q \\
    &= (a-1)(a^2 - 2a + 1) + p(a-1) + q \\
    &= (a-1)(a-1 - 2a + 1) + p(a-1) + q \\
    &= (a-1)(- a) + p(a-1) + q \\
    &= -a^2 + a + p(a-1) + q \\
    &= 1 + p(a-1) + q \\
\end{aligned}
$$

由对称性，即：

$$
    p(a-1) + (q+1) = 0 \\
    p(b-1) + (q+1) = 0
$$

两式相减，可知 $ p(a-b) = 0$，由于$a \not = b$，所以$p = 0$，进而$q = -1$，
即$p + q = -1$得解。

> 这题有一个简化运算的方法：

注意到： $x^3 + 1 = (x+1)(x^2 - x + 1)$，所以$a^3 = -1$, $b^3 = -1$，带入，得

$$
    0 = a^6 + pa^2 + q = 1 + p(a-1) + q
$$

下略


# 8

求函数

$$
    f(x) = \sqrt{x^2 + 2x + 10} - \sqrt{x^2 - 6x + 10}
$$

的最大值

***Solution***

数形结合，

$$
    f(x) = \sqrt{(x+1)^2 + 3^2} - \sqrt{(x-3)^2 + 1}
$$

即$f(x)$是点$(x,0)$到两个定点$(-1,3)$和$(3, 1)$的距离差，使
这个距离差最大的点就是从$(-1,3)$到$(3,1)$的射线（$x + 2y -5 = 0$）与$x$轴的交点$(5,0)$，距离差为

$$
    f(x) = \sqrt{4^2 + 2^2} = 2\sqrt{5}
$$

# 9

已知实数$a$满足$a+b+c+d = 3$，$a^2 + 2b^2 + 3c^2 + 6d^2 = 5$，
求$a$的取值范围

***Solution***

由条件

$$
    b + c + d = 3-a \\
    2b^2 + 3c^2 + 6d^2 = 5 - a^2
$$

由Cauchy不等式

$$
    (b+c+d)^2 \leqslant (\frac{1}{2} + \frac{1}{3} + \frac{1}{6})
        (2b^2 + 3c^2 + 6d^2)  \\
$$

带入，得：

$$
    (3-a)^2 \leqslant 5-a^2 \\
    \implies (a-1)(a-2) \leqslant 0 \\
    \implies 1 \leqslant a \leqslant 2
$$

等号成立的条件即为Cauchy不等式成立的条件，构造略。

# 10

数列$a_n$满足

$$
    a_n = \sqrt[3]{n^2 + 2n + 1} + \sqrt[3]{(n+1)(n-1)}
        + \sqrt[3]{n^2 - 2n + 1}
$$

求$\sum_{i=1}^{1013} \frac{1}{a_{2i-1}}$

***Solution***

注意到

$$
    x^3 - y^3 = (x-y)(x^2 + xy + y^2)
$$

在上式中取$a = \sqrt[3]{n+1}$, $b = \sqrt[3]{n-1}$，不难验证

$$
    a_n = \frac{x^3 - y^3}{x - y} 
    = \frac{(n+1) - (n-1)}{ \sqrt[3]{n+1} - \sqrt[3]{n-1} } 
    = \frac{2}{ \sqrt[3]{n+1} - \sqrt[3]{n-1} } 
$$

所以

$$
\begin{aligned}
    \sum_{i=1}^{1013} \frac{1}{a_{2i-1}} 
        &= \sum_{i=1}^{1013} \frac{\sqrt[3]{2i-1+1} - \sqrt[3]{2i-1-1}}{2} \\
        &= \frac{1}{2}\sum_{i=1}^{1013} \Big ( \sqrt[3]{2i} - \sqrt[3]{2i-2} \Big) \\
        &= \frac{1}{2}\sum_{i=1}^{1013} \sqrt[3]{2i}
        - \frac{1}{2}\sum_{i=1}^{1013} \sqrt[3]{2i-2} \\
        &= \frac{1}{2}\sum_{i=1}^{1013} \sqrt[3]{2i}
        - \frac{1}{2}\sum_{i=0}^{1012} \sqrt[3]{2i} \\
        &= \frac{1}{2} \sqrt[3]{2026}
\end{aligned}
$$

# 11

若函数$y = 2x^2 - ax + a $与线段$OB$有交点，其中$O(0,0)$，$B(1,1)$，
求$a$的取值范围。

***Solution***

> 这题没有说交点唯一，靠图像其实容易想失误，建议纯代数法就好。

显然交点不可能是$(1,1)$（此时$y = 2 - a + a = 2 \not = 1$），因此

原条件等价于存在一个点$(x,y) = (t,t)$（其中$0 \leqslant t < 1$），
满足该点在二次函数上，即

$$
    t = 2t^2 - at + a \implies a = \frac{2t^2 - t}{t-1}
$$

注意到

$$
\begin{aligned}
    a &= \frac{2t^2 - t}{t-1} \\
    &= \frac{2t^2 - 2t + t - 1 + 1}{t-1} \\
        &= 2t + 1 + \frac{1}{t-1} \\
        &= 2(t-1) + \frac{1}{t-1} + 3 \\
        &= - \Big (2(1-t) + \frac{1}{1-t} \Big ) + 3
\end{aligned}
$$

令$u = 1-t$，则$ 0 < u \leqslant 1$，显然

$$
    2u + \frac{1}{u} \geqslant 2 \sqrt{2}
$$

等号在$u = \frac{\sqrt{2}}{2} < 1$时成立

另一方面

$$
    \lim_{u \rightarrow 0} 2u + \frac{1}{u} = \infty
$$

所以 $g(u) = 2u + \frac{1}{u}$在$0 < u \leqslant 1$的条件下可以取得
$[2\sqrt{2}, \infty)$区间内的任意值，因此

$$
    a = 3-(2u + \frac{1}{u})  \leqslant 3 - 2\sqrt{2}
$$
为所求取值范围