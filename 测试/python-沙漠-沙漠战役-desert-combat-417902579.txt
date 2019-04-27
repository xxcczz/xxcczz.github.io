---
layout: default
title: desert-combat
---
## 沙漠战役
```

# while循环重复直到条件为否。

ordersGiven = 0
while ordersGiven < 5:
    # 在站场上移动和排列你的盟友。 （如果你是直接在他们面前，他们只能听到你的。）
    hero.moveXY(hero.pos.x, hero.pos.y-10)
    # Order your ally to "Attack!" with hero.say
    # They can only hear you if you are on the X.
    hero.say("Attack!")
    ordersGiven=ordersGiven+1

    # Be sure to increment ordersGiven!
    

while True:
    enemy = hero.findNearestEnemy()
    # 当你下达完命令，立即加入战斗！
    if enemy:
        hero.attack(enemy)

```
