---
layout: default
title: hunters-and-prey
---
## 猎手和猎物
```

# 食人魔正试图除掉你的驯鹿！
# 当召唤士兵进攻时，让弓箭手回来。
def pickUpCoin():
    # Collect coins.
    coin = hero.findNearest(hero.findItems())
    if coin:
        hero.move(coin.pos)
def summonTroops():
    # Summon soldiers if you have the gold.
    if hero.gold >= hero.costOf("soldier"):
        hero.summon("soldier")
# This function has an argument named soldier.
# Arguments are like variables.
# The value of an argument is determined when the function is called.
def commandSoldier(soldier):
    # Soldiers should attack enemies.
    enemy = soldier.findNearestEnemy()
    hero.command(soldier, "attack", enemy)
def commandarcher(archer):
    enemy = archer.findNearestEnemy()
    if enemy:
        if archer.distanceTo(enemy)<25:
            hero.command(archer, "attack", enemy)
# 编写一个命令弓箭手的函数来告诉你的弓箭手怎么做！
# 它应该有一个参数将表示在被调用时传递给函数的射手。
# 弓箭手应该只攻击距离25米以内的敌人，否则原地待命。
while True:
    pickUpCoin()
    summonTroops()
    friends = hero.findFriends()
    for friend in friends:
        
        if friend.type == "soldier":
            # This friend will be assigned to the variable soldier in commandSoldier
            commandSoldier(friend)
        elif friend.type == "archer":
            # Be sure to command your archers.
            commandarcher(friend)
            pass

```
