---
layout: default
title: leave-it-to-cleaver
---
## 交给屠夫
```

# 这里展示了如何定义一个叫作cleaveWhenClose的函数
# 函数定义了一个参数，名为target
def cleaveWhenClose(target):
    if hero.distanceTo(target) < 5:
        pass
        # 将你的攻击代码放到这里。
        # 如果cleave准备就绪，那就劈斩目标
        if hero.isReady("cleave"):
            hero.cleave(target)
        # 否则，使用attack攻击目标！
        else:
            hero.attack(target)

# 这段代码不是函数的一部分。
while True:
    enemy = hero.findNearestEnemy()
    if enemy:
        # 注意在cleaveWhenClose内部，我们用target指向敌人。
        cleaveWhenClose(enemy)

```
