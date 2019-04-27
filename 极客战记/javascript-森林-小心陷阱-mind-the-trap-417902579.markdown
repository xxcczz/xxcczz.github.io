---
layout: default
title: mind-the-trap
---
## 小心陷阱
```

// 如果你试图攻击一个远处的敌人，你的英雄会忽略掉所有的旗子而朝它冲过去。
// 你需要确保你只攻击靠近自己的敌人！
while (true) {
    var flag = hero.findFlag();
    var enemy = hero.findNearestEnemy();
    if (flag) {
        // 去拔旗子。
        hero.pickUpFlag(flag);
    } else if (enemy) {
        // 仅当敌人的距离小于10米时才攻击。
        var distance = hero.distanceTo(enemy);
        if (distance < 10) {
            var ready = hero.isReady("cleave");
            if (ready) {
                hero.cleave(enemy);
            } else {
                hero.attack(enemy);
            }
        }
    }
}

```
