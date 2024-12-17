---
layout: post
title: 上海高中自主招生-USAJMO-1
tags: math,education,algebra
category: math
---

# 1

已知$ a + \frac{1}{a} = 4$，求 $ a^4 + \frac{1}{a^4} $

***Solution***

有条件，$a^2 + \frac{1}{a^2} = (a+\frac{1}{a})^2 - 2 = 14$

$$
    a^4 + \frac{1}{a^4} = (a^2 + \frac{1}{a^2})^2 - 2 = 194
$$

# 2

已知$x^2 + mx + 8 = 0$和$x^2 + 4x + 2m = 0$有公共实根$t$，求$t$的值。

***Solution***

由条件，$t$满足

$$
    (t^2 + mt + 8) - (t^2 + 4t + 2m) = 0 \\
    \implies (m-4)t = 2(m-4)
$$

若$m = 4$，显然原方程无实数解，故$t = 2$

# 3

已知$\sqrt{x - 2\sqrt{x-1}}$和$\sqrt{y - 4\sqrt{y-4}}$互为相反数，求$\sqrt{x/y}$

***Solution***

由条件，由于两个数均为非负数，互为相反数则必然都是$0$，可知

$$
    x - 2 \sqrt{x-1} = y - 4\sqrt{y-4} = 0
$$

且由条件，显然$x,y > 0$，解得$x = 2$, $y = 8$

# 4

若$F(x)$是关于$x$的五次多项式，满足

$$
    F(-2) = F(-1) = F(0) = F(1) = 0 \\
    F(2) = 24 \\ 
    F(3) = 360
$$

取

$$
    u(x) = (x+2)(x+1)x(x-1) \\
    v(x) = (x+2)(x+1)x(x-1)(x-2)
$$

则对$x \in \{-2,-1,0,1\}$时，均有$u(x) = v(x)= 0$

而$u(2) = 24$，$v(2) = 0$

另外，$u(3) = v(3) = 5 \cdot 4 \cdot 3 \cdot 2 = 120$

取

$$
    G(x) = u(x) + 2v(x)
$$

则显然对$x \in \{ -2, -,1, 0, 1, 2,3\}$，均有$F(x) = G(x)$，所以$F(x) - G(x)$是一个不超过$5$次的多项式，但有$6$个根，则其必然恒等于$0$，即$F(x) \equiv G(x)$，所以

$$
    F(4) = G(4) = u(4) + 2v(4) = 1320
$$

# 5

解方程

$$
    x^2 - \lfloor x \rfloor = 3
$$

***Solution***

> 注意$x$是可以小于$0$的，别遗漏了

由于

$$
    x^2 = 3 + \lfloor x \rfloor \leqslant 3 + x \\ 
    \implies (2x - 1)^2 \leqslant 13 \\ 
    \implies \frac{1 - \sqrt{13}}{2} \leqslant x \leqslant \frac{1 + \sqrt{13}}{2} \\
$$

取整，可知 

$$
-2 \leqslant \lfloor x \rfloor \leqslant 2
$$

分别将$\lfloor x \rfloor = -2, -1, 0, 1, 2$带入原方程并验证，可知仅有一解$x = \sqrt{5}$

> 如果不想讨论这么多，可以再多一个不等式缩放

注意到 

$$
    x^2 = 3 + \lfloor x \rfloor \geqslant 2 + x \\ 
    \implies (2x-1)^2 \geqslant 9
$$

当$x < 0$时，$2x - 1 < 0 $，所以$2x - 1 \leqslant -3 $，即$x \leqslant -2$，若$x > 0$，相应需要$x \geqslant 2$

再结合此前已证明的$-2 \leqslant \lfloor x \rfloor \leqslant 2$，可知只有$\lfloor x \rfloor = 2$，因此解得$x = \sqrt{5}$

# 6

已知非零实数$a,b$满足$ab = a-b$，求$\frac{a}{b} + \frac{b}{a} -ab$

***Solution***

$$
\begin{aligned}
    \frac{a}{b} + \frac{b}{a} -ab
        &= \frac{a^2 + b^2}{ab} - ab \\ 
        &= \frac{(a-b)^2 + 2ab}{ab} - ab \\
        &= 2 + \frac{(ab)^2}{ab} - ab \\
        &= 2 
\end{aligned}
$$

# 7

已知$x,y$为实数，求

$$
    5x^2 + 4y^2 - 8xy + 2x + 4
