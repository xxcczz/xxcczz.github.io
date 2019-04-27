---
layout: default
title: passing-through
---
## 穿越
```

# Don't insult this tribe of peaceful ogres.

while True:
    item = hero.findNearestItem()
    if item:
        # If item.type IS NOT EQUAL TO "gem"
        if item.type != "gem":
            # 然后跟随你的宠物。
            hero.moveXY(pet.pos.x, pet.pos.y)
        # 否则:
        else:
            # 移动到宝石的坐标。
            hero.moveXY(item.pos.x, item.pos.y)

```
