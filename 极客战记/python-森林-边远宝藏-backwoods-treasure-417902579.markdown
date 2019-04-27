---
layout: default
title: backwoods-treasure
---
## 边远宝藏
```

# 从2~3个树丛里 收集100个金币
# 如果你赢了，接下来会变得更难，当然也会有更多奖励。
# 如果你输了，需要等待一天再次挑战
# 记得，每一次提交都会获得不同的地图。

while True:
    flag = hero.findFlag()
    if flag:
        pass  # “pass”是一个占位符，它没有任何作用
        # Pick up the flag.
        hero.pickUpFlag(flag)
    else:
        # Automatically move to the nearest item you see.
        item = hero.findNearestItem()
        if item:
            position = item.pos
            x = position.x
            y = position.y
            hero.moveXY(x, y)

```
