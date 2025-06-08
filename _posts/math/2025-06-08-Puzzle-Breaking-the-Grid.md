---
layout: post
title: Puzzle - Breaking the Grid
tags: math,education,puzzle
category: math
---

*From The Book: Mathematical Puzzles, Page 45*

# Breaking the Grid

Suppose that you are given an $n \times n$ grid of unit-length rods, jointed
at their ends. You may brace some subset $S$ of the small squares with
diagonal segments (of length 2).

Which choices of S suffice to make the grid rigid in the plane?

***Solution***

这题原解答写的非常直接（直接上来就上图论），这里我详细写一下我的思考过程。

这题的关键是想明白：什么情况下这个图是可以移动的？

![](https://crsando.github.io/images/2025-06-08/breaking.the.grid.001.png)


为了方便期间：我们称一个对角线的木棍称为一个“支撑”

先看$n = 1$的情况，此时显然如果我们一个支撑都不加，这一个正方形（四根木棍）显然是一个“压扁”的。所以$n=1$情况下必然也是一个支撑。

再看$n =2$，很自然想到，如果一行里面一个支撑都没有，那这一行可以压扁。所以每行必须至少一个支撑，每列也至少一个支撑，所以至少两个支撑。试一下放在对角线上，好像确实整个图形都动不了。

但是$n = 3$的情形一下子就复杂起来了，假设我们仿照$n =2$，保证每行每列都有一个支撑，那么自然仿照$n = 2$我们放在对角线上，那么此时图形仍然是可以压扁的。

![](https://crsando.github.io/images/2025-06-08/breaking.the.grid.002.png)