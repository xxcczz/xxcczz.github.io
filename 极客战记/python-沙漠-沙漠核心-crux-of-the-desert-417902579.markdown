---
layout: default
title: crux-of-the-desert
---
## 沙漠核心
```

# 找出食人魔是来自哪个方向的

while True:
    enemy = hero.findNearestEnemy()
    if enemy:
        # Left: enemy.pos.x is less than hero.pos.x
        isLeft = hero.pos.x  > enemy.pos.x
        # Above: enemy.pos.y is greater than hero.pos.y
        isAbove = hero.pos.y < enemy.pos.y
        # Right: enemy.pos.x is greater than hero.pos.x
        isRight = hero.pos.x < enemy.pos.x
        # Below: enemy.pos.y is less than hero.pos.y
        isBelow = hero.pos.y > enemy.pos.y
        # 如果敌人在上方 (isAbove) 和 左边 (isLeft)：
        # buildXY() a "fire-trap" at the X mark.
        if isLeft and isAbove:
            hero.buildXY("fire-trap", 40 - 20, 34 + 17)
        # 如果敌人在上方 (isAbove) 和右边 (isRight)：
        # buildXY() a "fire-trap" at the X mark.
        if isRight and isAbove:
            hero.buildXY("fire-trap", 40 + 20, 34 + 17)
        # 如果敌人在下方 (isBelow) 和左边 (isLeft)：
        # buildXY() a "fire-trap" at the X mark.
        if isLeft and isBelow:
            hero.buildXY("fire-trap", 40 - 20, 34 - 17)
        # 如果敌人在下方 (isBelow) 和右边 (isRight)：
        # buildXY() a "fire-trap" at the X mark.
        if isRight and isBelow:
            hero.buildXY("fire-trap", 40 + 20, 34 - 17)
        hero.moveXY(40, 34)
    else:
        hero.moveXY(40, 34)

```
