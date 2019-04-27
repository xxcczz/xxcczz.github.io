---
layout: default
title: friend-and-foe
---
## 友人和敌人
```

# 农民和士兵聚集在森林。
# 命令农民战斗，苦工远离！

while True:
    friend = hero.findNearestFriend()
    if friend:
        hero.say("To battle, " + friend.id + "!")
    # 寻找最近的敌人，然后让他们滚蛋
    enemy = hero.findNearestEnemy()
    if enemy:
        hero.say("To battle, " + enemy.id + "!")

```
