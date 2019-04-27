---
layout: default
title: timber-turncoat
---
## 木材的叛徒
```

while True:
    # 收集金子
    js()
    jianjinbi()
    # 如果你有足够的金币，召唤一个士兵。
    if hero.gold>=hero.costOf("soldier"):
        hero.summon("soldier")
    # 使用 for 循环来命令每个士兵。
    for friend in hero.findFriends():
        if friend.type == "soldier":
            # 如果这有一个敌人，命令她攻击。
            # Careful! If your soldiers are defeated, a warlock will appear!
            # 否则的话，移动她到地图的右边。
            if friend.pos.x<40:
                hero.command(friend, "move", {"x": 89, "y": 46})
            if friend.health<100:
                hero.command(friend, "move", {"x": 40, "y": 38})
                continue
            enemy = friend.findNearestEnemy()
            if enemy:
                hero.command(friend, "attack", enemy)
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
def js():    
    if hero.canCast("haste", hero):    
        hero.cast("haste", hero)    
    else:    
        cooldown = hero.getCooldown("haste")
        if cooldown!=0:
            hero.resetCooldown("haste")

```
