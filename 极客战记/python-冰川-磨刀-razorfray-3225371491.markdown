---
layout: default
title: razorfray
---
## 磨刀
```

while True:
    flag = hero.findFlag()
    if flag:
        if hero.isReady("throw") and hero.distanceTo(flag)<hero.throwRange:
            hero.throw(flag)
        hero.removeFlag(flag)

```
