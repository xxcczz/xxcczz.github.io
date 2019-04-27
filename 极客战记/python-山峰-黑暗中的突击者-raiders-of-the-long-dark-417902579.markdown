---
layout: default
title: raiders-of-the-long-dark
---
## 黑暗中的突击者
```

# 你的目标是保护农民并向右移动。    
# Arryn Stonewall将保卫前线，并指挥士兵。    
# 你需要覆盖后方并命令农民    
    
arryn = hero.findByType("raider")[0]    
peasant = hero.findByType("peasant")[0]    
    
def chooseHeroStrategy():    
    # Return either "fight" or "advance".    
    # 不要战斗时，尽量保持在农民后面5米。    
    #离农民不要超过15米。    
    enemy = hero.findNearestEnemy()
    if enemy and enemy.pos.x<hero.pos.x and hero.distanceTo(enemy)<10:
        return "fight"
    else:
        return "advance"
    
def heroFight():    
    # 阻止食人魔冲过你去找农民！    
    # 提示：如果可以，尽量减慢速度    
    enemy = hero.findNearestEnemy()
    if enemy and enemy.pos.x<hero.pos.x and hero.distanceTo(enemy)<10:
        while enemy.health>0:
            hero.attack(enemy)
    
def heroAdvance():    
    # 留在农民后面    
    hero.moveXY(peasant.pos.x-5, peasant.pos.y)    
    pass    
    
def choosePeasantStrategy():    
    # Return "follow", "build-above", or "build-below"    
    # 提示：使用isPathClear（）来确定走廊的位置    
    if hero.isPathClear(peasant.pos,  {'x': peasant.pos.x, 'y': peasant.pos.y+20}):    
        return "build-above"    
    if hero.isPathClear(peasant.pos,  {'x': peasant.pos.x, 'y': peasant.pos.y-20}):    
        return "build-below"    
    return "follow"    
    pass    
    
def peasantAdvance():    
    #让农民躲在阿林和她的士兵身后。    
    hero.command(peasant, "move", {"x": arryn.pos.x-5, "y": arryn.pos.y})    
    pass    
    
def peasantBuild(x,y):    
    # 命令农民建立一个栅栏。    
    hero.command(peasant, "buildXY", "palisade", x, y)    
    pass    
    
while True:    
    heroStrategy = chooseHeroStrategy()    
    if heroStrategy == "fight":    
        heroFight()    
    elif heroStrategy == "advance":    
        heroAdvance()    
        
    peasantStrategy = choosePeasantStrategy()    
    if peasantStrategy == "build-above":    
        peasantBuild(peasant.pos.x, peasant.pos.y + 5)    
    elif peasantStrategy == "build-below":    
        peasantBuild(peasant.pos.x, peasant.pos.y - 5)    
    elif peasantStrategy == "follow":    
        peasantAdvance()   
    
```
