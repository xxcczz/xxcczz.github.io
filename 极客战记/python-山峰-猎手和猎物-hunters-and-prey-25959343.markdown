---
layout: default
title: hunters-and-prey
---
## 猎手和猎物
```

# 食人魔正试图除掉你的驯鹿！
# 当召唤士兵进攻时，让弓箭手回来。
def pickUpCoin():
    # 收集硬币。
    icon = hero.findNearest(hero.findItems())
    if icon:
        hero.move(icon.pos)
    pass
num = 0
def summonTroops():
    # 如果num是奇数你有黄金就召唤弓手,否则就召唤士兵。
    if num%2 == 0:
        if hero.gold > hero.costOf("archer"):
            hero.summon("archer")
            num += 1
    else:
        if hero.gold > hero.costOf("soldier"):
            hero.summon("soldier")
            num += 1
    pass
# 这个函数有一个名为士兵的参数。
# 参数就像变量一样。
# 调用函数时确定参数的值。
def commandSoldier(soldier):
    # 士兵要攻击敌人。
    enemy = friend.findNearestEnemy()
    if enemy and friend.distanceTo(enemy)<25:
        hero.command(friend, "attack", enemy)
    else:
        hero.command(friend, "move", {"x":24,"y":friend.pos.y})
        #break
    pass
def commandarcher(soldier):
    # 士兵要攻击敌人。
    enemy = friend.findNearestEnemy()
    if enemy and friend.distanceTo(enemy)<25:
        hero.command(friend, "attack", enemy)
    else:
        hero.command(friend, "move", {"x":24,"y":friend.pos.y})
        #break
    pass
# 编写一个命令弓箭手的函数来告诉你的弓箭手怎么做！
# 它应该有一个参数将表示在被调用时传递给函数的射手。
# 弓箭手应该只攻击距离25米以内的敌人，否则原地待命。
while True:
    pickUpCoin()
    summonTroops()
    #commandSoldier()
    friends = hero.findFriends()
    for friend in friends:
        if friend.type == "soldier":
            # 这位朋友将被分配给commandSoldier函数中的士兵变量
            commandSoldier(friend)
        elif friend.type == "archer":
            # 务必指挥你的弓箭手。
            commandarcher(friend)

```
