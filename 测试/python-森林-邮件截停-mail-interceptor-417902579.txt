---
layout: default
title: mail-interceptor
---
## 邮件截停
```

#拦截来自伏击的所有食人魔使者。

函数(敌人):
    # 攻击目标，如果存在并返回标记。
    # 编写函数：
    如果有敌人:
        普通攻击
        移动到坐标(51, 36)
    pass

循环:
    找敌人
    函数(敌人)

#拦截来自伏击的所有食人魔使者。

def ambushAttack(target):
    # 攻击目标，如果存在并返回标记。
    # 编写函数：
    if target:
        hero.attack(target)
        hero.moveXY(51, 36)
    pass

while True:
    ogre = hero.findNearestEnemy()
    ambushAttack(ogre)

```
