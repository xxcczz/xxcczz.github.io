---
layout: default
title: short-sighted-burl
---
## 目光短浅的警卫
```

# 收集硬币并运行，以免burl会找到你。

# 该功能可以让你的英雄拿到物品。
def checkTakeRun(item):
    if item:
        hero.moveXY(item.pos.x, item.pos.y)
    hero.moveXY(40, 12)

#用一个参数写入函数“checkTakeRun”。
#如果该物品存在，请使用“takeItem”功能。
#移动到起始点（绿色标记）无论物品有无。


# 不要更改此代码。
while True:
    hero.moveXY(16, 56)
    coin = hero.findNearestItem()
    checkTakeRun(coin)
    hero.moveXY(64, 56)
    coin = hero.findNearestItem()
    checkTakeRun(coin)

```
