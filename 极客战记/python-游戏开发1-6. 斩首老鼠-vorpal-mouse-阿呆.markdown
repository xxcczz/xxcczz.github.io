---
layout: default
title: vorpal-mouse
---
## 6. 斩首老鼠
```

# 游戏中，点击食人魔来攻击！
# 这一关不需要键入任何代码，只需要点击测试关卡按钮！

# 下列代码将生成一个可供游戏的英雄：
game.spawnHeroXY("guardian", 40, 40)

# 这些将为关卡添加目标：
game.addDefeatGoal()
game.addSurviveGoal()

# 这将生成一些可供战斗的敌人：
game.spawnXY("munchkin", 40, 25)
game.spawnXY("munchkin", 15, 15)
game.spawnXY("munchkin", 65, 15)

# 这将为玩家生成一个迷宫：
game.spawnXY("forest", 30, 54)
game.spawnXY("forest", 50, 54)
game.spawnXY("forest", 30, 48)
game.spawnXY("forest", 50, 48)
game.spawnXY("forest", 30, 40)
game.spawnXY("forest", 50, 40)
game.spawnXY("forest", 30, 32)
game.spawnXY("forest", 50, 32)
game.spawnXY("forest", 30, 26)
game.spawnXY("forest", 50, 26)
game.spawnXY("forest", 30, 10)
game.spawnXY("forest", 50, 10)
game.spawnXY("forest", 22, 26)
game.spawnXY("forest", 58, 26)
game.spawnXY("forest", 14, 26)
game.spawnXY("forest", 66, 26)

```
