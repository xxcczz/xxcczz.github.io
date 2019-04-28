---
layout: default
title: forest-incursion
---
## 12. 森林入侵
```

# Okar需要干掉这些讨人厌的矮人！
# 不幸的是，他速度很慢，而且攻击伤害很低。
# 不过，作为游戏开发者，你能够完全控制游戏世界！
# 将Okar的属性提高，方便他屠戮食人魔！

game.addDefeatGoal()
game.addSurviveGoal()
hero = game.spawnHeroXY("goliath", 12, 10)

hero.maxSpeed = 9999999999999999999999999999999999999999999999999999999999999999999999999999
hero.maxHealth = 999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999
hero.attackDamage = 99999999999999999999999999999999999999999999999999999999999999999999999999999999

# Okar需要干掉这些讨人厌的矮人！
# 不幸的是，他速度很慢，而且攻击伤害很低。
# 不过，作为游戏开发者，你能够完全控制游戏世界！
# 将Okar的属性提高，方便他屠戮食人魔！
# 您可以在DOC面板上找到单位的默认值。

game.addDefeatGoal()
game.addSurviveGoal()
player = game.spawnPlayerXY("goliath", 12, 10)
# 增加英雄的maxSpeed，让他跑起来更快。
player.maxSpeed = 25
# 增加英雄的maxHealth，让他能够更持久地作战。
player.maxHealth = 1000
# 增加英雄的attackDamage，让他能够更快干掉食人魔。
player.attackDamage = 1000

```
