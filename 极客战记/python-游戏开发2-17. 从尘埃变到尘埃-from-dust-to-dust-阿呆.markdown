---
layout: default
title: from-dust-to-dust
---
## 17. 从尘埃变到尘埃
```

//创造并击败食人魔。
var munchkin = game.spawnXY("munchkin", 10, 10);
munchkin.defeat(); //我们可以看到被击败的食人魔。
// 创建并移除侦察兵
var scout = game.spawnXY("munchkin", 20, 20);
scout.destroy(); //这没有东西

# Create and defeat a munchkin.
munchkin = game.spawnXY("munchkin", 10, 10)
munchkin.defeat() # We can see the defeated ogre.
# Create and remove a scout
scout = game.spawnXY("munchkin", 20, 20)
scout.destroy() # Nothing here

# 用森林瓦片堵塞通道。
# 然后在玩家击败一些食人魔时摧毁他们。

# 设置玩家。
player = game.spawnPlayerXY("duelist", 6, 34)
player.attackDamage = 35
player.maxHealth = 750
player.maxSpeed = 15
# 玩家应该穿过森林才能获胜。
game.addMoveGoalXY(76, 34)

# 设置敌人。
munchkinSpawner = game.spawnXY("generator", 16, 56)
munchkinSpawner.spawnType = "munchkin"
munchkinSpawner.spawnDelay = 3
scoutSpawner = game.spawnXY("generator", 40, 10)
scoutSpawner.spawnType = "scout"
scoutSpawner.spawnDelay = 5

# 这些森林砖应该堵住通道
passageForest1 = game.spawnXY("forest", 28, 34)
# 创建第二个森林来阻止第二个通道：
passageForest2 = game.spawnXY("forest", 52, 34)

game.defeated = 0
ui.track(game, "defeated")

def onDefeat(event):
    defeated = event.target
    game.defeated += 1
    # 如果4个食人魔被击败：
    if game.defeated == 3:
        # 击败食人魔产卵器。
        munchkinSpawner.defeat()
        # 摧毁第一片森林通道。
        passageForest1.destroy()
    # 如果8个食人魔被击败：
    if game.defeated == 8:
        # 调用scoutSpawner的失败方法：
        scoutSpawner.defeat()
        # 摧毁第二片森林通道。
        passageForest2.destroy()
# 为"munchkin"s 和"scout"s设置"defeat"事件处理程序。
game.setActionFor("munchkin", "defeat", onDefeat)
game.setActionFor("scout", "defeat", onDefeat)


# 击败这个游戏！

```
