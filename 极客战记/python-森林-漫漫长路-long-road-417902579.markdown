---
layout: default
title: long-road
---
## 漫漫长路
```

# 移动到右边

# 补全这个函数：
def onSpawn(event):
    pass
    # 在 while-true 循环里：
    while True:
        
        item = hero.findNearestItem()
        
        # 使用hero.findNearestItem()
        
        # 如果有物品：
        if item:
            pet.fetch(item)
            # 使用pet.fetch(item)来拿取物品。
            

# 使用pet.on()来将onSpawn指派给"spawn"事件
pet.on("spawn", onSpawn)
hero.moveXY(78, 35)

```
