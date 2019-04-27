---
layout: default
title: return-to-thornbush-farm-a
---
## 返回荆棘农场 A
```

# 函数maybeBuildTrap定义了两个参数！
def maybeBuildTrap(x, y):
    # 使用x和y作为移动的坐标。
    hero.moveXY(x, y)
    enemy = hero.findNearestEnemy()
    if enemy:
        pass
        # 使用buildXY在指定xy坐标处建造一个"fire-trap"
        hero.buildXY("fire-trap", x, y)
while True:
    # 这会调用maybeBuildTrap，使用左侧入口的坐标。
    maybeBuildTrap(20, 34)
    
    # 下面在下方入口处使用maybeBuildTrap！
    maybeBuildTrap(38, 19)
    # 下面在右侧入口使用maybeBuildTrap！
    
    maybeBuildTrap(57,33)

```
