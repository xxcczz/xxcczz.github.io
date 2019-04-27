---
layout: default
title: bone-dance
---
## 骨头舞蹈
```

# Soothe the skeletons when they get too close.

# This function is useful to compare float numbers.
def almostEqual(a, b):
    return Math.abs(a - b) < 1

while True:
    skeleton = hero.findNearestEnemy()
    # Find the radius of the skeleton circle.
    circumference=2*Math.PI*hero.distanceTo(skeleton)
    # If the circumference is almost equal 100:
    if almostEqual(circumference, 100):
        # Say, sing, or shout anything once.
        hero.say("message")

```
