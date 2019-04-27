---
layout: default
title: zero-sum
---
## 零和
```

# 在两分钟内击败敌方英雄。
while True:
    enemies = hero.findEnemies()
    nearestEnemy = hero.findNearest(enemies)
    
    # 你的英雄能收集金币，召唤部队。
    if hero.gold > hero.costOf("soldier"):
        hero.summon("soldier")
    
    # 在站场上，她也可以命令你的盟友。
    friends = hero.findFriends()
    for friend in friends:
        hero.command(friend, "attack", friend.findNearest(enemies))
    
    # 使用你的英雄的能力力挽狂澜。
    jianjinbi()

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
