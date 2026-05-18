---
layout: post
title: 尝试整理题目
tags: posts
category: posts
last_updated: 2026-05-06
---

看了一点本周额度可能会用不完，尝试用 ***codex*** 和 ***GPT-5.5*** 来解决这个问题

![](https://raw.githubusercontent.com/crsando/picgo/main/20260507000531710.png)

感觉效果还可以

---

大概的 ***prompt*** 如下

```
帮我设计一整套流程方案：我的目录下有一些数学讲义为markdown格式的文件，我需要把所有的题目和对应的解答提取出来。新建一个Questions目录，
  该目录下每个文件是一个题目的题干内容和所有可能的解答。涉及一个将题干提取指纹的方法，将题干转成一串标识的字符串或者数字，作为文件名使
  用。
```

然后跑出来一个 *.py* 文件，运行之后即可。

现在的结果是每个题目生成一个对应的 `<fingerprint>.md` 文件，同样的 *fingerprint* 的题目合并

接下来打算看一下怎么用AI把这些文件处理一下，进行一下分类。

---

![](https://raw.githubusercontent.com/crsando/picgo/main/20260507002659875.png)


![](https://raw.githubusercontent.com/crsando/picgo/main/20260507002954366.png)