---
layout: default
title: stick-shift
---
## 15. 切换目标
```

myGoal = game.addManualGoal("击败骷髅，救下射手！")

def onDefeat(event):
    unit = event.target
    if unit.type == "skeleton":
        game.setGoalState(myGoal, True)
    if unit.type == "archer":
        game.setGoalState(myGoal, False)

game.setActionFor("archer", "defeat", onDefeat)
game.setActionFor("skeleton", "defeat", onDefeat)

# 现在你可以为你的游戏创建一个自定义目标
# 使用 game.addManualGoal（描述）方法！

# 构建一些侦察员，老板和迷宫。
game.spawnMaze(5)
game.spawnXY("scout", 60, 58)
game.spawnXY("scout", 28, 29)
game.spawnXY("scout", 61, 24)
ogref = game.spawnXY("ogre-f", 60, 12)

# 构建并配置英雄。
hero = game.spawnPlayerXY("captain", 12, 56)
hero.maxHealth = 550
hero.maxSpeed = 10
hero.attackDamage = 250

# 构建一个兽人生成器。
generator = game.spawnXY("generator", 41, 13)
generator.spawnDelay = 5
generator.spawnType = "munchkin"

# 存活目标。
game.addSurviveGoal()
game.spawnXY("potion-medium", 28, 12)

# addManualGoal添加一个描述不完整的目标
# 描述将显示给玩家。
# 注意要将其保存在名为scoutGoal的变量中
scoutGoal = game.addManualGoal("Defeat all scouts")

# 使用addManualGoal添加一个目标来击败Boss
# 将其保存在名为bossGoal的变量中
bossGoal = game.addManualGoal("Defeat the big boss!")

# 敌人的行为
def onSpawn(event):
    unit = event.target
    while True:
        enemy = unit.findNearestEnemy()
        if enemy:
            unit.attack(enemy)

game.setActionFor("scout", "spawn", onSpawn)
game.setActionFor("ogre", "spawn", onSpawn)

# 计算有多少侦察兵被打败..
scoutsDefeated = 0

# 每当敌人失败时更新我们的自定义目标。
# 这是一个使用if语句的算法的例子。
def onDefeat(event):
    unit = event.target
    if unit.type == "scout":
        scoutsDefeated += 1
        hero.say("Scout down!")
    if scoutsDefeated >= 3:
        # 使用setGoalState标记达成的侦察目标。
        game.setGoalState(scoutGoal, True)
        hero.say("All Scouts down!")
    if unit.type == "ogre":
        # 使用game.setGoalState标记boss目标达到。
        # 不要忘记第二个参数。
        game.setGoalState(bossGoal, True)
        hero.say("Defeated the big boss!")

# 将失败处理程序分配给食人魔"defeat"
# 注意兽人是不会成功的！
game.setActionFor("scout", "defeat", onDefeat)
game.setActionFor("ogre", "defeat", onDefeat)

```
