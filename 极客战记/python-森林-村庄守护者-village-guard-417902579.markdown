---
layout: default
title: village-guard
---
## 村庄守护者
```

# 在村口巡逻。
# 如果发现敌人，就攻击它。
while True:
    hero.moveXY(35, 34)
    left = hero.findNearestEnemy()
    if left:
        hero.attack(left)
        hero.attack(left)
    # 现在移动到右侧入口。
    hero.moveXY(59, 32)
    # 找到正确的敌人。
    # 如果有正确的敌人，使用if来攻击。
    left = hero.findNearestEnemy()
    if left:
        hero.attack(left)
        hero.attack(left)

```
