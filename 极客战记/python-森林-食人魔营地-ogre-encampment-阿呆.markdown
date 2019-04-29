---
layout: default
title: ogre-encampment
---
## 食人魔营地
```

# 如果有敌人，那么就攻击它
# 否则，攻击宝箱

while True:
    # 使用if/else语句
    enemy = hero.findNearestEnemy()
    if enemy:
        hero.attack(enemy)
    else:
        hero.attack("Chest")

```
