---
layout: default
title: wonderglade
---
## 梦境
```

# You need to collect several items.
# But, the burl wants the gems!
# Pick up all appearing items EXCEPT gems.

while True:
    item = hero.findNearestItem()
    if item:
        if item.type!="gems":
            yidong(item)
def yidong(mb):
    hero.moveXY(mb.pos.x, mb.pos.y)

```
