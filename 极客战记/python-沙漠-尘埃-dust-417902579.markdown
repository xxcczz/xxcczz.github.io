---
layout: default
title: dust
---
## 尘埃
```

# 使用循环直到你有足够的击杀10个芒奇金人 

attacks = 0
while attacks < 10:
    # 攻击最近的敌人！
    enemy = hero.findNearestEnemy()
    if enemy:
        hero.attack(enemy)
        if enemy.health <= 0:
            attacks += 1
    # Incrementing means to increase by 1.
    # 增加你的攻击统计量。
    

# 当你完成后，撤退到伏击点。
hero.say("I should retreat!") #∆ Don't just stand there blabbering!
hero.moveXY(79, 33)

```
