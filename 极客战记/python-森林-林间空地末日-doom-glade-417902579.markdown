---
layout: default
title: doom-glade
---
## 林间空地末日
```

# 一波食人魔靠近，使用旗子赢得战役！
while True:
    flag = hero.findFlag("green")
    enemy = hero.findNearestEnemy()
    if flag:
        hero.pickUpFlag(flag)
    if enemy:
        if hero.isReady("cleave"):
            hero.cleave(enemy)
        else:
            hero.attack(enemy)

```
