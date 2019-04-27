---
layout: default
title: bookkeeper
---
## 守书人
```

# 奋战沙场15秒。
# Keep count whenever an enemy is defeated.
defeated = 0
while True:
    enemy = hero.findNearestEnemy()
    if enemy:
        hero.attack(enemy)
        if enemy.health <= 0:
            defeated += 1
    if hero.time > 15:
        break

# Tell Naria how many enemies you defeated.
hero.moveXY(59, 33)
hero.say(defeated)

# 收集金币，直到时间达到30秒
while True:
    item = hero.findNearestItem()
    if item:
        yidong(item)
    if hero.time > 30:
        break
def yidong(mb):
    hero.moveXY(mb.pos.x, mb.pos.y)

# Tell Naria how much gold you collected.
hero.say(hero.gold)


# 攻击敌人，直到时间达到45秒
# 记得重置击败的敌人数。
defeated = 0
while True:
    enemy = hero.findNearestEnemy()
    if enemy:
        hero.attack(enemy)
        if enemy.health <= 0:
            defeated += 1
    if hero.time > 45:
        break

# Tell Naria how many enemies you defeated.
hero.moveXY(59, 33)
hero.say(defeated)

```
