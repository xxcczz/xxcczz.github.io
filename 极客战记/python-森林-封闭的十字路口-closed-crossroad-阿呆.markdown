---
layout: default
title: closed-crossroad
---
## 封闭的十字路口
```

# 只在看到敌人时进行建造。

# 该函数定义3个参数。
def maybeBuildSomething(buildType, x, y):
    # 移动到参数为X 和 Y的位置
    hero.moveXY(x, y)
    # 找到最近的敌人
    enemy=hero.findNearestEnemy()
    if enemy:
        hero.buildXY(buildType, x, y)
    # 如果存在敌人
    
        # 那么使用buildXY，参数buildType, x, 和 y
        
    pass
    
while True:
    # 调用 maybeBuildSomething，使用"fire-trap"及底部X的坐标。
    maybeBuildSomething("fire-trap", 40, 20)
    # 调用maybeBuildSomething，在左侧X处使用"fence"!
    maybeBuildSomething("fence", 26, 34)
    # 调用maybeBuildSomething，在顶部的X处使用"fire-trap"!
    maybeBuildSomething("fire-trap", 40, 50)
    # 调用maybeBuildSomething，在右侧X处使用"fence"!
    maybeBuildSomething("fence", 54, 34)

```
