---
layout: default
title: timber-guard
---
## 木材守卫
```

while True:
    # 收集金子
    item = hero.findNearestItem()
    if item:
        hero.move(item.pos)
    # 如果你有足够的金币，召唤一个士兵。
    if hero.gold>=hero.costOf("soldier"):
        hero.summon("soldier")
    # 使用 for 循环来命令每个士兵。
    # for 循环有两个部分『for X in Y』
    # Y 是被循环的数组结构
    #  Y 中的每个元素都会执行，X 会被设置称当前循环的个体
    if len(hero.findFriends())>0:
        for friend in hero.findFriends():
            if friend.type == "soldier":
                enemy = friend.findNearestEnemy()
                # 如果这有一个敌人，命令她攻击。
                # 否则的话，移动她到地图的右边。
                if enemy:
                    hero.command(friend, "attack", enemy)
                else:
                    hero.command(friend, "move", {"x": 72, "y": 36})

```
