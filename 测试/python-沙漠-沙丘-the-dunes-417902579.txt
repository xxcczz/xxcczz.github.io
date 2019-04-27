---
layout: default
title: the-dunes
---
## 沙丘
```

# 收集硬币，忽略砂耗牛和树榴。和投掷者，食人魔战斗。
while True:
    enemy = hero.findNearestEnemy()
    item = hero.findNearestItem()
    if enemy:
        if enemy.type == "sand-yak" or enemy.type == "burl":
            # 别和砂耗牛，树榴打！赶紧收集硬币。
            item = hero.findNearestItem()
            if item:
                hero.move(item.pos)
            pass
        else:
            # 但如果敌人的类型是『投掷者』或者『食人魔』，攻击他们
            hero.attack(enemy)
            pass
        
    elif item:
        # 收集钱币。
        yidong(item)
        pass
    else:
        hero.moveXY(41, 31)
def yidong(mb):
    hero.moveXY(mb.pos.x, mb.pos.y)

```
