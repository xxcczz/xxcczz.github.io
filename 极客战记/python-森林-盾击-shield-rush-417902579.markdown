---
layout: default
title: shield-rush
---
## 盾击
```

# 用shield盾牌和cleave顺势斩在两波进攻中活下来
# 如果cleave顺势斩没有准备好，就用你的shield盾牌技能。
# 你将会需要至少142健康值来保证活下来

while True:
    enemy = hero.findNearestEnemy()
    if enemy:
        if hero.isReady("cleave"):
            hero.cleave(enemy)
        else:
            hero.shield()

```
