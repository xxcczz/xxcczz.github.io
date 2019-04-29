---
layout: default
title: defend-the-garrison
---
## 保卫要塞
```

# 杀掉所有进攻的食人魔
# 使用旗子远离那些危险的食人魔
def xx():
    while True:
        enemy = hero.findNearestEnemy()
        if enemy:
            while True:
                hero.attack(enemy)
                if enemy.health<0:
                    break
        else:
            break
while True:
    enemy = hero.findNearestEnemy()
    if enemy:
        #if enemy.type!="munchkin" and enemy.type!="ogre" and enemy.type!="scout" and enemy.type!="shaman":
            #hero.say(enemy.type)
        if hero.time>30 and (enemy.type=="shaman" or enemy.type=="thrower"):
            hero.say("我得跑过去打远程了")
            xx()
        elif hero.pos.x<48:
            hero.moveXY(48,26)
        hero.shield()

while True:
    enemy = hero.findNearestEnemy()
    if enemy:
        hero.attack(enemy)

```
