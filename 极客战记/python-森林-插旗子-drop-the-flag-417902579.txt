---
layout: default
title: drop-the-flag
---
## 插旗子
```

# 在你想要建造陷阱的位置插旗
# 当你没有在建造陷阱的时候，收集金币！

while True:
    flag = hero.findFlag()
    if flag:
        # 我们该如何通过旗子的位置得到 flagX 和 flagY 呢？
        # （向下看如何得到物品的 x 和 y）
        flagX=flag.pos.x
        flagY=flag.pos.y
        hero.buildXY("fire-trap", flagX, flagY)
        hero.pickUpFlag(flag)
    else:
        item = hero.findNearestItem()
        if item:
            itemPos = item.pos
            itemX = itemPos.x
            itemY = itemPos.y
            hero.moveXY(itemX, itemY)

```
