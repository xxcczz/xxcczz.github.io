---
layout: default
title: to-arms
---
## 拿起武器！
```

#Ogres即将发起攻击。
# 在每个帐篷附近移动（到X标记）
# 在每个X上说一些东西来唤醒你的士兵。
# 当心：战斗开始时离开营地！
# Ogres如果看到英雄会派遣增援部队。

# 中士知道帐篷之间的距离。
sergeant =  hero.findNearest(hero.findFriends())

# X标记之间的距离。
stepX = sergeant.tentDistanceX
stepY = sergeant.tentDistanceY
# The number of tents.
tentsInRow = 5-1
tentsInColumn = 4-1

# 第一个帐篷标记具有恒定的坐标。
firstX = 10
firstY = 14
for y in range(firstY,firstY+stepY*tentsInColumn+1,stepY):
    # 使用嵌套循环并访问所有20个帐篷。
    # 重要提示：逐行移动 - 速度更快。
    for x in range(firstX,firstX+stepX*tentsInRow+1,stepX):
        a()
        # 在帐篷附近的标记处移动并说出任何内容。
        hero.moveXY(x, y)
        hero.say("0")

hero.moveXY(70, 49)
# 现在看战斗。
def a():    
    if hero.canCast("haste", hero):
        hero.cast("haste", hero)
    cooldown = hero.getCooldown("haste")
    if cooldown!=0:
        hero.resetCooldown("haste")

```
