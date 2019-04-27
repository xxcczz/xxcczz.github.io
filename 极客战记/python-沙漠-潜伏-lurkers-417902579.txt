---
layout: default
title: lurkers
---
## 潜伏
```

# 用findEnemies把敌人存在数组enemies中
# 只攻击萨满巫师，不要攻击牦牛！

enemies = hero.findEnemies()
enemyIndex = 0

# 把这段代码用一个while loop 功能循环遍历所有的敌人
# 当 enemyIndex 小于 enemies 的长度时：
while enemyIndex<len(enemies):
    enemy = enemies[enemyIndex]
    if enemy.type == 'shaman':
        while enemy.health > 0:
            hero.attack(enemy)
    enemyIndex=enemyIndex+1
# Remember to increment enemyIndex

```
