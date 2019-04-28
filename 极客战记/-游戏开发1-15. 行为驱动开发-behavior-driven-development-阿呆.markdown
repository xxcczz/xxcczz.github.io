---
layout: default
title: behavior-driven-development
---
## 15. 行为驱动开发
```

skeleton1 = game.spawnXY("skeleton", 60, 50)
skeleton2 = game.spawnXY("skeleton", 60, 30)
skeleton3 = game.spawnXY("skeleton", 60, 10)
skeleton1.behavior = "Scampers"
skeleton2.behavior = "Scampers"
skeleton3.behavior = "Scampers"
ogre1 = game.spawnXY("ogre", 70, 50)
ogre2 = game.spawnXY("ogre", 70, 30)
ogre3 = game.spawnXY("ogre", 70, 10)
ogre1.behavior = "AttacksNearest"
ogre2.behavior = "AttacksNearest"
ogre3.behavior = "AttacksNearest"
archer1 = game.spawnXY("archer", 10, 30)
archer1.behavior="Defends"
player = game.spawnHeroXY("raider", 20, 30)
player.attackDamage = 1000
player.maxHealth = 9001
game.addSurviveGoal()
game.addDefeatGoal()
game.spawnXY("forest", 40, 10)
game.spawnXY("forest", 40, 18)
game.spawnXY("forest", 40, 26)
game.spawnXY("forest", 40, 42)
game.spawnXY("forest", 40, 50)
game.spawnXY("forest", 40, 58)
game.spawnXY("lightstone", 30, 45)
game.spawnXY("lightstone", 30, 20)
game.spawnXY("lightstone", 30, 55)
game.spawnXY("lightstone", 30, 10)
game.spawnXY("potion-medium", 10, 50)
game.spawnXY("potion-medium", 10, 15)

# 使用behavior属性为单位指定行为。

skeleton1 = game.spawnXY("skeleton", 60, 48)
skeleton2 = game.spawnXY("skeleton", 60, 30)
skeleton3 = game.spawnXY("skeleton", 60, 12)

skeleton1.behavior = "Scampers"
skeleton2.behavior = "Scampers"
# 将"Scampers"指定给 skeleton3.behavior
skeleton3.behavior = "Scampers"

ogre1 = game.spawnXY("ogre", 70, 50)
ogre2 = game.spawnXY("ogre", 70, 30)
ogre3 = game.spawnXY("ogre", 70, 10)

ogre1.behavior = "AttacksNearest"
# 将"AttacksNearest"指定给 ogre2.behavior
ogre2.behavior = "AttacksNearest"
# 将"AttacksNearest"指定给 ogre3.behavior
ogre3.behavior = "AttacksNearest"

archer1 = game.spawnXY("archer", 10, 30)
# 将"Defends"指定给 archer1.behavior
archer1.behavior="Defends"

# 下面这里不要做任何修改。
# 不过不妨看看！
player = game.spawnPlayerXY("raider", 20, 30)
player.attackDamage = 10
player.maxHealth = 9001
game.addSurviveGoal()
game.addDefeatGoal()

game.spawnXY("forest", 40, 10)
game.spawnXY("forest", 40, 18)
game.spawnXY("forest", 40, 26)
game.spawnXY("forest", 40, 42)
game.spawnXY("forest", 40, 50)
game.spawnXY("forest", 40, 58)

game.spawnXY("lightstone", 30, 45)
game.spawnXY("lightstone", 30, 20)
game.spawnXY("lightstone", 30, 55)
game.spawnXY("lightstone", 30, 10)

game.spawnXY("potion-medium", 10, 50)
game.spawnXY("potion-medium", 10, 15)

```
