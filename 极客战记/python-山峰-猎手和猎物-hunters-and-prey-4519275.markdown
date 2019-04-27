---
layout: default
title: hunters-and-prey
---
## 猎手和猎物
```

# 食人魔正试图除掉你的驯鹿！
# 当召唤士兵进攻时，让弓箭手回来。
def pickUpCoin():
    # 收集硬币。
    item = hero.findNearestItem()
    hero.move(item.pos)
def summonTroops():
    # 如果你有黄金就召唤士兵。
    if hero.gold > hero.costOf("soldier"):
        hero.summon("soldier")
# 这个函数有一个名为士兵的参数。
# 参数就像变量一样。
# 调用函数时确定参数的值。
def commandSoldier(soldier):
    # 士兵要攻击敌人。
    enemy = hero.findNearestEnemy()
    if enemy:
        hero.command(soldier, "attack", enemy)
# 编写一个命令弓箭手的函数来告诉你的弓箭手怎么做！
# 它应该有一个参数将表示在被调用时传递给函数的射手。
# 弓箭手应该只攻击距离25米以内的敌人，否则原地待命。
def archer(f):
    x = f.pos.x
    y = f.pos.y
    enemy = hero.findNearestEnemy()
    if enemy and f.distanceTo(enemy) < 25:
        hero.command(f, "attack", enemy)
while True:
    pickUpCoin()
    summonTroops()
    friends = hero.findFriends()
    for friend in friends:
        if friend.type == "soldier":
            # 这位朋友将被分配给commandSoldier函数中的士兵变量
            commandSoldier(friend)
            if friend.health < friend.maxHealth*0.5 :
                hero.command(friend, "move", {"x":24,"y":friend.pos.y})
        elif friend.type == "archer":
            # 务必指挥你的弓箭手。
            archer(friend)



```
