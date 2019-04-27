---
layout: default
title: oasis
---
## 绿洲
```

# 向绿洲移动
# Move left to avoid nearby yaks.
while True:
    x = hero.pos.x
    y = hero.pos.y
    enemy = hero.findNearestEnemy()
    if enemy and hero.distanceTo(enemy) < 10:
        # 通过在你的X坐标上减去10来移动到左边
        hero.moveXY(x-10, y)
        # Use moveXY to move to the new x, y position.
        
        pass
    else:
        # 通过在你的X坐标上加上10来移动到右边
        hero.moveXY(x+10, y)
        # Use moveXY to move to the new x, y position.
        
        pass

```
