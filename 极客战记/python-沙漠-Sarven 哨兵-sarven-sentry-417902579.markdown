---
layout: default
title: sarven-sentry
---
## Sarven 哨兵
```

# 使用不同的颜色旗子来执行不同的任务。

while True:
    flagGreen = hero.findFlag("green")
    flagBlack = hero.findFlag("black")
    
    # 如果是绿色旗子，就建立一个栅栏。
    if flagGreen:
        hero.buildXY("fence", flagGreen.pos.x, flagGreen.pos.y)
        # Build a "fence" at flagGreen's position.
        hero.pickUpFlag(flagGreen)
        # 记住要捡起旗子，在你都完成之后！
        
    # 如果是黑色旗子，就建立一个火焰陷阱
    if flagBlack:
        hero.buildXY("fire-trap", flagBlack.pos.x, flagBlack.pos.y)
        # Build a "fence" at flagGreen's position.
        hero.pickUpFlag(flagBlack)
        # Build a "fire-trap" at flagBlack's position.
        
        # 记住要捡起旗子，在你都完成之后！
        
    # 回到中间。
    hero.moveXY(43, 31)

```
