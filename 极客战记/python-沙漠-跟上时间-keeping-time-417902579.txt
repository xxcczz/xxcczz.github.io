---
layout: default
title: keeping-time
---
## 跟上时间
```

# 使用你的新技能来选择你要做什么 

while True:
    # 如果是头十秒，进攻。
    if hero.time < 10:
        gongji()
        pass
    # 反之，如果是前35秒，收集金币。
    elif hero.time < 35:
        item = hero.findNearestItem()
        if item:
            yidong(item)
        pass
    # 后35秒，加入救助。
    else:
        gongji()
        pass
def gongji():
    enemy = hero.findNearestEnemy()
    if enemy:
        hero.attack(enemy)
def yidong(mb):
    hero.moveXY(mb.pos.x, mb.pos.y)

```
