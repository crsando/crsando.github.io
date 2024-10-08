---
layout: post
title: 整理一下如何配置家庭科学上网旁路有
tags: trading
category: posts
---

总结一下怎么在家庭网络部署软路由，实现各个设备的科学上网。


> 光猫 -> 路由器 -> 各个设备

## 0. 需要购置的东西

- 设备：推荐用R2S/R4S，直接淘宝上购买
- TF卡：买上面R2S/R4S送TF卡，或者自己买一张
- 读卡器，用于在TF卡上写入OpenWRT操作系统
- 网线

另外，需要注意：

* 主路由器最好是能支持一定的设备配置功能（详见下文），比较方便
* 建议：有一台单独的，能插网线的电脑，用于做一些安装配置。

## 1. 写入操作系统

这么说：OpenWRT是一个基于Linux的操作系统，然后由于原始的OpenWRT也只是一个系统，很多人做了基于OpenWRT预先安装好一堆软件
的打包版本，用起来比直接用OpenWRT更方便。

我选择的是 [nanopi-openwrt](https://github.com/stupidloud/nanopi-openwrt) 这个系统里已经配置好了 **Clash**， 足够我用了。

> [Download](https://github.com/stupidloud/nanopi-openwrt/tags)
默认用户名是root, 密码是password，局域网IP为192.168.2.1

1. 下载下来是一个后缀为**img.gz**的问题，这个文件不用特别处理（不用解压）
2. 用读卡器，将预先购买好的TF卡连接电脑。
3. 下载[Rufus](), 用这个软件，把下载的**img.gz**刷入到TF卡中。

## 2. 配置OpenWRT

把上面刷好系统的TF卡，插入R2S/R4S当中，接电，自动开机。

这时候，需要我们提起准备好的电脑，用网线，一头连接电脑，另一头连接R2S/R4S（接口**连LAN口**）

此时，由于R2S/R4S刷了系统，它自动开机相当于成为了一台路由器，这台路由器会自动给网线另一边的电脑分配一个IP地址、

在电脑上，打开浏览器，通过**192.168.2.1**，即可访问OpenWRT的配置界面。

接下来主要是配置两个东西：

1. 关闭dhcp
2. 启动clash，配置订阅。

这两个比较复杂，建议还是参考不良林的教学视频。

## 3. 接入家庭网络

弄完后，拔掉网线，重启（拔电）R2S/R4S，用网线，将自己家里的路由器的某一个Lan口，和R2S/R4S的WAN口，相连。

现在核心配置工作就做完了，接下来的关键是配置主路由的配置。

在主路由上，我们通过MAC地址绑定，给R2S/R4S指定一个固定IP：假设主路由为192.168.1.**1**, R2S/R4S为192.168.1.**2**。

这时候，我们通过MAC定制绑定，给家里每个设备指定一个固定IP和**网关**：

* 如果某台设备需要科学上网，就指定网关为192.168.1.**2**（即R2S/R4S）
* 如果某台设备不需要科学上网，就指定网关为192.168.1.**1**（即正常的路由器）

这样理论上就配置完了。让设备断网重连，确认网关已经更新（有些时候需要过一段时间才能更新），即可使用。