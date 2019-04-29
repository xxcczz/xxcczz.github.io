---
layout: default
title: gems-or-death
---
## 宝石或者死亡
```

# 在 if 条件下的命令只有在条件为真的时候运行。    
# 修复所有的 if 条件判定来赢得本关    
    
# ==的意思是等于    
if 1 + 1 + 1 == 4:  # ∆ 让条件不成立。    
    hero.moveXY(5, 15)  # 移动到第一个地雷位置    
    
if 2 + 3 == 5:  # ∆ 让条件成立。    
    hero.moveXY(15, 40)  # 移动到第一个宝石的位置。
    
# !=的意思是不等于    
if 2 + 3 != 4:  # ∆ 让条件成立。    
    hero.moveXY(25, 15)  # 移动到第二个宝石的位置
    
# <的意思是比什么小    
if 2 + 0 < 3:  # ∆ 让条件成立。    
    enemy = hero.findNearestEnemy()    
    hero.attack(enemy)    
    
if 2 < 1:  # ∆ 让条件不成立。    
    hero.moveXY(40, 55)
    
if False:  # ∆ 让条件不成立。    
    hero.moveXY(50, 10)
    
if True:  # ∆ 让条件成立。    
    hero.moveXY(55, 25)

```
