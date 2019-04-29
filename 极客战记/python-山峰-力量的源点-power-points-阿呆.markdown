---
layout: default
title: power-points
---
## 力量的源点
```

#寻找并击败骨骼通过审判
#你必须击败3个黑暗生物。
#但首先，你需要找到它们。
#召唤一个骨架或一些有用的东西
#你应该停留在权力的一个点上，并说“VEN /
#但是有太多的可能点和
#如果这个咒语在错误的地方说过，那么它可能是坏的（对你而言）。
#只有向导才能看到Power的要点。
#幸运的是，你知道其中的一个，他为你准备了地图。
#地图被表示为数字的二维数组（网格）。
#e是错误的地方。
#正数是功率点。
#遍历网格，找出要点并应对挑战
# 你需要找到并摧毁3个骷髅。
# 骨骼和物品在权力点召唤。
# 移动到一个点并说出咒语：“VENI”。
#要找到所需的点，请使用向导的地图。
#0是不好的一点。正数是好的。

spell = "VENI"
# 点的地图是一个二维的数字数组。
wizard = hero.findNearest(hero.findFriends())
powerMap = wizard.powerMap

# 该函数将网格转换为x-y坐标。
def convert(row, col):
    return {'x': 16 + col * 12, 'y': 16 + row * 12}

# 遍历powerMap以查找正数。
#首先，循环遍历索引的行。
for i in range(len(powerMap)):
    # 每一行都是一个数组。遍历它。
    for j in range(len(powerMap[i])):
        zz()
        # 获取第i行和第j列的值。
        pointValue = powerMap[i][j]
        # 如果这是一个正数：
        if pointValue>0:
            # 使用convert获取XY坐标。
            a=convert(i, j)
            #搬到那里，说“VENI”并做好准备！
            hero.moveXY(a.x, a.y)
            hero.say(spell)
#hero.moveXY(37, 63)
def zz():    
    item = hero.findNearestItem()    
    if item:    
        hero.moveXY(item.pos.x, item.pos.y)    
    enemy = hero.findNearestEnemy()
    if enemy:
        while enemy.health>0:
            hero.attack(enemy)

```