$$

的最小值


***Solution***

$$
\begin{aligned}
    &5x^2 + 4y^2 - 8xy + 2x + 4 \\
    =& (4x^2 + 4y^2 - 8xy) + (x^2 + 2x + 1) + 3 \\
    =& 4(x-y)^2 + (x+ 1)^2 + 3 \\
    \geqslant & 3
\end{aligned}
$$

> 如果万一同学因式分解不是很熟练，那么怎么做？通用的思路是逐步消元。从题目的结构上看，先消去$y$比较简单。

> 有微积分，特别是偏微分知识的同学，是不可能做错的

先视$x$为常数，考察$4y^2 - 8xy$，这个二次式的最小值为$4x^2$，当$y = x$时取得，所以...（下略）

# 8

*某卷子中的拓展题*

已知正整数$x,y$满足$2xy + x + y = 127$，求$x +y$

***Solution***

原方程（两边同时乘以$2$再加$1$）整理为

$$
    4xy + 2x + 2y + 1 = 255 \implies
    (2x + 1)(2y+1) = 255
$$

不妨设$x \leqslant y$，则$x+1 \leqslant y +1$，注意到
$255$仅有$5,51$两个素因子，且恰好有

$$
    255 = 5 \times 51
$$

（由于$3 \leqslant 2x + 1 \leqslant 2y + 1$），所以在$x \leqslant y$的假设下仅有唯一解$x = 2$, $y = 25$，所以$x +y = 27$

# 9

已知点$A(1,0)$，点$B(2,0)$，二次函数$y = x^2 + (a-3)x + 3$的图像与线段$AB$（不含端点）恰有一个交点，求$a$的取值范围。

***Solution***

> 这题主要是别遗漏定义中情况，就是图形与数轴相切的情形。

若判别式为$0$，此时不难验证$a = 3 + \sqrt{3}$时，图形与$x$轴相切于点$(\sqrt{3},0)$符合要求。

由二次函数图像的性质，若函数的判别式$>0$，则图形$y = f(x) = x^2 + (a-3)x + 3$与$AB$（不含端点）恰有一个交点当且仅当

$$
\begin{aligned}
    & f(1)f(2) < 0  \\
    \Leftrightarrow & (a+1)(2a+1) < 0 \\
    \Leftrightarrow & -1 < a < - \frac{1}{2}
\end{aligned}
$$

# 10

已知$a,b \in R$满足$a^2 + 1 = 3a$, $b^2 + 1 = 3b$，$a \not = b$。求$\frac{1}{a^2} + \frac{1}{b^2}$

***Solution***

由条件，$a,b$是方程$x^2 - 3x + 1$的两个不同的根，由韦达定理，可知$a+b = 3$, $ab = 1$，且显然两个根均非$0$，因此

$$
\begin{aligned}
    \frac{1}{a^2} + \frac{1}{b^2} &= \frac{a^2 + b^2}{a^2b^2} \\
    &= a^2 + b^2 \\ 
    &= (a+b)^2 - 2ab \\ 
    &= 7
\end{aligned}
$$

# 11

对于$x \in R$，求以下函数的最小值：

$$
    f(x) = \sqrt{x^2 + 4} + \sqrt{(8-x)^2 + 16}
$$

***Solution***

> 数形结合的做法比较简单

$f(x)$相当于点$(x,0)$到定点$(0,-2)$与$(8,4)$的距离之和，最小值当且仅当$(x,0)$在两个定点的连线之上（对应$x = \frac{8}{3}$），此时距离和即为两定点之间的距离即$10$。

> 这题纯代数的思路是凑个系数

先考虑$0 < x < 8$的情形，此时不妨取待定系数$\alpha > 0$，

由Cauchy不等式，可知

$$
    x^2 + 4 \geqslant \frac{ (x + 2\alpha)^2}{1 + \alpha^2} \\
    (8-x)^2 + 16 \geqslant \frac{ (8 - x + 4\alpha)^2}{1 + \alpha^2}
$$

此时

$$
\begin{aligned}
    f(x) &\geqslant \frac{1}{\sqrt{1+\alpha^2}}
        \Big (
            (x + 2\alpha) + (8-x + 4\alpha)
        \Big ) \\
    &= \frac{1}{\sqrt{1+\alpha^2}}
        \Big ( 
                8 + 6\alpha
            \Big)
\end{aligned}
$$

