---
layout: default
title: make-advances
---
## 推进
```

# Advance through the forgotten tomb.
# Be wary, traps lay in wait to ruin your day!

# The Paladins volunteer to lead the way.
# Command them to shield against incoming projectiles.
while True:
    friends = hero.findFriends()
    # findEnemyMissiles finds all dangerous projectiles.
    projectiles = hero.findEnemyMissiles()
    for friend in friends:
        if friend.type is "paladin":
            # Find the projectile nearest to the friend:
            nearest = friend.findNearest(projectiles)
            # If the projectile exists
            # AND is closer than 10 meters to the paladin:
            if nearest and friend.distanceTo(nearest)<10:
                # Command the friend to "shield":
                hero.command( friend, "shield")
            # ELSE, when there is no potential danger:
            else:
                # Advance the paladin:
                hero.command(friend, "move", {"x": friend.pos.x+10, "y": friend.pos.y})
            pass
        else:
            # If not a paladin, just advance:
            hero.command(friend, "move", {"x": friend.pos.x+1, "y": friend.pos.y})
        pass
    # Advance the hero in the x direction:
    hero.move(hero.move({'x': hero.pos.x+1, 'y': hero.pos.y}))

```
