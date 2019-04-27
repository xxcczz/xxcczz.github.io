---
layout: default
title: cursed-wonderglade
---
## 被诅咒的梦境
```

# Wonderglade has changed since our last visit.
# Ogres cursed it and we should defeat them.
# The burl still is collecting gems, so don't touch them.
# Also don't attack the burl.

while True:
    # Find the nearest item.
    # Collect it (if it exists) only if its type isn't "gem".
    item = hero.findNearestItem()
    if item and item.type!="gem":
        yidong(item)
    # Find the nearest enemy.
    # Attack it if it exists and its type isn't "burl".
    enemy = hero.findNearestEnemy()
    if enemy and enemy.type!="burl":
        hero.attack(enemy)
    pass
def yidong(mb):
    hero.moveXY(mb.pos.x, mb.pos.y)

```