我们希望等号可以被取到，对应的条件为：

$$
    \frac{1}{\alpha^2} = \frac{x^2}{4} = \frac{(8-x)^2}{16}
$$

解得$x = \frac{8}{3}$, $\alpha = \frac{3}{4}$，对应最小值为

$$
    \min_{0 < x < 8} f(x) = f(\frac{8}{3}) = 10
$$

若$x \leqslant 0$，则此时

$$
    f(x)  \geqslant 2 + \sqrt{8^2 + 16} = 2 + 4\sqrt{5} > 2 + 4 \cdot 2 = 10
$$

若$x \geqslant 8$，则此时

$$
    f(x)  \geqslant \sqrt{8^2 + 4} + \sqrt{16} = 4 + \sqrt{68} > 4 + 6 = 10
$$

综上，所求最小值为$10$。

# 12

二次函数$y = x^2 + ax + b$与$x$轴交于两点的横坐标为$m,n$，满足$|m| + |n| \leqslant 1$，设$b$的最大值为$p$，最小值为$q$，求$p,q$

***Solution***

由条件

$$
    m + n = -a \\ 
    mn = b
$$

根存在性的条件为$a^2 \geqslant 4b$

$$
\begin{aligned}
    1 &\geqslant (|m| + |n|)^2   \\
    &= m^2 + n^2 + 2|mn| \\ 
    &= (m+n)^2 - 2mn + 2|mn| \\
    &= a^2 - 2b + 2|b| \\ 
    &\geqslant 4b - 2b + 2|b| \\ 
    &\geqslant 2b + 2|b| \\ 
\end{aligned}
$$

若$b > 0$，则上式简化为$4b \leqslant 1$，所以$b \leqslant \frac{1}{4}$，故$p = \frac{1}{4}$（存在性的构造略）

另一方面，若$b < 0$，则$mn < 0$，不妨设$ m > 0 > n$，

此时
$$
\begin{aligned}
    1 &\geqslant (|m| + |n|)^2 = (m-n)^2 \\
    \implies & m \leqslant n + 1
\end{aligned}
$$

此时

$$
    b = mn \geqslant (n+1)n = \frac{1}{4}(2n+1)^2 - \frac{1}{4} \geqslant - \frac{1}{4}
$$

所以$q = - \frac{1}{4}$（存在性的构造略）

> 这题可以不要讨论，这么做

$$
\begin{aligned}
    1 & \geqslant (|m|+|n|)^2 \\
    & \geqslant (|m|+|n|)^2 - (|m| - |n|)^2 \\
    & = 4 |mn|  \\
    & = 4|b|
\end{aligned}
$$

# 13

已知$x,y,z \in R$，满足

$$
\begin{aligned}
    & \frac{1}{x} + \frac{1}{y+z} = \frac{1}{2} \\
    & \frac{1}{y} + \frac{1}{z+x} = \frac{1}{3} \\
    & \frac{1}{z} + \frac{1}{x+y} = \frac{1}{4} \\
\end{aligned}
$$

求

$$
    \frac{2}{x} + \frac{3}{y} + \frac{4}{z}
$$

记$t = x + y + z$，由条件，不难发现$t \not = 0$（否则第一个式子的左边为$0$），注意到

$$
\begin{aligned}
    & \frac{1}{x} + \frac{1}{y+z} = \frac{1}{2} \\
    \implies & (x+y+z) = \frac{1}{2}(y+z)x \\
    \implies & t = \frac{1}{2}(t-x)x \\
    \implies & x + \frac{2t}{x} = t
\end{aligned}
$$

同理可得

$$
    x + \frac{2t}{x} = t \\ 
    y + \frac{3t}{y} = t \\ 
    z + \frac{4t}{z} = t \\ 
$$

以上式子相加，可知

$$
    t + (\frac{2}{x} + \frac{3}{y} + \frac{4}{z})t = 3t \\ 
    \implies \frac{2}{x} + \frac{3}{y} + \frac{4}{z} = 2
$$

# 14

若$a,b,c\in R$满足 $a + b +c = 32$，且

$$
    \frac{b+c -a}{bc} 
    + \frac{c+a - b}{ca} + \frac{a + b -c }{ab} = 
    \frac{1}{4}
$$

求问:以$\sqrt{a},\sqrt{b},\sqrt{c}$为边长，能否构成三角形?

***Solution***

