---
layout: post
title: 研究Wi-Fi问题
tags: posts
category: posts
last_updated: 2025-10-27
---

人的思路就是这么发散。

起因是在梅梅的建议下，把为了给桌子腾位置挪开的沙发又挪回了房间的中间。

然后这样的话就发现，好像如果我再铺一个地毯，就可以从电视背后（客厅和卧室的墙上）的网线口拉一条明线，穿过沙发下面，走到我台式机这个地方来。

然后我就想到了家里的网络优化问题。

再然后，我想到还是得想办法测试一下家里的网络速率，尤其是我现在因为修修补补，家里实际上有两个信号发射器
1. 弱电箱里的主路由 + wifi6的 zte ax5400
2. 放在电视机背后的老wifi， netgear R7000，设置成ap模式

找了半天没有太好的测试方法，突然想一想，其实我更在乎的是稳定性和延迟，并不是那么在乎吞吐量。于是我想到了最普通的Ping来测试。

拿起我那台二手购入的垃圾T460（这方便啊，有网线接口，还是ThinkPad好），用几种方式测试了一下

1. 网线接R7000，ping 0.2~0.3 ms
2. 放在桌子上的台式机，连主路由，ping 10~13 ms左右，经常大波动
3. 放在桌子上的台式机，连R7000，ping 2~3 ms，稳定的时候，不稳定的时候大波动（如下图）

![](/images/2025-10-27/ping.png)

---

之前其实看过一些资料，陆陆续续的，没太仔细研究

这里还是把一些之前看到的以及今天新查的感觉比较好的资料整理一下

- [Understanding Wi-Fi - 一个非常非常详细的干货分享，纯文字](https://www.wiisfi.com/)
- [垃圾佬狂喜！2024企业级路由捡垃圾终极指南，选品、组网、调优全攻略【建议收藏】](https://www.bilibili.com/video/BV13i421a7Tj/?spm_id_from=333.337.search-card.all.click&vd_source=2c3b1cf87d67c244536d57d4d5b68285)
- [【科普实测】全屋WiFi满信号组网方案！MESH组网、AC+AP、WiFi信号放大器、电力猫、FTTR哪种方案更适合你？](https://www.youtube.com/watch?v=Hqof2IJ6QMg)
- [华为、TP、H3C AC+AP路由器实测！对比有线MESH！](https://www.youtube.com/watch?v=TdQ2BE221aM)
- [R7000 Suppor5](https://support.netgear.com/support/product/r7000#docs)
- [TxRate - measure Wi-Fi transmit speed in real-time](https://www.duckware.com/txrate/index.html)
- [WiFiAnalyzer - Android下的分析工具](https://github.com/VREMSoftwareDevelopment/WiFiAnalyzer)
- [mesh技术详解——不同品牌路由器怎么组mesh网络？路由器|无线路由器|openWRT|mesh网络](https://www.youtube.com/watch?v=zBoRFh8xTks)

--- 

目前我家里的光猫

![](/images/2025-10-27/gateway.jpg)

---

一个坑

掏出不知道啥时候老妈送的Redmi Note 13R，安装Wifi Analyzer，研究了半天，确认我一直看到的一个hidden ssid是从我的中兴5400发出来的。

搜索了一下，猜测这个可能是跟mesh有关，在路由器配置里关掉了所有mesh有关的东西，这个network消失了。