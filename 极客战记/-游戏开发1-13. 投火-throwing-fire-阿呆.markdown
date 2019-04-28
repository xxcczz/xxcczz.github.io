---
layout: default
title: throwing-fire
---
## 13. 投火
```

player = game.spawnHeroXY("knight", 40, 10)
game.addCollectGoal()
game.addSurviveGoal()
game.spawnXY("gem", 32, 55)
game.spawnXY("gem", 51, 55)
fs1 = game.spawnXY("fire-spewer", 12, 25)
fs2 = game.spawnXY("fire-spewer", 70, 30)
fs3 = game.spawnXY("fire-spewer", 12, 35)
fs4 = game.spawnXY("fire-spewer", 70, 40)
fs1.direction = "vertical"
fs2.direction = "vertical"
fs3.direction = "vertical"
fs4.direction = "vertical"

# 游戏对象可以设置属性。

# 不要改变这个，它是设置游戏的。
player = game.spawnPlayerXY("knight", 40, 10)
game.addCollectGoal()
game.addSurviveGoal()

game.spawnXY("gem", 32, 55)
game.spawnXY("gem", 51, 55)

fs1 = game.spawnXY("fire-spewer", 12, 25)
fs2 = game.spawnXY("fire-spewer", 70, 30)
fs3 = game.spawnXY("fire-spewer", 12, 35)
fs4 = game.spawnXY("fire-spewer", 70, 40)

# 将fs1.direction改成"vertical"：
fs1.direction = "vertical"

# 再将fs2.direction改成"vertical"：
fs2.direction = "vertical"
# fs3和fs4也这样做：
fs3.direction = "vertical"
fs4.direction = "vertical"
# 下面开始游戏并收集宝石！

```
