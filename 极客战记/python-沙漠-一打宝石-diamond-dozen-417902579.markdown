---
layout: default
title: diamond-dozen
---
## 一打宝石
```

# 打败前来劫掠的食人魔，让他们把金币交出来！

def findMostHealth(enemies):
    target = None
    targetHealth = 0
    enemyIndex = 0
    while enemyIndex < len(enemies):
        enemy = enemies[enemyIndex]
        if enemy.health > targetHealth:
            target = enemy
            targetHealth = enemy.health
        enemyIndex += 1
    return target

def valueOverDistance(item):
    return item.value / hero.distanceTo(item)

# 返回有最高 valueOverDistance(item) 的物品。
def findBestItem(items):
    bestItem = None
    bestValue = 0
    itemsIndex = 0
    
    # 循环于 items 数组内。
    # 发现这个物品的最高 valueOverDistance()
    while itemsIndex < len(items):
        item = items[itemsIndex]
        if valueOverDistance(item) > bestValue:
            bestItem = item
            bestValue = valueOverDistance(item)
        itemsIndex += 1
    return bestItem
    

while True:
    enemies = hero.findEnemies()
    enemy = findMostHealth(enemies)
    if enemy and enemy.health > 15:
        while enemy.health > 0:
            hero.attack(enemy)
    else:
        coins = hero.findItems()
        coin = None
        coin = findBestItem(coins)
        if coin:
            hero.moveXY(coin.pos.x, coin.pos.y)

def jianjinbi():
    items = hero.findItems()
    a=None
    maxjz=0
    for item in items:
        jz=item.value/hero.distanceTo(item)
        if jz>maxjz:
            maxjz=jz
            a=item
    if a:
        hero.move(a.pos)
while True:
    jianjinbi()

```
