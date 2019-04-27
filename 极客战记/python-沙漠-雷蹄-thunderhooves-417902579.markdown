---
layout: default
title: thunderhooves
---
## 雷蹄
```

# 到达绿洲，
# 用栅栏引导砂牦牛到你去的地方

while True:
    yak = hero.findNearestEnemy()
    if yak:
        # 如果它的 y 值大于你的，那么耗牛在你前面
        if yak.pos.y>hero.pos.y:
            # 如果耗牛在你前面，在它后面10米建立一个栅栏
            hero.buildXY("fence", yak.pos.x, yak.pos.y-10)
        else: 
            hero.buildXY("fence", yak.pos.x, yak.pos.y+10)
            # 如果耗牛在你后面，在它前面10m 建立一个栅栏
            
        pass
    else:
        # 向右移动10走向绿洲
        hero.moveXY(hero.pos.x+10, hero.pos.y)
        pass

```
