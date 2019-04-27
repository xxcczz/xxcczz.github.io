---
layout: default
title: village-rover
---
## 乡村漫游者
```

# 这定义了findAndAttackEnemy函数
def findAndAttackEnemy():
    enemy = hero.findNearestEnemy()
    if enemy:
        hero.attack(enemy)

# 这段代码不是函数的一部分。
while True:
    # 现在你可以使用findAndAttackEnemy在村子里巡逻
    hero.moveXY(35, 34)
    findAndAttackEnemy()
    
    # 现在移动到右侧入口。
    hero.moveXY(59, 31)
    # 使用findAndAttackEnemy
    findAndAttackEnemy()

```
