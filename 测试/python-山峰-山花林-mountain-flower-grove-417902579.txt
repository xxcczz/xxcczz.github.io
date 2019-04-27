---
layout: default
title: mountain-flower-grove
---
## 山花林
```

# This level is a place for making flower art.
# The real goal is to experiment and have fun!
# If you draw something with at least 1000 flowers, you will "succeed" at the level.
x=hero.pos.x
y=hero.pos.y
bj=10
while hero.time<100:
    hy(x,y,bj)
    bj=bj+10
def hy(x,y,bj):
    hero.toggleFlowers(False)
    hero.moveXY(x+bj, y)
    hero.toggleFlowers(True)
    jd=0
    while jd<Math.PI*2:
        x1=x+bj*Math.cos(jd)
        y1=y+bj*Math.sin(jd)
        hero.moveXY(x1,y1)
        jd=jd+1/180*Math.PI
    hero.toggleFlowers(False)
    hero.moveXY(x, y)

```
