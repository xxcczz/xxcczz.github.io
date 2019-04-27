---
layout: default
title: count-emptiness
---
## 空虚数
```

# Solve the riddler puzzle and find the treasure.
# Count the whitespace on both sides of a riddle.

# This function moves the hero N steps right.
def moveNSteps(n):
    hero.moveXY(hero.pos.x + 8 * n, hero.pos.y)

# Read the riddle.
riddle = hero.findNearestEnemy().riddle
# Trim whitespace from both sides and store in a variable
#hero.say(riddle)
trimmed = riddle.trim()
#hero.say(trimmed)
# Find the difference between the lengths:
#hero.say(len(riddle)+","+len(trimmed))
l=len(riddle)-len(trimmed)
# Use the result and moveNSteps function to move to the spot:
moveNSteps(l)
# Say something there!
hero.say("message")

```
