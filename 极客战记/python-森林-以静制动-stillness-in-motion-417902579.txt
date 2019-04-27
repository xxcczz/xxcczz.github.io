---
layout: default
title: stillness-in-motion
---
## 以静制动
```

# 你可以将一个if语句放到另一个if语句当中。
# 你必须注意这些if语句是如何互相影响的。
# 请确保代码缩进正确！
# 从外层if/else结构开始会有帮助
# 使用注释为内层if/else占位预留空间：

while True:
    enemy = hero.findNearestEnemy()
    # 如果有敌人出现，那么就...
    if enemy:
        # 使用distanceTo创建一个距离变量
        
        # 如果敌人与你的距离小于5米，那么就攻击它
        if hero.distanceTo(enemy)<5:
            hero.attack(enemy)
        # 否则（这名敌人还离得很远），就使用shield
        else:
            hero.shield()
        pass
    # 否则（没有敌人）...
    else:
        # …那么，回到X位置。
        hero.moveXY(40, 34)

```
