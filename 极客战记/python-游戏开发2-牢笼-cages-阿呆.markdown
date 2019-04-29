---
layout: default
title: cages
---
## 牢笼
```

if game.scoutsSpawned >= 5:
    someGenerator.defeat()
    someWall.destroy()

# 了解摧毁与击败的区别。

# 生成敌人
ogre1 = game.spawnXY("ogre", 12, 18)
ogre1.behavior = "AttacksNearest"
ogre2 = game.spawnXY("ogre", 68, 50)
ogre2.behavior = "AttacksNearest"

munchkinGenerator = game.spawnXY("generator", 12, 50)
munchkinGenerator.spawnAI = "Scampers"
munchkinGenerator.spawnType = "munchkin"

scoutGenerator = game.spawnXY("generator", 68, 12)
scoutGenerator.spawnAI = "Scampers"
scoutGenerator.spawnType = "scout"

# 我们将在之后摧毁的栅栏。
leftFence = game.spawnXY("fence", 26, 14)
rightFence = game.spawnXY("fence", 54 , 50)

player = game.spawnPlayerXY("knight", 40, 34)
player.maxSpeed = 16
player.attackDamage = 2000

# 游戏目标计数器
game.scoutsSpawned = 0
game.munchkinsSpawned = 0
game.bossesDefeated = 0
ui.track(game, "scoutsSpawned")
ui.track(game, "munchkinsSpawned")
ui.track(game, "bossesDefeated")

bossesGoal = game.addManualGoal("击败两个大食人魔。")

def onSpawn(event):
    unit = event.target
    if unit.type == "scout":
        game.scoutsSpawned += 1
    if game.scoutsSpawned >= 3:
        # 使用defeat() 方法击败scoutGenerator（战士生成器）
        scoutGenerator.defeat()
        # 使用destroy() 方法摧毁 rightFence（右边的栅栏）。
        rightFence.destroy()
        pass
    if unit.type == "munchkin":
        game.munchkinsSpawned += 1
    if game.munchkinsSpawned >= 2:
        # 击败munchkinGenerator（兽人生成器）。
        munchkinGenerator.defeat()
        # 摧毁 leftFence（左边的栅栏）
        leftFence.destroy()
        pass

def onDefeat(event):
    unit = event.target
    if unit.type == "ogre":
        # 往 the game.bossesDefeated加一
        game.bossesDefeated += 1

game.setActionFor("munchkin", "spawn", onSpawn)
game.setActionFor("scout", "spawn", onSpawn)
game.setActionFor("ogre", "defeat", onDefeat)

while True:
    if game.bossesDefeated >= 2:
        game.setGoalState(bossesGoal, True)

```
