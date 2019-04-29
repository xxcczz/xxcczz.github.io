---
layout: default
title: zoo-keeper
---
## 动物园管理员
```

# 保护笼子。
# 放一个士兵在每一个 X 的位置
points = []
points[0] = {"x": 33, "y": 42}
points[1] = {"x": 47, "y": 42}
points[2] = {"x": 33, "y": 26}
points[3] = {"x": 47, "y": 26}

# 1.收集80金币。
while hero.gold<80:
    item = hero.findNearestItem()
    if item:
        hero.move(item.pos)
#hero.say("message")
# 2.建造4个士兵。
for i in range(4):
    #hero.say(i)
    hero.summon("soldier")
#hero.say("message")
# 3.派你的士兵到特定的位置上。
while True:
    friends = hero.findFriends()
    for j in range(len(friends)):
        point = points[j]
        friend = friends[j]
        enemy = friend.findNearestEnemy()
        if enemy and enemy.team == "ogres" and friend.distanceTo(enemy) < 5:
            # 命令友方攻击。
            pass
            hero.command(friend, "attack", enemy)
        else:
            # 命令的朋友移动到特定点上。
            pass
            hero.command(friend, "move", point)
            
```
