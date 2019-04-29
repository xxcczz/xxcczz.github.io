---
layout: default
title: reaping-fire
---
## 收割火焰
```

# 目标是生存30秒，并且保持地雷完好至少30秒。
enemies1 = []
enemies2 = []
def chooseStrategy():
    enemies = hero.findEnemies()
    # 如果你可以召唤一个格里芬骑士，返回 "griffin-rider"
    if hero.gold >= hero.costOf("griffin-rider"):
        return "griffin-rider"
    # 否则，返回 "collect-coins"
    return "collect-coins"



def commandAttack():
    # 命令你的狮鹫骑士攻击食人魔。
    friends = hero.findFriends()
    for friend in friends:
        enemies = hero.findEnemies()
        for j in range(len(enemies)):
            enemy = enemies[j]
            if enemy.type == "fangrider" :
                continue
            enemies1.append(enemy)
        enemy1=friend.findNearest(enemies1)
        if enemy1:
            hero.command(friend, "attack", enemy1)
    pass
    
def pickUpCoin():
    # 收集硬币
    jianjinbi()
    pass
    
def heroAttack():
    # 你的英雄应该攻击对方的骑士，跨过雷区的那些。
    enemies = hero.findEnemies()
    for j in range(len(enemies)):
        enemy = enemies[j]
        if enemy.type == "fangrider" and enemy.pos.x<40:
            enemies2.append(enemy)
    if len(enemies2)>0:
        enemy2=hero.findNearest(enemies2)
        while enemy2.health>0:
            hero.attack(enemy2)
    pass
    
def jianjinbi():
    items = hero.findItems()
    a=None
    maxjz=0
    for item in items:
        jz=item.value/hero.distanceTo(item)
        if jz>maxjz:
            maxjz=jz
            a=item
    if a:
        hero.move(a.pos)
while True:
    commandAttack()
    heroAttack()
    strategy = chooseStrategy()
    # 调用一个函数，取决于目前决定要做什么。
    if strategy=="griffin-rider":
        hero.summon("griffin-rider")
        friends = hero.findFriends()
        hero.command(friends[len(friends)-1], "move", {"x": 116, "y": 40})
    elif strategy=="collect-coins":
        pickUpCoin()

```
