---
layout: default
title: interception
---
## 拦截
```

# Stand between the peasant and the tower.

while True:
    enemy = hero.findNearestEnemy()
    friend = hero.findNearestFriend()
    # Calculate x by adding friend.pos.x to enemy.pos.x
    # 然后除以2
    # Check the guide if you need more help!
    x=(enemy.pos.x+friend.pos.x)/2
    y=(enemy.pos.y+friend.pos.y)/2
    # Now do the same for y
    hero.moveXY(x, y)
    # 移动到您计算的X和Y坐标。

```
