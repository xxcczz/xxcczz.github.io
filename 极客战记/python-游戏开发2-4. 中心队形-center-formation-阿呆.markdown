---
layout: default
title: center-formation
---
## 4. 中心队形
```

# 夜晚来临！ 把所有的士兵向火移动。

def centerFormation(event):
    # event.target是运行此事件处理程序的单元。
    unit = event.target
    # 现在使用unit.moveXY将装置移动到火中。
    unit.moveXY(40, 36)

# 这产生了四名士兵：
game.spawnXY("soldier", 16, 57)
game.spawnXY("soldier", 15, 13)
game.spawnXY("soldier", 63, 13)
game.spawnXY("soldier", 67, 57)

# 这将士兵的重生行动设置为功能中心队形：
game.setActionFor("soldier", "spawn", centerFormation)

```
