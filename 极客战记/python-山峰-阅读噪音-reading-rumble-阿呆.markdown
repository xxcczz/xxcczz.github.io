---
layout: default
title: reading-rumble
---
## 阅读噪音
```

#击败食人魔
#巫师会帮助你击败食人魔，
#但他们每个人只能施放一次下拉螺栓。
#向目标巫师大喊（使用大写字母）最大食人魔的名字
#击败所有来袭的食人魔。

while True:
    #找到最近的敌人。
    enemy = hero.findNearestEnemy()
    # 如果有敌人，而且它是一个“搏斗者brawler”：
    if enemy and enemy.type=="brawler":
        #然后在大写中说出它的名字（.id）。
        word=enemy.id.toUpperCase()
        hero.say(word)
    # 对于其他的敌人，只是打架。
    if enemy and enemy.type!="brawler":
        hero.attack(enemy)
    pass

```
