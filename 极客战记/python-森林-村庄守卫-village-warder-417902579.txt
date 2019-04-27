---
layout: default
title: village-warder
---
## 村庄守卫
```

# 这个函数攻击最近的敌人。
def findAndAttackEnemy():
    enemy = hero.findNearestEnemy()
    if enemy:
        hero.attack(enemy)

# 定义一个函数来劈斩敌人（只在劈斩就绪时）
def findAndCleaveEnemy():
    # 找到最近的敌人：
    enemy = hero.findNearestEnemy()
    # 如果敌人存在：
    if enemy:
        # 如果"cleave"就绪了:
        if hero.isReady("cleave"):
            # 是时候使用劈斩了！
            hero.cleave(enemy)
    pass

# 在主循环中，巡逻、劈斩和攻击。
while True:
    # 移动到巡逻点，劈斩并攻击。
    hero.moveXY(35, 34)
    findAndCleaveEnemy()
    findAndAttackEnemy()
    
    # 移动到另一点：
    hero.moveXY(60, 31)
    # 使用findAndCleaveEnemy函数：
    findAndCleaveEnemy()
    # 使用findAndAttackEnemy函数：
    findAndAttackEnemy()

```
