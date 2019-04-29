---
layout: default
title: agony-of-defeat
---
## 13. 失败的痛苦
```

def onDefeat(event):
    unit = event.target
    unit.say("You got me!")

game.setActionFor("munchkin", "defeat", onDefeat)

function onDefeat(event) {
    var unit = event.target;
    unit.say("You got me!");
}

game.setActionFor("munchkin", "defeat", onDefeat)

# “失败”事件表示一个单位被击败。
player = game.spawnPlayerXY("captain", 40, 35)
game.addSurviveGoal()
game.addCollectGoal(8)
player.attackDamage = 9000
def onSpawn(event):
    while True:
        unit = event.target
        enemy = unit.findNearestEnemy()
        if enemy:
            unit.attack(enemy)

# 当一个单位被击败时，产生一枚金币。
def onDefeat(event):
    unit = event.target
    # 将x设置为unit.pos.x，再加上-5到5之间的数字
    x = unit.pos.x + game.randomInteger(-5, 5)
    # 将y设置为unit.pos.y，再加上一个介于-5和5之间的数字
    y = unit.pos.y + game.randomInteger(-5, 5)
    # 在x，y生成一个“金币”
    game.spawnXY("gold-coin", x,y)

game.setActionFor("munchkin", "spawn", onSpawn)
game.setActionFor("munchkin", "defeat", onDefeat)

spawnTime = 0
while True:
    if game.time > spawnTime:
        x = game.randomInteger(10, 70)
        y = game.randomInteger(10, 60)
        game.spawnXY("munchkin", x, y)
        spawnTime = game.time + game.randomInteger(1,4)

```
