---
layout: default
title: tomb-ghost
---
## 墓地阴魂
```

# 唯一的出口被食人魔堵住了。
# 躲着骷髅怪，并一个个击败食人魔

# 这个函数需要攻击敌人并隐藏。
def hitOrHide(target):
    # 如果'目标'存在：
    if target:
        hero.attack(target)
        # 攻击'目标'
        hero.moveXY(32, 17)
        # 然后移动到红色标记。
        
    pass

while True:
    enemy = hero.findNearestEnemy()
    hitOrHide(enemy)

```
