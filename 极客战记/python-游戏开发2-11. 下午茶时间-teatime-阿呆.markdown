---
layout: default
title: teatime
---
## 11. 下午茶时间
```

# 使用计时器生成敌人和物体。

# 这将生成两个富有攻击性的兽人。
def spawnMunchkins():
    munchkin1 = game.spawnXY("munchkin", 2, 12)
    munchkin2 = game.spawnXY("munchkin", 2, 56)
    munchkin1.behavior = "AttacksNearest"
    munchkin2.behavior = "AttacksNearest"

# 这将生成两个富有攻击性的投掷者。
def spawnThrowers():
    thrower1 = game.spawnXY("thrower", 2, 16)
    thrower1.behavior = "AttacksNearest"
    thrower2 = game.spawnXY("thrower", 2, 52)
    thrower2.behavior = "AttacksNearest"

# 这会在村庄附近生成一种健康药水。
def spawnPotion():
    game.spawnXY("potion-large", 46, 34)

# 生存30秒。
game.addSurviveGoal(20)

# 定时器的初始值定义了第一个外观。
game.munchkinSpawnTime = 0
game.throwerSpawnTime = 0
game.potionSpawnTime = 6
# 这用于UI。
game.nextPotionIn = 0

ui.track(game, "time")
# 让我们演示一下到下一瓶药水要多长时间。
ui.track(game, "nextPotionIn")

player = game.spawnPlayerXY("duelist", 40, 34)
player.maxSpeed = 15

# 这将检查和重设计时器。
def updateTimers():
    # 如果游戏时间比munchkinSpawnTime（兽人生成时间）长
    if game.time > game.munchkinSpawnTime:
        # 重设计时器并生成兽人。
        game.munchkinSpawnTime = game.munchkinSpawnTime + 6
        spawnMunchkins()
    # 如果游戏时间比potionSpawnTime（药水生成时间）长
    if game.time > game.potionSpawnTime:
        player.say("药水在这！")
        # Increase game.potionSpawnTime by 6:
        game.potionSpawnTime = game.potionSpawnTime + 6
        # 调用spawnPotion函数：
        spawnPotion()
    # 如果游戏时间比throwerSpawnTime（投掷者生成时间）长：
    if game.time > game.throwerSpawnTime:
        # Increase game.throwerSpawnTime by 9:
        game.throwerSpawnTime = game.throwerSpawnTime + 9
        # 调用spawnThrowers函数：
        spawnThrowers()
    # 在下一瓶药水前重设UI计时器
    game.nextPotionIn = game.potionSpawnTime - game.time
    
while True:
    updateTimers()

```
