---
layout: default
title: mega-munchkin-attacks
---
## 超级大的小食人魔 攻击
```

# That's a big'un! With some clever thinking, Ivy should be able to take care of this situation single-handedly.
while True:
    # Find the archer.
    friend = hero.findNearest(hero.findFriends())
    enemy = hero.findNearest(hero.findEnemies())
    
    # Tell the archer to attack the enemy!
    if friend and enemy:
        hero.command(friend, "attack", enemy)
    
    # Wait, no, that doesn't work that well. Maybe try something else?
    # The munchkin is awfully slow...
    if friend.distanceTo(enemy)<10:
        hero.command(friend, "move", {"x": friend.pos.x-1, "y": friend.pos.y-1})

```
