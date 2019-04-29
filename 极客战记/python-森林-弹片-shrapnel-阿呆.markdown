---
layout: default
title: shrapnel
---
## 弹片
```

# 使用炸药干掉食人魔
# 然后用你的弓干掉他们

while True:
    enemy = hero.findNearestEnemy()
    if enemy:
        if hero.isReady("throw"):
            distance = hero.distanceTo(enemy)
            # 如果食人魔距离多于15米的时候，扔炸药炸他
            # 使用 if 来比较距离和15
            if distance>15:
                hero.throw(enemy)
            # 使用 else 来攻击它如果你不能够炸它
            else:
                hero.attack(enemy)
        else:
            hero.attack(enemy)

```
