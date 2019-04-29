---
layout: default
title: stranded-in-the-dunes
---
## 滞留在沙丘
```

# Go to the far right edge of the level to find new areas.
# Check the guide for more details.
while True:
    flag = hero.findFlag()
    if flag:
        hero.pickUpFlag(flag)
    else:
        enemy = hero.findNearest(hero.findEnemies())
        if enemy:
            if enemy.type!="sand-yak":
                hero.attack(enemy)

```
