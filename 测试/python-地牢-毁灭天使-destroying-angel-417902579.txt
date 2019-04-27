---
layout: default
title: destroying-angel
---
## 毁灭天使
```

hero.moveDown()
hero.moveRight()
hero.moveDown()
# 妈妈总对我说，随便吃点你在地牢里找到的蘑菇。
hero.moveDown()
hero.moveDown()
hero.moveRight(3)
# 找到你去地牢守卫者的路。
hero.moveUp()
hero.moveLeft()
hero.moveUp()
hero.moveRight()
hero.moveUp()
hero.moveLeft()
hero.moveDown()
while True:
    enemy = hero.findNearestEnemy()
    if enemy:
        hero.attack(enemy)

```
