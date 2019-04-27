---
layout: default
title: thornbush-farm
---
## 荆棘农场
```

# 在村口巡逻。
# 当你见到食人魔，建造一个火焰陷阱"fire-trap"。
# 不要让任何农民受到伤害。

while True:
    hero.moveXY(43, 50)
    top = hero.findNearestEnemy()
    if top:
        hero.buildXY("fire-trap", 43, 50)

    hero.moveXY(25, 34)
    left = hero.findNearestEnemy()
    # 检查左边是否存在。
    if left:
        # 如果敌人存在，在25, 34处建造一个陷阱。
        hero.buildXY("fire-trap", 25, 34)
    hero.moveXY(43, 20)
    # 为下面的敌人设置一个变量。
    down = hero.findNearestEnemy()
    # 检查下面是否有敌人存在。
    if down:
        # 建造一个陷阱，如果敌人存在的话。
        hero.buildXY("fire-trap", 43, 20)

```
