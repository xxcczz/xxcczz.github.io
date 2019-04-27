---
layout: default
title: deadly-pursuit
---
## 致命追逐
```

# 收集金币使用旗子来建造陷阱
# 你在这处理这些食人魔

while True:
    flag = hero.findFlag()
    item = hero.findNearestItem()
    if flag:
        hero.pickUpFlag(flag)
        hero.buildXY("fire-trap", flag.pos.x, flag.pos.y)
    elif item:
        hero.moveXY(item.pos.x, item.pos.y)

```
