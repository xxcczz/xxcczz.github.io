---
layout: default
title: ice-soccer
---
## 冰球
```

# Use flags to tell your players where to ram the ball.
# 当一个选手接近旗帜的时候使用移除旗帜

while True:
    flagGreen = hero.findFlag("green")
    if flagGreen:
        friends = hero.findFriends()
        for friend in friends:
            hero.command(friend, "move", flagGreen.pos)
        hero.removeFlag(flagGreen)

```
