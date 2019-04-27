---
layout: default
title: bonemender
---
## 修骨者
```

# 拯救盟友的士兵来突围
while True:
    if hero.canCast("regen"):
        bernardDistance = hero.distanceTo("Bernard")
        if bernardDistance < 10:
            # Bernard需要治疗！
            hero.cast("regen", "Bernard")
        # 使用『if』和『distanceTo』来治疗 "Chandra"
        # 如果她小于10米的距离。
        bernardDistance = hero.distanceTo("Chandra")
        if bernardDistance < 10:
            hero.cast("regen", "Chandra")
    else:
        # 如果你没有执行 regen，使用 if 和 distanceTo 
        # 来攻击那些小于一定距离的敌人 hero.attackRange.
        enemy = hero.findNearestEnemy()
        if enemy and hero.distanceTo(enemy)<hero.attackRange:
            hero.attack(enemy)
        pass

```
