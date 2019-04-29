---
layout: default
title: forest-garden
---
## 森林公园
```

# Grow the perfect rectangular flower fence.

# Use the given dimensions for the flower rectangle.
gardener = hero.findNearest(hero.findFriends())
gardenWidth = gardener.gardenWidth
gardenHeight = gardener.gardenHeight
# Start the flower fence at the initial position.
hero.toggleFlowers(True)
x = hero.pos.x
y = hero.pos.y
# Move to each corner, one by one, and return to the start:
hero.moveXY(x+gardenWidth, y)
x = hero.pos.x
y = hero.pos.y
hero.moveXY(x, y-gardenHeight)
x = hero.pos.x
y = hero.pos.y
hero.moveXY(x-gardenWidth, y)
x = hero.pos.x
y = hero.pos.y
hero.moveXY(x, y+gardenHeight)

```
