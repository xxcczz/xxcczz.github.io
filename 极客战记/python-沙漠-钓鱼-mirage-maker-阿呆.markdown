---
layout: default
title: mirage-maker
---
## 钓鱼
```

# Lure the ogres into an ambush!

# 当你的金币小于25个的时候，收集金币。
while hero.gold<25:
    item = hero.findNearestItem()
    if item:
        yidong(item)
        
def yidong(mb):
    hero.moveXY(mb.pos.x, mb.pos.y)
# 然后建造诱饵来引诱食人魔离开路线。
hero.buildXY("decoy", 72, 68)

# 当你的生命值满了，冲着小食人魔喊叫侮辱他们，引诱他们。
hero.moveXY(68, 18)
hero.say("来打我呀")
# 然后退回到你的基地伏击他们。
hero.moveXY(22, 15)

```
