---
layout: post
title: 修复了一下OpenClaw和ShellCrash
tags: posts
category: posts
last_updated: 2026-03-10
---

安装OpenClaw没弄好，其实是两个问题：
- 不知道为什么连接chatgpt（我用的转发），会提示context windows不足
- 换其他模型能跑同，但是telegram回复巨慢。


这次研究了一下，加上之前openclaw的配置搞乱了，这次重头来过重新来。

```
    openclaw onboard
```

配置的时候，先配置chatgpt转发，然后手动进入`openclaw.json`中去把context windows那几行删掉就没事了。

至于telegram回复的问题，我这次直接碰到telegram无法pair，研究了一下，定位问题还是我的旁路由透明网关没有配置好。

我前阵子从OpenWrt + OpenClash换成了Armbian + ShellCrash，跑Mihomo内核，其实没太仔细研究，这次仔细看了一下，几个配置调整一下就好了

- 代理模式设置为 Tproxy（默认Mix）
- 打开域名嗅探

![](https://raw.githubusercontent.com/crsando/picgo/main/20260324131518724.png)

然后重新配置了一下订阅，我还是选择wgetcloud，这个这几年用下来稳定性最好，虽然也略贵但是没有nexi那么贵（笑）

顺带把各种都升级了一下，搞定。

开启域名嗅探前，这里connect都是各种ip，其实分流规则基本没有生效。开启后分流规则就正常了。

![](https://raw.githubusercontent.com/crsando/picgo/main/20260324132348868.png)

现在telegram里使用的效果：

![](https://raw.githubusercontent.com/crsando/picgo/main/20260324132425299.png)