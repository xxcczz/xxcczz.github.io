---
layout: default
title: double-cheek
---
## 复查
```

# 第一点，打败6位ogres~
# Then collect coins until you have 30 gold.

# 变量用来对ogres计数
defeatedOgres = 0

# 没打败6位ogres，就继续打
while defeatedOgres < 6:
    enemy = hero.findNearestEnemy()
    if enemy:
        hero.attack(enemy)
        defeatedOgres += 1
    else:
        hero.say("Ogres!")

# Move to the right side of the map.
hero.moveXY(49, 36)

# 钱没攒够30块，就继续捡
while hero.gold < 30:
    # 寻找并收集金币
    item = hero.findNearestItem()
    if item:
        yidong(item)
    # 去掉这行 say()。
    hero.say("我应该收集金币！")
def yidong(mb):
    hero.moveXY(mb.pos.x, mb.pos.y)

# 移动到出口。
hero.moveXY(76, 32)

```