> 这题主要是两个关键点：（1）齐次化进行化简；（2）构造

> 某些答案可能是说做因式分解，个人认为是不对的。即便最后结果不是直角三角形，这么构造$F$也是有意义的。

> 这里主要讲一下怎么计算比较不容易出错，怎么尽量利用求和符号简化运算。

### 1

引理一：
$$
    (\sum ab)(\sum a) = 3abc + \sum (a^2b + ab^2)
$$

这是因为：

$$
\begin{aligned}
    (\sum ab)(\sum a) 
        &= \sum \Big ( ab(\sum a) \Big ) \\
        &= \sum \Big ( ab (a+b) + abc \Big ) \\
        & = 3abc + \sum (a^2b + ab^2)
\end{aligned}
$$

### 2

引理二：
$$
    (\sum a ) (\sum a^2) = \sum a^3 + \sum (a^2b + ab^2)
$$

过程略

### 3
原条件整理为：

$$
    abc = 4(2\sum ab - \sum a^2)
$$

利用$a+b+c = 32$，齐次化后利用引理一和引理二：

$$
\begin{aligned}
    8abc &= (a+b+c)(2\sum ab - \sum a^2) \\
    &= 2(\sum a )(\sum ab) - (\sum a)(\sum a^2) \\
    &= 2\Big( 3abc + \sum(a^2b + ab^2) \Big) - \Big( \sum a^3 + \sum(a^2b + ab^2) \Big)
\end{aligned}
$$

即：
$$
    \sum a^3 + 2abc = \sum (a^2 b + a b^2)
$$

### 4

构造

$$
\begin{aligned}
    F &= \prod (b+c-a)    \\
        &= \prod( \sum a - 2a) \\
        &= (\sum a)^3 - (\sum 2a)(\sum a)^2  \\
        &\quad + (\sum 4ab)(\sum a) + 8abc \\
        &= - (\sum a)^3 + 4(\sum ab)(\sum a) - 8abc
\end{aligned}
$$


不难发现：

$$
    (\sum a)^3 = \sum a^3 + 3\sum(a^2b + ab^2) + 6abc
$$

并且利用引理一，可知

$$
\begin{aligned}
    F &= \prod (b+c-a)    \\
        &= - \sum a^3 + \sum(a^2b + ab^2) - 2abc
\end{aligned}
$$

带入条件，得$F = 0$，即

$$
    (b+c-a)(c+a-b)(a+b-c) = 0
$$

因此$\sqrt{a},\sqrt{b},\sqrt{c}$作为三条边可以构成直角三角形。

# 15

实数$x \not = y$满足

$$
    x^2 + \sqrt{3} y = 5 \\
    y^2 + \sqrt{3} x = 5 
$$

求

$$
    \frac{x}{y} + \frac{y}{x}
$$

***Solution***

原条件两式相减，可知

$$
    (x-y)(x+y - \sqrt{3}) = 0
$$

因为$x \not = y$，可知$x + y = \sqrt{3}$，代回原条件，可知

$$
    5 = x^2 + \sqrt{3}y = x^2 + (x+y)y = (x +y )^2 - xy
    \implies xy = -2
$$

综上：

$$
    \frac{x}{y} + \frac{y}{x} = \frac{x^2 + y^2}{xy}
    = \frac{(x+y)^2 - 2xy}{xy} = - \frac{7}{2}
$$

# 16

已知$x^2 - 3x - 2 = 0$，求

$$
    \frac{ (x-1)^3 - x^2 + 1 }{x-1}
$$

***Solution***

由条件，可知$(x-1)^2 = x + 3$

$$
\begin{aligned}
    &\frac{ (x-1)^3 - x^2 + 1 }{x-1} \\
    = &\frac{ (x-1)(x-1)^2 - x^2 + 1 }{x-1} \\
    = &\frac{ (x-1)(x+3) - x^2 + 1 }{x-1} \\
    = &\frac{ x^2 + 2x - 3 - x^2 + 1 }{x-1} \\
    = &\frac{ 2x - 2 }{x-1} \\
    = & 2
\end{aligned}
$$

# 17


关于$x,y$的方程:

$$
    x^2 - (\sqrt{2022}+1)x + \sqrt{2022}y - 12 = 0
$$

有整数解。求$y$的可能的值。

***Solution***

原方程整理为

$$
    x^2 - x - 12 = \sqrt{2022}(x-y)
$$

