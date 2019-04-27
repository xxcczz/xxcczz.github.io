---
layout: default
title: boulder-woods
---
## 巨石森林
```

# 使用 isPathClear 命令来在随机位置的巨石周围移动
# 自动寻路不能在本关使用
while True:
    angle = Math.PI / 2 - Math.PI / 16
    while angle >= -Math.PI / 2:
        targetX = hero.pos.x + 5 * Math.cos(angle)
        targetY = hero.pos.y + 5 * Math.sin(angle)
        # 使用 isPathClear 命令在你当前的位置和目标中间
        # 如果道路是干净的，可以移动到目标
        if hero.isPathClear(hero.pos, {'x': targetX, 'y': targetY}):
            hero.move({'x': targetX, 'y': targetY})
        else:
            # 否则的话，转一个角度再尝试。
            angle -= Math.PI / 16

```
