---
layout: default
title: unfair-support
---
## 不公平的支持
```

# 偷偷穿过森林，伏击萨满。
# 听从指挥官Craig 小心接近中的敌人。

# 放置旗子后，按提交。
while True:
    flag = hero.findFlag()
    enemy = hero.findNearestEnemy()
    if flag:
        # 捡起旗子。
        hero.pickUpFlag(flag)
        pass
    elif enemy:
        # 攻击视野内的敌人。
        hero.attack(enemy)
        pass

```
