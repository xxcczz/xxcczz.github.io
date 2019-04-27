---
layout: default
title: air-bridge
---
## 空中桥梁
```

# Help peasants to escape.

def onSpawn(event):
    # We need to save three peasants.
    remainingPeasants = 3
    while remainingPeasants > 0:
        # Take a good position.
        pet.moveXY(40, 55)
        peasant = pet.findNearestByType("peasant")
        if peasant:
            # Carry the peasant to the center passage.
            pet.carryUnit(peasant, 40, 34)
            remainingPeasants -= 1
    # Next find a weak ogre and carry it to the fire traps:
    for enemy in hero.findEnemies():
        if enemy.health<hero.health/10:
            pet.carryUnit(enemy, 40, 19)
            break

pet.on("spawn", onSpawn)
gj()
# Fight!
def gj():
    enemy = hero.findNearestEnemy()
    if enemy:
        hero.attack(enemy)

```
