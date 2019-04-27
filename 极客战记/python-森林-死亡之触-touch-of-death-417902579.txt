---
layout: default
title: touch-of-death
---
## 死亡之触
```

# 在短距离中释放你的『吸取生命』技能。
# 使用你的法丈在远距离攻击。

while True:
    enemy = hero.findNearestEnemy()
    if enemy:
        distance = hero.distanceTo(enemy)
        if distance < 15:
            # 在敌人里释放『吸取生命』技能。
            hero.cast("drain-life", enemy)
        else:
            # 使用你的盟友攻击敌人。
            hero.attack(enemy)

```
