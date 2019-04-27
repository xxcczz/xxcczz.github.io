---
layout: default
title: backwoods-ambush
---
## 边地伏击战
```

hero.moveXY(24, 42)
enemy = hero.findNearestEnemy()
if enemy:
    hero.attack(enemy)
    hero.attack(enemy)

hero.moveXY(27, 60)
enemy = hero.findNearestEnemy()
if enemy:
    # 攻击敌人，如果存在的话！
    hero.attack(enemy)
    pass # pass是一个占位符

hero.moveXY(42, 50)
enemy = hero.findNearestEnemy()
# 使用if语句检查敌人是否存在。
enemy = hero.findNearestEnemy()
    # 攻击敌人，如果存在的话！
if enemy:
    hero.attack(enemy)

hero.moveXY(39, 24)
# 找到最近的敌人：
enemy = hero.findNearestEnemy()
# 检查敌人是否存在：
if enemy:
    # 攻击敌人，如果存在的话！
    hero.attack(enemy)

```
