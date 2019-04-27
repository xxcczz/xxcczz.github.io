---
layout: default
title: the-mighty-sand-yak
---
## 强壮的沙牦牛
```

# 当牦牛靠近时向右移动10米来躲避
# 躲避4头牦牛完成此关

while True:
    # 使用你的灵石获取你当前的 x 和 y 位置。
    x = hero.pos.x
    y = hero.pos.y
    
    # 找到最近的耗牛。
    yak = hero.findNearestEnemy()
    
    # 使用 if 仅仅当牦牛少于10米距离的时候。
    if hero.distanceTo(yak) < 10:
        # 向右移动，添加10到你的x位置。
        hero.moveXY(x+10, y)
        # 使用 moveXY 来移动！
        
        pass
    
```