若$x,y$是一组整数解，则上述等式左边为整数，因此右边也是整数，但$\sqrt{2022}$是无理数，因此只有可能是$x = y$

因此方程简化为

$$
    x^2 - x - 12 = 0 \implies (x-4)(x+3) = 0
$$

解为$x = y = 4$或$x = y = -3$

# 18

不等式

$$
    x^2 + |2x - 6| \geqslant a
$$

对一切$x \in R$均成立，求$a$的最大值。

***Solution***

记

$$
    f(x) = x^2 + |2x - 6|
$$

分情况讨论。

若$x \geqslant 3$，此时

$$
    f(x) = x^2 + 2x - 6 = (x+1)^2 - 7 \geqslant 4^2 - 7 = 9
$$

等号在$x = 3$时成立。


若$x \leqslant 3$，此时
$$
    f(x) = x^2 - 2x + 6 = (x-1)^2 + 5 \geqslant 5
$$

等号在$x = 1$时成立。

综上，$f(x) \geqslant 5$恒成立，且$f(1) = 5$。故所求的$a$的最大值即为$5$

# 19

已知：不论$k$取什么数，关于$x$的方程

$$
    \frac{2kx + a}{3} - \frac{x - bk}{6} = 1
$$

的根总是$x = 1$，求常数$a,b$

***Solution***

原方程等价于：

$$
    (4k - 1)(x-1) + (4+b)k + (2a -7) = 0
$$

由于对于任意$k$，$x=1$均为解，即

$$
    (4+b)k + (2a -7) \equiv 0
$$

故$a = \frac{7}{2}$, $b = -4$

# 20

正实数$x,y,z$满足$xy + yz + zx = 1$，且

$$
    \frac{(x^2-1)(y^2-1)}{xy} + 
    \frac{(y^2-1)(z^2-1)}{yz} + 
    \frac{(z^2-1)(x^2-1)}{zx} = 4
$$

(1) 求$\frac{1}{xy} + \frac{1}{yz} + \frac{1}{zx}$

(2) 证明 $9(x+y)(y+z)(z+x) \geqslant 8xyz(xy + yz + zx)$

***Solution***

> 个人意见：这种类型的题目，去凑因式分解其实是不太容易的；
> 更多的是应该根据题目的条件，猜测以下大概需要构造一个什么样子的形式，用求和项互相抵消进行简化。

### 1

原条件整理为

$$
\begin{aligned}
    4 &= \sum \frac{(x^2-1)(y^2-1)}{xy} \\
    &= \sum \frac{x^2y^2 - x^2 - y^2 + 1}{xy} \\
    &= \sum xy - \sum \frac{x}{y} - \sum \frac{y}{x}
        + \sum \frac{1}{xy}
\end{aligned}
$$

即

$$
    \sum \frac{x}{y} + \sum \frac{y}{x} = \sum xy + \sum \frac{1}{xy} - 4
$$

构造

$$
\begin{aligned}
    F &= (\sum xy)(\sum \frac{1}{xy}) \\
    &= \sum \Big ( \frac{1}{xy}(\sum xy) \Big ) \\
    &= \sum \Big ( 1 + \frac{1}{xy}(yz + zx) \Big )
    &= 3 + \sum \Big ( \frac{yz}{xy} + \frac{zx}{xy} \Big ) \\
    &= 3 + \sum \Big ( \frac{z}{x} + \frac{z}{y} \Big ) \\
    &= 3 + \sum \frac{z}{x} + \sum \frac{z}{y} \\
    &= 3 + \sum \frac{x}{y} + \sum \frac{y}{x} \\
\end{aligned}
$$

带入条件，可知

$$
    F = (\sum xy)(\sum \frac{1}{xy}) = \sum xy + \sum \frac{1}{xy} - 1 \\
    \implies (\sum xy - 1)(\sum \frac{1}{xy} - 1) = 0
$$

由条件$\sum xy \not = 1$，因此只能是

$$
    \sum \frac{1}{xy} = 1
$$

### 2

由前证明的结论，可知：
$$
    \sum \frac{1}{xy} = 1 \\
    \implies xyz = \sum x
$$

另一方面，由Cauchy不等式

$$
    1 = \sum \frac{1}{xy} \geqslant \frac{9}{\sum xy} \\
    \implies \sum xy \geqslant 9
$$

构造

