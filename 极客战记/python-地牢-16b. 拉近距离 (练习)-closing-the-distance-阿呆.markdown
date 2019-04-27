---
layout: default
title: closing-the-distance
---
## 16b. 拉近距离 (练习)
```

while True:
    hero.moveRight()
    enemy = hero.findNearestEnemy()
    if enemy:
        hero.attack(enemy)

hero.moveRight()

# 通过上一个关卡，你应该能认识这个。
enemy1 = hero.findNearestEnemy()
# 现在，攻击enemy1
hero.attack(enemy1)
hero.attack(enemy1)
hero.moveRight()

# 通过上一个关卡，你应该能认识这个。
enemy1 = hero.findNearestEnemy()
# 现在，攻击enemy1
hero.attack(enemy1)
hero.moveRight()

```
