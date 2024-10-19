---
layout: post
title: ThinkBook 14+ AI 2024
tags: thinking,life
category: posts
---

原本的Surface Pro 9太卡了，其实主要是内存的问题。曾经我以为16g内存对于轻度办公已经足够了。
结果Edge(chrome) + TradingView + VSCode常年拉满95%的内存使用率。

现在Windows笔记本有没有感兴趣的，Surface新款一直不出。偶然看到朋友的ThinkBook感觉不错，
而且居然有32g内存的型号。基本是最便宜的能上32g内存的全能本了。

刚巧年初看到新款即发送，等了一下，发现买不到Ultra7版本的，后来想想也无所谓吧，换了Ultra5。

这里的小故事是纠结了一下要不要买4060独显版本的，毕竟8g显存似乎可以跑跑cuda。

纠结了一下还是算了，两个理由：（1）可以Oculink上外置显卡，还是牛很多的；（2）选了32g的乞丐版比较便宜，
主要是想等Surface新款出了咬咬牙上个顶配，然后这台就可以淘汰拿去玩Linux之类的了。


# First Impression
A面质感不错。D面垃圾。厚度难受（伪装成轻薄本，实际又厚又重，1.55kg）

我还是喜欢Surface Pro 7+的模具，真的舒服。

键盘手感一般般，我用惯了Surface键盘。

触摸板很大，但是感觉手感略奇怪（滑动的触感、阻尼感）。

# Reinstall Windows 11
看了一眼预装的windows，好吧，这么多预装软件。

其实哪怕没有这些我也要重新安装。这代Windows 11的底层语言是跟着安装介质走的，安装了中文版，哪怕重新下载安装
英文语言包，很多地方（主要是设置那里）还是保持中文。所以要彻底修改语言只能重新安装（垃圾巨硬）

然后连续踩坑

先是用微软的MediaCreation，慢死。

直接微软官网下载iso文件（10min），然后Rufus。

跑楼下买了一个30元的algo优盘。

然后启动无法识别U盘。进BIOS，关了几个secure boot选项，换了一个usb口，似乎可以了，也不知道是哪里的真的影响。

安装系统，这步还顺利。

安装后启动进第一次配置，发现网络识别不出来。卡在配置流程中啥也做不了。

ThinkBook居然有Ethernet接口，插了网线，多次重启，有线也识别不出来。

网络搜索方法：Shift+F10调出cmd，然后explorer.exe调出界面，然后哪个U盘从别的机器里吧驱动下载好copy过来安装。

好在这步成功了，顺利，安装驱动重启，重新进，这次识别出来了。完成，重启，进系统。

# Customize

我习惯了从Win10留下来的配置：Windows用Dark Mode, App用Light Mode

Classic Context Menu (Right Click Menu) : 通过改注册表的方式

因为安装的是英文版本的系统，适配中文环境，要额外改一下：Administrative Langauage Settings => Language for non-Unicode programs (Chinese)

# App & Utilities

- 7-zip: Post-WinRar best choice
- Wechat / Weixin (from Microsoft Store)
- Office 365
- Visual Studio Code
- Git

# Windows Subsystem for Linux

之前Surface Pro不知道为什么升级不了WSL（无法安装Microsoft Store版本），这次换电脑总算可以了。回头试下systemd能否启用。