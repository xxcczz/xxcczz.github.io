---
layout: default
title: chokepoint
---
## 5. 瓶颈
```

# 食人魔正在前进通过森林小道！
# 产生一些士兵，让他们保卫他们的车道！

def defendLane(event):
    # 记住为目标创建一个变量，要记住：
    unit = event.target
    # 保存设备的起始位置
    startX = unit.pos.x
    while True:
        enemy = unit.findNearestEnemy()
        # 如果有敌人，使用unit.attack攻击！
        if enemy:
            # Use unit.attack to attack the enemy:
            unit.attack(enemy)
            pass
        else:
            # 将设备移回到x和y的起始位置。
            unit.moveXY(startX, 16)
        

game.spawnXY("soldier", 9, 16)
game.spawnXY("soldier", 30, 16)
game.spawnXY("soldier", 54, 16)
game.spawnXY("soldier", 75, 16)

# Set the event handler defendLane on "spawn" event for "soldier"s.
game.setActionFor("soldier", "spawn", defendLane)

```
