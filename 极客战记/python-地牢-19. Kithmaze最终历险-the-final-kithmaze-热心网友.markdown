---
layout: default
title: the-final-kithmaze
---
## 19. Kithmaze最终历险
```
# 使用loop循环移动并攻击目标

while True:
    hero.moveRight()
    hero.moveUp()
    enemy = hero.findNearestEnemy()
    hero.attack(enemy)
    hero.moveRight()
    hero.moveDown(2)
    hero.moveUp()

```
