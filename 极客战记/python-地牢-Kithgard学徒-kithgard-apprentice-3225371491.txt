---
layout: default
title: kithgard-apprentice
---
## Kithgard学徒
```
hero.summon("peasant")
hero.moveXY(45, 30)
while True:
    
    enemy = hero.findNearestEnemy()
    if enemy:
        hero.attack(enemy)
    flag = hero.findFlag("green")
    if flag:
        hero.pickUpFlag(flag)
mightier-than-the-sword
password = 'Secret Message'
hero.moveUp()
hero.moveRight()
hero.say(password)

# A variable changes its value whenever you assign it.
password = 'So Many Doors'
hero.moveRight()

# Change the string in this line to the password variable.
hero.say(password) # ∆ Change this!

password = 'Let Me Out Of Here'
# Move to the last door and say the password variable to open it.
hero.moveRight()

hero.say(password)
```
