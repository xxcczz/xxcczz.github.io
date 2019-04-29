---
layout: default
title: army-training-2
---
## 2. 陆军训练2
```

game.spawnXY("soldier", 30, 20)
game.spawnXY("soldier", 35, 20)
game.spawnXY("soldier", 40, 20)
game.spawnXY("soldier", 45, 20)

def lol(event):
    while True:
        unit = event.target
        unit.say("lol")

game.setActionFor("soldier", "spawn", lol)

# 使用事件处理程序来命令单位以击败来击败食人魔。 

# 产生2名 "soldier"s。
game.spawnXY("soldier", 35, 20)
game.spawnXY("soldier", 45, 20)
# 产生2名"archer"s。
game.spawnXY("archer", 35, 20)  # 人类弓箭手
game.spawnXY("archer", 35, 20)  # 人类弓箭手
def fightEnemies(event):
    while True:
        # event.target是执行这个事件处理函数的单元！
        friendUnit = event.target
        enemy = friendUnit.findNearestEnemy()
        # 然后会有队友攻击敌人！
        friendUnit.attack(enemy)

# 这将把fightEnemies处理程序添加到所有士兵的“spawn”事件中。
game.setActionFor("soldier", "spawn", fightEnemies)

# 现在，将敌人添加到弓箭手的“spawn”事件上：
game.setActionFor("archer", "spawn", fightEnemies)

```
