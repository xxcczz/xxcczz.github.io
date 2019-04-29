---
layout: default
title: berserker
---
## 狂战士
```

function onCollide(event) {
    var who = event.target;
    var withWhat = event.other;
    who.say("I collided with " + withWhat.id);
}

def onCollide(event):
    who = event.target
    withWhat = event.other
    who.say("I collided with " + withWhat.id)

# 蘑菇允许玩家摧毁围墙一段时间。

player = game.spawnPlayerXY('captain', 12, 34)
player.maxSpeed = 15
game.addMoveGoalXY(76, 34)
ui.track(game, "time")

# 蘑菇动力的持续时间。
game.powerDuration = 3
# 蘑菇能量到期的时间。
game.powerEndTime = 0

# "mushroom"s 是没有默认效果的收藏品。
game.spawnXY("mushroom", 12, 52)
game.spawnXY("mushroom", 12, 16)
game.spawnXY("mushroom", 36, 16)
game.spawnXY("mushroom", 36, 52)
game.spawnXY("mushroom", 56, 12)
game.spawnXY("mushroom", 56, 56)
game.spawnXY("mushroom", 56, 34)

#  "collect" 事件的事件处理程序。
def onCollect(event):
    unit = event.target
    item = event.other
    if item.type == "mushroom":
        # "scale" 改变了单位的视觉尺寸。
        unit.scale = 2
        game.powerEndTime = game.time + game.powerDuration
        unit.say("ARRRGH!!!")

#  "collide"事件的事件处理程序。
def onCollide(event):
    # 事件拥有者与某事物相撞。
    unit = event.target
    # 单位碰撞的对象。
    collidedObject = event.other
    # 如果它是围墙。
    if collidedObject.type == "fence":
        if unit.scale == 2:
            # 对collidedObject使用 "destroy" 方法。
            collidedObject.destroy()
            pass

# 将onCollide分配给玩家的 "collide"事件。
player.on("collide", onCollide)
# 将onCollect分配给播放器上的 "collect"事件。
player.on("collect", onCollect)

def checkTimers():
    # 如果游戏时间大于game.powerEndTime
    if game.time>game.powerEndTime:
        # If player.scale is equal to 2: 
        if player.scale==2:
            # 将玩家的比例设置为1。
            player.scale=1
    pass

while True:
    checkTimers()

```
