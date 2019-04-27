---
layout: default
title: sacred-grove
---
## 神圣树林
```

# Don’t let ogres step into the grove.

def onSpawn():
    while True:
        scout = pet.findNearestByType("scout")
        if scout and pet.isReady("charm"):
            pet.charm(scout)


# Assign the event handler to the pet's "spawn" event.
pet.on("spawn", onSpawn)

# Fight!
enemy = hero.findNearestEnemy()
if enemy:
    hero.attack(enemy)

```
