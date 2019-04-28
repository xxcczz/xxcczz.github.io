---
layout: default
title: a-maze-ing
---
## 4. 太-棒-了
```

# Alejandro喜欢挑战！
# 为关卡增加更多"森林"对象，来创建更长的迷宫。

# 设置游戏目标。
game.addCollectGoal()
# 生成一个英雄和宝箱。
game.spawnHeroXY("duelist", 9, 59)
game.spawnXY("chest", 19, 35)

game.spawnXY("forest", 26, 51)
# 再添加2个"森林"对象。记得不要把宝石彻底挡死。
game.spawnXY("forest", 26, 51)
game.spawnXY("forest", 26, 51)

```
