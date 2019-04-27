---
layout: default
title: borrowed-sword
---
## 借刀
```

# 你的英雄不需要在本关参与战斗。
# 命令你的弓箭手集中在火攻敌人。
#攻击血最多的敌人
def findMostDangerous(enemies):
    mostDangerous = None
    mostHealth = 0
    for i in range(len(enemies)):
        enemy = enemies[i]
        if enemy.health > mostHealth:
            mostDangerous = enemy
            mostHealth = enemy.health
    return mostDangerous
while True:
    friends = hero.findFriends()
    for j in range(len(friends)):
        enemies = hero.findEnemies()
        enemy=findMostDangerous(enemies)
        friend = friends[j]
        hero.command(friend, "attack", enemy)

```
