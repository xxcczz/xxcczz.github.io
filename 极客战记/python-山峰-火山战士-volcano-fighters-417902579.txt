---
layout: default
title: volcano-fighters
---
## 火山战士
```

# Complete the paladin rectangle to protect the village.

# This function finds the left-most unit.
def findMostLeft(units):
    if len(units) == 0:
        return None
    mostLeft = units[0]
    for unit in units:
        if unit.pos.x < mostLeft.pos.x:
            mostLeft = unit
    return mostLeft

# This function finds the bottom-most unit:
def findMostBottom(units):
    if len(units) == 0:
        return None
    mostBottom = units[0]
    for unit in units:
        if unit.pos.y < mostBottom.pos.y:
            mostBottom = unit
    return mostBottom

paladins = hero.findByType("paladin")
# Find the top left paladin with findMostLeft function:

# Find the bottom right paladin with findMostBottom function:


# Use X coordinate from the top left paladin:
# and Y coordinate from the bottom right paladin:

# Move to the {X, Y} point from the previous step:
x=findMostLeft(paladins).pos.x
y=findMostBottom(paladins).pos.y
hero.moveXY(x, y)
# Continue to shield while the volcano is erupting:
while True:
    hero.shield()

```
