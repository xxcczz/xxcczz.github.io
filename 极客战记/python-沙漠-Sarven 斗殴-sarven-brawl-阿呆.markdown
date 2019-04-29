---
layout: default
title: sarven-brawl
---
## Sarven 斗殴
```

# 活两分钟。
# 如果你赢了，接下来会变得更难，当然也会有更多奖励。
# 如果你输了，你必须等一天之后再提交。
# 记得，每一次提交都会获得不同的地图。
while True:
    flag = hero.findFlag()
    if flag:
        hero.pickUpFlag(flag)
    else:
        gjxlzsd()
def gjxlzsd():
    #优先攻击远程(血量少的)
    mb=None
    zsxl=99999
    enemies = hero.findEnemies()
    for enemy in enemies:
        if enemy.type=="ogre":
            continue
        if enemy.type=="sand-yak":
            continue
        if enemy.health<zsxl:
            zsxl=enemy.health
            mb=enemy
    if mb:
        #hero.say(mb.type)
        while mb.health>0:
            if hero.isReady("cleave"):
                hero.cleave(mb)
            if hero.isReady("bash"):
                hero.bash(mb)
            hero.attack(mb)

```
