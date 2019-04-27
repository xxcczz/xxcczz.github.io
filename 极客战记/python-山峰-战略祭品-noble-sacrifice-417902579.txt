---
layout: default
title: noble-sacrifice
---
## 战略祭品
```

# 收集80金币
while hero.gold<80:
    item = hero.findNearestItem()
    if item:
        hero.move(item.pos)
# 建造4个士兵用来做诱饵
for i in range(4):
    hero.summon("soldier")
# 派你的士兵到指定位置。
points = []
points[0] = { "x": 13, "y": 73 }
points[1] = { "x": 51, "y": 73 }
points[2] = { "x": 51, "y": 53 }
points[3] = { "x": 90, "y": 52 }
friends = hero.findFriends()
for j in range(len(friends)):
    point = points[j]
    friend = friends[j]
    hero.command(friend, "move", point)
# 使用范围来在数组中循环
# 让friends去指定地点，命令他们移动

```
