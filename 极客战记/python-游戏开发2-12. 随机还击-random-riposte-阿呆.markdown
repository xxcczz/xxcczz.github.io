---
layout: default
title: random-riposte
---
## 12. 随机还击
```

#随机选择1到10之间的数字
num = game.randomInteger(1, 10)

# 使用game.randomInteger（min，max）添加随机数！
game.spawnPlayerXY("knight", 40, 35)
game.addSurviveGoal()
game.addDefeatGoal(8)

def onSpawn(event):
    while True:
        unit = event.target
        enemy = unit.findNearestEnemy()
        if enemy:
            unit.attack(enemy)

game.setActionFor("munchkin", "spawn", onSpawn)

# 每0到4秒产生一个食人魔。
spawnTime = 0
while True:
    if game.time > spawnTime:
        # 在随机位置产生一个"munchkin"
        # 将x设置为10到70之间的随机数
        x = game.randomInteger(10, 70)
        # 将y设置为10到60之间的随机数
        y = game.randomInteger(10, 60)
        # 在x，y产生一个"munchkin"
        game.spawnXY("munchkin", x, y)
        # 0至4秒再次产生
        spawnTime = game.time + game.randomInteger(0,4)

```
