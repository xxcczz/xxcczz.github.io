---
layout: default
title: seeing-is-believing
---
## 眼见为实
```

# 玩家想看到分数，这就可以使用ui.track()！
# 它会为玩家创建用户界面元素。
hero = game.spawnHeroXY("samurai", 20, 20)

game.addSurviveGoal(20)

spawner = game.spawnXY("generator", 50, 50)
spawner.maxHealth = 9001
spawner.spawnType = "munchkin"
# 添加更多生成器，用于在战场上生成更多敌人：
spawner = game.spawnXY("generator", 50, 50)

# ui.track()为玩家显示对象属性！
ui.track(game, "time")
# 使用ui.track来跟踪游戏的"defeated"属性：
ui.track(game, "defeated")
hero.attackDamage = 1000
# 增加英雄的最大速度：
hero.maxSpeed = 12

# 点击Play并打败6个矮人或骷髅怪！

```
