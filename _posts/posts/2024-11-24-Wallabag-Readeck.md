---
layout: post
title: Bye Omnivore, Try Wallabag, Then Readeck
tags: life,software
category: posts
---

*Omnivore* 是我用的一个web service，提供read-it-later功能

虽然用的很少，但我却发现用它来保存微信公众号的文章非常方便（微信几乎没有提供任何整理功能）

突然发现这个网站马上就要到11月底关闭了。

研究了一下alternatives，贵的当然是Readwise，但是感觉没必要，今天在家尝试安装self-hosted的
Wallabag，似乎是open-source社区比较流行的选择

安装不困难，直接docker，参考这篇即可

但是安装后我在保存文章上似乎遇到了一定的问题，而且这个app的界面实在是有够粗糙的。

换了一下，用Readeck，这个无论是安装host还是安装browser extension都简单很多，一下就成功了。

![](/images/2024-11-24/Screenshot%202024-11-24%20133150.png)

安装在我的Thinkpad T460s上，

```
host: http://192.168.5.10:8000
```

启动代码

```bash
docker run --rm \
        -p 8000:8000 \
        -v /opt/readeck:/readeck \
        --name readeck \
        -d codeberg.org/readeck/readeck:latest
```

然后在crontab里定时重启一下

![](/images/2024-11-24/Screenshot%202024-11-24%20135134.png)


* [Readeck - Codeberg.org](https://codeberg.org/readeck/readeck)