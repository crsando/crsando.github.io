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

# 8

已知

$$
    a + \frac{1}{b} = 3 \\
    b + \frac{1}{c} = 17 \\
    c + \frac{1}{a} = \frac{11}{25}
$$

求$abc$

***Solution***

注意到

$$
    (a+\frac{1}{b})(b + \frac{1}{c})(c+\frac{1}{a})
    = abc + b + a + \frac{1}{c} + c + \frac{1}{a} + \frac{1}{b} + \frac{1}{abc}
$$

即

$$
    abc + \frac{1}{abc} = \prod (a+\frac{1}{b}) - \sum (a + \frac{1}{b}) = 2
$$

所以$abc = 1$

> 这题作为一个填空题，很明显不能硬算，要利用轮换对称性

> 但这题其实有一点坑，如果硬算的话，会发现解不是实数

原题可以整理为$a = 3 - \frac{1}{b} = \frac{3b - 1}{b}$，以及
$c = \frac{1}{17 - b}$，带入最后一个式子，可知

$$
    \frac{1}{17 -b} + \frac{b}{3b-1} = \frac{11}{25}
$$

展开整理，最后发现

$$
    (2b - 9)^2 + 5 = 0 
$$

# 9

对正整数$k$，函数
$$
    y = - \frac{k}{k+1} x + \frac{1}{k+1}
$$

与$x$轴，$y$轴分别交于点$A$, $B$，记$S_k$为对应的三角形$AOB$的面积
（$O$为数轴原点），求

$$
    S_1 + S_2 + \cdots + S_{2023}
$$

***Solution***

显然$A(\frac{1}{k}, 0)$，$B(0, \frac{1}{k+1})$，所以

$$
    S_k = \frac{1}{2} \cdot \frac{1}{k(k+1)}
$$

所以

$$
\begin{aligned}
    \sum_{k=1}^{2023} S_k 
        &= \frac{1}{2}\sum_{k=1}^{2023}\frac{1}{k(k+1)} \\
        &= \frac{1}{2}\sum_{k=1}^{2023} (\frac{1}{k} - \frac{1}{k+1} ) \\
        &= \frac{1}{2} ( 1 - \frac{1}{2024}) \\ 
        &= \frac{2023}{4048}
\end{aligned}
$$

# 10

求方程

$$
    x^2 + y^2 = |x| + |y|
$$

的整数解的个数

令$u = |x|$, $v = |y|$，则方程化为

$$
    u^2 + v^2 = u + v  \\
    \implies (2u-1)^2 + (2v-1)^2 = 2
$$

由于$u,v \in Z$，上式左边是两个奇数的平方和（都不能是$0$），因此只能是$(2u-1)^2 = (2v-1)^2 = 1$，再由于$u,v \geqslant 0$，因此只能是

$$
    (u,v) = (0,0),(0,1),(1,0),(1,1)
$$

换句话说，任意$(x,y) \in \{-1,0,1\}^2$的$(x,y)$均是原方程的解，且这就是全部解，因此一共有9种。

# 11

解方程

$$
    \frac{1}{x^2 + x} + \frac{1}{x^2 + 3x + 2} + \frac{1}{x^2 + 5x + 6} = \frac{3}{40}
$$

***Solution***

$$
\begin{aligned}
    \frac{3}{40} &= \frac{1}{x^2 + x} + \frac{1}{x^2 + 3x + 2} + \frac{1}{x^2 + 5x + 6}  \\
        &= \frac{1}{x(x+1)} + \frac{1}{(x+1)(x+2)} + \frac{1}{(x+2)(x+3)} \\
        &= \frac{1}{x} - \frac{1}{x+1} + \frac{1}{x+1} - \frac{1}{x+2} + \frac{1}{x+2} - \frac{1}{x+3} \\ 
        &= \frac{1}{x} - \frac{1}{x+3} \\ 
        &= \frac{3}{x(x+3)} 
\end{aligned}
$$

因此，原方程整理为

$$
    x(x+3) = 40 \implies (x-5)(x+8) = 0
$$

解为$x = 5$或者$x = -8$

# 12

已知$x,y,z \in Z$为某个三角形的三边长，且满足

$$
    xyz = 2(x-1)(y-1)(z-1)
$$

求所有符合要求的$(x,y,z)$

***Solution*** 

> 像这个题目，右边大概是$2xyz$的量级，而左边只有$xyz$，所以我们大概能猜到$x,y,z$不可能太大。所以考虑缩放。

由条件，因等式的左边显然为正整数，考虑右边，则有$x,y,z \geqslant 2$

另一方面，考虑奇偶性，可知$x,y,z$不可能全为奇数或者全为偶数。

考察$\min\{x,y,z\}$，分情况讨论

### 1

若$\min\{x,y,z\} \geqslant 4$，即$x,y,z \geqslant 4$，则

$$
    z = 2(z-1) \cdot \frac{x-1}{x} \cdot \frac{y-1}{y}
        \geqslant 2(z-1) (\frac{3}{4})^2 \\
    \implies z \leqslant 9