$$
\begin{aligned}
    \Delta &= 9\prod (x+y) - 8xyz \sum xy \\
    &= 9 \prod( \sum x - z) - 8xyz\sum xy \\
    &= 9 \prod( xyz - z) - 8xyz\sum xy \\
    &= 9 xyz \prod( yz - 1) - 8xyz\sum xy \\
    &= - 9 xyz \prod( 1- yz) - 8xyz\sum xy \\
    &= - 9 xyz \Big( 1 - \sum yz + \sum xyz^2 - x^2y^2z^2 \Big) - 8xyz\sum xy \\
    &= - 9 xyz \Big( 1 - \sum yz + xyz \sum z - xyz\sum x \Big) - 8xyz\sum xy \\
    &= - 9 xyz \Big( 1 - \sum yz \Big) - 8xyz\sum xy \\
    &= xyz \Big( \sum xy - 9 \Big)  \\
    & \geqslant 0
\end{aligned}
$$

得证。

> 上面是我自己做的时候的思路。第二问，有另外一个思路进行构造

展开：

$$
\begin{aligned}
    \prod(x+y) &= (x^2 + \sum xy)(y+z) \\
        &= x^2(y+z) + (\sum xy)(\sum x) - x \sum xy \\
        &= (\sum xy)(\sum x) - xyz
\end{aligned}
$$

所以（注意到前述证明的$\sum x = xyz$，我们这里的代换是为了实现齐次化）

$$
\begin{aligned}
    \Delta &= 9\prod (x+y) - 8xyz \sum xy \\
    &= 9\Big( (\sum xy)(\sum x) - xyz \Big) - 8(\sum x) (\sum xy) \\
    &= (\sum xy)(\sum x) - 9xyz \\
    &\geqslant 3 ( \prod xy )^{1/3} \cdot 3 ( \prod x )^{1/3} - 9xyz \\
    &= 9xyz - 9xyz = 0
\end{aligned}
$$

# 21

已知$x^2 - x - 1 = 0$，求$x^3 - 2x^2 + 3$的值

***Solution***

条件化为$x^2 = x + 1$，代入

$$
\begin{aligned}
    x^3 - 2x^2 + 3 &= x(x+1) - 2x^2 + 3 \\
    &= x - x^2 + 3 \\
    &= x - (x+1) + 3 \\
    &= 2
\end{aligned}
$$

# 22

若关于$x$的方程

$$
    (x-4)(x^2 - 6x + m) = 0
$$

的三个根恰好可以组成某个直角三角形的三边长，求$m$

***Solution***

显然$x = 4$是一个根，不妨设另两个根为$u,v$，则

$$
    u + v = 6 \\ 
    uv = m
$$

由于

$$
    2(u^2 + v^2) \geqslant (u+v)^2 = 36 > 2 \cdot 4^2 \\
    \implies u^2 + v^2 > 4^2
$$

由于$u,v,4$构成直角三角形的三边，结合上式，可知最长边不能为$4$，由于$u,v$的对称性，不妨设最长边为$u$，即

$$
    u^2 = v^2 + 4^2 \implies (u-v)(u+v) = 16 \\
    \implies u-v = \frac{8}{3}
$$

解得

$$
    u = 3 + \frac{4}{3} \\
    v = 3 - \frac{4}{3}
$$

所以

$$
    m = uv = 3^2 - (\frac{4}{3})^2 = ...
$$

# 23

因式分解$x^4 - 3x^2 + 9$

***Solution***

$$
\begin{aligned}
    x^4 - 3x^2 + 9 &= x^4 + 6x^2 + 9 - 9x^2 \\
        &= (x^2 + 3)^2 - (3x)^2 \\
        &= (x^2 - 3x + 3)(x^2 + 3x + 3)
\end{aligned}
$$

> 这题也可以用待定系数法，大概看一下应该没有平凡根，由于奇数项的系数为$0$，所以大概可以这么猜

$$
\begin{aligned}
    F &= (x^2 + ax + 3)(x^2 - ax + 3) \\
    &= x^4 + (6-a^2)x + 9
\end{aligned}
$$

取$a = 3$即可

# 24

关于$x$的方程

$$
    x^2 - (\sqrt{2021} +2)x + \sqrt{2021}n - 8 = 0
$$

有整数解，求整数$n$的值。

***Solution***

整理为：

$$
    x^2 - 2x - 8 = \sqrt{2021}(x -n)
$$

