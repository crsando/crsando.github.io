---
layout: post
title: OpenClaw使用规划 & API 究极折磨
tags: posts
category: posts
last_updated: 2026-04-26
---

# 中转站之旅

随着对AI的用法挖掘的越来越多，包括：
- 我自己的教培方面，改讲义，OCR，转格式等等各种，用法非常丰富。
- Meimei：法律文书，搜索法律意见；生活上的减肥指南，充当心理医生等等。

对API的TOKEN需求也就越来越大了，所以急于寻找又便宜又稳定的好用API中转。

### Chateverywhere

最早（GPT）刚开始的时候的，因为用起来太麻烦加上不是那么好管理就没用了。

### Chatbox.Ai

最早我是直接从Chatbox买额度的，这个特别方便但是额度框框掉根本扛不住，有段时间我妹子几天就把我买的额度包用完了。

### app.ofox.ai

一开始在Twitter上看到的选择，实际用下来也是最稳定的一个，但是感觉还是偏贵。发现烧不起。

### dragoncode.codes

也是Twitter上看到的，这个花了最多时间测试，价格便宜而且一开始真的挺稳定的，结果。。。

![](https://raw.githubusercontent.com/crsando/picgo/main/20260501210026119.png)

### aigocode.com

这个也是Twitter上大V推荐的，看了好多排名里都有推荐这个，最近发现价格和dragoncode.codes基本一样，有一些小问题，但是GPT这块确实便宜而且还挺稳定的，决定先用他了。

后续还是继续测试继续维护。

# Clash 新增规则

哦对了：发现clash对访问还是有点影响的，手动在软路由和本地都加了额外的分流逻辑。

ShellCrash的自定义规则增加特别简单，直接找 `/etc/ShellCrash/yamls/rules.yaml`，新增即可

```yaml
- DOMAIN-SUFFIX,dragoncode.codes,DIRECT
- DOMAIN-SUFFIX,aigocode.com,DIRECT
- DOMAIN-SUFFIX,ofox.ai,DIRECT
```

# OpenClaw 实践： 结合MEMOS 进行交易/投研笔记收集

之前我主要是把openclaw-weixin当做一个语音识别的输入大模型的渠道利用，后端也是接 ***Gemini 3.1 Pro*** 用来主要做分析和搜索查找等任务。

最近研究了一下context和token的计费规则，搞明白乱用小龙虾还是有点太浪费token了：主要是如果上下文 ***context*** 设置的比较大，经常问着问着出现保量的 context size 导致模型的输入token消耗极大，一条调用就几块钱飞走了（惨！）

最近结合一些试验的结果，决定还是把日常分析放到本地的ChatBox/Alma中，每次有需要就新开一个session不会污染上下文，也节约费用。而OpenClaw这边我给他找了一个更加贴近我日常需求的流程：***交易/投研的笔记收集任务*** 。

这个任务依赖一个外部存储，我选择用 ***memos***（此 ***memos*** 非彼 ***MemOS*** ）

[Memos](https://usememos.com/)是一个在本地 ***self-hosted*** 的一个类似Twitter东西（够直白了吧！），Timeline 形式一条一条，支持标签，特别适合碎片化的收集点东西，部署可以用 *Docker* 所以特别简单。

以前我就尝试拿他来记录交易，但是发现每次打开然后自己写比较麻烦。

现在微信支持小龙虾了，本质上符合我一直希望的： ***把所有的交互尽量集中在一个入口处*** 这个设想，给了我新的希望。

给小龙虾安装 [SKILL.md for the Memos skill](https://lobehub.com/skills/openclaw-skills-memos)，简单配置就可以直接让OpenClaw给MEMOS创建/查找笔记。

最终的工作流大概是这样的

- 交易流
    1. 发送比如“买入中国核电@9.05 止损@8.5”这种内容直接给WeixinClawBot
    2. 模型识别到是“买入/卖出”性质的内容，增加一个 memos 笔记，并打上 `#trade` 标签
- 投研流
    1. 碎片化的找到任何值得搜集的资料/截图
    2. 发给 WeixinClawBot，图片自动识别内容
    3. OpenClaw根据记忆的规则，简单整理后，创建一个新的 memos 笔记，并打上 `#research` 标签

目前几经波折暂时选择用 `aigocode/gpt-5.4` 来作为后端。

### Examples & Screenshots

![](https://raw.githubusercontent.com/crsando/picgo/main/e129b73665af1124a9f9b47ecc4e2d8c.png)

![](https://raw.githubusercontent.com/crsando/picgo/main/690a0b638fba26a2ad6f008f48859482.png)

![](https://raw.githubusercontent.com/crsando/picgo/main/d5a2c265058ffebb3b69919a3f805fd0.png)

![](https://raw.githubusercontent.com/crsando/picgo/main/51105a522929137440b277309a4103c6.png)

### To be continued

后续其实还有很多可以挖掘的空间，比如如何更好的复盘，整理等等，这个慢慢磨合吧。在这个过程中也考察并使用了腾讯的 ***ima***，这个作为一个辅助记忆的工具的好处是天然云同步，我手机上也好看，缺点毕竟是私有的。我先尝试拿 ***ima*** 帮我做一些归档的笔记之类的，碎片化的先用 ***memos***，笔记这个可以支持标签还是非常方便的。

# Other to be considered

待考察的中转站：
- [APIMart](https://apimart.ai/zh): 看了一下Gemini似乎不支持原生接口，不太确定靠不靠谱，没深入试验
- [Packy](https://www.packyapi.com)：感觉推荐的人也很多，还没来得及试验