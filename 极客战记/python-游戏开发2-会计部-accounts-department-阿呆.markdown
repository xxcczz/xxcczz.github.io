---
layout: default
title: accounts-department
---
## 会计部
```

def onCollect(event):
    who = event.target
    what = event.other
    game.score += what.value
    who.say("I found " + what)

somebody.on("collect", onCollect)

# 计算收集的项目值并将其用于评分。

# 设置字符。
player = game.spawnPlayerXY("captain", 40, 34)
player.maxSpeed = 20

# 宝石是最有价值的物品。
game.spawnXY("chest", 68, 56)
game.spawnXY("chest", 14, 14)

# 这个函数随机产生一个随机项目。
def spawnRandomItem():
    itemNumber = game.randomInteger(1, 3)
    x = game.randomInteger(12, 68)
    y = game.randomInteger(12, 56)
    if itemNumber == 1:
        game.spawnXY("bronze-coin", x, y)
    elif itemNumber == 2:
        game.spawnXY("gold-coin", x, y)
    elif itemNumber == 3:
        game.spawnXY("gem", x, y)

itemInterval = 1
itemSpawnTime = 0

def checkSpawnTimer():
    if game.time >= itemSpawnTime:
        # Call the spawnRandomItem function.
        spawnRandomItem()
        itemSpawnTime += itemInterval

game.score = 0

#  "collect" 事件是通过收集东西来触发的。
def onCollect(event):
    # event.target包含收集器。
    collector = event.target
    # event.other包含收集的项目。
    item = event.other
    if item.value:
        # Adding health power for valuable items.
        collector.health += item.value
        # 通过该项目的`value`增加游戏分数：
        game.score = game.score+item.value
        pass

# 在“collect”事件上为“player”分配onCollect处理程序。
player.on("collect", onCollect)

# 玩家需要赢得的比分。
requiredScore = 220
goldGoal = game.addManualGoal('在20秒内收集至少220金币。')
ui.track(game, "score")

def checkGoals():
    if game.score >= requiredScore:
        game.setGoalState(goldGoal, True)

while True:
    checkSpawnTimer()
    checkGoals()

```
