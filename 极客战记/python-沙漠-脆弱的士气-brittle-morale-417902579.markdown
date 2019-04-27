---
layout: default
title: brittle-morale
---
## 脆弱的士气
```

# You have one arrow. Make it count!

# 这将返回一个最多生命值的敌人
def findStrongestEnemy(enemies):
    strongest = None
    strongestHealth = 0
    enemyIndex = 0
    # 当 enemyIndex 少于敌人的长度
    while enemyIndex<len(enemies):
        enemy=enemies[enemyIndex]
        # Set an enemy variable to enemies[enemyIndex]
        if enemy.health>strongestHealth:
            strongest=enemy
            strongestHealth=enemy.health
        # 如果 enemy.health 大于 strongestHealth
        
            # 将 strongest 赋值为 enemy
            # Set strongestHealth to enemy.health
            
        # 让 enemyIndex 递增
        enemyIndex=enemyIndex+1
    
    return strongest

enemies = hero.findEnemies()
leader = findStrongestEnemy(enemies)
if leader:
    hero.say(leader)

```
