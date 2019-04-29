---
layout: default
title: vital-powers
---
## 维他力量
```

# 这关会教你怎么定义你自己的函数。
# 放在函数内的代码并不会立刻执行, 而是先保存好, 以备后用.
# 这个函数会让你的英雄收集最近的金币。
def pickUpNearestCoin():
    items = hero.findItems()
    nearestCoin = hero.findNearest(items)
    if nearestCoin:
        hero.move(nearestCoin.pos)

# 这个函数会让你的英雄召唤一个士兵。
def summonSoldier():
    # 在这里写下代码：当你有足够金币时召唤士兵
    if hero.gold>hero.costOf("soldier"):
        hero.summon("soldier")
    pass


# 这个函数会命令你的士兵攻击最近的敌人
def commandSoldiers():
    for soldier in hero.findFriends():
        enemy = soldier.findNearestEnemy()
        if enemy:
            hero.command(soldier, "attack", enemy)

while True:
    # 在你的循环里，你可以"调用"你在上面定义的函数
    # 下面几行代码会让 "pickUpNearestCoin" 函数里的代码被执行。
    pickUpNearestCoin()
    # 在这里调用 summonSoldier
    summonSoldier()
    # 在这里调用 commandSoldiers
    commandSoldiers()

```
