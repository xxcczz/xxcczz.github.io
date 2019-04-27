---
layout: default
title: crag-tag
---
## 峭壁追逐
```

# 抓住 Pender Spellbane 去了解她的秘密。

while True:
    # Pender是这里唯一的朋友，所以她总是在最近的位置。
    pender = hero.findNearest(hero.findFriends())
    
    if pender:
        # moveXY()将移动到 Pender 在的位置，
        # 但是她会向远离你的位置移动。
        #hero.moveXY(pender.pos.x, pender.pos.y)
        
        # move()只一次移动一步。
        # 所以你可以用它来追踪你的目标。
        hero.move(pender.pos)

```
