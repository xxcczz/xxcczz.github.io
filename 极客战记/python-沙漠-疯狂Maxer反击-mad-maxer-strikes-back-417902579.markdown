---
layout: default
title: mad-maxer-strikes-back
---
## 疯狂Maxer反击
```

# 小一点的食人魔会造成更多的伤害！
# 优先攻击血少的敌人
while True:
    weakest = None
    leastHealth = 99999
    enemyIndex = 0
    enemies = hero.findEnemies()
    
    # 循环检查所有敌人。
    for enemy in enemies:
        # 如果当前对象的血量更少
        if enemy.health<leastHealth:
            # 标为最弱的，更新 leastHealth 变量
            leastHealth=enemy.health
            weakest=enemy
    if weakest:
        # 攻击最弱的食人魔。
        hero.attack(weakest)
        pass

```
