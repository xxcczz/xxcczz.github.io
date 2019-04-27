---
layout: default
title: sarven-gaps
---
## Sarven 的距离
```

# 每次向下移动10米，来走到绿洲。
# 在每个食人魔左边20米的位置建造栅栏。

while True:
    enemy = hero.findNearestEnemy()
    if enemy:
        # 在敌人左边建造20个单位的栅栏。
        hero.buildXY("fence", enemy.pos.x-20, enemy.pos.y)
        hero.moveXY(hero.pos.x-3, hero.pos.y)
        pass
    else:
        # 每次向下移动10个单位。
        hero.moveXY(hero.pos.x, hero.pos.y-10)
        pass

```
