---
layout: post
title: OpenCTP关于OrderRef的一个坑
tags: posts
category: posts
last_updated: 2025-01-06
---

在CTP中，插入一个新的报单（order）可以自行填写OrderRef栏位，方便区分不同的报单。

这个OrderRef是一个```char[12]```，但是一般就放一个自增的数字，我一般是放一个数字然后前面补零到12位。

但是在OpenCTP测试中，发现即便发出去的报单是```000000000020```这样的，返回时OnRtnOrder会返回一个```20```这样的值，导致前后不匹配，真的非常的坑爹呢。