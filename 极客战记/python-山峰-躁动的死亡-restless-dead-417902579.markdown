---
layout: default
title: restless-dead
---
## 躁动的死亡
```

# 这个关卡应该是非常难的！你也许需要一个很棒的战略与或装置去完成它！

# 找到然后杀死雪人，为了仪式去收集他的血液。
# 你也许想收集雪人遗留下的金币，你需要他们去召唤一只军队。
# 站在召唤石旁（红色X），开始召唤。
# 
hero.moveXY(55, 12)
a=0
while a!=1:
    enemy = hero.findNearestEnemy()
    if enemy:
        while enemy.health>0:
            hero.attack(enemy)
        a=a+1
while True:
    item = hero.findNearestItem()
    if item :
        hero.move(item.pos)
    else:
        break
while hero.gold >= hero.costOf("soldier"):
    hero.summon("archer")
friends = hero.findFriends()
for j in range(len(friends)):
    friend = friends[j]
    hero.command(friend, "move", {"x": 46, "y": 39})
hero.moveXY(18, 40)   
hero.moveXY(60, 51)   
while True:    
    friends = hero.findFriends()
    for j in range(len(friends)):
        friend = friends[j]
        enemy = friend.findNearestEnemy()
        if enemy:
            hero.command(friend, "attack", enemy)
    hero.shield()
    if hero.isReady("stomp") :
        hero.stomp()

```
