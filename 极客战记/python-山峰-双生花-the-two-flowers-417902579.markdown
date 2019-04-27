---
layout: default
title: the-two-flowers
---
## 双生花
```

# 如果花匠受伤了,双生花会缩小！

def summonSoldiers():
    if hero.gold >= hero.costOf("soldier"):
        hero.summon("soldier")

# 定义函数:commandSoldiers
def commandSoldiers():
    friends = hero.findFriends()
    for j in range(len(friends)):
        friend = friends[j]
        if friend.type=="peasant":
            continue
        hero.command(friend, "defend", peasant)

# 定义函数:pickUpNearestCoin
def pickUpNearestCoin():
    #item = hero.findNearestItem()
    #if item:
    #    hero.move(item.pos)
    flag = hero.findFlag("green")
    if flag:
        hero.pickUpFlag(flag)
    jianjinbi()

peasant = hero.findByType("peasant")[0]

while True:
    summonSoldiers()
    commandSoldiers()
    pickUpNearestCoin()
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

```
