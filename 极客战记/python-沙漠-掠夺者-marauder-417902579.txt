---
layout: default
title: marauder
---
## 掠夺者
```

# 打几下泡泡人捡走掉出的币

while True:
    coin = hero.findNearestItem()
    # 当存在金币时：
    if coin:
        # 移动到金币处。
        hero.moveXY(coin.pos.x, coin.pos.y)
        # ‘coin’应该是最近的那枚 捡到手以后要另找一枚最近的
        
    enemy = hero.findNearestEnemy()
    if enemy:
        # 如果敌人还会动
        while not si(enemy):
            hero.attack(enemy)
            # 就打它
            
        pass
def si(enemy):
    if enemy.health <= 0:
        return True
    else:
        return False

```
