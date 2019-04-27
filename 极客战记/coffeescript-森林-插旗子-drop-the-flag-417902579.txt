---
layout: default
title: drop-the-flag
---
## 插旗子
```

# 在你想要建造陷阱的位置插旗
# 当你没有在建造陷阱的时候，收集金币！

loop
    flag = @findFlag()
    if flag
        # 我们该如何通过旗子的位置得到 flagX 和 flagY 呢？
        # （向下看如何得到物品的 x 和 y）
        flagX=flag.pos.x
        flagY=flag.pos.y
        @buildXY "fire-trap", flagX, flagY
        @pickUpFlag flag
    else
        item = @findNearestItem()
        if item
            itemPos = item.pos
            itemX = itemPos.x
            itemY = itemPos.y
            @moveXY itemX, itemY
        else
            @say "放置一个旗子让我走过去。"

```
