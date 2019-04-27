---
layout: default
title: while-ogres-were-sleeping
---
## 沉睡的食人魔
```

# 敌人正在睡觉。这是破坏的最佳时机！
points = [{"x": 21, "y": 8}, {"x": 33, "y": 8},
    {"x": 45, "y": 8}, {"x": 57, "y": 8}, {"x": 68, "y": 8},
    {"x": 68, "y": 18}, {"x": 68, "y": 28}, 
    {"x": 68, "y": 38}, {"x": 68, "y": 48},
    {"x": 68, "y": 58}, {"x": 56, "y": 58},
    {"x": 44, "y": 58}, {"x": 32, "y": 58}, 
    {"x": 20, "y": 58}, {"x": 10, "y": 60}]

pointIndex = 0;

while pointIndex < len(points):
    point = points[pointIndex];
    hero.moveXY(point["x"], point["y"])
    enemy = hero.findNearestEnemy()
    coin = hero.findNearestItem()
    # 只有当enemy.team是“食人魔”时才会进行攻击
    # 并且敌人的健康不到10
    if enemy.team=="ogres" and enemy.health<10:
        hero.attack(enemy)
    # 如果coin.value小于5，则收集一枚硬币
    #并且它的距离小于7
    if coin.value<5 and hero.distanceTo(coin)<7:
        hero.moveXY(coin.pos.x, coin.pos.y)
    # 只有在敌方健康少于10的情况下才能进行攻击
    # 并且敌人的类型是 "skeleton".
    if enemy.health<10 and enemy.type=="skeleton":
        hero.attack(enemy)
    pointIndex += 1

```
