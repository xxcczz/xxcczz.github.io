---
layout: default
title: tactical-strike
---
## 战术打击
```

# 成功击败所有食人魔
hero.moveUp()
hero.moveRight(3)
hero.moveDown(2)
while True:
    enemy = hero.findNearestEnemy()
    if enemy:
        hero.attack(enemy)
    else:
        hero.moveLeft()
        hero.moveDown()

```
