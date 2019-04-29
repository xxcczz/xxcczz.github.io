---
layout: default
title: backwoods-standoff-b
---
## 边地僵局 B
```

# 矮人正在攻击！
# 攻击会有规律的一波波袭来。
# 可以的话，使用劈斩来清理大量敌人。

while True:
    enemy = hero.findNearestEnemy()
    # 使用带有‘isReady’的if语句来检查 “cleave”
    if hero.isReady("cleave"):
        # 劈斩！
        hero.cleave(enemy)
    # 否则，如果 cleave 还没准备好的话：
    else:
        # 攻击最近的食人魔！
        hero.attack(enemy)

```
