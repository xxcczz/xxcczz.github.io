---
layout: default
title: underground-business
---
## 地下商业
```

# Accumulate 300 gold and escape from the dungeon.

def onSpawn(event):
    # Send the pet to walk around the dungeon:
    pet.moveXY(22, 58)
    pet.moveXY(69, 56)
    pet.moveXY(71, 11)
    pet.moveXY(21, 11)
    pet.moveXY(21, 35)
    # Don't forget to return it to the hero:
    pet.moveXY(hero.pos.x, hero.pos.y)
    pass


pet.on("spawn", onSpawn)

while True:
    # Guard peasants:
    enemy = hero.findNearestEnemy()
    if enemy:
        hero.attack(enemy)
    # When you have 300+ gold move to the red mark:
    if hero.gold>300:
        hero.moveXY(50, 34)
    pass

```
