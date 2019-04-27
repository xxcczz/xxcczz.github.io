---
layout: default
title: sarven-shepherd
---
## Sarven 牧羊人
```

# 使用 while 循环来对付食人魔。
while True:
    enemies = hero.findEnemies()
    enemyIndex = 0
    # 将攻击逻辑放到 while 循环里来攻击所有的敌人。
    # Find the array's length with:  len(enemies)
    while enemyIndex<len(enemies):
        enemy = enemies[enemyIndex]
        # "!=" 意思是 "不等于"
        if enemy.type != "sand-yak":
            # 当敌人的健康值大于0，攻击它！
            while enemy.health>0:
                hero.attack(enemy)
        enemyIndex=enemyIndex+1
        # 在两波敌人之间，移动回中央。
    hero.moveXY(40, 33)

while True:
    enemies = hero.findEnemies()
    for enemy in enemies:
        if enemy.type != "sand-yak":
            while enemy.health>0:
                hero.attack(enemy)
        hero.moveXY(44, 32)

无代码

while True:
    hero.shield()

```
