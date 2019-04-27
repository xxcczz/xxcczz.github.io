---
layout: default
title: wandering-souls
---
## 游魂
```

# 攻击骷髅捡走宝石

while True:
    enemies = hero.findEnemies()
    enemyIndex = 0
    while enemyIndex < len(enemies):
        enemy = enemies[enemyIndex]
        # Attack while enemy has health.
        while enemy.health > 0:
            hero.attack(enemy)
        enemyIndex += 1
    items = hero.findItems()
    itemIndex = 0
    # 遍历所有的物品。
    while itemIndex < len(items):
        item = items[itemIndex]
        # While the distance greater than 2:        
        while hero.distanceTo(item)>2:
            # 试着拿到物品
            yidong(item)
        # 别忘了让itemIndex变大 （itemIndex+=1）或（itemIndex=itemIndex+1）
        itemIndex += 1
def yidong(mb):
    hero.moveXY(mb.pos.x, mb.pos.y)

```
