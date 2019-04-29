---
layout: default
title: return-to-thornbush-farm-b
---
## 返回荆棘农场 B
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
    # 这会调用maybeBuildTrap，使用下方入口的坐标。
    maybeBuildTrap(38, 20)
    
    # 下面在右侧入口使用maybeBuildTrap！
    maybeBuildTrap(57, 33)
    # 现在在上方入口处使用maybeBuildTrap！
    maybeBuildTrap(38, 48)
    
```
