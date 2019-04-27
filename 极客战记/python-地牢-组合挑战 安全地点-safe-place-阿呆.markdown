---
layout: default
title: safe-place
---
## 组合挑战: 安全地点
```

# 移动到宝藏室并击败所有食人魔。

hero.moveUp(4)#向上走
hero.moveRight(4)#向右走
hero.moveDown(3)#向下走
hero.moveLeft(1)#向左走
while True:
    enemy = hero.findNearestEnemy()
    if enemy:
        hero.attack(enemy)
    else:
        hero.moveLeft()#向左走

```
