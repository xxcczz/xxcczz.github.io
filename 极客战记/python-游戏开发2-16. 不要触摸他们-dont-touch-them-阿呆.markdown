---
layout: default
title: dont-touch-them
---
## 16. 不要触摸他们
```

goal = game.addManualGoal("Do the thing.")
# This marks the goal as a success.
game.setGoalState(goal, True)
# This marks the goal as a failure.
game.setGoalState(goal, False)
# Checking the goal state.
if goal.success:
    hero.say("Done!")

var goal = game.addManualGoal("Do the thing.");
// This marks the goal as a success.
game.setGoalState(goal, true);
// This marks the goal as a failure.
game.setGoalState(goal, false);
// Checking the goal state.
if (goal.success) {
    hero.say("Done!");
}

# 使用手动目标来指定哪些食人魔被击败。

def createGenerator(spawnType, x, y, spawnAI):
    generator = game.spawnXY("generator", x, y)
    generator.spawnType = spawnType
    generator.spawnAI = spawnAI

# 侦察员是积极活跃的，munchkins只是在行走。
createGenerator("scout", 12, 12, "AttacksNearest")
createGenerator("scout", 68, 56, "AttacksNearest")
createGenerator("munchkin", 12, 56, "Scampers")
createGenerator("munchkin", 68, 12, "Scampers")

player = game.spawnPlayerXY("duelist", 40, 34)
player.maxHealth = 1000
player.attackDamage = 2000
player.maxSpeed = 20

# 这些是我们的目标。 注意我们将它们保存在变量中！
spawnMunchkinsGoal = game.addManualGoal("产生6个munchkins")
dontTouchGoal = game.addManualGoal("不要攻击munchkins。")
defeatScoutsGoal = game.addManualGoal("击败6名侦察兵。")
# 游戏属性用于统计新的和失败的食人魔。
game.spawnedMunchkins = 0
game.defeatedScouts = 0
ui.track(game, "spawnedMunchkins")
ui.track(game, "defeatedScouts")

def onSpawn(event):
    game.spawnedMunchkins += 1

def onDefeat(event):
    unit = event.target
    if unit.type == "scout":
        game.defeatedScouts += 1
    if unit.type == "munchkin":
        # 如果munchkin被击败，dontTouchGoal失败。
        game.setGoalState(dontTouchGoal, False)
        player.say("Oops.")

def checkGoals():
    # 如果game.defeatedScouts大于5：
    if game.defeatedScouts>5:
        # 设置defeatScoutsGoal状态为成功。.
        game.setGoalState(defeatScoutsGoal, True)
    # 如果game.spawnedMunchkins大于5：
    if game.spawnedMunchkins>5:
        # 设置spawnMunchkinsGoal状态为成功。.
        game.setGoalState(spawnMunchkinsGoal, True)
    # 如果其他目标都完成了。
    if spawnMunchkinsGoal.success:
        if defeatScoutsGoal.success:
            # 将dontTouchGoal状态设置为成功。.
            game.setGoalState(dontTouchGoal, True)

game.setActionFor("munchkin", "spawn", onSpawn)
game.setActionFor("munchkin", "defeat", onDefeat)
game.setActionFor("scout", "defeat", onDefeat)

while True:
    checkGoals()

```
