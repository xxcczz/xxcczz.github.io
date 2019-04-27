---
layout: default
title: second-gem
---
## 第二宝石
```

# One gem is safe, the others are bombs.
# But you know the answer: always take the second.

while True:
    items = hero.findItems()
    if len(items)>=2:
        
        # Move to the second item in items
        yidong(items[1])
    else:
        # Move to the center mark.
        hero.moveXY(40, 34)
    
def yidong(mb):
    hero.moveXY(mb.pos.x, mb.pos.y)

```
