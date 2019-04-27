---
layout: default
title: distraction-maneuver
---
## 牵引策略
```

# Protect the peasants!

# This function find the furthest one from units.
def findFurthest(units):
    furthestUnit = None
    maxDistance = 0
    unitIndex = 0
    while unitIndex < len(units):
        currentUnit = units[unitIndex]
        # Find the distance to currentUnit:
        distance1 = hero.distanceTo(currentUnit)
        # If that distance greater than maxDistance:
        if distance1>maxDistance:
            # Reassign furthestUnit and maxDistance:
            maxDistance=distance1
            furthestUnit=currentUnit
        unitIndex += 1
    return furthestUnit

# It's like findNearestEnemy but vice versus.
def findFurthestEnemy():
    enemies = hero.findEnemies()
    furthestEnemy = findFurthest(enemies)
    # Return furthestEnemy:
    return furthestEnemy

# The function makes the hero attack without distractions.
def attackWhileAlive(target):
    # Attack target while it's health > 0:
    while target.health>0:
        hero.attack(target)
    pass

while True:
    # To protect peasants, hunt for furthest ogres.
    furthestOgre = findFurthestEnemy()
    if furthestOgre:
        attackWhileAlive(furthestOgre)

```
