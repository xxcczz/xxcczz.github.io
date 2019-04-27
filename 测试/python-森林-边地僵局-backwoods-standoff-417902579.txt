---
layout: default
title: backwoods-standoff
---
## 边地僵局
```

#循环
while True:
    #找敌人
    enemy = hero.findNearestEnemy()
    #如果有敌人
    if enemy:
        #如果技能劈斩准备好了
        if hero.isReady("cleave"):
            #劈斩
            hero.cleave(enemy)
        # 否则
        else:
            #普通攻击
            hero.attack(enemy)

```
