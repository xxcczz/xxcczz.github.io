---
layout: default
title: swift-dagger
---
## 敏捷的匕首
```

# 长距离用你的弓，短距离用匕首

while True:
    enemy = hero.findNearestEnemy()
    if enemy:
        distance = hero.distanceTo(enemy)
        if distance < hero.throwRange:
            # 向敌人扔你的匕首
            hero.throw(enemy)
        else:
            # 用你的弓攻击敌人
            hero.attack(enemy)

```
