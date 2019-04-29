---
layout: default
title: operation-killdeer
---
## 操作 “杀鹿”
```

# Lure the ogres into a trap. These ogres are careful.
# They will only follow if the hero is injured.

# This function checks the hero's health 
# 并返回一个布尔型(Boolean)的值。
def shouldRun():
    if hero.health < hero.maxHealth / 2:
        return True
    else:
        return False

while True:
    # Move to the X only if shouldRun() returns True
    if shouldRun():
        hero.moveXY(75, 37)
    # Else, attack!
    else:
        gongji()
def gongji():
    enemy = hero.findNearestEnemy()
    if enemy:
        hero.attack(enemy)

```
