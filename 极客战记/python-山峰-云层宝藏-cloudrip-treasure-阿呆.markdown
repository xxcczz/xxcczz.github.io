---
layout: default
title: cloudrip-treasure
---
## 云层宝藏
```

#你的目标是收集硬币/宝石。
#这个级别是可重复的。 如果你赢了，困难和奖励会增加。
#如果你失败了，你必须等待一天才能重新提交。
#这个级别是可选的挑战级别。 你不需要击败它继续运动！
points = []
points[0] = {"x": 27, "y": 94}
points[1] = {"x": 123, "y": 94}
points[2] = {"x": 123, "y": 27}
points[3] = {"x": 27, "y": 27}
def onSpawn (event):
    while True:
        pet.moveXY(27,94)
        pet.moveXY(27,27)

pet.on("spawn", onSpawn)
friends = hero.findFriends()
for j in range(len(friends)):
    point = points[j]
    friend = friends[j]
    hero.command(friend, "move", point)
while True:    
    friends = hero.findFriends()
    for j in range(len(friends)):
        point = points[j]
        friend = friends[j]
        item=friend.findNearest(friend.findItems())
        if item:
            hero.command(friend, "move", item.pos)
    hero.shield()

```
