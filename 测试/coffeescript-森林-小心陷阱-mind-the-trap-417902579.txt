---
layout: default
title: mind-the-trap
---
## 小心陷阱
```

# 如果你试图攻击一个远处的敌人，你的英雄会忽略掉所有的旗子而朝它冲过去。
# 你需要确保你只攻击靠近自己的敌人！

loop
    flag = @findFlag()
    enemy = @findNearestEnemy()
    
    if flag
        # 去拔旗子。
        @pickUpFlag(flag)
        @say "我应该去把旗子拔起来。"
    else if enemy
        # 仅当敌人的距离小于10米时才攻击。
        distance = @distanceTo(enemy)
        if distance<10
            ready = hero.isReady "cleave"
            if ready
                @cleave enemy
            else
                @attack enemy

```
