---
layout: default
title: hit-and-freeze
---
## 冰冻打击
```

# 你掉进陷阱里了！别动！你会受伤的！
# 这个函数检查敌人是否再攻击范围。
def inAttackRange(enemy):
    distance = hero.distanceTo(enemy)
    # 几乎所有的剑都有3的攻击范围。
    if distance <= 3:
        return True
    else:
        return False
# 只有在触手可及的范围内才能攻击食人魔。
while True:
    # 找到最近的敌人，并将其储存在一个变量中。
    enemy = hero.findNearestEnemy()                     
    # 调用 inAttackRange(enemy)，将 enemy 作为参数
    # 把结果保存于 “canAttack” 变量中
    canAttack=inAttackRange(enemy)                      
    # 如果结果存储在一个攻击中 True, 然后下手！
    if canAttack:                       
        hero.attack(enemy)   

```
