---
layout: default
title: distracting-dungeon
---
## 分散的地牢
```

# Navigate the mountain maze with a peasant pal.
# Advanced while-loop usage is required!

peasant = hero.findNearest(hero.findFriends())
while True:
    # Command your friend to build a decoy towards x + 1:
    hero.command(peasant, "buildXY", "decoy", hero.pos.x+1, hero.pos.y)
    tDest = {"x": hero.pos.x, "y": hero.pos.y + 28};
    tDes = {"x": hero.pos.x-5, "y": hero.pos.y + 28};
    while hero.distanceTo(tDest) > 1:
        hero.move(tDest)
        hero.command(peasant, "move", tDes)
    # Create a new x/y dict +28 units away in the x dir:
    tDest = {"x": hero.pos.x+ 28, "y": hero.pos.y };
    tDes = {"x": hero.pos.x+ 28-5, "y": hero.pos.y };
    # Find the nearest enemy:
    enemy = hero.findNearestEnemy()
    # While there is an enemy:
    if enemy:
        # While the enemy's health is > 0:
        while enemy.health>0:
            # Attack the enemy:
            hero.attack(enemy)
    enemy = hero.findNearestEnemy()
    # While there is an enemy:
    if enemy:
        # While the enemy's health is > 0:
        while enemy.health>0:
            # Attack the enemy:
            hero.attack(enemy)
        # Update the variable to the next nearest enemy:
        
    # While friend's distance to the new x/y dict > 1:
    while hero.distanceTo(tDest) > 1:
        hero.move(tDest)
        hero.command(peasant, "move", tDes)
        # Move the hero and peasant towards the x/y dict:

```
