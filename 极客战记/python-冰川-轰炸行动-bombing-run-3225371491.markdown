---
layout: default
title: bombing-run
---
## 轰炸行动
```

while True:
    enemy = hero.findNearestEnemy()
    if enemy:
        o=enemy.pos.y-hero.pos.y
        a=enemy.pos.x-hero.pos.x
        hero.say(Math.atan2(o,a)*180/Math.PI)

```
