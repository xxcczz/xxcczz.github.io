---
layout: default
title: copper-meadows
---
## 金币草地
```

# 收集每片草地的所有金币。
# 使用旗子在草地间移动。
# 当你准备好放置旗子时点击“提交”

loop
    flag = @findFlag()
    if flag
        # 捡起旗子。
        @say "Delete this and pick up the flag instead."
        @pickUpFlag(flag)
    else
        # 自动移动到你能看见的最近的物品。
        item = @findNearestItem()
        if item
            position = item.pos
            x = position.x
            y = position.y
            @moveXY x, y
        else
            @say "放置一个旗子给我前往。"

```
