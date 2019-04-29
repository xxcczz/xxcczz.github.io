﻿---
layout: default
title: fence-builder
---
## 栅栏建造者
```

# Build a fence around the farm.

# Take coordinates of the opposite corners.
customer = hero.findNearest(hero.findFriends())
x1 = customer.leftBottom.x
y1 = customer.leftBottom.y
x2 = customer.rightTop.x
y2 = customer.rightTop.y
step = 4

# Let's build the bottom side.
for x in range(x1 , x2 + 1, step):
    hero.buildXY("fence", x, y1)
# Then the right side.
for y in range(y1 + step, y2 + 1, step):
    hero.buildXY("fence", x2, y);
# Build the top side.
for x in range(x2 ,x1 + step-1 , -step):
    hero.buildXY("fence", x, y2)
# Build the left side.
for y in range( y2,y1 + step-1, -step):
    hero.buildXY("fence", x1, y);

```
