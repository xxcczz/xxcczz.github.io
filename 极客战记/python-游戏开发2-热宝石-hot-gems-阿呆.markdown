---
layout: default
title: hot-gems
---
## 热宝石
```

function onCollect（event）{
     var who = event.target;
     var what = event.other;
     if（what.type ==“potion”）{
         who.say（“哦，它中毒了。”）;
        who.defeat（）;
    }
}

somebody.on（“collect”，onCollect）;

def onCollect（event）：
     who = event.target
     what = event.other
     如果what.type =="potion" ：
         who.say（“哦，它中毒了。”）
        who.defeat（）
    }

somebody.on（“collect”，onCollect）

# 金币应该治愈你，宝石会伤害你。

player = game.spawnPlayerXY("captain", 40, 34)
player.maxSpeed = 20
# 我们使用相对健康价值的宝石/硬币。。
healthValue = player.maxHealth / 4

# 该函数在随机地点产生一个物品/单位。
def spawnRandomPlaced(type):
    x = game.randomInteger(12, 68)
    y = game.randomInteger(12, 56)
    game.spawnXY(type, x, y)

# 辅助变量，goal和UI。
itemInterval = 2
itemSpawnTime = 0
game.collected = 0
ui.track(game, "time")
ui.track(game, "collected")
ui.track(player, "health")
game.addCollectGoal(10)
game.addSurviveGoal()

# 来，我们让食人魔狂暴。
def onSpawn(event):
    unit = event.target
    unit.behavior = "AttacksNearest"

game.setActionFor("munchkin", "spawn", onSpawn)

# 这定义了收集不同物品的结果。
def onCollect(event):
    # event.target 包含是收集者。
    collector = event.target
    # event.other包含收集的物品。
    item = event.other
    # 通过1 增加game.collected。
    game.collected += 1
    # 如果物品的类型是"gold-coin"：
    if item.type=="gold-coin" :
        # 通过healthValue增加collector.health ：
        collector.health += healthValue
    # 如果商品的类型是"gem"：
    if item.type=="gem" :
        # 通过healthValue降低收集者的生命值：
        collector.health -= healthValue

# 在"collect"事件中为玩家分配onCollect处理程序。
player.on("collect", onCollect)

def checkSpawnTimer():
    if game.time >= itemSpawnTime:
        spawnRandomPlaced("gem")
        spawnRandomPlaced("gold-coin")
        spawnRandomPlaced("munchkin")
        itemSpawnTime += itemInterval

while True:
    checkSpawnTimer()

```
