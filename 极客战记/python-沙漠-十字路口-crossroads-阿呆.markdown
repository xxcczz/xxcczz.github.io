---
layout: default
title: crossroads
---
## 十字路口
```

# 使用  fire-trap 打败进攻的食人魔

while True:
    enemy = hero.findNearestEnemy()
    if enemy:
        # If the enemy is to the left of the hero:
        if enemy.pos.x < hero.pos.x:
            # 如果敌人从左边进攻,在左边建一个fire-trap（火焰陷阱）
            hero.buildXY("fire-trap", 25, 35)
            pass
        # If the enemy is to the right of the hero:
        elif enemy.pos.x > hero.pos.x:
            # 如果敌人从右边进攻,在右边建一个fire-trap（火焰陷阱）
            hero.buildXY("fire-trap", 55, 35)
            pass
        # If the enemy is below the hero:
        elif enemy.pos.y < hero.pos.y:
            # 如果敌人从下边进攻,在下边建一个fire-trap（火焰陷阱）
            hero.buildXY("fire-trap", 40, 20)
            pass
        # If the enemy is above the hero:
        elif enemy.pos.y > hero.pos.y:
            # 如果敌人从上边进攻,在上边建一个fire-trap（火焰陷阱）
            hero.buildXY("fire-trap", 40, 50)
            pass
    # Move back to the center.
    hero.moveXY(40, 34)

```
