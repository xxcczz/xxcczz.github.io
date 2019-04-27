---
layout: default
title: goalkeeper
---
## 守门员
```

# 命令农民，防止食人魔得分。
# 火球是输入 "ball"。
points = []
points[0] = {"x": 20, "y": 43}
points[1] = {"x": 20, "y": 35}
while True:
    ball = hero.findByType("ball")[0]
    friends = hero.findFriends()
    for j in range(len(friends)):
        point = points[j]
        friend = friends[j]
        if friend.distanceTo(ball)<5:
            hero.command(friend, "move", ball.pos)
        else:
            hero.command(friend, "move", point)

```
