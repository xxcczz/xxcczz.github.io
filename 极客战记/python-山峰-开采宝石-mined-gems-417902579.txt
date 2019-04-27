---
layout: default
title: mined-gems
---
## 开采宝石
```

# Collect 4 gems. Don't touch gems from the inner circle.

# The radius of the gem-trap circle.
innerRadius = hero.distanceTo(hero.findNearestItem())

# This function check that a is definitely greater than b.
def definitelyGreater(a, b):
    return a > b + 0.5

centre = {"x": 40, "y": 34}
gems = hero.findItems()

# Iterate all gems:
for gem in gems:
    # Use definitelyGreater to check if a gem's distance
    # is greater than the inner radius:
    if definitelyGreater(hero.distanceTo(gem), innerRadius):
        # Collect the gem.
        hero.moveXY(gem.pos.x, gem.pos.y)
        # Return to the centre.
        hero.moveXY(centre.x, centre.y)

```
