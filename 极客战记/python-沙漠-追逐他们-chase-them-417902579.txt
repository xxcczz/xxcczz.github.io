---
layout: default
title: chase-them
---
## 追逐他们
```

# Defeat the ogres and cure the hero.

# The pet is your only hope.
def onSpawn(e):
    while True:
        enemy = pet.findNearestByType("munchkin")
        if enemy and pet.isReady("chase"):
            pet.chase(enemy)
        if not enemy:
            mushroom = pet.findNearestByType("potion")
            pet.fetch(mushroom)
        # Find and fetch a "potion":
        

# Assign "onSpawn" handler on the "spawn" event:

pet.on("spawn", onSpawn)

```
