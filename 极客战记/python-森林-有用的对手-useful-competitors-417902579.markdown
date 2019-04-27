---
layout: default
title: useful-competitors
---
## 有用的对手
```

# 这片金币地中暗藏了致命的毒药。
# 兽人正在进攻，而苦力尝试偷你的金币！

while True:
    enemy = hero.findNearestEnemy()
    if enemy:
        # 只在敌人类型不是 "peon" 的时候攻击。
        if enemy.type != "peon":
            hero.attack(enemy)
    item = hero.findNearestItem()
    if item:
        # 只在物品的类型不是 "poison" 的时候收集。
        if item.type != "poison":
            yidong(item)
def yidong(mb):
    hero.moveXY(mb.pos.x, mb.pos.y)

```
