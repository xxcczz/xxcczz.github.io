---
layout: default
title: cloudrip-commander
---
## 安息之云指挥官
```

# 召唤一些士兵，然后引导他们去你的基地。

# 每个士兵消耗20金币。
while hero.gold > hero.costOf("soldier"):
    hero.summon("soldier")
    
soldiers = hero.findFriends()
soldierIndex = 0
# 添加一个while 循环来命令所有的士兵。
while soldierIndex<len(soldiers):
    soldier = soldiers[soldierIndex]
    hero.command(soldier, "move", {"x": 50, "y": 40})
    soldierIndex=soldierIndex+1

# 去加入你的朋友！
while True:
    hero.move({'x': 50, 'y': 40})

```
