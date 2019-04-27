---
layout: default
title: spring-thunder
---
## 春雷
```

# Certain coins and gems attract lightning.
# 这个英雄应只收集银币和蓝宝石

while True:
    item = hero.findNearestItem()
    # A silver coin has a value of 2.
    # Collect if item.type is equal to "coin"
    # AND item.value 相等于2
    if item.type == "coin" and item.value == 2:
        hero.moveXY(item.pos.x, item.pos.y)
    # 一个蓝宝石价值10
    # Collect if item.type is equal to "gem"
    # AND item.value is equal to 10.
    if item.type == "gem" and item.value == 10:
        hero.moveXY(item.pos.x, item.pos.y)

```
