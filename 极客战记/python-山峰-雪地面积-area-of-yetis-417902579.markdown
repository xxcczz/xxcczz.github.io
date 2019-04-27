﻿---
layout: default
title: area-of-yetis
---
## 雪地面积
```

# Defeat Yetis.

# The chosen one can stun yetis with a Shout.
chosen = hero.findFriends()[0]

# The power of the Shout is equal to the area of a circle.
radius = chosen.distanceTo(chosen.findNearestEnemy())
# The area of a circle can be calculated with the formula:
area = radius * radius * Math.PI
# Tell the area to the chosen one.
hero.say(area)
# Don't just stand there! Fight!
hero.moveXY(33, 31)

```
