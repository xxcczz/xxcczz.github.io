﻿---
layout: default
title: arrowproof-wolf
---
## 无箭狼
```

# Collect mushrooms.

# First, come to the wolf pet and wake up it (say).
hero.moveXY(12, 34)
hero.say("wake up")
# Next collect mushrooms just usual items.
while True:
    item = hero.findNearestItem()
    if item:
        hero.moveXY(item.pos.x, item.pos.y)

```
