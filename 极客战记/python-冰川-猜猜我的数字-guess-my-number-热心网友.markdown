---
layout: default
title: guess-my-number
---
## 猜猜我的数字
```

def number():
    return Math.round((topEnd - lowEnd) / 2) + lowEnd
    # return Math.round(Math.random()*(topEnd-lowEnd)) + lowEnd


lowEnd = 0
topEnd = 1000
curnumber = 500
while True:
    # You need to kill the enemy before the next attempt.
    enemy = hero.findNearestEnemy()
    if enemy:
        if enemy.type == 'scout':
            lowEnd = curnumber + 1
        else:
            topEnd = curnumber - 1
        # "scout" is 'greater', "munchkin" is less.
        # Prepare for the next attempt and wipe out the ogre.

        hero.attack(enemy)
    else:
        # Make your next attempt and say it.
        curnumber = number()
        hero.say(curnumber)

```
