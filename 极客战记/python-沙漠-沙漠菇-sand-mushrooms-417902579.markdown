﻿---
layout: default
title: sand-mushrooms
---
## 沙漠菇
```

# Collect 9 mushrooms.

# This function makes the pet fetch potions for you.
def onSpawn(event):
    while True:
        # Pets can find the nearest item by its type.
        potion = pet.findNearestByType("potion")
        # Make the pet fetch the potion if it exists:
        if potion:
            pet.fetch(potion)

pet.on("spawn", onSpawn)

# Mushrooms are toxic, don't collect them too quickly.
while True:
    someItem = hero.findNearestItem()
    if someItem and hero.health > hero.maxHealth / 3:
        # Collect the someItem:
        yidong(someItem)
        pass
def yidong(mb):
    hero.moveXY(mb.pos.x, mb.pos.y)

```
