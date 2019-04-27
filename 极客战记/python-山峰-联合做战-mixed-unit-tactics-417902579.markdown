---
layout: default
title: mixed-unit-tactics
---
## 联合做战
```

# 练习用取模从数组中循环取值

# 在数组array中编排好兵种组合
summonTypes = ["soldier","archer"]
def jianjinbi():
    coin = hero.findNearest(hero.findItems())
    if coin:
        hero.move(coin.pos)
def summonTroops():
    # 用%取模来循环预设的征兵方案 len(self.built)
    type = summonTypes[len(hero.built) % len(summonTypes)]
    if hero.gold >= hero.costOf(type):
        hero.summon(type)
def mlgj():
    friends = hero.findFriends()
    for j in range(len(friends)):
        friend = friends[j]
        enemy = friend.findNearestEnemy()
        if enemy:
            hero.command(friend, "attack", enemy)
        

while True:
    jianjinbi()
    summonTroops()
    mlgj()

```
