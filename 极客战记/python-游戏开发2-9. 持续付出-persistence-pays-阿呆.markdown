---
layout: default
title: persistence-pays
---
## 9. 持续付出
```

# 你可以使用数据库来存储持久性数据。
# 持久性数据在两次游戏间保持不变！

generator = game.spawnXY("generator", 60, 40)
generator.spawnType = "munchkin"
generator.spawnDelay = 1
player = game.spawnPlayerXY("raider", 36, 30)
player.maxHealth = 70
player.attackDamage = 10
game.addSurviveGoal(8)

# db表示数据库
# db.add(key, value) 让数据库中存储的值递增。
# 这会为数据库中的"plays"键加1。
db.add("plays", 1)

# 显示数据库中"plays"和其他键的值。
ui.track(db, "plays")
ui.track(db, "wins")
ui.track(db, "total defeated")

ui.track(game, "time")

# 显示游戏对象"defeated"属性的值
ui.track(game, "defeated");
# 下列代码将在玩家获胜时运行。
def onVictory(event):
    db.add("wins", 1)
    # 使用db.add(key, value)增加键的值。
    # 增加game.defeated到数据库的"total defeated"键
    db.add("total defeated", game.defeated)

game.on("victory", onVictory)

```
