---
layout: default
title: rational-defense
---
## 理性防御
```

#保护农民
#怪物会从正面攻击和后面。在正确的顺序建造防御设施来保护农民从森林的攻击
# 保护农民。

#让农民远离树林。
def hideUnits(units):
    for i in range(len(units)):
        unit = units[i]
        hero.command(unit, "move", {'x': 34, 'y': 10 + i * 12})

#农民知道建立陷阱的顺序。
peasants = hero.findFriends()
buildOrder = peasants[0].buildOrder
hero.say(buildOrder)
separator = ","
# 用逗号分割buildOrder（“，”）
#并将结果保存到变量“types”中：
types = buildOrder.split(",")
# 农民的数量与种类相同。
for index in range(len(peasants)):
    peasant = peasants[index]
    x = 16
    y = 10 + index * 12
    # 通过类型数组中的索引获取buildType：
    buildType=types[index]
    #命令农民在x和y处构建XTY buildType：
    hero.command(peasant, "buildXY", buildType, x, y)

#在食人魔攻击时监视敌人并移动农民。
while True:
    enemy = hero.findNearestEnemy()
    if enemy:
        hideUnits(peasants)
        break

#和食人魔战斗：
while True:    
    enemy = hero.findNearestEnemy()
    if enemy:
        hero.attack(enemy)

```
