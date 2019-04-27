---
layout: default
title: the-final-kithmaze
---
## Kithmaze最终历险
```

#循环
while true        
    #右
    hero.moveRight()
    #上
    hero.moveUp()
    #找敌人
    enemy = hero.findNearestEnemy()
    #如果有敌人
    if enemy
        #攻击
        hero.attack(enemy)
        #攻击
        hero.attack(enemy)
    #右
    hero.moveRight()
    #下下
    hero.moveDown(2)
    #上
    hero.moveUp()

```
