---
layout: default
title: tactical-timing
---
## 战术时机
```

# 帮助前线。
# 如果任何人溜，放回一个旗子。

        
while True:
    enemy = hero.findNearestEnemy()
    flag = hero.findFlag("green")
    if flag:
        hero.pickUpFlag(flag)
    if enemy:
        hero.attack(enemy)

```
