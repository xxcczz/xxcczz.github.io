---
layout: default
title: dangerous-tracks
---
## 危险的路线
```

#Ogres必须被击败
#人类必须生存
#通往村庄的入口很多。
#保护村庄和我的所有入口
#在食人魔猎人队到达前你有80秒。
#使用for-loop来节省时间并使代码更清晰。.
# 用灭火器保护村庄。
#在四个方向上挖掘所有的段落。
#食人魔攻击前80秒。

# 在步长= 24的情况下，从x = 40到x = 112的y = 114行建立陷阱。
def buildNorthLine():
    for x in range(40, 113, 24):
        hero.buildXY("fire-trap", x, 114)

# 在y = 110到y = 38的行x = 140上建立陷阱，步长= 18。
def buildEastLine():
    # 完成此功能：
    for y in range(110, 37, -18):
        hero.buildXY("fire-trap", 140, y)
    pass

# 从x = 132到x = 32，步长= 20，在y = 22行建立陷阱。
def buildSouthLine():
    # 完成此功能：
    for x in range(132, 31, -20):
        hero.buildXY("fire-trap", x, 22)
    pass

# 在y = 28到x = 20的行上建立陷阱，步长= 16。x=20 from y=28 to y=108 with step=16.
def buildWestLine():
    # 完成此功能：
    for y in range(28, 109, 16):
        hero.buildXY("fire-trap", 20, y)
    pass

buildNorthLine()
buildEastLine()
buildSouthLine()
buildWestLine()
hero.moveXY(40, 94)

```
