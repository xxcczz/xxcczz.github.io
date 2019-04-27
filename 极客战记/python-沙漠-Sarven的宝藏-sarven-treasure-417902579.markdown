---
layout: default
title: sarven-treasure
---
## Sarven的宝藏
```

# 用传输机躲避食人魔收集150个金币
# 如果你赢了，接下来会变得更难，当然也会有更多奖励。
# 如果你输了，需要等待一天再次挑战
# 记得，每一次提交都会获得不同的地图。
x1=5
x2=76
y1=19
y2=49
x3=0
y3=0
while True:
    #如果有敌人,跑到叉叉那
    #enemy = hero.findNearestEnemy()
    enemy = hero.findNearest(hero.findEnemies())
    if enemy and hero.distanceTo(enemy)<20:
        x=hero.pos.x
        y=hero.pos.y
        if abs(x-x1)<(x2-x):
            x3=x1
        else:
            x3=x2
        if abs(y-y1)<(y2-y):
            y3=y1
        else:
            y3=y2
        hero.move({'x': x3, 'y': y3})
    #如果没有敌人在附近,就捡金币
    if enemy and hero.distanceTo(enemy)>15:
        jianjinbi()

def jianjinbi():
    items = hero.findItems()
    a=None
    maxjz=0
    for item in items:
        jz=item.value/hero.distanceTo(item)
        if jz>maxjz:
            maxjz=jz
            a=item
    if a:
        hero.move(a.pos)

```
