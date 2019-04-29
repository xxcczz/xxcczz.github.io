---
layout: default
title: ogre-gorge-gouger
---
## 食人魔山谷挖宝
```

# 一大群食人魔来之前你只有20秒时间！
# 尽可能去捡金币，然后你撤退到你栅栏后面的基地里！
while hero.time < 20:
    # 收集金币
    #hero.say("我应该捡点金币")
    coins = hero.findItems()
    coin = hero.findNearest(coins)
    hero.move(coin.pos)
    
while hero.pos.x > 16:
    # 撤退到栅栏后面
    #hero.say("我应该撤退")
    hero.move({'x':16,'y':37})
    
# 建立栅栏挡住食人魔
hero.buildXY("fence",21,37)

```
