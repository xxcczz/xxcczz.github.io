---
layout: default
title: village-champion
---
## 村庄守护神
```

# 矮人来袭！保护镇子！

# 定义你自己的函数来对抗敌人！
def cleaveOrAttack():
    # 在函数中找到敌人，然后劈斩或是攻击它。
    enemy = hero.findNearestEnemy()
    if enemy:
        if hero.isReady("cleave"):
            hero.cleave(enemy)
        else:
            hero.attack(enemy)
    pass

# 在巡逻点之间移动并调用函数。
while True:
    hero.moveXY(35, 34)
    # 使用上面定义的cleaveOrAttack函数。
    cleaveOrAttack()
    hero.moveXY(47, 27)
    # 再次调用函数。
    cleaveOrAttack()
    hero.moveXY(60, 31)
    # 再次调用函数。
    cleaveOrAttack()

```
