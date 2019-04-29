---
layout: default
title: wild-horses
---
## 野马
```

while True:
    # 你怎么寻找最近的友好单位？
    # 马=？
    horse = hero.findNearest(hero.findFriends())
    
    if horse:
        x1 = horse.pos.x - 7
        x2 = horse.pos.x + 7
        if x1 >= 1:
            # 移动到马的y坐标，但使用x1作为x坐标。
            hero.moveXY(x1, horse.pos.y)
        elif x2 <= 79:
            # 移动到马的y坐标，但使用x2作为x坐标。
            hero.moveXY(x2, horse.pos.y)
        distance = hero.distanceTo(horse)
        if distance <= 10:
            hero.say("Whoa")
            # 移到到红色的x来使马返回农场。
            hero.moveXY(27, 54)
            # 移回牧场开始寻找下一匹马。

```
