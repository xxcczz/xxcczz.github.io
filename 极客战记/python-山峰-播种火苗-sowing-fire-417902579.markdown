---
layout: default
title: sowing-fire
---
## 播种火苗
```

# 目标：建造三排九个 fire-traps.

# 返回"retreat", "attack", "start-next-trap-column", or "build-next-trap-in-column"
def chooseStrategy():
    enemies = hero.findEnemies()
    
    # 如果有巨大的食人魔力量，则返回 the "retreat" strategy.
    if len(enemies) > 20:
        return "retreat"
    
    # 如果有一些食人魔，则返回 "attack" strategy.
    if len(enemies) < 20 and len(enemies)!=0:
        return "attack"
    # 使用x％9为0来查看x是否可以被9整除。
    # 使用len（self.built）来查看你已经构建了多少陷阱。
    # 如果您完成了9个陷阱列，请返回“start-next-trap-column”
    if len(hero.built)%trapsInColumn==0:
        return "start-next-trap-column"
    # 否则，返回“build-next-trap-in-column”
    else:
        return "build-next-trap-in-column"

trapsInColumn = 9
startX = 40
columnX = startX

#在正确的地方在列中构建下一个陷阱。
def buildNextTrapInColumn(columnX,numTraps):
    # 更改newY以使用％环绕并仅构建每列trapsInColumn（9）陷阱
    newY = 7 * (numTraps%9) + 10 # ∆ Change this to use % 9!
    if hero.pos.y < newY:
        hero.move({"x": columnX - 5, "y": newY})
    else:
        buildTrap(columnX,newY)

#开始一个新的陷阱列。
def startNextTrapColumn(columnX, numTraps):
    newX = startX - (Math.floor(numTraps / trapsInColumn) * 6)
    if hero.pos.y > 10:
        hero.move({"x": newX - 5, "y": 10})
        return columnX
    else:
        buildTrap(newX,10)
        return newX

def buildTrap(x, y):
    hero.buildXY("fire-trap", x, y)

def commandAttack():    
    # 让你的格里芬车手抵挡攻击者。    
    friends = hero.findFriends()
    for j in range(len(friends)):
        friend = friends[j]
        enemy = friend.findNearestEnemy()
        if enemy:
            hero.command(friend, "attack", enemy)
    
def commandRetreat():    
    hero.say("Retreat!")    
    # 你和你的格里芬车手在陷阱后退到安全地点。    
    friends = hero.findFriends()    
    for j in range(len(friends)):    
        friend = friends[j]    
        hero.command(friend, "move", {"x": 5, "y": 41})    
    hero.moveXY(5, 41)    
    
    
    
while True:    
    strategy = chooseStrategy()    
    if strategy == "attack":    
        commandAttack()    
    elif strategy == "build-next-trap-in-column":    
        buildNextTrapInColumn(columnX, len(hero.built))    
    elif strategy == "start-next-trap-column":    
        columnX = startNextTrapColumn(columnX, len(hero.built))    
    elif strategy == "retreat":    
        commandRetreat()    

```
