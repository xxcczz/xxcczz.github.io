---
layout: default
title: give-and-take
---
## 8. 取舍
```

# 移动到所有的X标记。
# 那些火焰陷阱会伤人！

game.spawnHeroXY("samurai", 40, 50)
game.addSurviveGoal()
game.addMoveGoalXY(25,40)
game.spawnXY("fire-trap", 25, 40)
game.addMoveGoalXY(55,40)
game.spawnXY("fire-trap", 55, 40)
game.addMoveGoalXY(40,20)
game.spawnXY("fire-trap", 40, 20)

# 生成一些"potion-small"对象，来治愈玩家！
game.spawnXY("potion-small", 25, 20)
game.spawnXY("potion-small", 30, 20)
game.spawnXY("potion-small", 35, 20)

```
