---
layout: default
title: mind-the-trap
---
## 小心陷阱
```

# 如果你试图攻击一个远处的敌人，你的英雄会忽略掉所有的旗子而朝它冲过去。
# 你需要确保你只攻击靠近自己的敌人！

while True:
    flag = hero.findFlag()
    enemy = hero.findNearestEnemy()
    
    if flag:
        # 去拔旗子。
        hero.pickUpFlag(flag)
        hero.say("我应该去把旗子拔起来。")
    elif enemy:
        # 仅当敌人的距离小于10米时才攻击。
        if hero.distanceTo(enemy)<10:
            if hero.isReady("cleave"):
                hero.cleave(enemy)
            else:
                hero.attack(enemy)

```
