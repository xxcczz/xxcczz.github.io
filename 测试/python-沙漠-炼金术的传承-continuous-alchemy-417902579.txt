---
layout: default
title: continuous-alchemy
---
## 炼金术的传承
```

# Race munchkins to the water distilled by Omarn Brewstone!
# 使用 "continue" 验证丛林中的条件。
while True:
    enemy = hero.findNearestEnemy()
    item = hero.findNearestItem()
    
    # 如果没有敌人，跳出循环继续。
    if not enemy:
        continue
    
    # 如果有敌人却没物品，要一瓶药，跳到下次循环。
    if not item:
        hero.say("把喝的拿来！")
        continue
    
    # 使用 if 语句检查物品的类型。如果类型是 "poison"，跳出循环继续运行。
    if item.type=="poison":
        continue
    else:
        yidong(item)
        hero.moveXY(34, 47)
    # 如果不是，那瓶子里装的是水，所以走向它，返回出发点！
    # so moveXY to the potion, then back to the start!
    
def yidong(mb):
    hero.moveXY(mb.pos.x, mb.pos.y)

```
