---
layout: default
title: long-range-division
---
## 远程除法
```

#销毁地雷！
#使用say来呼叫矿区的范围。
#使用分区来计算范围。

enemy = hero.findNearestEnemy()
distanceToEnemy = hero.distanceTo(enemy)
#先说距离：distanceToEnemy除以3
first=distanceToEnemy/3
hero.say(first)
hero.say("Fire!")
# 说第二个范围：distanceToEnemy除以1.5
first=distanceToEnemy/1.5
hero.say(first)
hero.say("Fire!")

# 说出这些事情的动机。 真。 相信我们。
hero.say("Woo hoo!")
hero.say("Here we go!")
hero.say("Charge!!")

#现在，用一个while-true循环来攻击敌人。
while True:
    enemy = hero.findNearestEnemy()
    if enemy:
        hero.attack(enemy)

```