$$

由轮换对称性，可知只需要考虑$4 \leqslant x,y,z \leqslant 9$情形下的解。

由于$x,y,z$不可能全为奇数或者全为偶数，进一步分情况讨论。若$x,y,z$中恰好
一个奇数两个偶数，即存在整数$u,v,w$，使得$x,y,z$是$2u,2v,2w+1$的一个排列，
则方程简化为

$$
    uv(2w+1) = (2u-1)(2v-1)w \\
    2 \leqslant u,v,w \leqslant 4
$$

且不妨设$u \leqslant v$

若$u,v$中有一个为$4$（不妨设$v=4$），则右边必然是$7$的倍数，则只能是$w = 3$，此时方程化为$4 \cdot 7 u = (2u-1) \cdot 7 \cdot 3$，无整数解。

若$2 \leqslant u \leqslant v \leqslant 3$，用枚举法，易于验证有且仅有解

$$
    (u,v,w) = (2,2,3), (2,3,2)
$$

对于$(u,v,w) = (2,2,3)$的情形，此时对应的的$x,y,z$为$4,4,9$，不满足三角形两边之和大于第三边的条件，因此不是一组有效的解。

对于$(u,v,w) = (2,3,2)$，此时对应的$x,y,z$是$4,6,5$的一个排列，符合题目要求。

若$x,y,z$中有两个奇数一个偶数，则存在$u,v,w$使得$x,y,z$为$2u+1,2v+1,2w$的一个排列，原方程简化为

$$
    (2u+1)(2v+1)w = 4uv(2w-1) \\
    2 \leqslant u,v,w \leqslant 4
$$

由于右边是$4$的倍数，所以只能是$w = 4$。此时右边是$7$的倍数，所以$u,v$中必有一个为$3$，进一步的，此时右边必然是$3$的倍数，但左边不可能是$3$的倍数，无解。

### 2

若$\min\{x,y,z\} = 3$，不妨设$x \geqslant y \geqslant z = 3$，此时方程
整理为

$$
    3xy = 4(x-1)(y-1) \\
    \implies 3xy = 4xy - 4(x+y) + 4 \\
    \implies 0 = xy - 4(x+y) + 4 \\
    \implies 12 = (x-4)(y-4)
$$

结合$y + z > x$的要求，用枚举法易于验证，此时只有解$(x,y,z) = (8,7,3)$

### 3
若$\min\{x,y,z\} = 2$，不妨设$x \geqslant y \geqslant z = 2$，此时方程整理为

$$
    2xy = 2(x-1)(y-1)
$$

此方程显然没有正整数解。

### 4

综上，题意所求的三角形三边长$x,y,z$为$3,7,8$或$4,5,6$及其对应的所有排列。

> 这题做复杂了，事实上，可以用下面的方法:

不妨设$x \geqslant y \geqslant z$，则

$$
    \frac{1}{2} = \prod (1 - \frac{1}{x}) \geqslant (1 - \frac{1}{z})^3
$$

上式仅当$z \leqslant 4$才可能成立，因此只需要考虑$z=2,3,4$的情形，下略。

# 13

已知

$$
    x + y + z = 5 \\
    4x + y - 2z = 2
$$

求 $4x - 4z  + 1$

***Solution***

> 很显然，要消去$y$，所以两式减一下

两式相减，有

$$
    3x - 3z = -3 \implies x-z = -1
$$

所以 $4x - 4z + 1 = -3$

# 14

有理数$a,b,c$满足

$$
    a^2+ b^2 + 1 = 2(c^2 + ab + b-a)
$$

求$a-b-c$

***Solution***

整理如下：

$$
\begin{aligned}
    & a^2+ b^2 + 1 = 2(c^2 + ab + b-a) \\
    \implies & (a-b)^2 + 1 = 2c^2 + 2(b-a) \\
    \implies & (b-a)^2 - 2(b-a) + 1 = 2c^2 \\
    \implies & (b-a - 1)^2 = 2c^2 \\
\end{aligned}
$$

由于$a,b,c$均为有理数，只能是$c = 0$，$b-a-1=0$

因此$a-b-c = -1$，得解。

# 15

已知$a,b,c \in N$是某个三角形的三边长，满足

$$
    a^2 + b^2 + c^2 - ab - bc - ca = 13 \\ 
    a + b +c < 30 \\
    a \geqslant b \geqslant  c
$$

求这样的三角形有多少个。

***Solution***

原条件第一式整理为

$$
    (a-b)^2 + (b-c)^2 + (c-a)^2 = 26
$$

记$m = \max \{|a-b|, |b-c|, |c-a| \}$，则

$$
    3m^2 \geqslant 26 \geqslant m^2 + 1 + 1  \\
    \implies 3 \leqslant m \leqslant 4
$$

不难通过枚举法验证在$m = 3$的情况下无整数解。对于$m =4$，不难验证此时
$|a-b|,|b-c|,|c-a|$是$1,3,4$的某个排列。

