---
layout: default
title: siege-of-stonehold
---
## 围攻Stonehold
```

# 帮助你的朋友击败索科塔派出的手下。
# 你需要更好的装备和策略去赢得战斗。
# 标记可能有用，不过这取决于你——要有创造性哦！
# 在围栏后有位医生。移动到 X 处得到治疗！

while True:
    enemy = hero.findNearestEnemy()
    if enemy:
        if hero.isReady("cleave"):
            hero.cleave(enemy)
        else:
            hero.attack(enemy)

```