上式左边为整数，由于$\sqrt{2021}$为无理数，故只能是$x = n$，方程转化为$x^2 - 2x - 8 = 0$，解为$x = 4$或$x = -2$，
因此$n = 4$或$n = -2$

# 25

已知方程

$$
    (x+1)(x+21) + (x+1)(x+22) + (x+21)(x+22) = 0
$$

的两个根为$x_1, x_2$，求$(x_1+1)(x_2 + 1)$

***Solution***

原方程整理为

取$a,b,c = 1,21,22$

原方程整理为：

$$
    x^2 + 2(\sum a)x + (\sum ab) = 0
$$

所以

$$
    x_1 + x_2 = - 2 \sum a \\
    x_1 x_2 = \sum ab
$$

所以

$$
\begin{aligned}
    (x_1 + 1)(x_2 + 1) &= x_1 x_2 + (x_1 + x_2) + 1 \\
    &= \sum ab - 2 \sum a + 1 \\
    &= \sum ab - \sum (a+b) + 1 \\
    &= -2 + \sum (a-1)(b-1) \\
    &= -2 + 20 \cdot 21 = 418
\end{aligned}
$$

# 26

方程

$$
    (x - \sqrt{2021})(x^2 -kx + 1) = 0
$$

的三个根能组成三角形的三边长，求$k$的取值范围。

***Solution***

显然其中一个根为$a = \sqrt{2021}$，另两个根$b,c$满足

$$
    b + c = k \\
    bc = 1
$$

三个根能构成三角形三边长当且仅当

$$
    a+b-c > 0 \\ 
    b+c-a > 0 \\
    c+a-b > 0
$$

不妨设$b \geqslant c$，则自然$a + b -c > 0$

$$
    c + a - b > 0 \implies a > b - c
$$

同时$ k = b+c > a$

因此

$$
    4 = 4bc = (b+c)^2 - (b-c)^2 > k^2 - a^2 \\
    \implies k < \sqrt{a^2 + 4}
$$

综上，$k$的取值范围为：$\sqrt{2021} < k < \sqrt{2025}$

# 27

已知$f(x) = ax^2 + bx + c$，$f(20) = 2021$， $f(21) = 2021$，其中$a,b,c$都是整数，且$|c| < 100$，求$c$的值。

***Solution***

由条件

$$
    0 = f(21) - f(20) = 41a + b \implies b = -41a
$$

再考虑

$$
    2021 = f(20) = 400a - 820a + c \\
    \implies c = 2021 + 420a
$$

由于$ |c| < 100$，可知

$$
    -100 < c = 2021 + 420 a < 100 \\
    \implies \frac{-100 - 2021}{420} < a < \frac{100 - 2021}{420} \\
$$

结合$a$是整数，可知$a = -5$，$c = 2021 - 420 \cdot 5 = -79$

# 28

求代数式

$$
    a^2 + b^2 + ab - a - 2b
$$

的最小值

***Solution***

令

$$
    F = a^2 + b^2 + ab - a - 2b
$$

则

$$
\begin{aligned}
    4F = & 4a^2 + 4b^2 + 4ab - 4a - 8b \\
    = & 4a^2 - 4a + 4b^2 + 4(a-2)b  \\
    = & 4a^2 - 4a + (2b + a-2)^2 - (a-2)^2 \\
    = & 3a^2 - 4 + (2b + a-2)^2 \\
    \geqslant & -4
\end{aligned}
$$

因此$F \geqslant -1$，等号成立当且仅当$a = 0$, $b = 1$

# 29

求代数式

$$
    \frac{4x^2 + 3xy + 3y^2}{x^2 + xy + y^2}
$$

的最小值

***Solution***

> 这题莫名其妙的

$$
    \frac{4x^2 + 3xy + 3y^2}{x^2 + xy + y^2}
    \geqslant \frac{3x^2 + 3xy + 3y^2}{x^2 + xy + y^2} = 3
$$

等号成立当且仅当$x = 0$，$y \not = 0$

# 30

解方程

$$
    (x+1)^{1/3} + (y-1)^{1/3} = 2 \\
    x + y = 26
$$

***Solution***

令

$$
    u = (x+1)^{1/3} \\
    v = (y-1)^{1/3}
$$

则原方程整理为：

$$
    u + v = 2 \\
    u^3 + v^3 = 26
$$


考虑到