在$a \geqslant b \geqslant c$条件下，只有两种可能的情形

$$
    a-b = 1, b-c = 3, a-c = 4 \\
    a-b = 3, b-c = 1, a-c = 4
$$

分情况讨论

### 1

对于
$$
    a-b = 1, b-c = 3, a-c = 4
$$

此时$30 > a + b + c = 3c + 7$，因此$c \leqslant 7$

再由于三角形三边长的条件，可知$b+c > a$，即$c > a - b = 1$, $c \geqslant 2$

则$c = 2,3,\cdots,7$每种对应一类三角形，共$6$类。

### 2

若
$$
    a-b = 3, b-c = 1, a-c = 4
$$

则$30 > a + b +c = 3c + 5$，因此$ c \leqslant 8$

再由$c > a- b = 3$，得$ c \geqslant 4$

则$c = 4,5,6,7,8$每种对应一类三角形，共$5$类。

综上，一共有$5+6 = 11$种不同的三角形符合题目要求。

# 16

求函数

$$
    f(x) = \sqrt{\frac{1}{2} - x} + \sqrt{x - \frac{1}{3}}
$$

的最大最小值

***Solution***

由函数的定义，可知$ \frac{1}{2} \geqslant x \geqslant \frac{1}{3}$

注意到
$$
    f^2(x) = \frac{1}{6} + \sqrt{ - (x-\frac{5}{12})^2 + \frac{1}{144} }
$$

上式右边的最大值在$x = \frac{5}{12}$时取得，最小值只能在$x = \frac{1}{3}$或者$x = \frac{1}{2}$时取得，下略。

# 17

已知实数$x,y,z$满足$x+y = xy$, $x+y+z = xyz$，求$z$的取值范围

***Solution***

由$x +y = xy$，显然$x \not = 1$，$y = \frac{x}{x-1}$，带入，得

$$
    \frac{x^2}{x-1} + z = \frac{x^2}{x-1}z
    \implies (z-1)x^2 + zx - z = 0
$$

有实数解的充分必要条件是

$$
    z^2 \geqslant 4z(z-1)
    \implies 0 \leqslant z \leqslant \frac{3}{4}
$$

即为所求的取值范围。

# 18

已知$a,b,c \in Z^+$，关于$x$的方程$ax^2 + bx + c = 0$的两个不同实根的
绝对值均小于$\frac{1}{3}$，求$a+b+c$的最小值。

***Solution***

由于判别式，可知（注意是两个不同的根，所以不能取等号）

$$
    b^2 > 4ac \implies b^2 \geqslant 4ac + 1 \geqslant 4a +1
$$

所以

$$
    a \leqslant \frac{b^2 -1}{4}
$$

若设两个根为$u,v$，则显然

$$
\begin{aligned}
    \frac{2}{9} &> u^2 + v^2  \\
    &= (u+v)^2 - 2uv \\
    &= \frac{b^2 - 2ac}{a^2} \\
    &> \frac{2ac}{a^2} = \frac{2c}{a}
\end{aligned}
$$

因此$a > 9c$，即$a \geqslant 9c + 1 \geqslant 10$

代回$b^2 \geqslant 4ac + 1 \geqslant 41$，可知$b \geqslant 7$

由于$a,b > 0$，可知

$$
    \frac{- b - \sqrt{b^2 - 4ac}}{2a} > - \frac{1}{3} \\
    \implies \frac{1}{3} > \frac{b + 1}{2a} \\
    \implies a > \frac{3}{2}(b+1)
$$


综上，有

$$
    \frac{3}{2}(b+1) < a \leqslant \frac{b^2 - 1}{4} \\
    c < \frac{b^2}{4a} \\
    b \geqslant 7
$$


分情况讨论：

### 1

若$ b = 7$，则 $12 < a \leqslant 12 $，显然无解

### 2

若$ b = 8$，$\frac{27}{2} <  a \leqslant 15$，所以直接是$a = 15$，进而此时只能是$c = 1$

易于验证也没有符合要求的解（最好的是刚好$\frac{1}{3}）。

### 3

若$b = 9$，此时$ 15 < a \leqslant 20$，故$ a \geqslant 16$，易于验证$a = 16,17,18$时均不满足条件，而$(a,b,c) = (19,9,1)$符合要求，所以
$a+b+c \geqslant 29$


### 4

若$b \geqslant 10$，则$a \geqslant 17$，易于验证$a = 17$不满足条件，因此$a \geqslant 18$，则$a + b + c \geqslant 10 + 18 + 1 = 29$

综上，$a+b+c$的最小值为$29$。

> 这题有一个比较简单的分类讨论方法

注意到由于$a,b,c$都是正整数，所以方程的两个根都是负数，且均在$(-\frac{1}{3},0)$区间内

由二次函数的性质，必然有$f(-\frac{1}{3}) > 0$，整理得 $a - 3b + 9c > 0$，
其它略。