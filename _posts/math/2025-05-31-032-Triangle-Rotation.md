---
layout: post
title: 直角三角形与旋转的题目
tags: math,education,geometry
category: math
---

已知三角形$\triangle ADE$, $\triangle ABC$都是等腰直角三角形，且$AE, AC$分别是长边。在$EC$上选取一点$F$，使得$\triangle BDF = 45^\circ$。

求证：$\triangle BDF$是等腰直角三角形

![](https://crsando.github.io/images/2025-05-31/A-001.png)

***Solution 1***

先放我自己的证明方法

![](https://crsando.github.io/images/2025-05-31/A-001-Ans-1.png)

等腰直角三角形多，自然考虑旋转。先围绕点$D$，把$\triangle EDC$转$90^\circ$，使得$ED$旋转到$AD$，然后$EC$旋转到$AP$（即$E$到$A$，$C$到$P$），注意在这个过程中，$F$被旋转到$AP$上的一点$G$。

那么很自然的，$GD = DF$，又$\angle GDF = 90^\circ$（即旋转的角度）。利用全等，不难发现$GB = BF$

很自然的想法是，如果围绕点$B$，把$\triangle EBC$转到$PBA$，那么就得证了，所以实际上只要证明一个全等即可。这很容易，因为$AP = EC$，然后$AB = BC$，再算一下夹角$\angle PAB = \angle ECB$（利用直角，四点共圆，或者找中间角算一下即可）

那么为什么$F$被旋转到$G$内，其实就是利用一下线段的比例关系，因为$EF = PG$, $CF = AG$，所以$F$只能被旋转到$G$。

由于旋转角度也必然是$90^\circ$，所以$\angle GBF = 90^\circ$，剩下的是显然的。

***Solution 2***