---
layout: default
title: hunting-party
---
## 狩猎派对
```

# 命令你的部队向东移动，攻击任何看到的食人魔。
# 使用 for 循环和 findFriends方法。
# 你能在你的士兵上使用findNearestEnemy()来获取他们的而不是你的最近的敌人。
while True:
    friends = hero.findFriends()
    for j in range(len(friends)):
        friend = friends[j]
        if friend.type=="soldier":
            x=friend.pos.x+10
        elif friend.type=="archer":
            x=friend.pos.x+5   
        y=friend.pos.y
        enemy = friend.findNearestEnemy()
        if enemy:
            if friend.health<friend.maxHealth*0.5:
                x=13
                hero.command(friend, "move", {"x": x, "y": y})
                continue
            hero.command(friend, "attack", enemy)
        else:
            hero.command(friend, "move", {"x": x, "y": y})

```
