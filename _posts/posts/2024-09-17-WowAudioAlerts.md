---
layout: post
title: 魔兽世界语音提示
tags: wow
category: posts
---

这次回归，在B站上发现出现了许多up主（vtuber为主）发布了一系列大秘境语音包，用自己录制的声音（嘛，好听的女声？）。

我研究了一下, 才发现居然可以这么玩。

其实我甚至很长时间dbm都是不开语音提示的。但是想了想这么玩确实有不少好处（可能？）。

不过这些语音包，一般配套的大秘境技能提示都比较繁琐复杂（比如一整个包含372个WA）。

我自己可以还是老一套，觉得用dbm就行了，或者直接看姓名板，很多时候并不是很需要这么WA。这些这么多的wa，很多其实就是boss用一个啥技能啊，
或者是地图上的某个小怪有个技能啊，做一个进度条的提示之类的。我觉得没必要。有些高伤害dot的提示，我更习惯看团队框架，而且打熟悉都记住了，也必要性不高。

所以想着参考这些WA的写法，自己按自己的需求弄一套，一些关键技能监控一下，做一下提示（最好是语音提示就行了）。

这里两个问题：

1. 地图上小怪读条技能（比如格瑞姆巴托的龙，读的晦暗之风，需要及时卡视野），怎么监视？
2. 语音如何来？

### 技能监视的WA写法

BOSS的监控我都用dbm了。对于地图上的小怪的重要技能，写法可以参考[这里](https://wago.io/twwdungeons)

基本思路就是监控对象是“姓名版”，找到对应的法术ID，监控读条即可。对于有内置CD（不读条的）还是需要dbm/littlewigs，这个我暂时没研究，不发表观点。

我自己写好的wa后续准备找个地方备份一下。

关于需要监控的技能，可以从这个[nga帖子](https://nga.178.com/read.php?tid=40501640)里去找.

### 语音生成：采用GPT-SoVITS

其实现在语音生成技术真的很成熟了。我大概搜了一下，选择了这个用的很多的：GPT-SoVITS

作者提供了一个在线的demo生成器，对于我的需求来说，直接用就行：[link](http://gsv.acgnai.top)

![](/images/2024-09-17/demo-1.png)

本地部署我也弄了一下，可以在本地开webui，比较繁琐吧，但最后弄ok了。中间主要是安装一个依赖包的时候报了一个涉及*nmake*的错误，研究了一下才想明白是因为我在Windows环境下编译Cython的包，需要**Visual Studio Build Tools**提供的C/C++编译器和NMAKE。

### 其它

有一个音量问题。在WoW中，WA的音效是受“主音量”控制的。所以比较建议的做法是把主音量调到100%，其它音量根据需求调整（低一点）。

### Reference

- [colab_webui.ipynb](https://colab.research.google.com/github/RVC-Boss/GPT-SoVITS/blob/main/colab_webui.ipynb#scrollTo=0NgxXg5sjv7z)
