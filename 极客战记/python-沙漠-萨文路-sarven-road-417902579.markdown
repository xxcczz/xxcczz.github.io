---
layout: default
title: sarven-road
---
## 萨文路
```

# 到达绿洲。小心新的敌人：食人魔侦察兵！
# 通过添加你当前的X位置和Y位置以向上向右走

while True:
    # If there's an enemy, attack.
    enemy = hero.findNearestEnemy()
    if enemy:
        hero.attack(enemy)
    else:
        hero.moveXY(hero.pos.x+1, hero.pos.y+1)
    # Else, keep moving up and to the right. 
    
    pass

```
