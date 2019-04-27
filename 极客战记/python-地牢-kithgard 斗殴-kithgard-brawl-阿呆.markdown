---
layout: default
title: kithgard-brawl
---
## kithgard 斗殴
```

# 在一波波的食人魔攻击中活下来。
# 如果你赢了，本关会变得更难，但给更多的奖励。
# 如果你输了，你必须等一天之后才能重新提交。
# 每次提交都会获得新的随机种子。
while True:
    enemy = hero.findNearestEnemy()
    if enemy:
        if hero.isReady("cleave") and hero.distanceTo(enemy)<10:
            hero.cleave(enemy)
        else:
            hero.shield()

```
