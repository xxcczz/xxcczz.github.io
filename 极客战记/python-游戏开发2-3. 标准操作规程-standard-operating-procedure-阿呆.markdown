---
layout: default
title: standard-operating-procedure
---
## 3. 标准操作规程
```

# 使用event.target，所有单位都可以使用相同的事件处理函数
def sayHello(event):
    unit = event.target
    unit.say("Hi!")

game.setActionFor("soldier", "spawn", sayHello)

# 事件具有诸如event.target之类的属性
# 这使您可以为许多不同的单位使用相同的事件处理程序。
game.addDefeatGoal()
soldier1 = game.spawnXY("soldier", 50, 30)
soldier2 = game.spawnXY("soldier", 50, 35)
soldier3 = game.spawnXY("soldier", 50, 40)
munchkin1 = game.spawnXY("munchkin", 25, 30)
munchkin2 = game.spawnXY("munchkin", 25, 35)
munchkin3 = game.spawnXY("munchkin", 25, 40)

# 这个函数让兽人1攻击它的敌人。
# 使用event.target使这个函数适用于所有单位！
def fightEnemies(event):
    while True:
        # 创建一个单位变量，并将事件对象分配给它
        unit = event.target
        # 现在将下面的行改为使用单元而不是兽人 1。
        enemy = unit.findNearestEnemy() # ∆
        if enemy:
            unit.attack(enemy) # ∆

# 使用game.setActionFor() 将事件处理程序分配给许多单位。
game.setActionFor("munchkin", "spawn", fightEnemies)
game.setActionFor("soldier", "spawn", fightEnemies)

```
