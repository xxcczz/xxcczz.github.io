---
layout: default
title: match-cord
---
## 匹配火线
```

# Ogres mined the field to protect their Chieftain.
# But we can use the "domino" effect get our target.
# The scout has prepared the map of the minefield.
# All mines are placed the same distance apart.
# The map is an array of strings, where "x" is a mine and "." is nothing.
# The first row in the array is the row nearest to the hero.

# The map and helpful constants are listed below.
fieldMap = hero.findFriends()[0].getMap()

mine = "x"
empty = "."
mineDistance = 5
firstXPos = 15
firstYPos = 40

# Find which starting mine connects to the ogre Chieftain.


resultColumn = 1 # ∆ Change this to your actual result!

hero.say("I think it's column number: " + resultColumn)
resultX = resultColumn * mineDistance + firstXPos
hero.moveXY(resultX, hero.pos.y)
hero.moveXY(resultX, firstYPos)

```
