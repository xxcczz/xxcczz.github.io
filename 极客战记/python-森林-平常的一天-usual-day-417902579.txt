---
layout: default
title: usual-day
---
## 平常的一天
```

# 打败食人魔，收集金币。一切都那么平常。
# 使用 与(AND) 在同一行检查存在性和类型。

while True:
    enemy = hero.findNearestEnemy()
    # 有了与(AND)，只在敌人存在时检查类型
    if enemy and enemy.type == "munchkin":
        hero.attack(enemy)
    # 寻找最近的物品
    a=hero.findNearestItem()
    if a and a.type=="coin":
        hero.moveXY(a.pos.x, a.pos.y)
    # 如果有名为 “coin” (金币)的物品存在，那就快去收集它！

```
