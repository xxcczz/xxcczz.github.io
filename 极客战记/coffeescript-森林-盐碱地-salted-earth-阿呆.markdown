---
layout: default
title: salted-earth
---
## 盐碱地
```

# 食人族正在攻击附近的一个定居点！
# 小心，食人族在地上放了毒药。
# 收集硬币并击败食人魔，但避免树枝和毒药！

while true        
    enemy = hero.findNearestEnemy()
    if enemy.type == "munchkin" or enemy.type == "thrower"
        hero.attack(enemy)
    item = hero.findNearestItem()
    # 检查物品类型，确保英雄不会捡起毒药！
    # Look for types: 'gem' and 'coin'
    if item.type == "gem" or item.type == "coin"
        hero.moveXY(item.pos.x,item.pos.y)

```
