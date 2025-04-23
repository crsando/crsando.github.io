---
layout: post
title: 正方形中心连线，垂直且相等
tags: math,education,geometry
category: math
---

[Source](https://www.bilibili.com/video/BV1GKZ2YBEWp/?spm_id_from=333.337.search-card.all.click&vd_source=2c3b1cf87d67c244536d57d4d5b68285)

任意给一个凸四边形（凸应该是不需要的）$ABCD$，各条边向外做正方形，四个正方形的中心按顺序分别记为$M,N,O,P$（分别对应边$AB, BC, CD, DA$），则$MO \perp NP$且$MO = NP$

![](https://crsando.github.io/images/2025-04-23/A001.png)

***Solution***

找对角线$AC$的中点$Q$。

考虑一下旋转，很显然$AG = CF$，且$AG \perp CF$，然后利用中点的性质，很容易发现$MQ = \frac{1}{2}CF = \frac{1}{2} AG = QN$，且$MQ \perp QN$（这两个线段分别平行于$CF, AG$，而后两者垂直）。

同理，$QO =QP$且$QO \perp QP$。

然后立即可以看出来$\triangle QNP \cong QMO$，且是旋转$90^\circ$的关系，得证。

![](https://crsando.github.io/images/2025-04-23/A001-Ans.png)

***Remark***

这个问题如果出难一点，就省略正方形，直接向外做一个等腰直角三角形。