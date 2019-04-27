---
layout: default
title: convenient-enemy
---
## 方便敌方
```

#保护农民
#农民知道哪些食人魔藏在森林里
#聆听他们说出的最后一句话，召唤正确的队伍与食人魔战斗。
#Ogres躲在树林里。 保护农民。
# 农民信息中的最后一个字是暗示。

for x in range(8, 73, 16):
    hero.moveXY(x, 22)
    #农民知道该召唤谁。
    peasant = hero.findNearest(hero.findFriends())
    message = peasant.message
    if message:
        # 词语被空白分隔。
        words = message.split(" ")
        # “words”是来自“消息”的单词的数组。
        #说出最后一句话。 这是所需的单位类型。
        hero.say(words[len(words)-1])
        # 召唤所需的单位类型。
        hero.summon(words[len(words)-1])

for i in range(len(hero.built)):
    unit = hero.built[i]
    # 命令单位保卫单位的位置。
    hero.command(unit, "defend", unit.pos)

#保护你自己的最后一点：
while True:
    enemies = hero.findEnemies()
    nearest = hero.findNearest(enemies)
    if nearest:
        hero.attack(nearest)

```
