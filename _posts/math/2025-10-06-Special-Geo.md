---
layout: post 
title: 一个很有意思的特殊角问题（一题多解）
tags: math,education,geometry
category: math
---

### 1

*很有意思的特殊角问题*

[Source](https://www.bilibili.com/video/BV1Uhx7zLEfS/?spm_id_from=333.1365.list.card_archive.click&vd_source=2c3b1cf87d67c244536d57d4d5b68285)

给定三角形$\triangle ABC$，$\angle B = 60^\circ$。其中$D$在$AB$上，满足$CA = CD$。点$E$在$BC$上，满足$\angle EDC = 30^\circ$。

求证：$AE = CE$

![](https://crsando.github.io/images/2025-10-06/H-002.png)

***Solution***

这图首先分析题目的条件，这里算一遍角显然是算不出东西的，核心肯定是利用$60^\circ$和$30^\circ$这两个特殊角。

$\angle B = 60^\circ$怎么用还是比较清楚的，从$AC = CD$来看，本质是一个对称性（如果我们把$AD$的中点$M$找到的话，更是如此），所以自然的想法是把$B$也对称过去到$P$，然后就会发现这实际上就是补完一个等边三角形$\triangle PBC$。（注意，这里隐含了$AB < AC$）

所以实际上我们可以这么考虑，从画图的角度，本质应该是先画$\triangle PBC$，然后找$D$，再找$E$。然后$A$其实是根据$D$对称出来的。

![](https://crsando.github.io/images/2025-10-06/H-002-Ans.png)

这里其实$60^\circ$用的差不多了，关键是$30^\circ$怎么用。

一开始想四点公园，垂直，构造特殊三角形，其实试了一下都不太行。

然后就会发现其实反过来考虑$E$的轨迹更自然，如果$D$再$PB$的中点$M$时，$E$再$BC$的中点。如果$D$一路移动到$B$，那么同时$E$也往那个方向移动。

所以这里会想到：$\angle EDC$太难用了，那么反过来，如果我们画图的时候先画$E$，再画$D$，会不会好一点？那么此时，$D$是一个定角，所以找圆，所以自然想圆心在哪里，想到这点就会发现圆心角$\angle EOC = 60^\circ$，所以本质上$\triangle EOC$是一个正三角形，然后就会发现：实际从我们从$E$点出发作一条平行于$PB$的直线，于$PC$的交点就是圆顶$O$。

然后这里就会发现：$O$和$E$实际上也是对称的，和$D,A$一样有相同的对称轴$CM$。

剩下就很显然的：因为$O$是圆心，所以$OD = OE = OC = EC$。又由于对称性，所以$OD = AE$，所以$AE = OD = OE = OC = EC$，得证。

这个证明要写严谨会比较麻烦，请读者自行尝试。（提示：大的思路是先作正三角形$EOC$，确定$O$，然后证明$OD = OE$，证明$AOED$是等腰梯形）

***Solution 2***

![](https://crsando.github.io/images/2025-10-06/H-002-Ans-2.png)

这里给另一个更偏向全等基本功，更加朴实无华（但是比较依赖基本功和解题经验）的做法。

同样的思路是考虑如何利用$30^\circ$，那么考虑构造直角三角形，我们可以构造出$\frac{1}{2} CD$。注意到如果$AE = EC$，那么$\triangle AEC$是等腰三角形，那么三线合一，故如果我们做$EF \perp AC$，那么$F$需要是中点，那么$CF = \frac{1}{2} AC$。所以这里都出现了$\frac{1}{2} AC = \frac{1}{2} CD$，所以解题从这里入手。

我们延长$DE$到$G$，使得$\angle DGC = 90^\circ$，那么$CG = \frac{1}{2} CD$。

记$\angle DCB = \alpha$，这里通过算角，可以计算出来$\angle ACE = 60^\circ - \alpha = \angle ECG$，再结合公共边$CG$，两个直角三角形全等$\triangle FCE \cong \triangle GCE$，所以$CF = CG = \frac{1}{2} CD = \frac{1}{2} AC$，所以$AF = FC$，所以$\triangle AFE \cong \triangle CFE$，所以$\triangle AEC$必然是等腰三角形，得证。

***Solution 3***

![](https://crsando.github.io/images/2025-10-06/H-002-Ans-3.png)

最后再给一种处理思路，利用翻折，把$\triangle DEC$沿着$DE$翻过去，得到等边三角形$\triangle DCX$。

所以$EC = EX$，我们只需要证明$AE = EX$，这里大胆去猜$A,X$关于$BC$对称，所以只需要证明$\triangle ABC \cong \triangle XBC$即可。

这其实非常容易，因为$CX = CD = AC$，然后同样算角度可以算出来$\angle ACB = \angle XCB = 60^\circ - \angle DCB$。再结合公共边$BC$，所以全等$\triangle ACB \cong \triangle XCB$

### 2

已知$\triangle ABC$，$BC$边上有一点$D$，满足$\angle BAD = \angle CAD = 30^\circ$，且$AB = 2$, $BC = \sqrt{6}$。求$AD$的长度。

![](https://crsando.github.io/images/2025-10-06/H-003.png)

***Solution***

这题角平分线和$30^\circ, 60^\circ$，比较自然的想法是从$B$想$AD$作垂直线，把等边三角形$\triangle ABP$补出来。

所以从画图的角度来说，其实核心是先画一个边长为$2$的正三角形，然后从$B$为圆心，以$\sqrt{6}$为半径画圆，交$AP$的延长线于$C$

![](https://crsando.github.io/images/2025-10-06/H-003-Ans.png)

那么我们自然考虑怎么确定$C$的位置，既然是这么画，那么从$B$想$AC$作垂直就比较自然的，作$BE \perp AC$于$E$，那么$BE = \sqrt{3}$，所以$BE : BC = 1 : \sqrt{2}$，这里不需要勾股定理直接看出来$\triangle BEC$是一个等腰直角三角形，$\angle C = 45^\circ$。

所以$EC = \sqrt{3}$, $AC = 1 + \sqrt{3}$。

现在为了计算$AD$，我们需要考虑$BC$上的高来构造勾股定理。

作$AF \perp BC$于$F$，那么$AF = \frac{\sqrt{6} + \sqrt{2}}{2}$，这里其实看出来$\angle BAF = 15^\circ$（实际上不需要看出来，直接用$45^\circ$计算即可）

所以$\angle BAF = \angle DAF$，故$\triangle BAF \cong \triangle DAF$，所以$AD = AB = 2$