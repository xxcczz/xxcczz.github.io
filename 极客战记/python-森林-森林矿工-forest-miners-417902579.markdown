---
layout: default
title: forest-miners
---
## 森林矿工
```

# 检查工人们是否能安全通过雷区。

def checkEnemyOrSafe(target):
    # 如果目标（参数）存在：
    if target:
        # 然后攻击目标
        hero.attack(target)
    # 否则：
    else:
        # 使用say()来叫农民。
        hero.say("message")
    pass

while True:
    # 移动到并检查右上的X标记。
    hero.moveXY(64, 54)
    enemy1 = hero.findNearestEnemy()
    checkEnemyOrSafe(enemy1)
    
    # 移动到左下的X标记处。
    hero.moveXY(15, 15)
    # 将findNearestEnemy()的结果存到一个变量中。
    enemy2 = hero.findNearestEnemy();
    # 调用checkEnemyOrSafe，并传递
    # findNearestEnemy的结果作为参数
    checkEnemyOrSafe(enemy2)

```
