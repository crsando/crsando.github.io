---
layout: post
title: 更换主板的无线网卡
tags: life,wow
category: posts
---

现在主力台式机的电脑式还是微星Z390的ITX小板，原装的无线网卡是Intel AC9462，据说特别垃圾。

前端时间网络问题出的比较多，最近下定决心还是更换一下。

其实更换计划挺早就研究过了，由于这个主板比较老，只支持CNVio接口，实际上新的WiFi 6的无线网卡
都不支持（哪怕是同样CNVio接口的AX201，实际上只支持10代以后CPU主板，我这个9代U是不支持的）

所以其实能升级的选项只有9560

之前在网上大概看过一下拆解更换视频，感觉挺简单的，这次都没复习直接上手操作了。拆的过程中发现
似乎我这块主板的网卡也被人动过的感觉，哎毕竟是二手的主板（有一次更换主板出了问题无法点亮，然后
临时买了一块相同规格的主板更换上去了）

![](/images/2024-11-19/1.jpg)

![](/images/2024-11-19/2.jpg)

![](/images/2024-11-19/3.jpg)

没仔细测试，但是内网通过wifi向nas拷贝电影的速度从20MB/s提升到60MB/s，还是挺显著的，后面观察一下稳定性吧，
主要还是稳定性对游戏比较关键。

不过似乎同样的问题依旧发生：

![](/images/2024-11-19/Screenshot 2024-11-19 181415.png)

###

网卡更换后有一个小问题：原本的蓝牙连接都不能用了，且在windows控制面板中无法移除设备和重新连接。

解决这个问题的方法是，在Device Manager中，View -Show hidden devices，然后把所有的蓝牙设备移除，
重启电脑，让电脑自动重新安装蓝牙驱动，然后就重新连接所有的设备就行了。

```
I solved this problem by clicking the "View - Show hidden devices" in the Device Manager then manually remove all the Bluetooth devices. 

It turned out that  this is not a hardware issue, but the system picking up redundant device info from the previous motherboard. 

Problem solved, I'm all good now.
```