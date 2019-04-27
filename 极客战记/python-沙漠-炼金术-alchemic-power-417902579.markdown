---
layout: default
title: alchemic-power
---
## 炼金术
```

# Wait for alchemist's commands to fetch potions.

# The event handler for the pet's event "hear".
def onHear(event):
    # Find the nearest potion.
    potion = pet.findNearestByType("potion")
    # If the event's message is "Fetch"
    if event.message=="Fetch":
        # Have the pet fetch the potion.
        pet.fetch(potion)
    # Else (for any other messages):
    else:
        # Return the pet to the red mark.
        pet.moveXY(54, 34)

pet.on("hear", onHear)

# You don't have to change the code below.
while True:
    enemy = hero.findNearest(hero.findEnemies())
    if enemy:
        hero.attack(enemy)
    else:
        hero.moveXY(40, 34)

```
