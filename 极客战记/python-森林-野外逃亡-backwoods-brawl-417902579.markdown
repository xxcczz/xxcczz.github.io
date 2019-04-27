---
layout: default
title: backwoods-brawl
---
## 野外逃亡
```

# 生存一分钟。
# 如果你赢了，接下来会变得更难，当然也会有更多奖励。
# 如果你输了，你必须等待24小时后才能再次挑战。
# 记得，每一次提交都会获得不同的地图。

while True:
    hero.shield()

# 生存一分钟。
# 如果你赢了，接下来会变得更难，当然也会有更多奖励。
# 如果你输了，你必须等待24小时后才能再次挑战。
# 记得，每一次提交都会获得不同的地图。
while True:
    enemy = hero.findNearestEnemy()
    distance = hero.distanceTo(enemy)
    if enemy and distance<10 and hero.isReady("cleave"):
        hero.cleave(enemy)
    hero.shield()

```
