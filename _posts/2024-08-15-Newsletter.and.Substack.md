---
layout: post
title: 关于lservice与lctpc的重构
tags: trading,weekly
---

# background

最近一个月亏的人有点崩溃，不多说，努力振作起来吧！。

# Fund

在考虑和股神和伯伯一起弄一个Fund，调研了一下借壳的事情，关键还是募资吧

为了募资，在怂恿伯伯一起吧Newsletter弄起来，先继续养一批潜在客户，每周发一些投顾性质的文章，增强信任。

# Newsletter

之前在小蓝鸟上偶然看到一个substack.com的platform，感觉其实还挺适合的，针对newsletter相关的功能做的非常好。

（而且目标吗，肯定是赚国外人的钱对吧）

稍微研究了一下，发现在建立publication之后，可以用RSS Feed的方式，直接从别的地方（比如Github Pages）导入内容。

这样就实现了用Markdown写文章，然后Markdown => Github Pages => Substack的自动过程。同时借用了Github Pages的版本管理功能。

试了一下是OK的，顺便看了一下这篇（虽然实际上，默认配置已经弄好了）[https://dzhavat.github.io/2020/01/19/adding-an-rss-feed-to-github-pages.html]

# Misc.

空了要研究一下更新Jekyll的Theme

还有这篇关于Feed的研究一下：[https://gist.github.com/roachhd/f664d2cae2da899be3f6]