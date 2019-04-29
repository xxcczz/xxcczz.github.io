---
layout: default
title: attack-wisely
---
## 明智的攻击！
```

hero.attack("Door A")
hero.moveUp(2)
enemy = hero.findNearestEnemy()
while enemy.health>0:
    hero.attack(enemy)
hero.moveDown(3)
hero.moveRight(2)
hero.moveUp()
hero.attack("Door B")
hero.moveUp(2)
enemy = hero.findNearestEnemy()
while enemy.health>0:
    hero.attack(enemy)
hero.moveDown(2)
hero.moveRight(2)
hero.attack("Door C")
hero.moveUp(2)
enemy = hero.findNearestEnemy()
while enemy.health>0:
    hero.attack(enemy)
hero.moveDown(2)
hero.moveRight(2)
hero.moveUp(3)
enemy = hero.findNearestEnemy()
while enemy.health>0:
    hero.attack(enemy)
enemy = hero.findNearestEnemy()
while enemy.health>0:
    hero.attack(enemy)
hero.moveRight()
hero.moveDown(4)
hero.moveLeft(3)
hero.moveDown(1)
hero.moveLeft(2)

```
