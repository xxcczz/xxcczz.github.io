---
layout: default
title: lernaean-hydra
---
## 14. 水蛇许德拉
```

# 为每个被击败的食人魔，产生两个新食人魔。

player = game.spawnPlayerXY("knight", 40, 34)
player.attackDamage = 20

# 用这个来计算被击败的食人魔。
game.defeated = 0
# 玩家需要击败多少食人魔
game.toDefeat = 16
game.addDefeatGoal(game.toDefeat)
# 使用ui.track将这些有用的变量显示给玩家
ui.track(player, "health")
ui.track(game, "defeated")
ui.track(game, "toDefeat")

# 最开始i的敌人。
game.spawnXY("munchkin", 30, 14)
game.spawnXY("munchkin", 50, 54)

# 这使得新的敌人很有侵略性。
def onSpawn(event):
    unit = event.target
    unit.behavior = "AttacksNearest"

# 计数击败的敌人并产生新的敌人。
def onDefeat(event):
    unit = event.target
    # 减少游戏的击败收获：
    game.toDefeat -= 1
    # 增加游戏的战败损失：
    game.defeated += 1
    # 获得新的敌人的随机坐标。
    x1 = game.randomInteger(10, 40)
    x2 = game.randomInteger(40, 70)
    y = game.randomInteger(12, 56)
    game.spawnXY("potion-small", unit.pos.x, unit.pos.y)
    # Spawn a "munchkin" at the point x1, y:
    game.spawnXY("munchkin", x1, y)
    # Spawn a "munchkin" at the point x2, y:
    game.spawnXY("munchkin", x2, y)

game.setActionFor("munchkin", "spawn", onSpawn)
# 将"munchkin"的"defeat"事件处理程序设置为onDefeat：
game.setActionFor("munchkin", "defeat", onDefeat)

```
