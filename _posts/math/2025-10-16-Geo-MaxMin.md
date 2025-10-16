---
layout: post 
title: 一个比较搞人的几何极值问题
tags: math,education,geometry
category: math
---

[Source](https://www.bilibili.com/video/BV14z54zrEjK/?spm_id_from=333.1387.upload.video_card.click&vd_source=2c3b1cf87d67c244536d57d4d5b68285)

![](https://crsando.github.io/images/2025-10-16/A-001.png)

这题比较搞心态，这里给一个更自然的分析方法，首先图中$G$这个是比较清楚的，然后这里有一个小正三角形和大正三角形，很显然考虑几何中心$O$是公共的，那么我们这里注意到一个问题，就是$\triangle DFE$是固定形状的，$\triangle DOE$也是固定形状的，所以$\triangle OEF$也是固定形状的（唯一的问题是角度不好求）

所以$OE \rightarrow OF$实际上是一个旋转相似的过程，由于$E$的轨迹实际上一条直线，所以$F$的轨迹也必然是一条直线。

这道题上述解法无非是把这条直线具象化了，但是也可以换一种思路，我们考虑一下这条轨迹上必然经过的两个点，两点确定一条直线。

当$D$到$A$重合的时候，$F$到$T$，当$D$移动到$B$时，$F$到$S$

![](https://crsando.github.io/images/2025-10-16/A-001-Ans.png)

所以这个定直线是非常好求的，求$A$到他们的距离即可。这个距离用面积法简单一点，容易计算$AO = 2$，$A$到$BT$的高为$3$，$A$到$BS$的高为$\sqrt{3}$

这里容易注意到$BT = 4\sqrt{3}$, $BS = 6$, $TS = \sqrt{48 + 36} = \sqrt{84} = 2\sqrt{21}$

所以

$$
\begin{aligned}
    & S_{STB} = \frac{1}{2} (4\sqrt{3}) \cdot 6 = 12\sqrt{3} \\
    & S_{ABT} = \frac{1}{2} (4\sqrt{3}) \cdot 3 = 6\sqrt{3} \\
    & S_{ABS} = \frac{1}{2} 6 \cdot \sqrt{3} = 3\sqrt{3} \\
    \implies & S_{AST} = S_{STB} - S_{ABT} - S_{ABS} = 3\sqrt{3} \\
\end{aligned}
$$

所以$A$到$TS$的距离为

$$
    h = \frac{6\sqrt{3}}{2\sqrt{21}} = \frac{3\sqrt{7}}{7}
$$