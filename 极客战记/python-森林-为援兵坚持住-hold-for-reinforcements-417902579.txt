---
layout: default
title: hold-for-reinforcements
---
## 为援兵坚持住
```

# 食人魔正在爬悬崖
# 为集结民兵组织保护足够长时间的农民。
while True:
    flag = hero.findFlag()
    enemy = hero.findNearestEnemy()
    if flag:
        # 捡旗子
        hero.pickUpFlag(flag)
    
    elif enemy:
        # 否则，攻击！
        # 使用旗子移动到指定位置，如果 “cleave” 技能冷却完毕，就使用 “cleave” 技能。
        gj()
def gj():
    enemy = hero.findNearestEnemy()
    if enemy:
        if hero.isReady("cleave"):
            hero.cleave(enemy)
        else:
            hero.attack(enemy)

```
