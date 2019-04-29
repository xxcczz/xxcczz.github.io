---
layout: default
title: 待
---
## 金色幻影
```

# Collect 10 real coins.
sz=[]
while True:
    items = hero.findItems()
    for j in range(len(items)):
        item = items[j]
        sz[item.value]=0
    for j in range(len(items)):
        item = items[j]
        #hero.say(item.value)
        sz[item.value]=sz[item.value]+1
        #hero.say("."+sz[item.value])
    for j in range(len(items)):
        item = items[j]
        if sz[item.value]==1:
            hero.moveXY(item.pos.x, item.pos.y)

```
