---
layout: default
title: guard-duty
---
## 1. 守卫的职责
```

def soldierLogic():
    while True:
        enemy = soldier.findNearestEnemy()
        if enemy:
            soldier.attack(enemy)

soldier = hero.spawnXY("soldier", 42, 48)
soldier.on("spawn", soldierLogic)

# 添加一名士兵到该关卡，以防止食人魔穿过道路。
# 使用事件处理函数命令士兵。

def soldierLogic():
    # 在这里填写士兵行动的代码。
    # 记得用'soldier'代替'hero'！
    while True:
        enemy = soldier.findNearestEnemy()
        # 如果敌人存在，则攻击敌人。
        if enemy:
            # 单位有attack（）方法。
            # 你用士兵攻击（敌人）的方法：
            soldier.attack(enemy)
            pass
        # 否则，请回到起始位置。
        else:
            # 单位有moveXY（）方法。
            soldier.moveXY(42, 48)
            pass

# 这将生成的单位分配给士兵变量。
soldier = game.spawnXY("soldier", 42, 48)
# 这就是说，当士兵生成时，就可以执行士兵逻辑功能。
soldier.on("spawn", soldierLogic)

```
