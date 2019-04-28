---
layout: default
title: them-bones
---
## 14. 他们骨头
```

# 生成器会随时间生成敌人。
# 骷髅怪害怕发光石。

player = game.spawnHeroXY("champion", 15, 35)
player.attackDamage = 6000
player.maxSpeed = 8
game.addSurviveGoal()
game.addDefeatGoal()
game.spawnXY("x-mark-stone", 60, 35)
generator=game.spawnXY("generator",20,20)
generator.spawnType="skeleton"
generator.spawnDelay=5
game.spawnXY("lightstone",21,20)
# 现在，通关你的游戏！

# 生成器会随时间生成敌人。
# 骷髅怪害怕发光石。

player = game.spawnPlayerXY("champion", 15, 35)
player.attackDamage = 600
player.maxSpeed = 8

game.addSurviveGoal()
game.addDefeatGoal()
game.spawnXY("x-mark-stone", 60, 35)
# 生成一个"生成器"
generator=game.spawnXY("generator",20,20)
# 生成一个"发光石"
game.spawnXY("lightstone",21,20)
# 现在，通关你的游戏！

```
