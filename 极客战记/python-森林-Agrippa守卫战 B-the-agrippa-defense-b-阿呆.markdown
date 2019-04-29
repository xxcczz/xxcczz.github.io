---
layout: default
title: the-agrippa-defense-b
---
## Agrippa守卫战 B
```

while True:
    enemy = hero.findNearestEnemy()
    if enemy:
        pass  # 用你自己的代码替换这行
        # 用 distanceTo 获取与敌人的距离。
        
        # 如果距离小于5米...
        if hero.distanceTo(enemy)<5:
            # ...如果 “cleave”技能准备好了，就用“cleave”干掉他们！
            if hero.isReady("cleave"):
                hero.cleave(enemy)
            # ...否则，仅仅进行普通攻击。
            else:
                hero.attack(enemy)

```
