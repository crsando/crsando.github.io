---
layout: post
title: 在Thinkpad T460s上安装Ubuntu 24.04 LTS
tags: life,network,home
---

# Thinkpad

之前在无锡的时候想玩Linux就买了一台二手的Thinkpad T460s，价格不到1500，感觉还是挺好玩的。

自己上学的时候真的玩过很多太二手Thinkpad，非常快乐：X40, X41, X41T, X220。当时很想要X301但是一直没有。后来的X1也买不起。但是最开心的应该还是买了一台X61然后换了高分屏（1400x1050），那个年代这种12寸上的这种分辨率，真的感觉完全不一样了。再加上Thinkpad一直比较方便更换键盘和内存条，上了SSD之后其实性能真的不错了。

后来毕业的时候买了一台T430s，用来很多年。现在这台电脑基本上开不了机起了，以今天的眼光来看厚度也确实比较厚，也重。但是可扩展性，已经当时蹦着原生的高分辨率屏幕，非常开心。购买的时候是找了一家买水货的店，在中关村，跑到写字楼里面，不是商铺就是直接去办公区提回来的。

这次的T460s确实是不如当年的有老Thinkpad味道（或者说IBM味）了，不过感觉还是可以的，手感很轻，键盘手感也不错，低配8G+256G，也算够用，至少比(我买的便宜的)Aliyun服务器性能高哈哈哈。

# Choice of Distribution : Ubuntu

之前为了玩装了Nitrux，但是用了一段时间感觉不是很舒服。在想重新安装一个。纠结了一下选择烂大街的Ubuntu，主要是

* 之前Nitrux默认是KDE，感觉确实很舒服但是比较繁琐（啥都能customize），看了一下似乎GNOME更简单一点。
* 这次考虑是用作quant服务器用。我的WSL和Aliyun都是用Debian的，所以还是想Debian/Ubuntu系，用apt习惯了。
* Debian的软件似乎老一点，虽然用于服务器更好。Ubuntu烂大街但是确实感觉默认界面好用一点，还是兼顾一下Desktop需求。

安装Ubuntu的时候碰到grub安装失败的问题，感觉可能是默认的UEFI/Legacy的配置有问题，在BIOS里改了一下UEFI Only，然后重新做了一下安装USB，重新安装好了。

用了一下的感觉： Ubuntu从开箱即用的角度确实不错，简单，方便，没啥要改的，默认配置足够好用。电脑性能确实还是可以的（比另外那台Macbook Pro好多了，哎），跑TradingView也不卡了，开网页响应速度也相当不错，以至于甚至都想用Linux做主力Desktop了。

# Customization

主要是改了一个：笔记本关盖不要suspend，这个搜索了一下，主要是改 `/etc/systemd/logind.conf` 里的一个配置项目即可，具体哪个一看就只。

其它没啥特别的，安装docker，安装 `build-essential`，弄 `luajit` 和 `luarocks` 

哦对，安装 `tmux` 之后就和aliyun一样，方便从电脑上随时ssh上去了。