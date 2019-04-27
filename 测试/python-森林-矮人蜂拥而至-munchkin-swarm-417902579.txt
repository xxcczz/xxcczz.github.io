---
layout: default
title: munchkin-swarm
---
## 矮人蜂拥而至
```

while True:
    # 检查与最近敌人的距离
    enemy = hero.findNearestEnemy()
    # 如果它接近到10m以内，对它使用cleave！
    if enemy and hero.distanceTo(enemy)<10:
        hero.cleave(enemy)
    # 否则，攻击某名字的宝箱（“Chest”）
    else:
        hero.attack("Chest")
    pass

```
