---
layout: default
title: ring-bearer
---
## 戒指运送人
```

# 你必须护送一个强大的魔戒回城研究。
# 我们的目标是要逃脱，不是打仗。有更多食人魔潜伏在周围的山脉！
# 让士兵把农民围在里面！
# 我们给你两个函数来帮助你：

# 
# 第一个参数'士兵'应该是你的士兵阵列。
# 
def findSoldierOffset(soldiers, i):
    soldier = soldiers[i]
    angle = i * 360 / len(soldiers)
    return radialToCartesian(5, angle)

# 这个函数做数学运算来确定一个战士应该站的位置。
def radialToCartesian(radius, degrees):
    radians = Math.PI / 180 * degrees
    xOffset = radius * Math.cos(radians)
    yOffset = radius * Math.sin(radians)
    return {"x": xOffset, "y": yOffset}

peasant = hero.findByType("peasant")[0]
soldiers = hero.findByType("soldier")
# Use findByType to get an array of your soldiers.
while True:
    # 
    for j in range(len(soldiers)):
        soldier = soldiers[j]
        # 找到士兵的位置。
        a = {"x": 41, "y": 40}
        # Add the offset.x and offset.y to the peasant's pos.x and pos.y.
        a.x=peasant.pos.x+findSoldierOffset(soldiers, j).x
        a.y=peasant.pos.y+findSoldierOffset(soldiers, j).y
        # 命令士兵移动到新位置。
        hero.command(soldier, "move", a)
    # 英雄应跟上农民！
    hero.move({"x": hero.pos.x + 0.2, "y": hero.pos.y})

```