$$
    26 = u^3 + v^3 = (u+v)(u^2 - uv + v^2) \\
    \implies u^2 - uv + v^2 = 13
$$

$$
    3uv = (u+v)^2  - (u^2 - uv + v^2) = - 9 \\
    \implies uv = -3
$$

所以$u,v$是方程

$$
    x^2 -2x -3 = 0 \implies (x-3)(x+1) = 0
$$

的两个根，分情况讨论：

情形一：若$(u,v) = (3,-1)$，则$(x,y) = (26,0)$

情形一：若$(u,v) = (-1,3)$，则$(x,y) = (-2,28)$

# 31

抛物线$y = 2x^2 - px + 4p + 1$，若满足对于任意$p$，该抛物线都通过定点，
求该定点的坐标。

***Solution***

整理为：

$$
    y = 2x^2 + 1 + p(4-x)
$$

显然必然通过定点$(x,y) = (4,65)$

# 32

关于$x$的方程$ax^2 + (a+2)x + 9a = 0$有两个不相等的实数根$x_1,x_2$，满足
$x_1 < 1 < x_2$，求实数$a$的取值范围。

***Solution***

由题意，显然$x \not = 0$，则方程可整理为

$$
    f(x) = x^2 + \frac{a+2}{a}x + 9 = 0
$$

由二次函数图像的性质，两个根$x_1 < 1 < x_2$当且仅当$f(1) < 0$，即

$$
    1 + \frac{a+2}{a} + 9 < 0 \implies \frac{a+2}{a} < -10
    \implies 11a < -2 \implies a < - \frac{2}{11}
$$

即为所求取值范围

# 33

设$m$是不小于$-1$的实数, 关于$x$的方程

$$
    x^2 + 2(m-2)x + m^2 - 3m + 3 = 0
$$

由两个不相等的实数根$x_1,x_2$

(1) 若$x_1^2 + x_2^2 = 6$，求$m$

(2) 求

$$
    \frac{mx_1^2}{1 -x_1} + \frac{mx_2^2}{1-x_2}
$$

的最大值。

***Solution***


由条件

$$
    x_1 + x_2 = - 2(m-2) \\
    x_1 x_2 = m^2 - 3m + 3
$$

判别式

$$
    0 < \Delta  = 4(m-2)^2 - 4(m^2 - 3m + 3) = -4m + 4
$$

故$m < 1$


### 1

由第一问的条件：

$$
\begin{aligned}
    6 &= x_1^2 + x_2^2  \\
    &= (x_1 + x_2)^2 - 2 x_1 x_2 \\
    &= 4(m-2)^2 - 2(m^2 - 3m + 3)  \\
\end{aligned}
\\
\implies  m^2 - 5m  + 2=  0 \\
$$
由于$-1 \leqslant m < 1$，只有唯一解

$$
    m = \frac{5 - \sqrt{17}}{2}
$$

### 2


若$m \not = 0$，则（注意$m<1$，所以$m-1 \not =0$）

$$
\begin{aligned}
    S &= \frac{mx_1^2}{1 -x_1} + \frac{mx_2^2}{1-x_2} \\
    \frac{S}{m} &= \frac{x_1^2}{1-x_1} + \frac{x_2^2}{1-x_2} \\
    &= \frac{x_1^2 + x_2^2 - x_1 x_2(x_1 + x_2)}{1 - (x_1+x_2) + x_1 x_2} \\
    &= \frac{4(m-2)^2 - 2(m^2 - 3m + 3) + 2(m-2)(m^2 - 3m + 3)}{1 + 2(m -  2)  + (m^2 - 3m + 3)}  \\
    &= \frac{2m^2 - 10m + 10 + 2(m-2)(m^2 - 3m + 3)}{m^2 - m}  \\
    &= \frac{2m^3 - 8m^2 + 8m - 2}{m^2 - m}  \\
    &= \frac{(m-1)(2m^2 - 6m + 2)}{m^2 - m}  \\
    &= \frac{(2m^2 - 6m + 2)}{m}  \\
    \implies S&= 2m^2 -6m + 2
\end{aligned}
$$

故

$$
    S = 2(m-\frac{3}{2})^2 - \frac{5}{2} \quad m \not = 0 \\
    S = 0 \quad m = 0
$$

由于$ -1\leqslant m < 1$，$S$在$m < \frac{3}{2}$时单调递减，所以最大值在$m = -1$时取得，此时$S = 10$为所求最大值。

