---
layout: default
title: elseweyr
---
## Else之战
```

# 劈斩正在10秒冷却中。
# 使用 else 语句在恢复时防守。

while True:
    enemy = hero.findNearestEnemy()
    if hero.isReady("cleave"):
        hero.cleave()
    # 写个 else: 当 “cleave” 没有准备好时去做点什么。
    else:
        # 确保攻击了敌人：
        hero.attack(enemy)

```
