---
title: 博弈论八-选址模型和种族隔离
date: 2025-10-07 20:02:13
tags: 
   - "博弈论"
categories: 
   - [Study-Note, 博弈论（耶鲁大学公开课）]
---

# 混合策略

混合策略Pi，表示参与人i采用每个纯策略的概率

Pi(Si)表示在混合策略Pi下参与人采用策略Si的概率，即Pi赋予纯策略Si的概率

Pi(Si)可以是0，也可以是1（此时是纯策略）



如何计算混合策略Pi的期望收益

![](https://cdn.jsdelivr.net/gh/1935Zz/1935zz.github.io@main/source/img/game-theory/images9/image.png)

如上图，Pi的期望收益为每个纯策略的期望收益的加权平均，下面给出了一个计算混合策略P的期望收益

**结论：混合策略的预期收益一定介于所包含的纯策略的预期收益之间**

引出另一个结论

**结论：如果一个混合策略是BR，那么该混合策略包含的纯策略也都是BR，即代表每个纯策略期望收益相同**

一个混合策略集合（P1，P2,...,Pn)是一个混合策略纳什均衡，如果对每个参与者i，他的混合策略Pi是其他人的混合策略的BR

结论：如果Pi(Si)>0，那么Si也是其他人混合策略的BR



# 网球博弈

![](https://cdn.jsdelivr.net/gh/1935Zz/1935zz.github.io@main/source/img/game-theory/images9/image-1.png)

V针对S的BR是反方向击球，S针对V的BR是同方向击球，因此没有交集的最佳对策

没有纯策略NE，只有混合策略NE



![](https://cdn.jsdelivr.net/gh/1935Zz/1935zz.github.io@main/source/img/game-theory/images9/image-2.png)

![](https://cdn.jsdelivr.net/gh/1935Zz/1935zz.github.io@main/source/img/game-theory/images9/image-3.png)

* 技巧

为了找到Serena的NE混合策略(q,1-q),看Venus的纯策略的收益

因为Venus在NE中是混合策略，那么两个纯策略的收益一定一样，可以求得Serena的NE混合策略

同理可得Venus的NE混合策略

> 如果Serena不采用恰好是这个分布的混合策略，那么Venus的BR就不是混合策略而是纯策略（因为此时无法满足Venus的混合策略的两个纯策略收益相同）
>
> 比如Serena击左的概率大于0.6，那么Venus的BR就是始终击右



![](https://cdn.jsdelivr.net/gh/1935Zz/1935zz.github.io@main/source/img/game-theory/images9/image-4.png)

假设收益矩阵改变，(L,l)的收益由（50,50）变为（30,70）

影响：

1. 直接影响：Serena会采用l策略更多->q增加

2. 策略影响：Venus左击球更少了，所以Serena采用l也更少->q减少

![](https://cdn.jsdelivr.net/gh/1935Zz/1935zz.github.io@main/source/img/game-theory/images9/image-5.png)

![](https://cdn.jsdelivr.net/gh/1935Zz/1935zz.github.io@main/source/img/game-theory/images9/image-6.png)

采用类似的方法计算Serena的混合策略，算出q更小了，因此策略的影响更大

同样算出Venus的混合策略，算出p更小了，即Venus左击球更少了，验证了上面的影响

