---
layout: default
title: freeze-tag
---
## 冻结标签
```

# 让我们制作一个冻结标签的游戏！

# game.tagged用于计数标记的弓箭手。
game.tagged = 0
ui.track(game, "tagged")
goal = game.addManualGoal("Tag all archers.")

# 孵化弓箭手。
game.spawnXY("archer", 12, 52)
game.spawnXY("archer", 12, 16)
game.spawnXY("archer", 24, 52)
game.spawnXY("archer", 24, 16)

player = game.spawnPlayerXY('captain', 68, 24)
player.maxSpeed = 20
# 让玩家变大一些，这样标记弓箭手就更容易了。
player.scale = 2

# 设置弓箭手的速度和行为属性onSpawn
def onSpawn(event):
    unit = event.target
    unit.behavior = "Scampers"
    unit.maxSpeed = 8

game.setActionFor("archer", "spawn", onSpawn)

#  "collide" 事件的事件处理程序。
def onCollide(event):
    # 事件拥有者与某事物相撞。
    unit = event.target
    # 单位碰撞的对象。
    other = event.other
    # 使用行为作为当前冻结状态的标记。
    # "Scampers"意味着射手尚未被标记。
    if unit.behavior == "Scampers":
        # 如果"other" 是玩家。
        if other.type == "captain":
            # 将unit.behavior设置为 "Defends"：
            unit.behavior == "Defends"
            # 增加game.tagged 1：
            game.tagged += 1
        pass
    if unit.behavior == "Defends":
        # 如果其他人的类型是 "archer"：
        if other.type == "archer":
            # 将unit.behavior设置为"Scampers"：
            unit.behavior = "Scampers"
            # 减少 game.tagged by 1.
            game.tagged -= 1

# 使用setActionFor将onCollide分配给"archer"s的"collide"事件。
game.setActionFor("archer", "collide", onCollide)

while True:
    if game.tagged >= 4:
        game.setGoalState(goal, True)

```
