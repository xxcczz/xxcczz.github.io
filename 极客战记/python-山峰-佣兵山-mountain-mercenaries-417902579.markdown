---
layout: default
title: mountain-mercenaries
---
## 佣兵山
```

# 收集金币招募士兵，指挥他们攻击敌人。

while True:
    # 走到最近的金币处。
    # 使用 move 取代 moveXY，以便于你可以不断发出命令。
    coin = hero.findNearest(hero.findItems())
    if coin:
        hero.move(coin.pos)
    
    #hero.say("我需要金币！")
    
    # 如果钱够了就招募士兵。
    if hero.gold > hero.costOf("soldier"):
        #hero.say("我应该召集些什么帮手！")
        hero.summon("soldier")
    enemy = hero.findNearest(hero.findEnemies())
    if enemy:
        # 遍历你所有的士兵，命令他们攻击。
        
        soldiers = hero.findFriends()
        for soldier in soldiers:
            hero.command(soldier, "attack", enemy)
        
        # 使用 attack 命令让你的士兵们攻击。

```
