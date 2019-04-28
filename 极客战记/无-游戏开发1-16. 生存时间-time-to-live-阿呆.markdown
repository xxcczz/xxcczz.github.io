---
layout: default
title: time-to-live
---
## 16. 生存时间
```

game.addSurviveGoal(20)
generator=game.spawnXY("generator",20,20)
generator.spawnType="munchkin"
hero = game.spawnHeroXY("knight", 30,20)
hero.maxHealth = 100
hero.attackDamage = 10


# 开始游戏！

# 将参数传给addSurviveGoal()，以指定时间。


# 这表示玩家必须存活20秒。
game.addSurviveGoal(20)

# 使用spawnXY生成一个生成器。
# 使用变量来修改下面生成器的属性。
generator = game.spawnXY("generator", 60, 40)
# 将生成器的生成类型设为"munchkin"
generator.spawnType="munchkin"

# 使用spawnPlayerXY为玩家生成一个英雄。
player = game.spawnPlayerXY("knight", 15, 15)
# 将英雄的最大生命值设为100
player.maxHealth = 100
# 将英雄的攻击伤害值设为10
player.attackDamage = 10

# 开始游戏！

```
