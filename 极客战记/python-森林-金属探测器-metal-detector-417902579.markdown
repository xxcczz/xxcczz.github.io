---
layout: default
title: metal-detector
---
## 金属探测器
```

# The artillery uses coins as a target.
# You'll be the rangefinder for the artillery.

# Write the function.
def coinDistance():
    # Find the nearest coin,
    item = hero.findNearestItem()
    if item:
        return juli(item)
    # If there is a coin, return the distance to it.
    else:
        return 0
    # Else, return 0 (zero).
    
    pass
def juli(duixiang):
    result = hero.distanceTo(duixiang)
    return result

while True:
    distance = coinDistance()
    if distance > 0:
        # Say the distance.
        hero.say(distance)
        pass

```
