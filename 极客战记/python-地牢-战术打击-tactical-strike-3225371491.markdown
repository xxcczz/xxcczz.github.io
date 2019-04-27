---
layout: default
title: tactical-strike
---
## 战术打击
```
while True:
    hero.moveUp()
    hero.moveRight(3)
    hero.moveDown(2)
    enemy= hero.findNearestEnemy()
    hero.attack(enemy)
    enemy= hero.findNearestEnemy()
    hero.attack(enemy)
    hero.moveLeft()
    hero.moveDown()
```
