---
layout: default
title: gardener
---
## 园丁
```

# We need square flower fences around the statues.

# This function should make a square with the certain side
#  around the center {cx, cy} point.
def growSquare(cx, cy, side):
    # Move to any corner of the square.
    hero.moveXY(cx-side/2, cy+side/2)
    # Start growing.
    hero.toggleFlowers(True)
    # Now move to all other corners one by one.
    # Use clockwise or countercloclwise order.
    x=hero.pos.x+side
    y=hero.pos.y
    hero.moveXY(x,y)
    x=hero.pos.x
    y=hero.pos.y-side
    hero.moveXY(x,y)
    x=hero.pos.x-side
    y=hero.pos.y
    hero.moveXY(x,y)
    x=hero.pos.x
    y=hero.pos.y+side
    hero.moveXY(x,y)
    # Don't forget to return in the first corner.
    
    # Stop growing.
    hero.toggleFlowers(False)

# The keeper will tell you where to grow flowers.
keeper = hero.findNearest(hero.findFriends())
points = keeper.pointsForWork
# All squares should have the same size.
squareSize = 8
# We don't need excess flowers.
hero.toggleFlowers(False)

for pos in points:
    # Don't forget complete this function.
    growSquare(pos.x, pos.y, squareSize)

```
