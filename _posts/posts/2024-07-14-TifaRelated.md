---
layout: post
title: tifa.lua的关于k线部分的修改
tags: trading,weekly
category: posts
---

之前写tifa.lua的k线聚合模块的时候感觉搞的太复杂了，尝试简化回来。

# Before

原本的考虑是针对日内场景，做了一个非常tricky的方案。

一个k线的对象其实核心就是一个`update`功能，每次一个

数据存在C部分的struct当中，然后这个struct中存在一个锚点（`t0`），实际插入数据的时候，是用数据的时间戳（`t`）
和`t0`比较，计算出对应的偏移量，大概这个意思：

```
    offset = (t - t0) / interval
    k->open[offset] = ...
```

一个交易日可以分成很多个连续的交易时间段（session），比如说早上9:00~11:00，下午13:00 ~ 15:00，那么每次时间段变化的时候，就重置
这个锚点`t0`，比如到了下午，锚点就变成了13:00，依次类推...

原本的考虑是从性能出发，这个方案后面测起来感觉还是太复杂了一点。。。

# After

新的方案改成在struct利加一个`ending`变量, 对应当前bar的理论上的结束。

比如说，最后一次插入的tick是在13:14:00，对于一个15min的bar来说，理论上结束在13:15:00。

那么我们在接下来更新一个新的tick数据的时候，如果新的时间戳超过了`ending`，那么就开启一个新的bar，否则就更新当前的（也就是数组中）最后一个bar，当然如果时间戳的范围太早了也可能被直接忽略。

然后，另外单独做一个范围的判断，判断插入tick的时间戳是否在交易时间内，也就是是否有效。

这个单独在lua里做一套，还在写，感觉涉及时间的事情真的是麻烦啊。。。

# 一个坑

这里顺便记录一个涉及timezone的坑，凡是涉及日期时间都是大坑。

在questdb里是有市区的，我目前的代码里把unix epoch插入到questdb后，因为questdb默认是按照美国的时间（似乎），所以直接select
现实出来的时间和中国时间是对不上的。

因此要显示正确，需要在questdb里头`to_timezone(timestamp, 'Asia/Shanghai')`

但是将这个转化为unix epoch的时候，却需要直接`cast(timestamp as long)`（这样出来是microseconds，记住），如果用
`cast(to_timezone(timestamp, 'Asia/Shanghai') as long)`出来的反而是和直接代码里头转化unix epoch是不对的。

只能说，怎么插入的，怎么反向回来吧。。。