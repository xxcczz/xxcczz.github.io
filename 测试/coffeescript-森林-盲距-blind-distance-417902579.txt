---
layout: default
title: blind-distance
---
## 盲距
```

# 这个函数寻找最近的敌人，并返回距离。
@nearestEnemyDistance = ->
    enemy = hero.findNearestEnemy()
    result = 0
    if enemy
        result = hero.distanceTo(enemy)
    return result

while true
    enemyDistance = @nearestEnemyDistance()
    if enemyDistance>0
        hero.say(enemyDistance)

```
