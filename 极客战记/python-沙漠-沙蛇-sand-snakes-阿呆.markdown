---
layout: default
title: sand-snakes
---
## 沙蛇
```

# 这片区域布满了火焰陷阱。幸好我们之前派出了侦察员，他沿路在地上留下了宝石作为暗号，我们只需要顺着最近的宝石走就能躲过这些陷阱。

# 沙漠峡谷似乎会干扰你使用眼镜的findNearest技能！
# 你需要自己找到离你最近的宝石。

while True:
    coins = hero.findItems()
    coinIndex = 0
    nearest = None
    nearestDistance = 9999
    
    # 搜索所有的宝石，找到离你最近的那一颗。
    while coinIndex < len(coins):
        coin = coins[coinIndex]
        coinIndex += 1
        distance = hero.distanceTo(coin)
        # 如果宝石与你的距离小于“最近距离（nearestDistance）”
        if distance<nearestDistance:
            # 设置该宝石为离你最近的宝石
            a=coin
            # 设置该距离为“最近距离（nearestDistance）”
            nearestDistance=distance
    if a:
        yidong(a)
    # 如果找到离你最近的宝石，移动英雄岛宝石的位置。你需要使用moveXY，不需要你抄近路，也不会踩到陷阱。
def yidong(mb):
    hero.moveXY(mb.pos.x, mb.pos.y)

```
