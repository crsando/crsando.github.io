---
layout: post
title: 倒腾了一下ShellCrash
tags: posts
category: posts
last_updated: 2026-02-18
---

一直觉得之前R4S上的OpenWrt问题好多，使用OpenClash总是订阅更新失败。

这次尝试了一下Armbian + ShellCrash（Mihomo内核）的组合，体感是换了之后速度快了。

踩了个坑：Armbian装完后没有iptables，导致国内可以访问但是外网不行，手动安装iptables，然后重新配置一下ShellCrash就好了

回头还是再找一找比较靠谱稳定的机场用在家用router上。