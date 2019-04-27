---
layout: default
title: seek-and-hide
---
## 捉迷藏
```

# 收集4个发光石，用来打败食人魔斗士。
# 如果发现发光石的话，藏起来。

def checkTakeHide(item):
    if item:
        # 物品在此，拿着它。
        hero.moveXY(item.pos.x, item.pos.y)
        # 然后移动到营地中央(40, 34)
        hero.moveXY(40, 34)

while True:
    # 移动到右上的X标记。
    hero.moveXY(68, 56)
    # 在那里搜索一块发光石。
    lightstone = hero.findNearestItem()
    # 调用checkTakeHide，并使用参数：lightstone
    checkTakeHide(lightstone)
    
    # 移动到左上角的标记。
    hero.moveXY(12, 56)
    # 搜索发光石。
    lightstone = hero.findNearestItem()
    # 调用checkTakeHide，并使用参数：lightstone
    checkTakeHide(lightstone)
    # 调用checkTakeHide函数。
    # 将搜索的结果作为参数传入。

```
