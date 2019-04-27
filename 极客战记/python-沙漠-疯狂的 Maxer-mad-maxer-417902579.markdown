---
layout: default
title: mad-maxer
---
## 疯狂的 Maxer
```

# 优先杀掉最远的敌人。

while True:
    farthest = None
    maxDistance = 0
    enemyIndex = 0
    enemies = hero.findEnemies()
    
    # 查看全部敌人，找出最远的那个。
    while enemyIndex < len(enemies):
        target = enemies[enemyIndex]
        enemyIndex += 1
            # 是不是存在远得看不到的敌人？
        distance = hero.distanceTo(target)
        if distance > maxDistance:
            maxDistance = distance
            farthest = target
    if farthest:
        # 干掉最远的敌人！
        # 如果敌人血量大于0就保持攻击。
        while not si(farthest):
            hero.attack(farthest)
def si(enemy):
    if enemy.health <= 0:
        return True
    else:
        return False

```
